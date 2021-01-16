<template>
<div id="Demo12">
    <h1 ref="title">Waiting for change by Ref</h1>
    <input ref="input1" type="text" placeholder="This will be foecred automatcally">
</div>
  
</template>

<script>
export default {
    name: "demo12",
    mounted(){
        this.$refs["title"].textContent = "Sashigyu change Ref";
        this.$refs["input1"].focus();
        this.$refs["input1"].value = "1234";
    }
};
</script>

<style>

</style>