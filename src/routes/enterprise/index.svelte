<script>
  import NavEnterprise from "../../components/NavEnterprise.svelte";
  let selectedOption = 0;

  const slideTexts = [
    {
      heading: `Desarrollamos Talento`,
      paragraphOne: `Nuestro programa se enfoca en mejorar las habilidades 
      técnicas de las personas para que tu empresa pueda contartar al mejor talento.`,
      paragraphTwo: ``
    },
    {
      heading: `Desarollamos soluciones`,
      paragraphOne: `Nuestro enfoque es construir software que solucione problemas de la vida real`,
      paragraphTwo: `Si estás por iniciar un proyecto, quieres validar o necesitas una solución para
      tu empresa, no dudes en contactarnos.`
    },
    {
      heading: `Colabora con nosotros`,
      paragraphOne: `Queremos que la comunidad sea más grande y fuerte.`,
      paragraphTwo: `Lleva a Hackademy a tu escuela, comunidad u organización.`
    }
  ];

  const slideImages = [
    "/padawans-slide-one.png",
    "/padawans-slide-three.png",
    "/padawans-slide-two.png"
  ];

  const safelyIncreaseOption = () => {
    selectedOption = selectedOption === 2 ? 0 : selectedOption + 1;
  };
  const safelyDecreaseOption = () => {
    selectedOption = selectedOption === 0 ? 2 : selectedOption - 1;
  };

</script>

<style>
  .padawans-main {
    display: grid;
    height: 100vh;
    width: 100vw;
    grid-template-columns: minmax(600px, 1fr) minmax(450px, 660px) 170px;
    background: white;
    overflow: hidden;
  }

  @media screen and (max-width: 1100px) {
    .padawans-main {
      grid-template-columns: 1fr;
      grid-template-rows: 4fr 1fr;
    }
    .carousel-images {
      display: none;
    }
    .carousel-controller {
      align-items: flex-start;
      justify-content: center;
    }
    .slider-buttons-wrapper {
      flex-direction: row;
    }
  }

  .carousel-images {
    background: grey;
  }

  .carousel-image {
    object-fit: cover;
    height: 100%;
    width: 100%;
  }

  .carousel-controller {
    display: flex;
    align-items: flex-end;
  }

  .text-wrapper {
    color: var(--main-black);
    display: flex;
    height: 100%;
    justify-content: center;
    align-items: center;
  }

  .text-container {
    max-width: 525px;
  }

  .text-container > h2 {
    font-weight: bold;
    font-size: 60px;
    line-height: 70px;
    margin-bottom: 42px;
  }

  .text-container > div > p {
    max-width: 325px;
    margin-bottom: 20px;
  }

  .slider-buttons-wrapper {
    display: flex;
    flex-direction: column;
    margin: 0 20px 20px;
  }

  .slider-button {
    height: 40px;
    width: 40px;
    border-radius: 50%;
    background: transparent;
    border: 1px solid var(--main-black);
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    margin-top: 12px;
  }

  .slider-button > img {
    margin: 0;
  }

  .more-button {
    height: 35px;
    width: 35px;
    border-radius: 50%;
    border: none;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
  }

  .more-wrapper {
    display: flex;
    align-items: center;
  }

  .more-wrapper > * {
    margin-right: 20px;
  }
</style>

<svelte:head>
  <title>Padawans - Hackademy Mx</title>
</svelte:head>

<NavEnterprise />

<div class="padawans-main">
  <div class="text-section">
    <div class="text-wrapper">
      <div class="text-container">
        <h2>{slideTexts[selectedOption].heading}</h2>
        <div>
          <p>{slideTexts[selectedOption].paragraphOne}</p>
          <p>{slideTexts[selectedOption].paragraphTwo}</p>
        </div>
        <div class="more-wrapper">
          <strong>Saber más</strong>
          <button class="more-button">
            <img src="more-arrow.svg" alt="Flecha botón para saber más" />
          </button>
        </div>
      </div>
    </div>
  </div>
  <div class="carousel-images">
    <img
      class="carousel-image"
      src={slideImages[selectedOption]}
      alt={`Imagen ${selectedOption + 1} del slider`} />
  </div>
  <div class="carousel-controller">
    <div class="slider-buttons-wrapper">
      <button class="slider-button" on:click={safelyDecreaseOption}>
        <img
          src="previous-slider-arrow-black.svg"
          alt="Flecha para imagen previa del slider" />
      </button>
      <button class="slider-button" on:click={safelyIncreaseOption}>
        <img
          src="next-slider-arrow-black.svg"
          alt="Flecha para imagen siguiente del slider" />
      </button>
    </div>
  </div>
</div>
