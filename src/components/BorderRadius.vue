<script setup>
import { ref } from 'vue'
import Card from '@/components/ui/cards/CardOne.vue'
import TheSlider from './ui/TheSlider.vue'

const borderRadius = ref(10);

function borderAll(value) {
  borderRadius.value = value;
}


</script>

<template>
  <div class="flex flex-col justify-evenly md:flex-row w-full md:w-4/5 mx-auto px-4 md:px16 py-8">
    <TheSlider title="All corners" id="all" @border-radius="borderAll" />
    <Card :borderAll="borderRadius" />
  </div>
</template>
<style scoped>
 
</style>