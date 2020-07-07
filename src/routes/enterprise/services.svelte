<script>
  // import { scrollto } from "svelte-scrollto";

  import ParagraphLayout from "../../components/ParagraphLayout.svelte";
  import ParagraphText from "../../components/ParagraphText.svelte";
  import ListLayout from "../../components/ListLayout.svelte";
  import PartnerGallery from "../../components/PartnerGallery.svelte";
  const lists = [
    {
      title: "TECNOLOGÍAS",
      items: [
        "Python / NodeJS",
        "Angular / ReactJS",
        "MongoDB / Postgresql",
        "AWS",
        "DialogFlow / Tensorflow",
        "React Native",
        "y mucho más..."
      ]
    },
    {
      title: "DESARROLLOS",
      items: [
        "Apps móviles",
        "Plataformas web",
        "Apps nativas",
        "PWA's",
        "Chatbots",
        "y mucho más..."
      ]
    },
    {
      title: "OTROS",
      items: [
        "Consultoría en transformación digital",
        "Asesoría en validación de proyectos y modelos de negocio",
        "Startup builder"
      ]
    }
  ];
</script>

<style>
  h1 {
    font-size: 60px;
    padding-top: 156px;
    margin: 0 auto 24px;
    max-width: var(--max-width);
  }
  h2 {
    display: inline-block;
    margin: 12px 30px 12px 0;
    max-width: 150px;
  }
  .mini-hero {
    width: 100%;
    height: 300px;
    object-fit: cover;
    margin: 60px 0;
    /* background-image: url("padawans.png"); */
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }
  .services-menu {
    display: flex;
    margin: 100px 0;
    flex-wrap: wrap;
    justify-content: flex-start;
  }
</style>

