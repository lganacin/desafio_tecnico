<template>
  <Navbar/>
  <router-view/>
  <Footer/>
</template>

<script>
import Footer from './components/Footer.vue'
import Navbar from './components/Navbar.vue'

export default {
  components:{
    Footer,
    Navbar
}
}
</script>

<style>
* {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  padding: 0;
  margin: 0;
  box-sizing: border-box; 
   
}

  .main-container {
    margin: 50px;
    min-height: 620px;
  }

  h1 {
    text-align: center;

  }
</style>
