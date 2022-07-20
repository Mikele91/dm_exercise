<template>
  <div class="container page">
    <div class="row main_row">
      <Login/>
      <Carousel/>
    </div>  
  </div>
</template>

<script>
import Login from './components/Login.vue'
import Carousel from './components/Carousel.vue'


export default {
  name: 'App',
  components: {
    Login,
    Carousel
  }
}
</script>

<style lang="scss">
@import "./assets/style/typography.scss";
#app {
  display: flex;
  justify-content: center;
  align-items: center;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height:100vh;
  background-color: #e7e8ec;
  
  .page{ 
        background-color:white ;
        max-width:75rem;
        height: 80%;
        margin:0 1.25rem;
      .main_row{
        height: 100%;
      }
        
    }
}
</style>
