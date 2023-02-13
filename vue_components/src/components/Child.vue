<template>
    <!--div>
      字數:{{msgCount}}
    </div-->
   data: {{ data }}
</template>
<script setup>
import { computed } from '@vue/reactivity'
defineProps(['data'])
//const msgCount = computed(()=>{
//    return XXX.length
//})
</script>



<style scoped lang="postcss">

</style>
