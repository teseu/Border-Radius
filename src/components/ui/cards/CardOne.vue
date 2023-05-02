<script setup lang="ts">
import { reactive} from 'vue'

// const borderRadius = ref(10);

const props = defineProps({
  borderAll: Number
})
// let borderR = 10
const borderR = reactive({
  borderR: props.borderAll,
})
// watch(props, () => {
//   borderR.valueOf = props.borderAll
// })
</script>

<template>
 <div class="flex flex-col bg-emerald-500 w-full md:w-[25rem] px-8 py-4" :style="{'border-radius': props.borderAll + 'px'}">
  <button class="btn w-full max-w-xs mx-auto">Copy result</button>
  <div class="mt-4 w-full max-w-xs mx-auto">
    <textarea placeholder="Bio" class="textarea textarea-bordered textarea-lg w-full" ></textarea>
  </div>
 </div>
</template>
<style scoped>
 
</style>