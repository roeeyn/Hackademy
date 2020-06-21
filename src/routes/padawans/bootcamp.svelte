<script>
  import PartnerGallery from "../../components/PartnerGallery.svelte";
  import Nav from "../../components/Nav.svelte";
  import PadawansRoadmap from "../../components/PadawansRoadmap.svelte";
  import FooterForm from "../../components/FooterForm.svelte";
  const benefits = [
    "Acceso a GitHub ",
    "Acceso a AWS educate",
    "Acceso a webinars",
    "Mejora en las habilidades",
    "Acceso a entrevistas de empleo",
    "Acceso a becas del 100%"
  ];
  const requirements = [
    "Resolver por lo menos 5 ejercicios del  Club de programación",
    "Agendar entrevista con el equipo de Hackademy",
    "Firmar carta compromiso",
    "Disponibilidad de 4 horas diarias",
    "Actitud y ganas de aprender"
  ];
</script>

<style>
  .bootcamp-container {
    background: var(--main-black);
    color: #ffffff;
    padding-top: 125px;
  }
  .bootcamp-wrapper {
    max-width: var(--max-width);
    margin: 0 auto;
  }
  .benefits-list {
    columns: 2;
  }
  .benefits-title {
    font-size: 24px;
    line-height: 204.19%;
    font-weight: bold;
    letter-spacing: 0.015em;
  }
  .benefit {
    font-size: 16px;
    line-height: 204.19%;
    letter-spacing: -0.05em;
  }
  .title {
    font-weight: bold;
    font-size: 60px;
    line-height: 70px;
  }
  .subtitle {
    font-size: 27px;
    line-height: 32px;
    letter-spacing: 0.04em;
    margin: 25px 0;
  }
  .text {
    font-size: 13px;
    line-height: 27px;
    letter-spacing: 0.04em;
    color: #c7c7c7;
  }
  .text-wrapper {
    margin: 25px 0;
  }
  .mini-hero {
    width: 100%;
    object-fit: cover;
    margin: 60px 0;
  }
  .programs-list {
    list-style-type: circle;
    margin-left: 20px;
  }
  #requisitos {
    margin-top: 20px;
  }
</style>

<svelte:head>
  <title>Bootcamp - Hackademy Mx</title>
</svelte:head>

<section class="bootcamp-container">
  <div class="bootcamp-wrapper">
    <div class="content">
      <h1 class="title">Bootcamp</h1>
      <h2 class="subtitle">
        El entrenamiento de Hackademy tiene como analogía el entrenamiento que
        los deportistas tienen para ir a las olimpiadas, trabajamos duro para
        ser los mejores
      </h2>
      <div class="text-wrapper">
        <p class="text">
          En Hackademy buscamos desarrollar el talento que tienes de la mejor
          manera y por eso hemos dividido nuestro programa en especialidades.
          Estas especialides cubren cada una de las partes que se requieren en
          el desarrollo de software: Backend, Frontend, desarrollo móvil,
          adminsitración de proyectos, desarrollo de chatbots y seguridad
          informtica.
        </p>
        <p class="text">
          Cada uno de los programas cuenta con un grupo de mentores que
          comparten su experiencia para que puedas mejorar tus habilidades de
          una mejor forma, para nosotros el talento y las habilidades son como
          los musculos y por eso hay que entrenar.
        </p>
      </div>
      <div>
        <div class="benefits-title">Beneficios</div>
        <div class="benefits-list">
          {#each benefits as benefit}
            <li class="benefit">{benefit}</li>
          {/each}
        </div>
      </div>
      <div>
        <div class="benefits-title" id="requisitos">Requisitos</div>
        <div class="benefits-list">
          {#each requirements as requirement}
            <li class="benefit">{requirement}</li>
          {/each}
        </div>
      </div>
    </div>
  </div>
  <img class="mini-hero" src="padawans.png" alt="Imagen de nuestros padawans" />
  <div class="bootcamp-wrapper">
    <div class="content">
      <div class="subtitle">
        Hackademy es un bootcamp intensivo donde nuestros padawans (llamamos así
        a nuestros aprendices) pueden mejorar sus habilidades técnicas a través
        de la práctica, desarrollando un proyecto de la vida real, apoyados por
        mentores expertos que están trabajando en la industria del desarrollo de
        software.
      </div>
      <div class="text-wrapper">
        <div class="text">
          Nuestros padawans tienen 16 semanas para desarrollar la versión 1 de
          un proyecto real con el que, durante las entrevistas, pueden demostrar
          lo que han aprendido, mejorado y lo que los diferencia del resto. El
          programa beneficia al padawan, mejorando sus habilidades, así como a
          las empresas que están en búsqueda de talento al obtener acceso a los
          elementos mejor preparados. Cada padawan inicia aprendiendo sobre GIT
          y SCRUM durante las 2 primeras semanas del bootcamp para tener las
          bases necesarias para iniciar el camino y especializarse en un área
          del desarrollo.nas
        </div>
        <section class="programs-list">
          <li>Development</li>
          <li>Frontend (ReactJS/Angular)</li>
          <li>Backend (NodeJS/Python)</li>
          <li>Android (React Native)</li>
          <li>Desarrollo de chatbots</li>
          <li>Administración de Proyectos</li>
          <li>Agile (Scrum)</li>
          <li>Management 3.0 - DevOps</li>
        </section>
      </div>
    </div>
  </div>
  <PadawansRoadmap />
  <PartnerGallery />
  <FooterForm />
</section>
