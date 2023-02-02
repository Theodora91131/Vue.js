<script setup>
import {ref} from "@vue/reactivity"
const data = "Hello Vue"
const text = ref("123")
const view = ref(1)
const changeView=(index)=>{
    view.value = index
}

</script>

<template>
<button v-on:click="changeView(1)">show one-way binding</button>
<button @click="changeView(2)">show two-way binding</button>
<button @click="changeView(100)">show black screen </button>
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
<div v-if="view !==1 && view !==2"> black screen </div>
</template>

<style >
div.container-1{
    border:2px red solid;
}
div.container-2{
    border:2px skyblue solid;
}
</style>