<script>
  export let title = "";
  export let subtitle = "";
  export let darkMode = true;
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
  .light-grid {
    color: #000;
  }
  .title {
    font-size: 12px;
    line-height: 14px;
    letter-spacing: 0.04em;
    color: #909090;
  }
  .light-title {
    color: #202020;
  }
  .subtitle {
    font-size: 27px;
    line-height: 32px;
    letter-spacing: 0.04em;
    margin-bottom: 24px;
  }
  .light-subtitle {
    color: #202020;
  }
</style>

<section class="grid" class:light-grid={!darkMode}>
  <p class="title" class:light-title={!darkMode}>{title}</p>
  <div>
    <p class="subtitle" class:light-subtitle={!darkMode}>{subtitle}</p>
    <slot />
  </div>
</section>
