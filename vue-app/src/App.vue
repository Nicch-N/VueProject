<script>
import HelloThere from './components/HelloThere.vue'
import HelloWorld from './components/HelloWorld.vue'
import NavBar from './components/NavBar.vue'

const routes = {
  '/':HelloWorld,
  'asd':HelloThere  
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
      //last page is for if route not found
      //currently set to helloWorld
    },
    getRoutes(){
      let output = []
      output = Object
      .entries(routes)
      .map(([key, value]) => [value.name, '#'+key]);
      output = Object.fromEntries(output)
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
  <component :is="currentView" />
</template>
