<script>
  import Nav from "../../components/Nav.svelte";
  export let segment;
</script>

<style>
  img {
    position: absolute;
    top: 2%;
    left: 2%;
  }
</style>

<Nav
  menuList={[{ name: 'Servicios', url: '/enterprise/services' }, { name: 'Nosotros', url: '/enterprise/about-us' }, { name: 'Escuelas e instituciones', url: '/enterprise/schools-institutions' }, { name: 'Contáctanos', url: '/enterprise/contact' }]} />
<img src="/hackademy_logo.svg" alt="Hackademy-logo" />
<slot />
