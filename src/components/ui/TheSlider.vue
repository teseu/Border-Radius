<script setup>
import { ref, defineEmits } from 'vue'

const value = ref(10)

 defineProps({
   title: String,
   id: String
 })
defineEmits(['update:value'])

 
</script>

<template>
 <div class="flex flex-col w-96">
  <div class="flex justify-between">
   <h3 class="text-xl">{{ title }}</h3>
   <input type="number" :name="id" :id="id" v-model="value" @input="$emit('border-radius', value)" class="input input-bordered input-sm w-20 max-w-xs">
  </div>
  <input type="range" min="0" max="100" v-model="value" @input="$emit('border-radius', value)" class="range" />
  <p>{{ value }}</p>
 </div>
</template>
<style scoped>
 
</style>