<script setup>
const openUser = (user) => {
    const router = useRouter();
    router.push('/users/' + user);
}
</script>
<template>
    <section>
        <h1>User Page</h1>
        <ul>
            <li v-for="user of 5" :key="user">
                <a href="#" @click.prevent="openUser(user)">User {{ user }}</a>
            </li>
        </ul>
    </section>
</template>
