<script>
  const links = [
    {
      name: "Backend",
      url: "/padawans/backend-program"
    },
    {
      name: "Frontend",
      url: "/padawans/front-program"
    },
    {
      name: "Móvil",
      url: "/padawans/mobile-program"
    },
    {
      name: "Chatbot",
      url: "/padawans/chatbot-program"
    }
  ];
</script>

<style>
  .programs-wrapper {
    display: flex;
    flex-wrap: wrap;
    max-width: var(--max-width);
    margin: 24px auto 24px;
    font-size: 24px;
  }
  .programs-title {
    color: #909090;
  }
  .links-wrapper {
    margin-left: 30px;
    display: flex;
    flex-wrap: wrap;
  }
  .links-wrapper > * {
    margin: 0 15px;
  }
  .link {
    color: white;
  }
</style>

<div class="programs-wrapper">
  <div class="programs-title">Programas</div>
  <div class="links-wrapper">
    {#each links as { name, url }}
      <a class="link" href={url}>{name}</a>
    {/each}
  </div>
</div>
