<template>
  <div class="container">
    <Navbar />
    <main class="main">
      <Nuxt />
    </main>
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
export default {
  components: {
    Navbar,
  },
};
</script>
<style >
@import url("@/assets/css/main.css");

</style>
