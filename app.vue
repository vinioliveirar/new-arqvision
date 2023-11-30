<template>
  <topHeader />
  <banner />
  <About />
  <Features />
  <Plans />
  <Accordion />
</template>
<script>
import topHeader from "./components/topHeader.vue";
import banner from "./components/banner.vue";
import Features from "./components/features.vue";
import Plans from "./components/plans.vue";
import Accordion from "./components/accordion.vue";
import About from "./components/about.vue";

export default {
  components: {
    Features,
    Plans,
    Accordion,
  },
};
</script>
