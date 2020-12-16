<template>
    <div id="demo3">
        <h1>Data</h1>
        <button @click="count++; isLogged=true;">Count++</button>
        <span>{{count}}</span>
        <div>{{message}}</div>
        <div>{{inLogged}}</div>
        <input type="text" placeholder="Enter a maessage" v-model="message">
        <h2 v-if="isLogged">Yahooo</h2>
        <div>{{account.username}} {{account.password}}</div>
        <div>{{courses}}</div>
        <ul>
            <li v-for="(item, index) in courses" :key="index">{{index}}. {{item}}</li>
        </ul>

        <span class="title">55555</span>
    </div>
</template>

<script>
export default {
    name: "Demo3",
    mounted() {
      this.message ="Welcome to Sashigyu"
    },
    data(){
        return {
            count: 0,
            message: "",
            inLogged: false,
            account: {
                username: "admin",
                password: "1234"
            },
            courses:[
                "Angular",
                "VueJs",
                "ReactJS",
                "Flutter",
                "UXUI"
            ]
        }
    }
}
</script>

<style scoped>
    
    .title{
        color: red
    }

</style>