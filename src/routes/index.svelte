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

  .section a {
    text-decoration: none;
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
  }

  .title {
    opacity: 1;
    transition: opacity 0.5s ease-in-out;
  }
  .disappear {
    opacity: 0;
  }

  @media screen and (max-width: 720px){
    .disappear {
      opacity: 1;
    }
  }
</style>

<!--
FIXES TODO: 
  - que se le pueda dar clic a cualquier parte de la sección y te
    lleve a la url.
  - Agregar imágenes faltantes al manifiesto
-->
<script>

let actualSection = ''; 
const handleMouseMove = section => actualSection = section;
</script>
<svelte:head>
  <title>Hackademy Mx</title>
</svelte:head>

<main>
  <section class="section" on:mousemove={() => handleMouseMove("padawans")}>
    <div class="image-wrapper">
      <img src="hackademy_logo.svg" alt="hackademy logo" />
    </div>
    <div class="title" class:disappear={actualSection == "enterprise"}>
      <a href="/padawans">Entrenamiento</a>
    </div>
  </section>
  <section class="section enterprise-section" on:mousemove={() => handleMouseMove("enterprise")}>
    <div class="image-wrapper">
      <img src="hackademy_logo_white.svg" alt="hackademy logo" />
    </div>
    <div class="title" class:disappear={actualSection == "padawans"}>
      <a href="/enterprise">Empresas</a>
    </div>
  </section>
</main>
