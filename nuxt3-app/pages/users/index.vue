<script setup>
const openUser = (user) => {
  const router = useRouter();
  router.push("/users/" + user);
};

const users = await $fetch('https://jsonplaceholder.typicode.com/users').catch((error) => error.data);
</script>
<template>
  <section>
    <h1>User Page</h1>
    <ul>
      <li v-for="user of users" :key="user.id">
        <a href="#" @click.prevent="openUser(user.id)">{{ user.name }}</a>
      </li>
    </ul>
  </section>
</template>
