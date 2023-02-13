<template>
  <input type=" text" v-model="msg"/>
  <br/>
  <Child v-bind:data="msg"/>
</template>


<script setup>
import {ref} from 'vue'
import Child from './components/Child.vue'
const msg = ref('')
</script>



<style >
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