<section class="services-wrapper">
  <h1>Servicios</h1>
  <ParagraphLayout darkMode={false}>
    <div class="services-menu">
      <h2>
        <a href="/enterprise/services#talent">Contratación de Talento</a>
      </h2>
      <h2>
        <a href="/enterprise/services#enterprise">Capacitación Empresarial</a>
      </h2>
      <h2>
        <a href="/enterprise/services#software">Desarrollo de Software</a>
      </h2>
    </div>
  </ParagraphLayout>
  <div id="talent" />
  <ParagraphLayout
    darkMode={false}
    title="TALENTO"
    subtitle="Lleva a tu empresa talento que genere valor y que su principal
    habilidad sea resolver problemas con su conocimiento y experiencia.">
    <ParagraphText darkMode={false}>
      El proceso de Hackademy te permite conocer la evolución de nuestros
      estudiantes (padawans) desde el día 1 hasta el momento de su graduación,
      ver como mejoró sus habilidades y cómo sumarlo a tu equipo generará valor
      a tu empresa.
    </ParagraphText>
  </ParagraphLayout>
  <ParagraphLayout
    darkMode={false}
    title="PROCESO"
    subtitle="Nuestro proceso es sencillo">
    <ParagraphText darkMode={false}>
      <ol>
        <li>
          Cuentanos sobre las necesidades de tu empresa ¿qué perfiles necesitas?
          ¿Cuántos perfiles necesitas? ¿Qué tecnologías implementas en tú
          empresa? ¿Quisieras que practicaran con alguna idea tuya durante el
          entrenamiento?
        </li>
        <li>
          Teniendo esta información empezaremos a perfilar para saber qué
          padawans hacen match con la cultura de tú empresa y que tengan las
          herramientas necesarias para ser un colaborador de valor.
        </li>
        <li>
          En la entrevista tendrás acceso a los repositorios con los que trabajó
          el padawan, no podrás ver el código completo por razones de seguridad,
          pero tendrás accesoa a información valiosa para conocer la experiencia
          del padawan.
        </li>
        <li>
          Pagas por padawan contratado, los precios van desde los $15,000 pesos
          hsata $35,000 pesos dependiendo del perfil que contrates. Con nosotros
          no hay pagos ocultos, pagas una sola vez por padawan contratado.
        </li>
      </ol>
    </ParagraphText>
  </ParagraphLayout>
  <ParagraphLayout
    darkMode={false}
    subtitle="Hay 2 momentos en los que puedes contratar padawans de Hackademy">
    <ParagraphText darkMode={false}>
      <ul>
        <li>
          Al iniciar la generación, con esto tienes acceso a todos los perfiles
          que se entrenarán y podrás darles seguimiento para contratar con mayor
          precisión y el costo de cada padawan contratado lo padrás cubrir en 4
          mensualidades durante el bootcamp.
        </li>
        <li>
          Al finalizar la generación, en esta etapa tendrás acceso a los
          padawans que no han sido seleccionados y contratados. En esta etapa se
          cubre el costo de contratación en un solo pago.
        </li>
      </ul>
    </ParagraphText>
  </ParagraphLayout>
  <div class="mini-hero" style="background-image: url('{'padawans.png'}')" />
  <div id="enterprise" />
  <ParagraphLayout
    darkMode={false}
    title="CAPACITACIÓN"
    subtitle="Actualiza a tu equipo de colaboradores, brindales las herramientas
    necesarias para seguir siendo competitivos en una industria que no se
    detiene nunca.">
    <ParagraphText darkMode={false}>
      Hackademy es un espacio para que las empresas y las personas mejoren sus
      habilidades para que puedan seguir desarrollandose y creciendo, sabemos
      que estamos en una industria en constante evolución que nos demanda
      mantenernos capacitados.
    </ParagraphText>
    <ParagraphText darkMode={false}>
      La ventaja de Hackademy es que va más allá de ser un curso y tus
      colaboradores vivirán toda la experiencia del mejor entrenamiento, ellos
      seguirán todo el proceso de 16 semanas durante las cuales implementarán
      nuevas herramientas para obtener el conocimiento y experiencia que se
      necesita para llevar esto a tu empresa.
    </ParagraphText>
  </ParagraphLayout>

  <div
    class="mini-hero"
    style="background-image: url('{'proceso-validacion.png'}')" />
  <div id="software" />
  <ParagraphLayout
    darkMode={false}
    title="DESARROLLO"
    subtitle="Ya sea que necesites el desarrollo de un prototipo o un desarrollo
    completo siempre podrás contar con nosotros.">
    <ParagraphText darkMode={false}>
      Si vas a emprender y quieres validar, si tu equipo esta saturado y quieres
      prototipar o si necesitas desarrollar un solucón robusta contamos con un
      equipo que tiene la habilidad de resolver problemas a traves del software,
      estamos a tur ordenes.
    </ParagraphText>
    <ParagraphText darkMode={false}>
      Con Hackademy tienes un equipo que te ayudará a desarrollar tu solución de
      software, que te acompañará todo el camino y que te asesorará desde la
      selección de las tecnologias hasta el modelo de negocio.
    </ParagraphText>
    <ListLayout {lists} />
  </ParagraphLayout>
  <PartnerGallery
    title="Colaboradores y Clientes"
    showCTA={false}
    darkMode={false} />
</section>

<!-- <div class="services-container">
  <div class="services-wrapper">
    <div class="content">
      <h1 class="title">Servicios</h1>
      <ParagraphLayout
        title="Talento"
        subtitle="Lleva a tu empresa talento que genere valor y que su principal
        habilidad sea resolver problemas con su conocimiento y experiencia">
        <ParagraphText>
          El proceso de Hackademy te permite conocer la evolución de nuestros
          estudiantes (padawans) desde el día 1 hasya el momento de su
          graduación, ver cómo mejoró sus habilidades y cómo sumarlo a tu equipo
          generará valor a tu empresa.
        </ParagraphText>
      </ParagraphLayout>
      <ParagraphLayout title="Proceso" subtitle="Nuestro proceso es sencillo">
        <ParagraphText>
          
        </ParagraphText>
      </ParagraphLayout>
      <ParagraphLayout
      title=" "
      subtitle="Hay 2 momentos en los que puedes contratar a padawans de Hackademy."
      >
        <ParagraphText >
          <ol>
            <li>
              al iniciar la generación, con esto tienes acceso a todos los perfiles que se entrenarán y podrás darles
              seguimiento para contratar con mayor precisión y el costo de cada padawan contratado lo padrás cubrir en 4 mensualidades durante el bootcamp.
            </li>
          </ol>
        </ParagraphText>
      </ParagraphLayout>
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
</div> -->
