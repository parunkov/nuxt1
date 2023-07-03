<script setup>
const route = useRoute();
const id = route.params.id;
definePageMeta({
  validate: async (route) => {
    // Check if the id is made up of digits
    return /^\d+$/.test(route.params.id);
  }
})
</script>
<template>
  <section>
    <h1>User {{ id }}</h1>
  </section>
</template>