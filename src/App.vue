<template>
  <div id='app'>
    <Header/>
    <ul>
      
    </ul>
    <router-view></router-view>
  </div>
</template>

<script>
import Header from "@/components/layout/Header.vue"
export default {
  name: "app",
  components: {
    Header
  }

}
</script>

<style scoped>
  
  .title{
        font-size: 30px;
        color: green;
    }
</style>