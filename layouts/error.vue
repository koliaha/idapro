<template>
  <div class="page">
    <h1 class="title">An error has occurred</h1>
    <p class="subtitle">Please refresh the page</p>
    <button class="btn" @click="reloadPage()">Reload page</button>
  </div>
</template>
<script>
export default {
  methods: {
    reloadPage() {
      window.location.reload();
    }
  },
};
</script>
<style  scoped>
@import url("@/assets/css/error.css");

</style>