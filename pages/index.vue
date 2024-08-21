<template>
    <UCarousel v-slot="{ item }" :items="items" :ui="{ item: 'basis-full md:basis-1/2 lg:basis-1/3' }">
    <img :src="item" class="w-full" draggable="false">
  </UCarousel>
  <UAccordion
    open-icon="i-heroicons-plus"
    close-icon="i-heroicons-minus"
    :items="[{ label: '1. What is Nuxt UI?', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit' }, { label: '2. Getting Started', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit' }, { label: '3. Theming', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit' }, { label: '4. Components', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit' }]"
  />
</template>
<script setup lang="ts">
const items = [
  'https://picsum.photos/600/600?random=1',
  'https://picsum.photos/600/600?random=2',
  'https://picsum.photos/600/600?random=3',
  'https://picsum.photos/600/600?random=4',
  'https://picsum.photos/600/600?random=5',
  'https://picsum.photos/600/600?random=6'
]
</script>
