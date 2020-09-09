<template>
  <div :class="$style.container">
    <div :class="$style.navigation">
      <div :class="$style.navi_left">
        <h1 :class="$style.title">
          Rent
          <span>{{selection}}</span>
        </h1>
       
      </div>
      <div :class="$style.navi_right">
        <span>Add new</span>
        <button :class="$style.btn" @click="clConsole">+</button>
      </div>
    </div>
    <div :class="$style.prod_list" v-if="show_list">
      <div
        :class="$style.prod_item"
        @click="openProd(item.id)"
        v-for="item in array_vehicles"
        :key="item.id"
      >
        <div :class="$style.item_img">
          <img :src="item.preview" :alt="item.name" />
        </div>
        <div :class="$style.item_content">
          <div :class="$style.title">{{ item.name }}</div>
          <p :class="$style.text">{{ item.description }}</p>
          <span :class="$style.price">{{item.rent}} $/h</span>
        </div>
      </div>
    </div>
    <div v-else>
     <Loading />
    </div>
  </div>
</template>

<script>
import { getVehicles } from "@/request";
import Loading from "../components/Loading";
export default {
  components: {
    Loading,
  },
  data() {
    return {
      requestVehicles: getVehicles,
      array_vehicles: [],
      show_list: false,
      selection: 'whatever'
    };
  },
  created() {
    this.requestVehicles()
      .then((response) => {
        return response;
      })
      .then((res) => res.map((el) => this.array_vehicles.push(el)))
      .then((el) => {
        el.length > 1 ? (this.show_list = true) : (this.show_list = false);
      });
  },
  methods: {
    openProd(num) {
      this.$router.push("/" + num);
    },
    clConsole() {
      console.log("hey");
    },
    reloadPage() {
      window.location.reload();
    },
  },
};
</script>

<style  module>
@import url("@/assets/css/index.css");
</style>