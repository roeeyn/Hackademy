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
    /* height: 10vh;
    grid-column-gap: 50%;
    width: 100%;
    background: white;
    display: flex;
    justify-content: center;
    align-items: center;
    align-content: space-around; */
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
</style>

<div class="grid">
  <section class="form-container">
    <div class="form-wrapper">
      <h2 class="form-title">CONTACTANOS</h2>
      <form class="form">
        <div class="name-email-wrapper">
          <input class="input" type="text" placeholder="Nombre" />
          <input class="input" type="email" placeholder="Correo" />
        </div>
        <input class="input" type="text" placeholder="Mensaje" />
        <button class="send-button">ENVIAR MENSAJE</button>
      </form>
    </div>
  </section>
</div>

<div class="grid-footer">
  <div class="info-container">
    <p>Fb/hackademymx // IG/hackademy // TT/hackademy</p>
    <p>www.hackademy.mx // hola@hackademy.mx // +52 6675738836</p>
  </div>
</div>
