<script>
  const inputs = [];
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
</style>

<main class="form-wrapper" id="club-form">
  <h1>Regístrate al club de programación</h1>
  <form>
    <input class="input" type="text" placeholder="Nombre completo" />
    <input class="input" type="email" placeholder="Correo Electrónico" />
    <input class="input" type="tel" placeholder="Teléfono" />
    <input
      class="input"
      type="text"
      placeholder="Ciudad y Estado donde vives" />
    <input
      class="input"
      type="text"
      placeholder="Dónde estudias y en qué semestre vas?, o a qué te dedicas?" />
    <input
      class="input"
      type="text"
      placeholder="Cuál es tu usario en GitHub?" />
    <div>
      <label class="input" for="lang">A qué lenguaje quieres aplicar?</label>
      <select name="lang" id="lang">
        <option value="anyone">El que sea</option>
        <option value="js">JavaScript</option>
        <option value="python">Python</option>
      </select>
    </div>
    <div class="">
      <label class="input" for="after-club">
        Quieres aplicar a Hackademy después del club?
      </label>
      <input type="radio" id="yes" name="after-club" value="yes" />
      <label class="input" for="yes">Sí</label>
      <input type="radio" id="no" name="after-club" value="no" />
      <label class="input" for="no">No</label>
    </div>
    <div>
      <label class="input" for="lead">Cómo te enteraste?</label>
      <select name="lead" id="lead">
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
      <input type="submit" class="button" value="REGISTRARME" />
    </div>
  </form>
</main>
