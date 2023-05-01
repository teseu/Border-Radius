<script setup>
import Card from '@/components/ui/cards/CardOne.vue'
import TheSlider from './ui/TheSlider.vue';
</script>

<template>
  <div class="flex flex-col md:flex-row w-full md:w-4/5 mx-auto px-4 md:px16 py-8">
    <TheSlider title="All corners" id="all" />
    <Card />
  </div>
</template>
<style scoped>
 
</style>