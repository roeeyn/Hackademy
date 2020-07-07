<script>
  import ParagraphLayout from "../../components/ParagraphLayout.svelte";
  import ParagraphText from "../../components/ParagraphText.svelte";
  import ListLayout from "../../components/ListLayout.svelte";
  import PartnerGallery from "../../components/PartnerGallery.svelte";
  import FooterEnterprise from "../../components/FooterEnterprise.svelte";
  const images = [
    {
      img: "/backend-header.png",
      text: "CLUB DE PROGRAMACIÓN"
    },
    {
      img: "/mobile-header.png",
      text: "PRACTICAS PROFESIONALES"
    },
    {
      img: "/backend-header.png",
      text: "SERVICIO SOCIAL"
    },
    {
      img: "/chatbot-header.png",
      text: "ACTUALIZACIÓN DE PROFESORES Y COLABORADORES"
    },
    {
      img: "/front-header.png",
      text: "PROGRAMAS DE EMPRENDIMIENTO"
    }
  ];
</script>

<style>
  h1 {
    padding-top: 156px;
    font-size: 60px;
    margin: 0 auto 24px;
    max-width: var(--max-width);
  }
  .grid {
    max-width: var(--max-width);
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    /* grid-template-rows: 300px 300px 300px; */
    grid-gap: 30px 20px;
    justify-items: center;
  }
  .grid > div {
    text-align: center;
    padding: 20px 0;
    font-size: 30px;
    color: black;
  }
  .images-container > p {
    font-size: 15px;
    font-weight: 600px;
  }
  .images-container img {
    width: 100%;
  }
</style>

<section class="schools-institutions-wrapper">
  <h1>Escuelas e Institutos</h1>
  <ParagraphLayout
    darkMode={false}
    title="PROGRAMA"
    subtitle="Brinda acceso a tus colaboradores y estudiantes al mejor programa
    de capacitación de america latina">
    <ParagraphText darkMode={false}>
      Hackademy ofrece un set de ventajas a las escuelas e instituciones que
      implementan el programa hacia el interior, contamos con un grupo de
      mentores con una gran experiencia en la industria del software que
      comparten sus conocimientos de manera remota permitiendo aprender desde
      cualquier lugar. Tus profesores, alumnos y colaboradores podrán mejorar
      sus habilidades, realizar sus estancias profesionales y servicio social o
      actualizar sus herramientas y conocimientos para actualizarce.
    </ParagraphText>
  </ParagraphLayout>
  <ParagraphLayout title="IMPLEMENTA" subtitle=" " />
  <div class="grid">
    {#each images as image}
      <div class="images-container">
        <img src={image.img} alt={image.img} />
        <br />
        <p>
          <strong>{image.text}</strong>
        </p>
      </div>
    {/each}
  </div>
  <PartnerGallery
    title="Colaboradores y Clientes"
    showCTA={false}
    darkMode={false} />
  <FooterEnterprise />
</section>
