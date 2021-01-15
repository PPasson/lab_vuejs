<template>
  <div id="demo9">
    <ul>
      <li v-for="(item, index) in ['Angular', 'Vue', 'React']" :key="index">
        {{ item }}
      </li>
    </ul>

    <hr />

    <ul>
      <li v-for="(item, index) in mCourse" :key="index">
        {{ item.title }}, Price {{ item.price }}
      </li>
    </ul>

    <hr />

    <!--Destructuring-->
    <ul>
      <li v-for="({ title, price }, index) in mCourse" :key="index">
        {{ title }}, Price {{ price }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Demo9",
  data() {
    return {
      mCourse: [
        { title: "iOS", price: 11 },
        { title: "Android", price: 12 },
        { title: "Flutter", price: 13 }
      ]
    };
  }
};
</script>

<style>
</style>