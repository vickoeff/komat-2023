<template>
  <div>
    <heroHomeVue />
    <div style="background-color: #faf9f9">
      <contactHomeVue />
      <region />
      <v-container>
        <Timeline />
        <Terms />
      </v-container>
      <PrizeSection />
    </div>
  </div>
</template>

<script>
import contactHomeVue from "../components/Home/contact.home.vue";
import region from "../components/Home/region.home.vue";
import heroHomeVue from "../components/Home/hero.home.vue";
import Timeline from "../components/Home/Timeline.home.vue";
import Terms from "../components/Home/Terms.home.vue";
import PrizeSection from "../components/Home/PrizeSection.home.vue";

export default {
  name: "Home",

  components: {
    heroHomeVue,
    PrizeSection,
    contactHomeVue,
    Timeline,
    Terms,
    region,
  },
};
</script>
<style></style>
