<script setup>
import {ref} from "@vue/reactivity"
const data = "Hello Vue"
const text = ref("123")
const view = ref(1)
const changeView=()=>{
    view.value = 2
}
const changeView2=()=>{
    view.value = 1
}
</script>

<template>
<button v-on:click="changeView">show one-way binding</button>
<button v-on:click="changeView2">show two-way binding</button>
<div class ="container-1" v-if="view==1">
 <p>Hello World</p>
 <!--data one-way binding-->
   {{ data }}
</div>
<div class ="container-2" v-if="view==2">
<!--data two-way binding-->
<input type = "text" v-model="text"/> 
<p>{{ text }}</p>
</div>
</template>

<style >
div.container-1{
    border:2px red solid;
}
div.container-2{
    border:2px skyblue solid;
}
</style>