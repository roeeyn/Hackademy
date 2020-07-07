<script>
  export let image;
  export let text;
  // export let btnText;
  export let darkMode = true;
</script>

<style>
  .hero-wrapper {
    position: relative;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr;
    grid-template-areas: "main";
    height: 100vh;
    color: #ffffff;
  }
  .image {
    object-fit: cover;
    grid-area: main;
    filter: brightness(0.44);
    height: 100%;
    width: 100%;
  }
  .main-text {
    grid-area: main;
    align-self: end;
    max-width: 550px;
    position: relative;
    bottom: 30px;
    justify-self: center;
  }
  .contact-button-wrapper {
    position: absolute;
    bottom: 30px;
    right: 20px;
    display: flex;
    align-items: center;
  }
  .contact-button-wrapper > button {
    width: 65px;
    height: 65px;
    margin-left: 30px;
    border-radius: 50%;
    background: #ffffff;
    border: none;
  }
  @media screen and (max-width: 970px) {
    .contact-button-wrapper {
      display: none;
    }
  }
  .light-text {
    color: black;
  }
</style>

<section class="hero-wrapper">
  <img src={image} class="image" alt="hero" />
  <p class="main-text" class:light-text={!darkMode}>{text}</p>
</section>
