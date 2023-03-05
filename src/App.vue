<script>
import Header from './Header.vue'
import HeaderContent from './HeaderContent.vue'
import Content from './Content.vue'
import Footer from './Footer.vue'

export default {
  components: {
    Header,
    HeaderContent,
    Content,
    Footer
  },
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<template>
  <div id="app">
    <header class="sticky-top">
      <Header></Header>
    </header>
    <HeaderContent />
    <Content />
    <Footer></Footer>
  </div>
</template>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}


</style>
