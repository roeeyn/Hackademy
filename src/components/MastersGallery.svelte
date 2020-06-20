<script>
  export let content;
</script>

<style>
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    grid-gap: 20px;
    justify-items: center;
  }
  .gallery-wrapper {
    color: #ffffff;
  }

  .title {
    font-size: 27px;
    line-height: 32px;
    text-align: center;
    letter-spacing: 0.04em;
    max-width: min(1090px, calc(100vw - 24vmin));
    margin: 0 auto 10px;
  }
  .img {
    object-fit: contain;
    width: 100%;
    height: 500px;
    display: block;
  }
</style>

<div class="gallery-wrapper">
  <p class="title">{content.text}</p>
  <div class="grid">
    {#each content.images as { src, title, subtitle }}
      <div>
        <img {src} class="img" alt={`Image of ${title}`} />
        <div>
          <p>{title}</p>
          <p>{subtitle}</p>
        </div>
      </div>
    {/each}
  </div>
</div>
