<template>
  <div class="home">
    <UpperBanner />
    <TheFeatures />
    <TopOffers />
  </div>
</template>

<script>
import UpperBanner from "@/components/home_page/UpperBanner.vue";
import TheFeatures from "@/components/home_page/TheFeatures.vue";
import TopOffers from "@/components/home_page/TopOffers.vue";

export default {
  components: {
    UpperBanner,
    TheFeatures,
    TopOffers,
  },
  name: "HomeView",
};
</script>
