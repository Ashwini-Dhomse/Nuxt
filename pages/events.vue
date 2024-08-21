<script setup lang="ts">
const items = [{
  label: ' Events and Shows',
  icon: 'i-heroicons-information-circle',
  defaultOpen: true,
  content: 'With the idea of imparting programming knowledge, Mr. Sandeep Jain, an IIT Roorkee alumnus started a dream, GeeksforGeeks. Whether programming excites you or you feel stifled, wondering how to prepare for interview questions or how to ace data structures and algorithms, GeeksforGeeks is a one-stop solution. With every tick of time, we are adding arrows in our quiver. From articles on various computer science subjects to programming problems for practice, from basic to premium courses, from technologies to entrance examinations, we have been building ample content with superior quality. In a short span, we have built a community of 1 Million+ Geeks around the world, 20,000+ Contributors and 500+ Campus Ambassadors in various colleges across the nation. Our success stories include a lot of students who benefitted in their placements and landed jobs at tech giants. Our vision is to build a gigantic network of geeks and we are only a fraction of it yet.'
}, {
  label: '15 March',
  icon: 'i-heroicons-arrow-down-tray',
  content: 'Where is the event happening? With the idea of imparting programming knowledge, Mr. Sandeep Jain, an IIT Roorkee alumnus started a dream, GeeksforGeeks. Whether programming excites you or you feel stifled, how to ace data structures and algorithms, GeeksforGeeks is a one-stop solution.'
}, {
  label: '27 May',
  icon: 'i-heroicons-eye-dropper',
  content: 'Where is the event happening? With the idea of imparting programming knowledge, Mr. Sandeep Jain, an IIT Roorkee alumnus started a dream, GeeksforGeeks. Whether programming excites you or you feel stifled, how to ace data structures and algorithms, GeeksforGeeks is a one-stop solution.'
}, {
  label: '30 June',
  icon: 'i-heroicons-rectangle-group',
  content: 'Where is the event happening? With the idea of imparting programming knowledge, Mr. Sandeep Jain, an IIT Roorkee alumnus started a dream, GeeksforGeeks. Whether programming excites you or you feel stifled, how to ace data structures and algorithms, GeeksforGeeks is a one-stop solution.'
}, {
  label: '21 August',
  icon: 'i-heroicons-square-3-stack-3d',
  content: 'Where is the event happening? With the idea of imparting programming knowledge, Mr. Sandeep Jain, an IIT Roorkee alumnus started a dream, GeeksforGeeks. Whether programming excites you or you feel stifled, how to ace data structures and algorithms, GeeksforGeeks is a one-stop solution.'
}, {
  label: '5 July',
  icon: 'i-heroicons-wrench-screwdriver',
  content: 'Where is the event happening? With the idea of imparting programming knowledge, Mr. Sandeep Jain, an IIT Roorkee alumnus started a dream, GeeksforGeeks. Whether programming excites you or you feel stifled, how to ace data structures and algorithms, GeeksforGeeks is a one-stop solution.'
}]
</script>

<template>
  <UAccordion :items="items" :ui="{ wrapper: 'flex flex-col w-full' }">
    <template #default="{ item, index, open }">
      <UButton color="gray" variant="ghost" class="border-b border-gray-200 dark:border-gray-700" :ui="{ rounded: 'rounded-none', padding: { sm: 'p-3' } }">
        <template #leading>
          <div class="w-6 h-6 rounded-full bg-primary-500 dark:bg-primary-400 flex items-center justify-center -my-1">
            <UIcon :name="item.icon" class="w-4 h-4 text-white dark:text-gray-900" />
          </div>
        </template>

        <span class="truncate">{{ index + 1 }}. {{ item.label }}</span>

        <template #trailing>
          <UIcon
            name="i-heroicons-chevron-right-20-solid"
            class="w-5 h-5 ms-auto transform transition-transform duration-200"
            :class="[open && 'rotate-90']"
          />
        </template>
      </UButton>
    </template>
  </UAccordion>
</template>

