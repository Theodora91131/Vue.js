<template>
    <div>
      字數:{{ msgCount }}
    </div>
   data: {{ data }}
</template>
<script setup>
import { computed } from '@vue/reactivity'
import { watch } from 'vue'
const emit = defineEmits(['update'])
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
watch(msgCount,(newValue)=>{
    emit('update',newValue)

})
</script>



<style scoped lang="postcss">

</style>
