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

<main class="form-wrapper">
  <h1>Regístrate al club de programación</h1>
  <form>
    <input class="input" type="text" placeholder="Nombre completo" />
    <input class="input" type="email" placeholder="Correo Electrónico" />
    <input class="input" type="phone" placeholder="Teléfono" />
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
    <input
      class="input"
      type="text"
      placeholder="A qué lenguaje quieres aplicar?" />
    <input
      class="input"
      type="text"
      placeholder="Quieres aplicar a Hackademy al terminar el club?" />
    <input class="input" type="text" placeholder="Cómo te enteraste?" />
    <div class="button-wrapper">
      <input type="submit" class="button" value="REGISTRARME" />
    </div>
  </form>
</main>
