<template>
  <div id="app">
    <Navbar/>
    <Header/>
    <div class="container-fluid">
        <Services class="page-section"/>
        <Testimonies class="page-section"/>
        <Contact class="page-section"/>
    </div>
  </div>
</template>

<script>

import Navbar from './components/navbar-component';
import Header from './components/header-component';
import Services from './components/services-section-component';
import Testimonies from './components/testimonies-section-component';
import Contact from './components/contact-section-component';

export default {
  name: 'App',
  components: {
    Navbar,
    Header,
    Services,
    Testimonies,
    Contact
  }
}
</script>

<style scoped>
  #app {
    width: 100%;
    min-height: 100vh;
    padding-bottom: 1em;
  }
  .page-section {
    margin-top: 1.5em;
  }
  
</style>
