<template class="mainTemp">
  <div class="everything">
    <img src="./assets/Coding-Challenge-Image.png" class="image-fit" />
    <div class="maroon-rectangle"></div>

    <div class="explore-box">
      <div class="explore-text">Explore</div>
      <PlusCircle />
    </div>

    <div class="float-buttons">
      <img src="./assets/Facebook.svg" />
      <img src="./assets/Instagram.svg" />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import PlusCircle from "./components/PlusCircle.vue";
import AOS from "aos";

export default defineComponent({
  name: "MainVue",
  props: {
    msg: String,
  },
  data() {
    return {
      scrolled: 0,
    };
  },
  components: {
    PlusCircle,
  },
  mounted() {
    AOS.init();
  },
  methods: {
    onScroll() {
      this.scrolled += 1;
    },
  },
});
</script>
