<script>
  import Nav from "../../components/Nav.svelte";
  import Hero from "../../components/Hero.svelte";
  import ProgramsNav from "../../components/ProgramsNav.svelte";
  import ParagraphLayout from "../../components/ParagraphLayout.svelte";
  import ParagraphText from "../../components/ParagraphText.svelte";
  import MastersGallery from "../../components/MastersGallery.svelte";
  import PadawansRoadmap from "../../components/PadawansRoadmap.svelte";
  import PartnerGallery from "../../components/PartnerGallery.svelte";
  import FooterForm from "../../components/FooterForm.svelte";
  const heroText = `“El software se está comiendo el mundo”
-  Marc Andreessen`;
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
  <title>Programming Club - Hackademy Mx</title>
</svelte:head>

<Nav />
<div class="program-wrapper">
  <Hero image="padawans.png" text={heroText} btnText="Club" />
  <ProgramsNav />
  <ParagraphLayout
    title="CLUB"
    subtitle="Para nosotros la mejor forma de aprender es practicar y practicar
    para ir mejorando.">
    <ParagraphText>
      El club de programación es un espacio abierto donde buscamos que todas las
      personas se animen a experimentar la programación de la mejor forma:
      “programando”.
    </ParagraphText>
    <ParagraphText>
      Dentro del club de programación compartimos contenido que ha sido
      seleccionado por nuestros mentores y que se enfoca a cubrir los temas
      básicos de la programación para despues poner manos a la obra en 7
      ejercicios de logica donde se aplica lo que vemos en el contenido.
    </ParagraphText>
  </ParagraphLayout>
  <ParagraphLayout
    title="CLUB"
    subtitle="El club de programación es el primer paso para entrar a Hackademy.">
    <ParagraphText>
      Si bien el club de programación es el inicio del proceso para entrar a
      Hackademy no es un espacio exclusivo para Hackademy ya que buscamos que
      más personas inicien su camino dentro del mundo de la programación. Si no
      has decidido entrar a Hackademy o solamente quieres practicar elementos de
      logica puedes aplicar al club cuantas veces creas necesario.
    </ParagraphText>
    <ParagraphText>
      EL club lo vemos como parte del camino para cualquier rumbo que quieras
      tomar, aprenderas a desarrollar soluciones basadas en la logica y a ser
      autosuficiente en la busqueda de conocimiento lo cual te brinda una
      ventaja competitiva sobre cualquier estudiante o egresado promedio.
    </ParagraphText>
  </ParagraphLayout>
  <MastersGallery content={galleryContent} />
  <PadawansRoadmap />
  <PartnerGallery />
  <FooterForm />
</div>
