<script>
  //export let segment;
  import Nav from "../../components/Nav.svelte";
</script>

<Nav
  darkMode
  menuList={[{ name: 'Bootcamp', url: '/padawans/bootcamp' }, { name: 'Nosotros', url: '/padawans/about-us' }, { name: 'Club de Programación', url: '/padawans/programming-club' }, { name: 'Contacto', url: '/padawans/contact' }]} />
<slot />
