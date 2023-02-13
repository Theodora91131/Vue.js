<template>
    <!--div>
      字數:{{msgCount}}
    </div-->
   data: {{ data }}
</template>
<script setup>
import { computed } from '@vue/reactivity'
//defineProps(['data']) method1
defineProps({
    data:{
        type:String,
        default:'',
    },
})
//const msgCount = computed(()=>{
//    return XXX.length
//})
</script>



<style scoped lang="postcss">

</style>
