<script setup lang="ts">
const route = useRoute()

const links = [
[{
  label : "Sample Website",
  class : "text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl lg:text-5xl"
}],[{
  label: 'Home',
  icon: 'i-heroicons-home',
  to: `/`
}, {
  label: 'Profile',
  avatar: {
    src: 'https://avatars.githubusercontent.com/u/739984?v=4'
  },
  to:'/profile'
}, {
  label: 'Events',
  icon: 'i-heroicons-chart-bar',
  to: '/events'
}, {
  label: 'Contact Us',
  icon: 'i-heroicons-command-line',
  to: '/contact'
}], [{
    label: 'Login',
  }, {
    label: 'Help',
    icon: 'i-heroicons-question-mark-circle'
  }]
]
</script>

<template>
  <UHorizontalNavigation :links="links" class="border-b border-gray-200 dark:border-gray-800 bg-primary-400" />
</template>
