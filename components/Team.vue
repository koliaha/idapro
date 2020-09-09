<template>
  <div :class="$style.tab_compoment">
    <div :class="$style.tabs_content">
      <p :class="$style.tabs_text">{{this.tabText}}</p>
    </div>
    <div :class="$style.features">
      <h1 :class="$style.title">Qualified specialists:</h1>
      <div :class="$style.features_list">
        <div :class="$style.features_item">
          <div :class="$style.item_img">
            <img src="@/assets/img/man1.png" alt="man1" />
          </div>
          <div :class="$style.item_content">
            <div :class="$style.content_title">Marvin McKinney</div>
            <div :class="$style.content_text">Pilot assistant</div>
          </div>
        </div>
        <div :class="$style.features_item">
          <div :class="$style.item_img">
            <img src="@/assets/img/man2.png" alt="man2" />
          </div>
          <div :class="$style.item_content">
            <div :class="$style.content_title">Savannah Nguyen</div>
            <div :class="$style.content_text">Mechanic</div>
          </div>
        </div>
        <div :class="$style.features_item">
          <div :class="$style.item_img">
            <img src="@/assets/img/woman1.png" alt="man2" />
          </div>
          <div :class="$style.item_content">
            <div :class="$style.content_title">Courtney Henry</div>
            <div :class="$style.content_text">Stewardess</div>
          </div>
        </div>
      </div>
    </div>
    <div :class="$style.tabs_content">
      <p :class="$style.tabs_text">Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit. Exercitation veniam consequat sunt nostrud amet.</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['tabText'],
}
</script>
</script>
<style  module>
@import url("@/assets/css/team.css");

</style>