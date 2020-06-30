<script>
  import Nav from "../../components/Nav.svelte";
  // export let segment;
</script>

<Nav
  menuList={[{ name: 'Servicios', url: '/enterprise/services' }, { name: 'Nosotros', url: '/enterprise/about-us' }, { name: 'Escuelas e instituciones', url: '/enterprise/schools-institutions' }, { name: 'Contáctanos', url: '/enterprise/contact' }]} />
<slot />
