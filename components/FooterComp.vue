<script setup lang="ts">
const route = useRoute()

const links = [
[{
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
    label: 'Copyright © 2016-2024 Nuxt ',
  }]
]
</script>

<template>
  <UHorizontalNavigation :links="links" class="border-b border-gray-200 dark:border-gray-800 bg-primary-400" />
</template>
