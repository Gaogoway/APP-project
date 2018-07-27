<template>
  <div id="app">
    
    <app-header></app-header>
    <nav-list></nav-list>
  </div>
</template>

<script>
import appHeader from "./components/common/header/header.vue";
import navList from "./components/pages/home/home.vue";
export default {
  name: 'App',
  components: {
    	appHeader,
    	navList
  }
}
</script>

<style>

</style>
