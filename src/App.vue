<template>
 <navigation/>

 <router-view/>
 
 <Footer/>
</template>

<script>
import navigation from '@/components/navigation.vue'
import Footer from '@/components/footer.vue'
import spinner from '@/components/spinner.vue'

export default {
  name: 'HomeView',
  components: {
   navigation,
   Footer,
   spinner
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

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

</style>
