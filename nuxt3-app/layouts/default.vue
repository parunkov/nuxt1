<template>
  <div>
    <MainNavbar />
    <main>
      <div class="container">
        <slot />
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
