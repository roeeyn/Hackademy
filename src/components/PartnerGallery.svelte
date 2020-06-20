<script>
  export let title = "Nuestros Partners";
  export let images = [
    "/github.png",
    "/aws.png",
    "/claribot.png",
    "/unesco.png",
    "/tomato.png",
    "/ashoka.png",
    "/supercivicos.png"
  ];
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
</style>

<section class="gallery-wrapper">
  <p class="title">{title}</p>
  <div class="grid">
    {#each images as image}
      <img
        class="placeholder-image"
        src={image}
        alt={`Partner ${image.split('.')[0]}`} />
    {/each}
  </div>
</section>
