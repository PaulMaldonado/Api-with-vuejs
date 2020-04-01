<template>
  <div id="app">
    <Navbar />
    <Api />
    <Form />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Api from './components/Api.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Api,
  }
}
</script>

<style>


</style>
