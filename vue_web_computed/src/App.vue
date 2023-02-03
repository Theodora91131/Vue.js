<script setup>
import{computed,ref}from 'vue'

const num = ref(0)
const numFormat = computed(()=>{
  console.log('change')
  if(Number.isNaN(num.value*100)) return num.value
  return `${num.value*100}%`
})
//const numFormat=()=>{
//  if(Number.isNaN(num*100)) return num
 // return `${num*100}%`
//  }
</script>

<template>
  <h1>Computed計算屬性</h1>
  <input type="number" v-model="num"/> 
  <h3>{{numFormat}}</h3>

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
