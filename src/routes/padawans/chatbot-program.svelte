<script>
  import MastersGallery from "../../components/MastersGallery.svelte";

  import ParagraphLayout from "../../components/ParagraphLayout.svelte";

  import Nav from "../../components/Nav.svelte";
  import Hero from "../../components/Hero.svelte";
  import PadawansRoadmap from "../../components/PadawansRoadmap.svelte";
  import PartnerGallery from "../../components/PartnerGallery.svelte";
  import FooterForm from "../../components/FooterForm.svelte";
  import ParagraphText from "../../components/ParagraphText.svelte";
  import ListLayout from "../../components/ListLayout.svelte";
  import ProgramsNav from "../../components/ProgramsNav.svelte";
  const heroText = `El desarrollo de software no es un tema de memoria es un tema de habilidad y talento resolver problemas.`;
  const lists = [
    {
      title: "HERRAMIENTAS",
      items: [
        "GIT / GitHub",
        "AWS",
        "Integración continua",
        "NodeJS",
        "Django",
        "Dialogflow",
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
        src: "/magaly.png",
        title: "Magaly Peña",
        subtitle: "Administración de proyectos"
      },
      { src: "/fer.png", title: "Fer Ochoa", subtitle: "Chatbot" }
    ]
  };
</script>

<style>
  .program-wrapper {
    background: var(--main-black);
  }
</style>

<svelte:head>
  <title>Chatbot - Hackademy Mx</title>
</svelte:head>

<Nav />
<div class="program-wrapper">
  <Hero image="chatbot-header.png" text={heroText} btnText="CHATBOT" />
  <ProgramsNav />
  <ParagraphLayout
    title="CHATBOT"
    subtitle="En este programa trabajamos el desarrollo de chatbot
    conversacionales usando diferentes herramientas">
    <ParagraphText>
      Al entrar a este programa formarás parte de un equipo en el cual tendrás
      el rol de desarrollar un chatbot que pueda consumir API’s y birndar
      servicios automatizados.
    </ParagraphText>
  </ParagraphLayout>
  <ParagraphLayout
    title="INDUSTRIA"
    subtitle="En los últimos años ha crecido la demanda del desarrollo de
    chatbot por ser una herramienta versátil.">
    <ParagraphText>
      Dentro de la industria de software hemos visto como cerce la demanda por
      talento con los conocimientos y experiencia suficiente en el desarrollo de
      chatbot y en el uso de las herramientas que nos permiten desarrollar
      plataformas robustas y seguras.
    </ParagraphText>
    <ListLayout {lists} />
  </ParagraphLayout>
  <MastersGallery content={galleryContent} />
  <PadawansRoadmap />
  <PartnerGallery />
  <FooterForm />
</div>
