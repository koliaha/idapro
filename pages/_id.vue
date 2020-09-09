<template>
  <section id="elzero-app" :class="$style.main_sec">
    <div :class="$style.main_wrap" v-if="show_list">
      <div :class="$style.left_img">
        <img :src="vehicle.image" alt />
      </div>
      <div :class="$style.right_content">
        <h1 :class="$style.title">{{vehicle.name}}</h1>
        <nav :class="$style.tabs">
          <ul :class="$style.tabs_list">
            <li :class="$style.tabs_item">
              <a
                
                @click.prevent="activeTab = '1'"
                :class="[activeTab === '1' ? 'active' : '']"
                href
              >Specifications</a>
            </li>
            <li :class="$style.tabs_item">
              <a
                
                @click.prevent="activeTab = '2'"
                :class="[activeTab === '2' ? 'active' : '']"
                href
              >Team</a>
            </li>
            <li :class="$style.tabs_item">
              <a
                
                @click.prevent="activeTab = '3'"
                :class="[activeTab === '3' ? 'active' : '']"
                href
              >Rent terms</a>
            </li>
          </ul>
        </nav>

        <div :class="$style.content_tab">
          <div v-if="activeTab === '1'">
            <Spec :tabText=vehicle.specifications_text />
          </div>
          <div v-if="activeTab === '2'">
            <Team :tabText=vehicle.team_text />
          </div>
          <div v-if="activeTab === '3'">
            <Rent :tabText=vehicle.term_text />
          </div>
        </div>

        <div :class="$style.price_btn">
          <div :class="$style.price">
            Rent for
            <span>{{vehicle.rent}} $/h</span>
          </div>
          <button :class="$style.btn">Rent now</button>
        </div>
      </div>
    </div>
    <div v-else>
      <Loading />
    </div>
  </section>
</template>

<script>
import Spec from "../components/Spec.vue";
import Team from "../components/Team.vue";
import Rent from "../components/Rent.vue";
import Loading from "../components/Loading";
import { getVehicles } from "@/request";
export default {
  layout: "empty",
  components: {
    Spec,
    Team,
    Rent,
    Loading,
  },
  data() {
    return {
      activeTab: "1",
      requestVehicles: getVehicles,
      vehicle: {},
      show_list: false,
    };
  },
  created() {
    this.requestVehicles()
      .then((response) => {
        return response;
      })
      .then((res) =>
        res.map((el) => {
          if (el.id == this.$route.params.id) {
            this.vehicle = el;
            console.log(this.vehicle);
          }
        })
      ).then((el) => {
        el.length ? (this.show_list = true) : (this.show_list = false);
      });
  },

};
</script>

<style  module>
@import url("@/assets/css/id.css");
</style>  