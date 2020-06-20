<script>
  let isNavbarOpen = false;
  export let menuList;
  export let darkMode = false;
  const toggleNavbar = () => (isNavbarOpen = !isNavbarOpen);
</script>

<style>
  .hamburger-menu {
    position: absolute;
    top: 75px;
    right: 40px;
    z-index: 3;
    cursor: pointer;
  }

  .hamburger-menu > div {
    margin-bottom: 10px;
  }

  .line {
    width: 30px;
    height: 2px;
    background: var(--main-black);
    transition: transform 0.3s ease-in-out;
  }

  .line-dark {
    width: 30px;
    height: 2px;
    background: white;
    transition: transform 0.3s ease-in-out;
  }

  .menu {
    background: white;
    position: fixed;
    height: 100vh;
    width: 100vw;
    z-index: 2;
    transition: clip-path 0.5s ease-out;
    color: var(--main-black);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .menu-dark {
    background: var(--main-black);
    position: fixed;
    height: 100vh;
    width: 100vw;
    z-index: 2;
    transition: clip-path 0.5s ease-out;
    color: white;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .menu-item {
    font-family: Roboto;
    font-weight: bold;
    font-size: 91px;
    line-height: 107px;
    color: var(--main-black);
  }

  .menu-item-dark {
    font-family: Roboto;
    font-weight: bold;
    font-size: 91px;
    line-height: 107px;
    color: white;
  }

  .closed-line-one {
    transform: translateY(6px) rotate(45deg);
  }

  .closed-line-two {
    transform: translateY(-6px) rotate(-45deg);
  }

  .open-clip-path {
    clip-path: circle(120vmax at calc(100% - 70px) 80px);
  }

  .closed-clip-path {
    clip-path: circle(0 at calc(100% - 70px) 80px);
  }

  .link > a {
    text-decoration: none;
  }
  @media screen and (max-width: 920px) {
    .menu-item {
      font-size: 72px;
    }
  }

  @media screen and (max-width: 768px) {
    .menu-item {
      font-size: 22px;
    }
  }
</style>

<main>
  <div class="hamburger-menu" on:click={toggleNavbar}>
    <div
      class={darkMode ? 'line-dark' : 'line'}
      class:closed-line-one={isNavbarOpen} />
    <div
      class={darkMode ? 'line-dark' : 'line'}
      class:closed-line-two={isNavbarOpen} />
  </div>

  <div
    class={darkMode ? 'menu-dark' : 'menu'}
    class:open-clip-path={isNavbarOpen}
    class:closed-clip-path={!isNavbarOpen}>
    {#each menuList as { name, url }}
      <div class="link">
        <a href={url}>
          <div class={darkMode ? 'menu-item-dark' : 'menu-item'}>{name}</div>
        </a>
      </div>
    {/each}
  </div>
</main>
