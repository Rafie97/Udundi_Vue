<template>
  <img src="../assets/Coding-Challenge-Image.png" class="image-fit" />
  <div data-aos="fade-in">{{ msg }}</div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import AOS from "aos";

export default defineComponent({
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      scrolled: 0,
    };
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
