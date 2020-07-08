<script>
  let name;
  let email;
  let cellphone;
  let state;
  let education;
  let userName;
  let language;
  let afterClub;
  let channel;

  const handleSubmit = event => {
    event.preventDefault();
    const inputs = {
      name,
      email,
      cellphone,
      state,
      education,
      userName,
      language,
      afterClub,
      channel
    };
    if (
      name &&
      email &&
      cellphone &&
      state &&
      education &&
      userName &&
      language &&
      afterClub &&
      channel
    ) {
      fetch(
        "https://us-central1-hackademy-backend.cloudfunctions.net/emailMessage",
        {
          method: "POST",
          body: JSON.stringify(inputs),
          headers: {
            "Content-Type": "application/json"
          }
        }
      )
        .then(res => res.json())
        .then(response => {
          name = "";
          email = "";
          cellphone = "";
          state = "";
          education = "";
          userName = "";
          language = "";
          afterClub = "";
          channel = "";
          alert("Información enviada con éxito.");
        })
        .catch(error => {
          alert("Ocurrió un error, inténtalo de nuevo.");
          console.log("%cError: ", "color: #7f2200", error);
        });
    } else {
      alert("Favor de llenar todos los campos.");
    }
  };
</script>

<style>
  .form-wrapper {
    max-width: var(--max-width);
    margin: 0 auto;
  }
  form {
    display: grid;
    column-gap: 20px;
    row-gap: 66px;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: 1fr;
  }

  h1 {
    color: #ffffff;
    display: block;
    margin: 33px 0;
  }
  .input {
    box-sizing: border-box;
    padding: 0 0 5px 5px;
    width: 100%;
    color: white;
    background: none;
    border: none;
    line-height: 44px;
    border-bottom: 1px solid #757575;
  }
  label.input {
    color: #757575;
    margin-right: 16px;
  }
  .input::placeholder {
    font-size: 13px;
    line-height: 15px;
    letter-spacing: 0.025em;
    color: #757575;
  }
  .button-wrapper {
    grid-column: 1/-1;
  }
  .button {
    padding: 18px 36px;
    border-radius: 12px;
  }
  @media screen and (max-width: 1060px) {
    form {
      grid-template-columns: 1fr;
      row-gap: 33px;
    }
    input {
      line-height: 20px;
    }
  }
  .without-border {
    border: none;
  }
</style>

<main class="form-wrapper" id="club-form">
  <h1>Regístrate al club de programación</h1>
  <form on:submit={handleSubmit}>
    <input
      class="input"
      bind:value={name}
      type="text"
      placeholder="Nombre completo" />
    <input
      class="input"
      bind:value={email}
      type="email"
      placeholder="Correo Electrónico" />
    <input
      class="input"
      bind:value={cellphone}
      type="tel"
      placeholder="Teléfono" />
    <input
      bind:value={state}
      class="input"
      type="text"
      placeholder="Ciudad y Estado donde vives" />
    <input
      bind:value={education}
      class="input"
      type="text"
      placeholder="Dónde estudias y en qué semestre vas?, o a qué te dedicas?" />
    <input
      bind:value={userName}
      class="input"
      type="text"
      placeholder="Cuál es tu usario en GitHub?" />
    <div>
      <label class="input without-border" for="lang">
        A qué lenguaje quieres aplicar?
      </label>
      <select bind:value={language} name="lang" id="lang">
        <option value="anyone">El que sea</option>
        <option value="js">JavaScript</option>
        <option value="python">Python</option>
      </select>
    </div>
    <div class="">
      <label class="input without-border" for="after-club">
        Quieres aplicar a Hackademy después del club?
      </label>
      <label>
        <input
          bind:group={afterClub}
          type="radio"
          id="yes"
          name="after-club"
          value={'yes'} />
        Sí
      </label>
      <label>
        <input
          bind:group={afterClub}
          type="radio"
          id="no"
          name="after-club"
          value={'no'} />
        No
      </label>
    </div>
    <div>
      <label class="input without-border" for="lead">Cómo te enteraste?</label>
      <select bind:value={channel} name="lead" id="lead">
        <option value="fb">Facebook</option>
        <option value="ig">Instagram</option>
        <option value="tw">Twitter</option>
        <option value="shark-tank">Shark Tank</option>
        <option value="startup-mx">Startup México</option>
        <option value="neural">The big neural project</option>
        <option value="recommended">Por recomendación</option>
      </select>
    </div>
    <div class="button-wrapper">
      <input
        type="submit"
        class="button"
        value="REGISTRARME"
        on:click={handleSubmit} />
    </div>
  </form>
</main>
