<script>
  import Nav from "../../components/Nav.svelte";
  import Hero from "../../components/Hero.svelte";
  import ParagraphLayout from "../../components/ParagraphLayout.svelte";
  import ParagraphText from "../../components/ParagraphText.svelte";
  import ProgramsNav from "../../components/ProgramsNav.svelte";
  import ListLayout from "../../components/ListLayout.svelte";
  import PadawansRoadmap from "../../components/PadawansRoadmap.svelte";
  import PartnerGallery from "../../components/PartnerGallery.svelte";
  import FooterForm from "../../components/FooterForm.svelte";
  const heroText = `Hackademy no es un curso, nos enfocamos en el nivel más alto de la capacitación y trabajamos directamente en la practica y la implementación de los conocimientos que han adquirido previamente.`;
  const aboutUsLists = [
    {
      title: "PROCESO",
      items: [
        "Registro en el club de programación",
        "Entrevista",
        "Firma de carta compromiso",
        "Acceso al entrenamieto técnico",
        "Acceso a la agenda de entrevistas"
      ]
    },
    {
      title: "BENEFICIOS",
      items: [
        "Acceso a GitHub",
        "Acceso a AWS educate",
        "Acceso a webinars",
        "Mejora en las habilidades",
        "Acceso a entrevistas de empleo",
        "Acceso a becas del 100%"
      ]
    }
  ];
  const menuList = [
    {
      name: "Bootcamp",
      url: "/padawans/bootcamp"
    },
    {
      name: "Nosotros",
      url: "/padawans/about-us"
    },
    {
      name: "Club de Programación",
      url: "/padawans/programming-club"
    },
    {
      name: "Programas",
      url: "/padawans/backend-program"
    },
    {
      name: "Contacto",
      url: "/padawans/contact"
    }
  ];
  const darkMode = true;
</script>

<style>
  .about-us-wrapper {
    background: var(--main-black);
  }
</style>

<svelte:head>
  <title>Padawans - Hackademy Mx</title>
</svelte:head>

<section class="about-us-wrapper">
  <Hero image="about-us-header.png" text={heroText} btnText="HACKADEMY" />
  <ProgramsNav />
  <ParagraphLayout
    title="THE STORY"
    subtitle="Hackademy es un entrenamiento de alto rendimiento donde ponemos
    manos a la obra y, durante 16 semanas, desarrollamos un prototipo funcional
    de una solucion a un problema del mundo real. Para desarrollar este
    prototipo seguiremos el proceso completo del desarrollo de software">
    <ParagraphText>
      En Hackademy sabemos que hay mucho contenido en la red sobre programación
      desde cero más lo poco o mucho que vemos en la escuela.
    </ParagraphText>
    <ParagraphText>
      Es por esto que Hackademy no es un curso, nos enfocamos en el nivel más
      alto de la capacitación y trabajamos directamente en la practica y la
      implementación de los conocimientos que han adquirido previamente.
    </ParagraphText>
  </ParagraphLayout>
  <ParagraphLayout
    title="THE STORY"
    subtitle="Desarrolla tu talento a travez de la practica y con apoyo de
    mentores que compartiran contigo su experiencia.">
    <ParagraphText>
      Nuestro compromiso es que desarrolles todo tu potencial y que obtengas tu
      primer empleo o mejores el que tienes demostrando que tienes todas las
      herramientas necesarias y el talento que la industria demanda.
    </ParagraphText>
    <ParagraphText>
      Para lograr esto hemos desarrollado un modelo que se enfoca 100% a la
      práctica donde aplicaras tus conocimientos en proyectos reales
    </ParagraphText>
    <ListLayout lists={aboutUsLists} />
  </ParagraphLayout>
  <PadawansRoadmap />
  <PartnerGallery />
  <FooterForm />
</section>
