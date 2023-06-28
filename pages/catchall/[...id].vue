<script setup>
const route = useRoute();
console.log("route",route.params.id);
</script>

<template>
  <div>test-{{ $route.params.id }}</div>
</template>
