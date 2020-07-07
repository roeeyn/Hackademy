<script>
  import Nav from "../../components/Nav.svelte";
  let selectedOption = 0;
  const slideTexts = [
    {
      heading: `Desarrollamos Talento`,
      paragraphOne: `En Hackademy sabemos que hay mucho contenido en la red sobre
    programación desde cero más lo poco o mucho que vemos en la
    escuela.`,
      paragraphTwo: `Es por esto que Hackademy no es un curso, nos enfocamos en el
    nivel más alto de la capacitación y trabajamos directamente en
    la practica y la implementación de los conocimientos que han
    adquirido previamente.`
    },
    {
      heading: `Trabajamos con los mejores`,
      paragraphOne: `Para poder obtener experiencia, en esta industria tan competida, necesitas tener una imagen general de las herramientas que estan cambiando el panorama.`,
      paragraphTwo: `Al entrar a Hackademy obtienes acceso a herramientas empresariales de GitHub y AWS de manera gratuita.`
    },
    {
      heading: `Sin costo, sin cobros`,
      paragraphOne: `La educación siempre debe de ser de facil acceso para mejorar las condiciones en las que vivimos y estos por esto que Hackademy nunca te cobrará un solo centavo.`,
      paragraphTwo: `En Hackademy tu inversión es tú tiempo y tú conocimiento, de lo demás nos encargamos nosotros.`
    }
  ];

  const slideImages = [
    "/padawans-slide-one.png",
    "/padawans-slide-two.png",
    "/padawans-slide-three.png"
  ];

  const safelyIncreaseOption = () => {
    selectedOption = selectedOption === 2 ? 0 : selectedOption + 1;
  };
  const safelyDecreaseOption = () => {
    selectedOption = selectedOption === 0 ? 2 : selectedOption - 1;
  };

  const selectOption = optionNumber => (selectedOption = optionNumber);
  const slidesInterval = setInterval(safelyIncreaseOption, 5000);
</script>

<style>
  .padawans-main {
    display: grid;
    height: 100vh;
    width: 100vw;
    grid-template-columns: minmax(600px, 1fr) minmax(450px, 660px) 170px;
    background: var(--main-black);
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
    color: #fff;
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
    /* display: flex; */
    display: none;
    flex-direction: column;
    margin: 0 20px 20px;
  }

  .slider-button {
    height: 40px;
    width: 40px;
    border-radius: 50%;
    background: transparent;
    border: 1px solid white;
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
  .indicator {
    border-radius: 50%;
    width: 15px;
    height: 15px;
    cursor: pointer;
    background-color: rgba(128, 128, 128, 0.5);
  }
  .active-indicator {
    background-color: white;
  }
  .carrousel-indicators-wrapper {
    width: 10px;
    height: 100px;
    position: absolute;
    top: 50%;
    right: 4%;
  }
</style>

<!--
FIXES TODO: 
  - el click se debe de poder hacer en saber más y el botón
-->

<svelte:head>
  <title>Padawans - Hackademy Mx</title>
</svelte:head>

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
          <a href="/padawans/bootcamp">
            <button class="more-button">
              <img src="more-arrow.svg" alt="Flecha botón para saber más" />
            </button>
          </a>
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
    <div class="carrousel-indicators-wrapper">
      <p
        class="indicator"
        class:active-indicator={selectedOption == 0}
        on:click={() => selectOption(0)} />
      <p
        class="indicator"
        class:active-indicator={selectedOption == 1}
        on:click={() => selectOption(1)} />
      <p
        class="indicator"
        class:active-indicator={selectedOption == 2}
        on:click={() => selectOption(2)} />
    </div>
    <div class="slider-buttons-wrapper">
      <button class="slider-button" on:click={safelyDecreaseOption}>
        <img
          src="previous-slider-arrow.svg"
          alt="Flecha para imagen previa del slider" />
      </button>
      <button class="slider-button" on:click={safelyIncreaseOption}>
        <img
          src="next-slider-arrow.svg"
          alt="Flecha para imagen siguiente del slider" />
      </button>
    </div>
  </div>
</div>
