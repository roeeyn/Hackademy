<script>
  import Hero from "../../components/Hero.svelte";
  import ParagraphLayout from "../../components/ParagraphLayout.svelte";
  import ParagraphText from "../../components/ParagraphText.svelte";
  import ListLayout from "../../components/ListLayout.svelte";
  import PartnerGallery from "../../components/PartnerGallery.svelte";
  import FooterEnterprise from "../../components/FooterEnterprise.svelte";
  const lists = [
    {
      title: "PROGRAMAS",
      items: ["Backend", "Frontend", "Móvil", "Chatbot"]
    },
    {
      title: "SERVICIOS",
      items: [
        "Contratación de talento",
        "Capacitación empresarial",
        "Bootcamp escolar",
        "Startup builder",
        "Desarrollo de software",
        "Consultoría"
      ]
    },
    {
      title: "ACADÉMICO",
      items: [
        "Servicio social",
        "Residencias profesionales",
        "Webinars",
        "Hackathones",
        "Apoyo a profesores"
      ]
    }
  ];
</script>

<Hero
  image="padawans.png"
  text="El talento de nuestro equipo es lo que logra que nuestras empresas se
  desarrollen"
  btnText="Nosotros"
  darkMode={true} />
<ParagraphLayout
  darkMode={false}
  title="Nosotros"
  subtitle="Hackademy nace con el objetivo de disminuir el deficit de talento
  dentro de la industria del desarrollo de software">
  <ParagraphText darkMode={false}>
    Cada vez es más difícil encontrar el talento que tu empresa requiere y esto
    se va agravando año con año y es por esto que desarrollamos un modelo donde
    nuestros estudiantes (Padawans) mejoran sus habilidades a través de la
    práctica desarrollando un proyecto real durante 16 semanas y
    especializándose en un área del desarrollo de software.
    <br />
    Con esto la empresa que busca contratar talento puede conocer las
    habilidades, fortalezas y conocimientos de la persona que están
    entrevistando.
  </ParagraphText>
  <ParagraphText darkMode={false}>
    Para que el modelo funcione trabajamos con empresas y organizaciones con las
    que construimos un pool de proyectos interesantes en los cuales participan
    nuestros padawans.
  </ParagraphText>
  <ListLayout {lists} />
</ParagraphLayout>
<ParagraphLayout
  darkMode={false}
  title="NOSOTROS"
  subtitle="Hackademy busca democratizar el acceso a entrenamiento de calidad y
  el acceso a ofertas laborales para que empresas y personas puedan crecer de la
  mejor forma posible." />
<PartnerGallery
  title="Colaboradores y Clientes"
  showCTA={false}
  darkMode={false} />
<FooterEnterprise />
