<script>
  import { src } from "sapper/dist/chunk3";
</script>

<style>
  main {
    height: 100vh;
    width: 100vw;
    display: flex;
    flex-wrap: wrap;
  }

  .section {
    font-size: 50px;
    line-height: 59px;
    min-width: 360px;
    display: flex;
    flex: 1;
    justify-content: center;
    align-items: center;
    color: var(--main-black);
    flex-direction: column;
  }

  .image-wrapper {
    width: 100%;
    display: flex;
    padding: 16px;
    margin-bottom: 36px;
    justify-content: center;
  }

  img {
    width: 50%;
  }

  .enterprise-section {
    background: var(--main-black);
    color: white;
    text-decoration: none;
  }

  .enterprise-section a {
    text-decoration: none;
  }
</style>

<svelte:head>
  <title>Hackademy Mx</title>
</svelte:head>

<main>
  <section class="section">
    <div class="image-wrapper">
      <img src="hackademy_logo.svg" alt="hackademy logo" />
    </div>
    <div>Entrenamiento</div>
  </section>
  <section class="section enterprise-section">
    <div class="image-wrapper">
      <img src="hackademy_logo_white.svg" alt="hackademy logo" />
    </div>
    <div> <a href="/enterprise">Empresas</a></div>
  </section>
</main>
