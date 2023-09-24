<template>
  <div id="app">
    <NavBar />
    <router-view />
    <FooterComp />
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue';
import FooterComp from './components/FooterComp.vue';

export default {
  name: 'App',
  components: {
    NavBar,
    FooterComp
  }
}
</script>
