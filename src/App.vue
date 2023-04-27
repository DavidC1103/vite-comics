  <script>
    import Header from '../src/components/Header.vue'
    import Main from '../src/components/Main.vue'
    import Footer from './components/Footer.vue'
    
    export default{
      name : 'App',
      components:{
        Header,
        Main,
        Footer
      },
      data(){
        return{
          
        }
      }
      
    }
  </script>

<template>
  <Header />
  <Main />
  <Footer />
</template>


<style lang="scss">
  @use '../src/main.scss'as *;
</style>