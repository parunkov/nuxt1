<script setup>
const openUser = (user) => {
    const router = useRouter();
    router.push('/users/' + user);
}

const users = ref([]);
onMounted(async () => {
    const response = await fetch('https://jsonplaceholder.typicode.com/users');
    const result = await response.json();
    result.forEach((item) => {
       users.value.push(item) ;
    });
})
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
