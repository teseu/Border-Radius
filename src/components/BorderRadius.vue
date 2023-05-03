<script setup>
import { ref } from 'vue'
import Card from '@/components/ui/cards/CardOne.vue'
import SliderAll from './ui/SliderAll.vue'
import SliderTop from './ui/SliderTop.vue';

const borderRadius = ref(10);

function borderAll(value) {
  borderRadius.value = value;
}

function borderTop(value) {
  borderRadius.value = value;
}

</script>

<template>
  <div class="flex flex-col justify-evenly md:flex-row w-full md:w-4/5 mx-auto px-4 md:px16 py-8">
    <SliderAll title="All corners" id="all" @border-radius="borderAll" />
    <SliderTop title="Top corner" id="top" @border-radius="borderTop" />
    <Card :borderAll="borderRadius" :borderTop="borderRadius" />
  </div>
</template>
<style scoped>
 
</style>