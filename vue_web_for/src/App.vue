<script setup>
import {ref} from 'vue';
const test = ref('test')
const dataList = {
  key1:'a',
  key2:'b',
  key3:'c',
  key4:'d'
}
</script>

<template>
  <p class="test-cls">{{ test }}</p>
  <p v-for="(value,key,index) in dataList"
  :key="value">
    <span class="hint" v-show="key !=='key3'">
      {{ index }}.{{ key }}:{{ value }}

    </span>
   
  </p>
  
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
.test-cls{
  font-size:40px;
  animation:openln 1s ease-in-out;
}
@keyframes openln{
  0%{
    opacity:0;
    transform:translateY(20px);
  }
  100%{
    opacity:1;
    transform:translateY(0);
  }


}



</style>
