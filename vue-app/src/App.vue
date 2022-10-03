<script>
import HelloWorld from './components/HelloWorld.vue'
import NavBar from './components/NavBar.vue'

const routes = {
  '/':HelloWorld,
  'asd':HelloWorld  
}

export default {
  name: 'App',
  components: {
    HelloWorld,
    NavBar
  },
  data() {
    return {
      currentPath: window.location.hash
    }
  },
  computed: {
    currentView() {
      return routes[this.currentPath.slice(1) || '/'] || HelloWorld
    },
    getRoutes(){
      let output = [Object.values(routes),Object.keys(routes)]
      output = Object
      .entries(routes)
      .map(([key, value]) => [value, key]);

      Object.fromEntries(output);
      return output;
    }
  },
  mounted() {
    window.addEventListener('hashchange', () => {
      this.currentPath = window.location.hash
		})
  } 
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>

<template>
  <NavBar :route-links='getRoutes' test="adada"/>
  <img alt="Vue logo" src="./assets/logo.png">
  <component :is="currentView" />
</template>
