<template>
  <div id="footer" class="footer">
    <span>{{title}}</span>
  </div>
</template>

<script>
export default {
    name: "footer",
    props:[
        "title",
    ]

};
</script>

<style scoped>
.footer{
    font-size: 12px;
    color: gray;
    padding-top: 16px;
  }
</style>>