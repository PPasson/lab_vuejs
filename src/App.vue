<template>
  <div id='app'>
    <Header/>
    <router-view></router-view>
    <Footer title="Copyright 2020 by Sashigyu"/>
  </div>
</template>

<script>
import Header from "@/components/layout/Header.vue"
import Footer from "@/components/layout/Footer.vue"
export default {
  name: "app",
  components: {
    Header,
    Footer
  }

}
</script>

<style scoped>
  
  .title{
        font-size: 30px;
        color: green;
    }
  
  
</style>