<template>
  <div id="app">
    <Header />
      <Content />
    

    <Footer @onClock="onClock" title="Copyright 2020 by Sashigyu" />
    <div class="clock">{{ time }}</div>
  </div>
</template>

<script>
import Header from "@/components/layout/Header.vue";
import Footer from "@/components/layout/Footer.vue";
import Content from "@/components/layout/Content.vue";
import moment from "moment";
export default {
  name: "app",
  methods: {
    onClock(value) {
      this.time = moment(value).format("MM/DD/YYYY hh:mm:ss");
    }
  },
  data() {
    return {
      time: ""
    };
  },
  components: {
    Header,
    Footer,
    Content
  }
};
</script>

<style scoped>
.title {
  font-size: 30px;
  color: green;
}

.clock {
  font-size: 12px;
}


</style>