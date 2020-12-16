<template>
  <div id="demo5">
    <img v-bind:src="imageUrl" v-bind:height="height" />
    <br />
    <a :href="link">Plai Website</a>
    <br />
    <div :class="[false ? error : '', important]">Sashigyu</div>
    <div :style="{color, fontSize: fontSize}">Binding style</div>
    <div :style="isActive ? styleObj : '' ">Binding style obj</div>
    <button @click="isActive = !isActive">Toggle Active</button>
  </div>
</template>

<script>
export default {
  name: "Demo5",
  data() {
    return {
      imageUrl:
        "https://www.matichon.co.th/wp-content/uploads/2018/09/66310-1024x683.jpg",
      height: 200,
      link: "https://www.facebook.com/plaipp",
      error: "error_class",
      important: "important",
      color: "green",
      fontSize: "30px",
      styleObj: {
          backgroundColor: 'yellow',
          color: 'green'
      },
      isActive: false
    };
  },
};
</script>


<style>
.error_class {
  background-color: red;
  color: white;
}

.important {
  font-weight: 900;
}
</style>