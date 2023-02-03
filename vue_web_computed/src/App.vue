<script setup>
const num = "0.5"
const numFormat=()=>{
  if(Number.isNaN(num*100)) return num
  return `${num*100}%`
  }
</script>

<template>
  <h1>Computed計算屬性</h1>
  <h3>{{numFormat()}}</h3>

</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
