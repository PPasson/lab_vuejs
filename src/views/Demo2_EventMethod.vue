<template>
  <div app="demo2">
    <h1>Event and Method</h1>
    <button v-on:click="clickMe">Click Me</button>
    <button v-on:click="clickMe2('welcome to Vue')">Click Me2</button>
    <button @click="clickMe2('welcome to Sashigyu')">Click Me3</button>
    <h2>{{getTimeStamp()}}</h2>
  </div>
</template>

<script>
export default {
  name: "Demo2",
  mounted() {
    this.initial()
  },
  methods: {
    initial(){
      console.log("Initialization")
    },
    clickMe() {
      alert("Hi");
    },
    clickMe2(message){
        alert(message);
    },
    getTimeStamp(){
        return Date()
    }
  }
};
</script>

<style>
</style>