<script>
  import Nav from "../../components/Nav.svelte";
  import Hero from "../../components/Hero.svelte";
  import ProgramsNav from "../../components/ProgramsNav.svelte";
  import ParagraphLayout from "../../components/ParagraphLayout.svelte";
  import ParagraphText from "../../components/ParagraphText.svelte";
  import ListLayout from "../../components/ListLayout.svelte";
  import MastersGallery from "../../components/MastersGallery.svelte";
  import PartnerGallery from "../../components/PartnerGallery.svelte";
  import FooterForm from "../../components/FooterForm.svelte";
  const heroText =
    "El desarrollo de software no es un tema de memoria es un tema de habilidad y talento resolver problemas.";
  const lists = [
    {
      title: "HERRAMIENTAS",
      items: [
        "GIT / GitHub",
        "AWS",
        "Integración continua",
        "React Native",
        "MongoDB"
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
      { src: "/jesus.png", title: "Jesús Lara", subtitle: "React Native" }
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

<Nav />

<section class="program-wrapper">
  <Hero image="mobile-header.png" text={heroText} btnText="MÓVIL" />
  <ProgramsNav />
  <ParagraphLayout
    title="MÓVIL"
    subtitle="En este programa trabajamos con React Native una de las
    herramientas con mayor demanda para el desarrollo móvil">
    <ParagraphText>
      Al entrar a este programa formarás parte de un equipo en el cual tendrás
      el rol de desarrollar la app móvil de una solución que consuma API y haga
      uso de otros dispositivos.
    </ParagraphText>
  </ParagraphLayout>
  <ParagraphLayout
    title="Industria"
    subtitle="El desarrollo de aplicaciones moviles en una de las áreas de mayor
    crecimiento en los últimos 10 años y cada vez hay más empresas buscando
    talento que cubra estos perfiles.">
    <ParagraphText>
      Dentro de la industria de software hemos visto como cerce la demanda por
      talento con los conocimientos y experiencia suficiente en el desarrollo de
      móvil y en el uso de las herramientas que nos permiten desarrollar
      plataformas robustas y seguras.
    </ParagraphText>
    <ListLayout {lists} />
  </ParagraphLayout>
  <MastersGallery content={galleryContent} />
  <PartnerGallery />
  <FooterForm />
</section>
