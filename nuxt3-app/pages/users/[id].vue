<script setup>
const route = useRoute();
const id = route.params.id;
definePageMeta({
  validate: async (route) => {
    // Check if the id is made up of digits
    return /^\d+$/.test(route.params.id);
  }
})

const user = await $fetch(`https://jsonplaceholder.typicode.com/users/${id}`).catch((error) => error.data);
</script>
<template>
  <section>
    <h1>{{ user.name }}</h1>
    <hr>
    <h3>{{ user.email }}</h3>
  </section>
</template>