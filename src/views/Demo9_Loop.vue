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

    <input type="text" placeholder="Title" v-model="course.title" /><br />
    <input type="number" placeholder="Price" v-model="course.price" /><br />
    <button @click="addCourse">Submit</button>

    <!--Dynamic-->
    <ul>
      <li v-for="(course, index) in dynamicCourse" :key="index">
        {{ course.title }}, Price {{ course.price }} <button @click="removeCourse(index)">X</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Demo9",
  methods: {
      addCourse(){
          this.dynamicCourse.push(this.course)
          this.course = {title: "", price: 0}

      },
      removeCourse(index){
          this.dynamicCourse.splice(index, 1)
      }
  },
  data() {
    return {
      course: { title: "", price: 0 },
      dynamicCourse: [],
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