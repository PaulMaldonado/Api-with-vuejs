<template>
  <div id="app">
    <Navbar />
    <Api />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Api from './components/Api.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Api
  }
}
</script>

<style>


</style>
