<template>
  <div id="content" class="content-wrapper">
    <router-view></router-view>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.content-wrapper {
  margin: 24px;
  padding: 24px;
  border-width: 1px;
  border-color: gray;
  border-style: dashed;
}
</style>