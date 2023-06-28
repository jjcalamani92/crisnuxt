<!-- import { PageHeadings, SlideOvers } from '../../.nuxt/components'; -->

<script setup>
  useSeoMeta({
  title: 'Dashboard',
  description: 'This is the about page',
})
  definePageMeta({
    layout: 'dashboard'
  })
  const site = await useFetch('https://crisapi.vercel.app/api/v3/portfolio2/query/sites/6498b9fa86f3aec7afbbfe19')
  console.log('sites', site.data.value)

</script>

<template>
  <NuxtLayout >
  <div class="min-h-full">
    <header class="bg-white shadow">
      <div class="mx-auto max-w-7xl px-4 py-6 sm:px-6 lg:px-8">
        <h1 class="text-3xl font-bold tracking-tight text-gray-900">{{site.data.value.data.info.name}}</h1>
        <!-- <h1 class="text-3xl font-bold tracking-tight text-gray-900">Dashboards</h1> -->
      </div>
    </header>
    <main>
      <div class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8">
        <PageHeadings />
      </div>
    </main>
  </div>

  <SlideOvers />

</NuxtLayout>

</template>

