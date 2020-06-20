<script>
  let isNavbarOpen = false;

  const toggleNavbar = () => (isNavbarOpen = !isNavbarOpen);

  const menuList = [
    {
      name: "Bootcamp",
      url: "/padawans/bootcamp"
    },
    {
      name: "Nosotros",
      url: "/padawans/about-us"
    },
    {
      name: "Club de Programación",
      url: "/padawans/programming-club"
    },
    {
      name: "Programas",
      url: "/padawans/backend-program"
    },
    {
      name: "Contacto",
      url: "/padawans/contact"
    }
  ];

  $: console.log(isNavbarOpen);
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
    background: #fff;
    transition: transform 0.3s ease-in-out;
  }

  .menu {
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
    color: #ffffff;
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
    <div class="line" class:closed-line-one={isNavbarOpen} />
    <div class="line" class:closed-line-two={isNavbarOpen} />
  </div>

  <div
    class="menu"
    class:open-clip-path={isNavbarOpen}
    class:closed-clip-path={!isNavbarOpen}>
    {#each menuList as { name, url }}
      <div class="link">
        <a href={url}>
          <div class="menu-item">{name}</div>
        </a>
      </div>
    {/each}
  </div>
</main>
