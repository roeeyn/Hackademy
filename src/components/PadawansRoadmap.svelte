<script>
  const points = [
    `Tu camino inicia en el club de programación donde tendrás que resolver minimo 5 ejercicos y donde conoceras a tus futuros compañeros de generación`,
    `Una vez ternimano el club podrás agendar una entrevista con el equipo de Hackademy para conocernos mejor.Durante la entrevista podrás seleccionar a qué programa quieres aplicar`,
    `Si pasas con exito el club y la entrevista ¡Bienvenido! Se te enviará una carta compromiso a tu correo personal para después asignarte tu correo @hackademy.mx`,
    `Empiezan 16 semanas super emocionantes donde deberas, junto con tu equipo, desarrollar la versión 1 del proyecto asignado... Todo esto con el apoyo de nuestros Masters`,
    `Al cierre de la generación tendrás una agenda de entrevistas con empresas que buscan contratar al mejor talento... Nosotros te acompañaremos en todo momento para que sea la mejor experiencia`
  ];
</script>

<style>
  .text {
    font-family: Roboto;
    font-size: 16px;
    line-height: 19px;
    letter-spacing: 0.01em;
    color: #ffffff;
    margin-bottom: 10px;
  }

  .text-container {
    position: relative;
  }

  .text-container:nth-child(1) {
    top: 20px;
  }
  .text-container:nth-child(2) {
    top: 5vmax;
    left: -3vmax;
  }
  .text-container:nth-child(3) {
    top: 3vmax;
  }
  .text-container:nth-child(4) {
    top: 10vmax;
    left: -4vmax;
  }
  .text-container:nth-child(5) {
    top: 25vmax;
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(5, 205px);
    justify-content: space-between;
  }

  .roadmap-text-wrapper {
    padding: 0 30px;
  }

  .pointer {
    display: block;
    margin: 0 auto;
  }

  .roadmap-img {
    position: relative;
    z-index: 2;
    margin-top: -6vmin;
    width: 100%;
  }

  .subtitle {
    max-width: var(--max-width);
    color: #ffffff;
    margin: 25px auto;
    margin-top: 120px;
    font-size: 27px;
    line-height: 32px;
    letter-spacing: 0.04em;
  }

  @media screen and (min-width: 800px) {
    .mobile-wrapper {
      display: none;
    }
  }
  @media screen and (max-width: 1205px) {
    .text {
      font-size: 14px;
    }
    .grid {
      grid-template-columns: repeat(5, 125px);
    }
  }

  @media screen and (max-width: 800px) {
    .roadmap-wrapper {
      display: none;
    }
  }

  .mobile-wrapper {
    max-width: var(--max-width);
    margin: 0 auto;
  }
  .step {
    display: flex;
    margin: 32px 0;
  }
  .number {
    font-size: 188px;
  }
  .step-description {
    font-size: 18px;
    display: flex;
    padding: 0 14px;
    align-items: center;
  }
</style>

<section class="roadmap-wrapper">
  <div class="roadmap-text-wrapper">
    <h2 class="subtitle">El camino del padawan</h2>
    <div class="grid">
      {#each points as point}
        <div class="text-container">
          <p class="text">{point}</p>
          <img
            class="pointer"
            src="pointer.png"
            alt="Paso en el camino del Padawan" />
        </div>
      {/each}
    </div>
  </div>
  <img
    class="roadmap-img"
    src="padawan-roadmap.png"
    alt="Roadmap del padawan" />
</section>

<section class="mobile-wrapper">
  <h2 class="subtitle">El camino del padawan</h2>
  <div class="step-wrapper">
    <div class="step">
      <div class="number">1</div>
      <div class="step-description">
        Tu camino inicia en el club de programación donde tendrás que resolver
        minimo 5 ejercicos y donde conocerás a tus futuros compañeros de
        generación
      </div>
    </div>
    <div class="step">
      <div class="number">2</div>
      <div class="step-description">
        Una vez terminando el club podrás agendar una entrevista con el equipo
        de Hackademy para conocernos mejor. Durante la entrevista podrás
        seleccionar a qué programa quieres aplicar
      </div>
    </div>
    <div class="step">
      <div class="number">3</div>
      <div class="step-description">
        Si pasas con exito el club y la entrevista ¡Bienvenido! Se te enviará
        una carta compromiso a tu correo personal para despues asignarte tu
        correo @hackademy.mx
      </div>
    </div>
    <div class="step">
      <div class="number">4</div>
      <div class="step-description">
        Empiezan 16 semanas súper emocionantes donde deberás, junto con tu
        equipo, desarrollar la versión 1 del proyecto asignado... Todo esto con
        el apoyo de nuestros Masters
      </div>
    </div>
    <div class="step">
      <div class="number">5</div>
      <div class="step-description">
        Al cierre de la generación tendrás una agenda de entrevistas con
        empresas que buscan contratar al mejor talento... Nosotros te
        acompañaremos en todo momento para que sea la mejor experiencia.
      </div>
    </div>
  </div>
</section>
