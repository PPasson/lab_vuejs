<template>
  <div id="demo8">
    <div v-if="type === 'A'">
      A
    </div>
    <div v-else-if="type === 'B'">
      B
    </div>
    <div v-else-if="type === 'C'">
      C
    </div>
    <div v-else>
      Not A/B/C
    </div>

    <div v-if="isShow">
    Blink1
    </div>
    <div v-else>
    Blink2
    </div>

    <div v-show="isShow">
    Blink V-Show
    </div>
  </div>

</template>

<script>
export default {
  name: "Demo8",
  mounted(){
      setInterval(()=>{
          this.isShow = !this.isShow;
      }, 500)
  },
  data() {
    return {
      type: "B",
      isShow: false
    };
  }
};
</script>
   

<style>
</style>>