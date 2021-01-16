<template>
  <div id="Demo13">
    <h2>{{ 1234 | currency("THB ")}}</h2>
    <h2>{{ 200000000000 | bytes }}</h2>
    <h2>{{ "sashigyu" | capitalize({ onlyFirstLetter: true }) }}</h2>
    <h2>{{ "sashigyu" | uppercase }}</h2> 
    <h2>{{ [1, 2, 3] | reverseArray }}</h2>
  </div>
</template>

<script>
export default {
    name: "Demo3",
    filters: {
        reverseArray(value) {
            return value.slice().reverse();
        }
    }
}
</script>

<style>

</style>