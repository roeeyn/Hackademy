<script>
  import ParagraphLayout from "../../components/ParagraphLayout.svelte";
  import ParagraphText from "../../components/ParagraphText.svelte";
  import ListLayout from "../../components/ListLayout.svelte";
</script>

<div class="services-container">
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
          <ol>
            <li>
              Cuentanos sobre las necesidades de tu empresa ¿qué perfiles
              necesitas? ¿Cuántos perfiles necesitas? ¿Qué tecnologías
              implementas en tú empresa? ¿Quisieras que practicaran con alguna
              idea tuya durante el entrenamiento?
            </li>
            <li>
              Teniendo esta información empezaremos a perfilar para saber qué
              padawans hacen match con la cultura de tú empresa y que tengan las
              herramientas necesarias para ser un colaborador de valor.
            </li>
            <li>
              En la entrevista tendrás acceso a los repositorios con los que
              trabajó el padawan, no podrás ver el código completo por razones
              de seguridad, pero tendrás accesoa a información valiosa para
              conocer la experiencia del padawan.
            </li>
            <li>
              Pagas por padawan contratado, los precios van desde los $15,000
              pesos hsata $35,000 pesos dependiendo del perfil que contrates.
              Con nosotros no hay pagos ocultos, pagas una sola vez por padawan
              contratado.
            </li>
          </ol>
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
</div>
