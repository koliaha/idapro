<template>
  <nav :class="$style.navbar">
    <ul :class="$style.nav_list">
      <li :class="$style.nav_item">
        <nuxt-link :class="$style.nav_link" exact no-prefetch active-:class="$style.active" to="/">
          <img src="@/assets/img/logo.svg" alt="logo" />
          <span :class="$style.logoname">Pepelane</span>
        </nuxt-link>
      </li>
      <li :class="$style['nav_item sub_right']">
        <span :class="$style.subtitle">World's first affordable airsharing</span>
      </li>
      <li :class="$style['nav_item moon_right']">
        <img :class="$style.moon" src="@/assets/img/moon.svg" alt="moon" />
        <span :class="$style.subtitle">Night mod</span>
      </li>
      <li :class="$style.nav_item">
        <img src="@/assets/img/chat.svg" alt="chat" />
      </li>
      <li :class="$style.nav_item">
        <img src="@/assets/img/ring.svg" alt="ring" />
      </li>
      <li :class="$style.nav_item">
        <div :class="$style.avatar">
          <span :class="$style.title">Bessie Cooper</span>
          <img src="@/assets/img/ava.png" alt="ava" />
        </div>
      </li>
    </ul>
  </nav>
</template>

<style  module>


@import url("@/assets/css/nav.css");

</style>