<script>
  import { goto } from "@sapper/app";
  export let title = "Nuestros Partners";
  export let darkMode = true;
  export let showCTA = true;
  export let images = [
    "/github.png",
    "/aws.png",
    "/claribot.png",
    "/unesco.png",
    "/tomato.png",
    "/ashoka.png",
    "/supercivicos.png"
  ];
  const goToForm = () => goto("/padawans/programming-club#club-form");
</script>

<style>
  .gallery-wrapper {
    max-width: var(--max-width);
    margin: 0 auto;
    padding-bottom: 60px;
  }
  .title {
    font-size: 28px;
    margin: 60px 0 32px 0;
    line-height: 33px;
    letter-spacing: 0.01em;
    color: #ffffff;
  }
  .light-title {
    color: black;
  }
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    grid-gap: 20px;
    justify-items: center;
  }
  .placeholder-image {
    padding: 6px;
    width: 220px;
    height: 220px;
    background: #c4c4c4;
    border-radius: 10px;
    object-fit: scale-down;
  }
  .cta-wrapper {
    width: 100%;
    padding: 125px 0;
    justify-content: center;
    display: flex;
  }

  .call-to-action {
    padding: 32px 36px;
    border-radius: 22px;
    letter-spacing: 0.055em;
    font-weight: bold;
    font-size: 34px;
    cursor: pointer;
    transition: transform ease 500ms;
  }

  @media screen and (max-width: 800px) {
    .call-to-action {
      font-size: 26px;
      width: 50%;
    }
  }

  .call-to-action:hover {
    transform: translateY(-12px);
  }
  .call-to-action:active {
    transform: translateY(-4px);
  }
</style>

{#if showCTA}
  <div class="cta-wrapper">
    <button class="call-to-action" on:click={goToForm}>
      Iniciar el camino del Padawan
    </button>
  </div>
{/if}
<section class="gallery-wrapper">
  <p class="title" class:light-title={!darkMode}>{title}</p>
  <div class="grid">
    {#each images as image}
      <img
        class="placeholder-image"
        src={image}
        alt={`Partner ${image.split('.')[0]}`} />
    {/each}
  </div>
</section>
