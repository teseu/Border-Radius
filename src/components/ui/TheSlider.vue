<script setup>
import { ref } from 'vue'

const value = ref(10)

 defineProps({
   title: String,
  //  value: String,
   id: String
 })
//  defineEmits(['update:value'])
</script>

<template>
 <div class="flex flex-col">
  <div class="flex justify-between">
   <h3 class="text-xl">{{ title }}</h3>
   <input type="number" :name="id" :id="id" v-model="value" class="input input-bordered input-sm w-full max-w-xs">
  </div>
  <input type="range" min="0" max="100" v-model="value" class="range" />
  <p>{{ value }}</p>
 </div>
</template>
<style scoped>
 
</style>