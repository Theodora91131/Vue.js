<script setup>
import {ref} from "@vue/reactivity"
const data = "Hello Vue"
const text = ref("123")
</script>

<template>
 <p>Hello World</p>
 <!--data one way binding-->
   {{ data }}
<!--data two way binding-->
<input type = "text" v-model="text"/> 
<p>{{ text }}</p>
</template>

<style >

</style>