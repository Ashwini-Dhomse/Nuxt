<template>
  <div>
    <HeaderComp />
   <NuxtLayout>    
    <header>
      <UBreadcrumb :links="links" />
    </header>
    <NuxtPage />
   </NuxtLayout>
  </div>
</template>
<script setup lang="ts">
const links = [{
  label: 'Home',
  icon: 'i-heroicons-home',
  to: '/'
}, {
  label: 'Navigation',
  icon: 'i-heroicons-square-3-stack-3d'
}, {
  label: 'Breadcrumb',
  icon: 'i-heroicons-link'
}]
</script>