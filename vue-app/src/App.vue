<script>
import HelloThere from './components/HelloThere.vue'
import HelloWorld from './components/HelloWorld.vue'
import NavBar from './components/NavBar.vue'
import CssTest from './components/CssTest.vue'
import TargetPracticeVue from './components/TargetPractice.vue'
const routes = {
  'HelloWorld':HelloWorld,
  'HelloThere':HelloThere,
  'css':CssTest,
  'TargetPractice':TargetPracticeVue
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
  height: 100%;
}
html, body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
}
.content{
  padding-top: 1vw;
  height: 100%;
  width: 100%;
}
</style>

<template>
  <NavBar :route-links='getRoutes' test="adada"/>
  <component :is="currentView" class="content"/>
</template>
