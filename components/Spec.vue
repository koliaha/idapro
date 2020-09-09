<template>
     <div class="tabCompoment">
        <div :class="$style.tabsContent">
          <p
            :class="$style.tabsText"
          >{{this.tabText}}</p>
        </div>
        <div :class="$style.features">
          <h1 :class="$style.title">Features:</h1>
          <div :class="$style.featuresList">
            <div :class="$style.featuresItem">
              <div :class="$style.itemImg">
                <img src="@/assets/img/cub.svg" alt="cub" />
              </div>
              <div :class="$style.itemContent">
                <div :class="$style.contentTitle">A challenge for a true champion</div>
                <div
                  :class="$style.contentText"
                >Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit.</div>
              </div>
            </div>
            <div :class="$style.featuresItem">
              <div :class="$style.itemImg">
                <img src="@/assets/img/man.svg" alt="man" />
              </div>
              <div :class="$style.itemContent">
                <div :class="$style.contentTitle">Pilot's sweaty hands</div>
                <div
                  :class="$style.contentText"
                >Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit.</div>
              </div>
            </div>
          </div>
        </div>
      </div>
</template>

<script>
export default {
  props: ['tabText'],
}
</script>
<style  module>
@import url("@/assets/css/spec.css");
 
</style>