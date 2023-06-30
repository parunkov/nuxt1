<template>
  <div>
    <MainNavbar />
    <main>
      <div class="container">
        <NuxtPage />
      </div>
    </main>
  </div>
</template>
<script>
import '@/node_modules/bootstrap/dist/css/bootstrap.min.css';
import MainNavbar from '@/components/MainNavbar.vue';
export default {
  components: {MainNavbar}
}
</script>
<style>
/* @import url("@/node_modules/bootstrap/dist/css/bootstrap.min.css"); */
</style>