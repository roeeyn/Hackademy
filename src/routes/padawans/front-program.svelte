<script>
  import MastersGallery from "../../components/MastersGallery.svelte";

  import ParagraphLayout from "../../components/ParagraphLayout.svelte";
  import ProgramsNav from "../../components/ProgramsNav.svelte";

  import Nav from "../../components/Nav.svelte";
  import Hero from "../../components/Hero.svelte";
  import PadawansRoadmap from "../../components/PadawansRoadmap.svelte";
  import PartnerGallery from "../../components/PartnerGallery.svelte";
  import FooterForm from "../../components/FooterForm.svelte";
  import ParagraphText from "../../components/ParagraphText.svelte";
  import ListLayout from "../../components/ListLayout.svelte";
  const heroText =
    "El desarrollo de software no es un tema de memoria es un tema de habilidad y talento resolver problemas.";
  const lists = [
    {
      title: "HERRAMIENTAS",
      items: [
        "GIT / GitHub",
        "AWS",
        "Integración continua",
        "TypeScript",
        "JavaScript",
        "Webpack",
        "SCRUM"
      ]
    },
    { title: "LENGUAJES", items: ["Angular", "ReactJS"] }
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
      { src: "/jesus.png", title: "Jesús Lara", subtitle: "Angular" }
    ]
  };
</script>

<style>
  .program-wrapper {
    background: var(--main-black);
  }
</style>

<svelte:head>
  <title>Frontend Program - Hackademy Mx</title>
</svelte:head>

<section class="program-wrapper">
  <Hero image="front-header.png" btnText="FRONTEND" text={heroText} />
  <ProgramsNav />
  <ParagraphLayout
    title="FRONTEND"
    subtitle="En el programa de Frontend trabajamos con Angular o ReactJS que
    son las herramientas más usadas en la industria">
    <ParagraphText>
      Al entrar a este programa formarás parte de un equipo en el cual tendrás
      el rol de desarrollar el frontend de una solución que puede cubrir las
      necesidades de los usuarios.
    </ParagraphText>
  </ParagraphLayout>
  <ParagraphLayout
    title="INDUSTRIA"
    subtitle="El frontend es uno de los elementos del desarrollo que más a
    evolucionado en los ultimos años">
    <ParagraphText>
      Dentro de la industria de software hemos visto como cerce la demanda por
      talento con los conocimientos y experiencia suficiente en el desarrollo de
      frontend y en el uso de las herramientas que nos permiten desarrollar
      plataformas robustas y seguras.
    </ParagraphText>
    <ParagraphText>
      En todos los programas aprenderas sobre andministración de proyectos
      agiles y Git
    </ParagraphText>
    <ListLayout {lists} />
  </ParagraphLayout>
  <MastersGallery content={galleryContent} />
  <PadawansRoadmap />
  <PartnerGallery />
  <FooterForm />
</section>
