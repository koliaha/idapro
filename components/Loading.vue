<template>
  <div :class="$style.loadCompoment">
     <p :class="$style.loadText">LOADING...</p> 
    <button :class="$style.btn" @click="reloadPage()">Reload page</button>
  </div>
</template>
<script>
export default {
  
  methods: {
    reloadPage() {
      window.location.reload();
    },
  },
}
</script>

<style  module>

.loadCompoment{
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
}
.loadText{
    font-size: 40px;
    color: #4959FF;
    margin: 20px 0;
}
 .btn {
    background: #4959FF;
    border-radius: 12px;
    font-size: 26px;
    color: #FCFCFC;
    outline: none;
    border: none;
    cursor: pointer;
    height: 48px;
    line-height: 48px;
    padding: 0 32px;
    transition:0.5s;
  }
  .btn:hover {
    opacity: 0.7;
  }
</style>