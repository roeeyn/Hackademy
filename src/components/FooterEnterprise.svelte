<script>
  let email = "";
  let name = "";
  let message = "";

  const sendEnterpriseMail = event => {
    const enterpriseInfo = {
      email,
      name,
      message
    };
    event.preventDefault();
    const regexValidateEmail = /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
    if (regexValidateEmail.test(email) && name && message) {
      fetch(
        "https://us-central1-hackademy-backend.cloudfunctions.net/enterpriseContact",
        {
          method: "POST",
          body: JSON.stringify(enterpriseInfo),
          headers: {
            "Content-Type": "application/json"
          }
        }
      )
        .then(res => res.json())
        .then(response => {
          email = "";
          name = "";
          message = "";
          alert("Correo enviado con éxito.");
        })
        .catch(error => {
          alert("Ocurrió un error, inténtalo de nuevo.");
          console.log("%cError: ", "color: #7f2200", error);
        });
    } else if (!regexValidateEmail.test(email)) {
      alert("Favor de verificar su correo.");
    } else {
      alert("Favor de verificar que los campos estén completos.");
    }
  };
</script>

<style>
  .grid {
    position: relative;
    display: grid;
    grid-template-columns: 2fr;
    grid-template-rows: 1fr;
    grid-template-areas: "main";
    height: 40vh;
  }
  .info-container {
    display: flex;
    justify-content: space-between;
    margin-top: 120px;
    padding: 0 12px;
  }
  .info-container > p {
    display: flex;
    align-items: center;
  }
  .grid-footer {
    align-content: space-around;
    position: relative;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 2fr;
    grid-template-areas: "main";
    height: 10vh;
  }
  .form-container {
    height: 40vh;
    width: 100%;
    background: white;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .form-wrapper {
    min-width: min(955px, calc(100vw - (2 * 15vmin)));
  }
  .form-title {
    margin: 0 auto;
    font-weight: bold;
    font-size: 28px;
    line-height: 33px;
    text-align: center;
    letter-spacing: 0.07em;
    color: black;
  }
  .input {
    box-sizing: border-box;
    padding: 0 0 5px 5px;
    width: 100%;
    color: black;
    background: none;
    border: none;
    border-bottom: 1px solid black;
  }

  .input::placeholder {
    font-size: 13px;
    line-height: 15px;
    letter-spacing: 0.025em;
    color: #757575;
  }

  .name-email-wrapper {
    display: flex;
    margin: 60px 0 40px;
  }

  .name-email-wrapper > * {
    flex: 1;
  }

  .name-email-wrapper > input:nth-child(2) {
    margin-left: 20px;
  }

  .send-button {
    border: none;
    width: 175px;
    height: 45px;
    background: #595393;
    border-radius: 22px;
    font-size: 13px;
    line-height: 15px;
    letter-spacing: 0.055em;
    text-transform: uppercase;
    color: #ffff;
    margin-top: 40px;
    cursor: pointer;
  }
  .social {
    margin-left: 16px;
    margin-right: 6px;
    height: 20px;
  }
</style>

<div class="grid">
  <section class="form-container">
    <div class="form-wrapper">
      <h2 class="form-title">CONTÁCTANOS</h2>
      <form class="form">
        <div class="name-email-wrapper">
          <input
            bind:value={name}
            class="input"
            type="text"
            placeholder="Nombre" />
          <input
            bind:value={email}
            class="input"
            type="email"
            placeholder="Correo" />
        </div>
        <input
          bind:value={message}
          class="input"
          type="text"
          placeholder="Mensaje" />
        <button class="send-button" on:click={sendEnterpriseMail}>
          ENVIAR MENSAJE
        </button>
      </form>
    </div>
  </section>
</div>

<div class="grid-footer">
  <div class="info-container">
    <p>
      <a href="https://www.facebook.com/hackademymx/">
        <img class="social" src="facebook.svg" alt="facebook logo" />
        Hackademy Mx
      </a>
      <a href="https://www.instagram.com/hackademymx/">
        <img class="social" src="instagram.svg" alt="instagram logo" />
        hackademymx
      </a>
      <a href="https://twitter.com/hackademymx">
        <img class="social" src="twitter.svg" alt="twitter logo" />
        hackademymx
      </a>
    </p>
    <p>
      <a href="https://www.hackademy.mx/">
        <img class="social" src="browser.svg" alt="browser logo" />
        www.hackademy.mx
      </a>
      <a href="mailto:hola@hackademy.mx">
        <img class="social" src="email.svg" alt="email logo" />
        hola@hackademy.mx
      </a>
      <a href="tel:+52 1 667 207 1066">
        <img class="social" src="phone.svg" alt="phone logo" />
        +52 6675738836
      </a>
    </p>
  </div>
</div>
