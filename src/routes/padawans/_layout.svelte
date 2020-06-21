<script>
  //export let segment;
  import Nav from "../../components/Nav.svelte";
</script>
<style>
  img {
    position: absolute;
    top: 2%;
    left: 2%;
  }
</style>
<Nav
  darkMode
  menuList={[{ name: 'Bootcamp', url: '/padawans/bootcamp' }, { name: 'Nosotros', url: '/padawans/about-us' }, { name: 'Club de Programación', url: '/padawans/programming-club' }, { name: 'Programas', url: '/padawans/backend-program' }, { name: 'Contacto', url: '/padawans/contact' }]} />
  <img src="/hackademy_logo.svg" alt="Hackademy-logo">
<slot />
