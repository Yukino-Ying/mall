<template>
  <div class="detail-swiper">
    <swiper class="detail-swiper">
      <swiper-item v-for="(item, index) in swiperImages" :key="index">
        <img :src="item" alt />
      </swiper-item>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperItem } from "components/common/swiper/index.js";

export default {
  name: "DetailSwiper",
  props: {
    swiperImages: {
      type: Array,
      return() {
        [];
      }
    }
  },
  components: {
    Swiper,
    SwiperItem
  }
};
</script>

<style scoped>
.detail-swiper {
  height: 300px;
  overflow: hidden;
}
</style>