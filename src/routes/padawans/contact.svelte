<script>
  import Nav from "../../components/Nav.svelte";
  import Hero from "../../components/Hero.svelte";
</script>

<style>
  .grid {
    position: relative;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr;
    grid-template-areas: "main";
    height: 100vh;
  }
  .form-container {
    height: 80vh;
    width: 100%;
    background: var(--main-black);
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
    color: #ffffff;
  }
  .input {
    box-sizing: border-box;
    padding: 0 0 5px 5px;
    width: 100%;
    color: white;
    background: none;
    border: none;
    border-bottom: 1px solid #757575;
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
    background: #ffffff;
    border-radius: 22px;
    font-size: 13px;
    line-height: 15px;
    letter-spacing: 0.055em;
    text-transform: uppercase;
    color: #000000;
    margin-top: 40px;
    cursor: pointer;
  }
</style>

<svelte:head>
  <title>Backend Program - Hackademy Mx</title>
</svelte:head>

<section class="grid">
  <Hero image="padawans.png" btnText="Contáctanos" text="" />
  <section class="form-container">
    <div class="form-wrapper">
      <h2 class="form-title">¡Hola! Queremos saber de ti</h2>
      <form class="form">
        <div class="name-email-wrapper">
          <input class="input" type="text" placeholder="Nombre" />
          <input class="input" type="email" placeholder="Email" />
        </div>
        <input class="input" type="text" placeholder="Mensaje" />
        <button class="send-button">ENVIAR MENSAJE</button>
      </form>
    </div>
  </section>
</section>
