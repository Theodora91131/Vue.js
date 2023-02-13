<template>
    <div>
      字數:{{ msgCount }}
    </div>
   data: {{ data }}
</template>
<script setup>
import { computed } from '@vue/reactivity'
//defineProps(['data']) method1
const props = defineProps({
    data:{
        type:String,
        default:'',
    },
})
const msgCount = computed(()=>{
   return props.data.length
})
</script>



<style scoped lang="postcss">

</style>
