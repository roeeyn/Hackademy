<script>
  export let lists;
</script>

<style>
  .list-container {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    width: 50%;
  }
  .list-title {
    font-weight: bold;
    font-size: 18px;
    line-height: 204.19%;
    letter-spacing: 0.015em;
  }
  .list {
    max-width: 200px;
    list-style: none;
  }
  .list-item {
    margin-top: 15px;
  }
</style>

<div class="list-container">
  {#each lists as { title, items }}
    <div>
      <div class="list-title">{title}</div>
      <ul class="list">
        {#each items as item}
          <li class="list-item">- {item}</li>
        {/each}
      </ul>
    </div>
  {/each}
</div>
