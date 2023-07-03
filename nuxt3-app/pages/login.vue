<script setup>
const isAuth = useAuth();

const onSubmit = () => {
  isAuth.value = true;
  console.log(isAuth);
}
</script>
<template>
  <section>
    <form>
      <h1>Login page</h1>
      <div class="form-group">
        <input type="text" class="form-control" />
      </div>
      <p>
        <nuxt-link to="/">To home page</nuxt-link>
      </p>
      <buttun class="btn btn-primary" type="button" @click="onSubmit">Login</buttun>
    </form>
  </section>
</template>
<style scoped>
form {
  width: 500px;
  margin: 0 auto;
}
</style>