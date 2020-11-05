<template>
   <b-navbar toggleable="lg" type="dark" variant="dark">
    <b-navbar-brand href="#" class="navbar-brand">Ares Datos</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item href="#" class="active">Home</b-nav-item>
        <b-nav-item href="#">Services</b-nav-item>
        <b-nav-item href="#">Our Clients</b-nav-item>
        <b-nav-item href="#">Contact Us</b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>

export default {
    name: 'Navbar',
}
</script>

<style scoped>
    .navbar {
      display: flex;
      flex-direction: row;
      align-items: center;
    }
    .navbar-brand, .navbar-link {
      font-weight: bold;
    }
    #nav-collapse {
      display: flex;
      flex-direction: row;
      justify-content: flex-end;
    } 
</style>