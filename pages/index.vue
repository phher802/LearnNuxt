<template>
  <div>
    <Nav />
    <div class="container">
      <Hero />
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo"
        :key="cardInfo.id"
        :cardSection="cardInfo"
      />
      <SmallCardDisplay
        v-for="cardInfo in smallCardSections"
        :key="cardInfo.id"
        :cardSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js";
import Nav from "../components/Nav.vue";

export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardSections,
    };
  },
};
</script>

<style scoped>
</style>