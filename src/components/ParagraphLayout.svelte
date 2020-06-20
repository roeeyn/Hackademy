<script>
  export let title;
  export let subtitle;
</script>

<style>
  .grid {
    max-width: var(--max-width);
    display: grid;
    grid-template-columns: 90px 1fr;
    grid-column-gap: 24px;
    margin: 0 auto 24px;
    color: #fff;
  }
  .title {
    font-size: 12px;
    line-height: 14px;
    letter-spacing: 0.04em;
    color: #909090;
  }
  .subtitle {
    font-size: 27px;
    line-height: 32px;
    letter-spacing: 0.04em;
    margin-bottom: 24px;
  }
</style>

<section class="grid">
  <p class="title">{title}</p>
  <div>
    <p class="subtitle">{subtitle}</p>
    <slot />
  </div>
</section>
