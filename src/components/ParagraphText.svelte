<script>
  export let darkMode = true;
</script>

<style>
  .text {
    font-size: 13px;
    line-height: 27px;
    letter-spacing: 0.04em;
    color: #c7c7c7;
    max-width: 720px;
  }
  .light-text {
    color: #141414;
  }
</style>

<p class="text" class:light-text={!darkMode}>
  <slot />
</p>
