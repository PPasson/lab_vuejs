<template>
  <div id="demo6">
    <form v-on:submit.prevent="submit">
      <div>
        <!-- Firstname -->
        <label for="first_name">Firstname</label>
        <input type="text" name="first_name" v-model="applicant.first_name" />
      </div>

      <!-- Lastname -->
      <div>
        <label for="last_name">Lastname</label>
        <input type="text" name="last_name" v-model="applicant.last_name" />
      </div>

      <!-- Sex -->
      <div>
        <label for="sex">Male</label>
        <input type="radio" name="sex" value="male" v-model="applicant.sex" />

        <label for="sex">Female</label>
        <input type="radio" name="sex" value="female" v-model="applicant.sex" />
      </div>

      <!-- Course -->
      <div>
        <select name="course" v-model="applicant.course">
          <option value="react">React</option>
          <option value="angular">Angular</option>
          <option value="vuejs">Vue</option>
        </select>
      </div>

      <!-- button -->
      <button @click="clear()">Clear</button>
      <button type="submit">Submit</button>
    </form>
    <div style="margin-top: 16px; color: red">
      #Spy {{ JSON.stringify(applicant) }}
    </div>
  </div>
</template>

<script>
export default {
  name: "demo6",
  data() {
    return {
      applicant: {
        first_name: "",
        last_name: "",
        sex: "male",
        course: "react",
      },
    };
  },
  methods: {
      submit(){
          //event.preventDefault();
          alert(JSON.stringify(this.applicant))
      },
      clear(){
          this.applicant = {
            first_name: "",
            last_name: "",
            sex: "male",
            course: "react"}
      }
  }
};
</script>

<style>
</style>