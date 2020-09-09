<template>
  <div class="tab-compoment" >
    <div :class="$style.tabsContent">
      <p :class="$style.tabsText">{{this.tabText}}</p>
      
    </div>
    <div :class="$style.features">
      <h1 :class="$style.title">Additional conditions:</h1>
      <ul :class="$style.featuresList">
        <li><p :class="$style.tabsText">Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit. Exercitation veniam consequat sunt nostrud amet.</p></li>
        <li><p :class="$style.tabsText">Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint.</p></li>
        <li><p :class="$style.tabsText">Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit.</p></li>
      </ul>
    </div>
    
  </div>
</template>
<script>
export default {
  props: ['tabText'],
}
</script>

<style  module>
@import url("@/assets/css/rent.css");



</style>