<template>
  <div class="container-banner">
    <v-row align="center" justify="center" class="hero" no-gutters>
      <v-col cols="12" xl="2" lg="2" />
      <v-col cols="12" xl="8" lg="8">
        <!-- <v-container>
          <p class="font-1 font-title white--text">
            Discover Your Life, Travel Where You Want
          </p>
          <p class="font-4 font-desc white--text">
            Would you explore natur paradise in the world, let’s find the best
            destination in world with us.
          </p>
        </v-container> -->
      </v-col>
      <v-col cols="12" xl="2" lg="2" />
    </v-row>
    <div class="overlay"></div>
  </div>
</template>

<script>
export default {
  name: "Hero",

  components: {},
};
</script>
<style>
.container-banner {
  position: relative;
}

.overlay {
  position: absolute;
  bottom: -1px;
  left: 0px;
  width: 100%;
  height: 260px;

  background: url("../../assets/images/banner-overlay.png");
  background-size: cover;
  background-position: top center;
  background-repeat: no-repeat;
}

.hero {
  height: 120vh;
  background: url("../../assets/images/banner-landscape.png");
  background-size: cover;
  background-position: top center;
  background-repeat: no-repeat;
}
.font-title {
  font-weight: 600;
  text-align: center;
}
.font-desc {
  font-weight: 500;
  text-align: center;
}

@media screen and (max-width: 450px) {
  .hero {
    height: 100vh;
    background: url("../../assets/images/banner-potrait.png");
    padding: 5%;
  }
}

@media screen and (max-width: 600px) {
  .hero {
    height: 100vh;
    background: url("../../assets/images/banner-landscape.png");
    background-size: cover;
    padding: 5%;
  }
  .font-title {
    text-align: left;
    line-height: 1.2;
  }

  .font-desc {
    font-weight: 500;
    text-align: left;
  }
}
</style>
