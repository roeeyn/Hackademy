<script>
  import { src } from "sapper/dist/chunk3";
</script>

<style>
  main {
    height: 100vh;
    width: 100vw;
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  .section {
    font-size: 50px;
    line-height: 59px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: var(--main-black);
  }

  .section > div {
    cursor: pointer;
    max-width: 370px;
  }

  .enterprise-section {
    background: var(--main-black);
    color: white;
  }
</style>

<main>
  <section class="section">
    <div>Entrenamiento</div>
  </section>
  <section class="section enterprise-section">
    <div>Empresas</div>
  </section>
</main>
