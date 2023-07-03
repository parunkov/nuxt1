<script setup>
import "@/node_modules/bootstrap/dist/css/bootstrap.min.css";

// const isToken = useState("isToken", () => false);
// console.log(isToken);
</script>

<template>
  <div>
    <NuxtLoadingIndicator />
    <MainNavbar />
    <main>
      <div class="container">
        <NuxtPage />
      </div>
    </main>
  </div>
</template>
<!-- <script>
import '@/node_modules/bootstrap/dist/css/bootstrap.min.css';
import MainNavbar from '@/components/MainNavbar.vue';
export default {
  components: {MainNavbar},
  setup() {
    const isToken = useState('isToken', () => false);
  }
}
</script> -->
<style>
/* @import url("@/node_modules/bootstrap/dist/css/bootstrap.min.css"); */
</style>