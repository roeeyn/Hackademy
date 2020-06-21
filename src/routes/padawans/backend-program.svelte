<script>
  import MastersGallery from "../../components/MastersGallery.svelte";
  import Nav from "../../components/Nav.svelte";
  import Hero from "../../components/Hero.svelte";
  import ProgramsNav from "../../components/ProgramsNav.svelte";
  import ParagraphLayout from "../../components/ParagraphLayout.svelte";
  import ParagraphText from "../../components/ParagraphText.svelte";
  import ListLayout from "../../components/ListLayout.svelte";
  import PadawansRoadmap from "../../components/PadawansRoadmap.svelte";
  import PartnerGallery from "../../components/PartnerGallery.svelte";
  import FooterForm from "../../components/FooterForm.svelte";

  const heroText = `El desarrollo de software no es un tema de memoria es un tema de habilidad y talento resolver problemas.`;
  const backendLists = [
    {
      title: "HERRAMIENTAS",
      items: [
        "GIT / GitHub",
        "SCRUM",
        "AWS",
        "Integración continua",
        "NodeJS",
        "Django",
        "MongoDB",
        "PostgresQL"
      ]
    },
    { title: "LENGUAJES", items: ["Python", "JavaScript"] }
  ];
  const galleryContent = {
    text: `Nuestros Masters`,
    images: [
      { src: "/max.png", title: "Max Rodríguez", subtitle: "CTO" },
      { src: "/oscar.png", title: "Oscar Oceguera", subtitle: "ReactJS" },
      {
        src: "/joel.png",
        title: "Joel Montijo",
        subtitle: "Administración de proyectos"
      },
      { src: "/rob.png", title: "Rob Martínez", subtitle: "Python" }
    ]
  };
</script>

<style>
  .program-wrapper {
    background: var(--main-black);
  }
</style>

<svelte:head>
  <title>Backend Program - Hackademy Mx</title>
</svelte:head>

<section class="program-wrapper">
  <Hero image="backend-header.png" btnText="BACKEND" text={heroText} />
  <ProgramsNav />
  <ParagraphLayout
    title="BACKEND"
    subtitle="En este programa trabajamos el desarrollo de API’s, el manejo de
    base de datos y manejo de servidores">
    <ParagraphText>
      Al entrar a este programa formarás parte de un equipo en el cual tu rol
      será desarrollar el backend de una solución que pueda cubrir las
      necesidades de una platafroma web, una app móvil o un chatbot
      conversacional.
    </ParagraphText>
  </ParagraphLayout>
  <ParagraphLayout
    title="INDUSTRIA"
    subtitle="El backend es uno de los elementos más importantes dentro de la
    industria de TI">
    <ParagraphText>
      Dentro de la industria de software hemos visto como cerce la demanda por
      talento con los conocimientos y experiencia suficiente en el desarrollo de
      backend y en el uso de las herramientas que nos permiten desarrollar
      plataformas robustas y seguras.
    </ParagraphText>
    <ParagraphText>
      En todos los programas aprenderas sobre andministración de proyectos
      agiles y Git
    </ParagraphText>
    <ListLayout lists={backendLists} />
  </ParagraphLayout>
  <MastersGallery content={galleryContent} />
  <PadawansRoadmap />
  <PartnerGallery />
  <FooterForm />
</section>
