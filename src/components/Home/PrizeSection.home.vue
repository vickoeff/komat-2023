<template>
  <div id="prize" style="position: relative" class="sp-container">
    <v-container>
      <div>
        <!-- container for the upcoming specials -->
        <p class="font-7 weight-600 text-center mb-0">KOMAT 2023</p>
        <h2 class="font-2 weight-600 text-center">Hadiah</h2>
        <br />

        <v-row no-gutters align="center" justify="center">
          <v-col cols="12" xl="4" lg="4" />
          <v-col cols="12" xl="4" lg="4">
            <div class="pa-2 tab">
              <v-row align="center" justify="space-between" no-gutters>
                <span
                  class="tab-width"
                  v-for="(tabItem, idx) in tabs"
                  :key="idx"
                >
                  <v-btn
                    @click="updateTab(tabItem)"
                    :color="tab == tabItem ? 'blue' : 'black'"
                    style="height: 100%"
                    elevation="0"
                    class="mr-1 btn font-7 btn-tab"
                    dark
                    >{{ tabItem }}</v-btn
                  >
                </span>
              </v-row>
            </div>
          </v-col>
          <v-col cols="12" xl="4" lg="4" />
        </v-row>
        <br />
        <v-row v-if="isLoading" no-gutters>
          <v-col cols="12" class="text-center mt-5">
            <Loading />
          </v-col>
        </v-row>
        <v-container v-else>
          <v-row no-gutters>
            <v-col
              cols="12"
              v-for="i in activeTab"
              :key="i[i + 1]"
              xl="4"
              lg="4"
            >
              <specialCardVue :info="i" />
            </v-col>
          </v-row>
        </v-container>
      </div>
    </v-container>
    <div class="overlay"></div>
  </div>
</template>

<script>
import specialCardVue from "./utilities/special.card.vue";
import Loading from "./utilities/loading.vue";

export default {
  name: "PrizeSection",
  components: {
    specialCardVue,
    Loading,
  },
  data() {
    return {
      specials: {
        smp: [
          {
            img: require("../../assets/images/juara-1.png"),
            date: "Juara 1",
            tag: "Relax",
            title: "Rp 4.000.000,-",
            additional: "Medali, Piala, Sertifikat",
            desc: "Hadiah yang didapat",
          },
          {
            img: require("../../assets/images/juara-2.png"),
            date: "Juara 2",
            title: "Rp 3.000.000,-",
            additional: "Medali, Piala, Sertifikat",
            desc: "Hadiah yang didapat",
          },
          {
            img: require("../../assets/images/juara-3.png"),
            date: "Juara 3",
            title: "Rp 2.000.000,-",
            additional: "Medali, Piala, Sertifikat",
            desc: "Hadiah yang didapat",
          },
        ],
        sma: [
          {
            img: require("../../assets/images/juara-1.png"),
            date: "Juara 1",
            tag: "Relax",
            title: "Rp 6.000.000,-",
            additional: "Medali, Piala, Sertifikat",
            desc: "Hadiah yang didapat",
          },
          {
            img: require("../../assets/images/juara-2.png"),
            date: "Juara 2",
            title: "Rp 4.500.000,-",
            additional: "Medali, Piala, Sertifikat",
            desc: "Hadiah yang didapat",
          },
          {
            img: require("../../assets/images/juara-3.png"),
            date: "Juara 3",
            title: "Rp 3.500.000,-",
            additional: "Medali, Piala, Sertifikat",
            desc: "Hadiah yang didapat",
          },
        ],
      },
      tab: "smp",
      tabs: ["smp", "sma"],
      sw: 1,
      isLoading: false,
    };
  },
  computed: {
    activeTab() {
      return this.specials[this.tab];
    },
  },
  methods: {
    updateTab(value) {
      this.tab = value;
      this.isLoading = true;
      setTimeout(() => {
        this.isLoading = false;
      }, 150);
    },
  },
};
</script>

<style scoped>
.overlay {
  position: absolute;
  bottom: -256px;
  left: 0px;
  width: 100%;
  height: 260px;
  transform: rotate(180deg);
  background: url("../../assets/images/banner-overlay.png");
  background-size: cover;
  background-position: top center;
  background-repeat: no-repeat;
  z-index: 1;
}
.tab {
  height: 52px !important;
}
.btn-tab {
  text-transform: uppercase !important;
  height: 36px !important;
}
.sp-container {
  padding: 4%;
}
.tab {
  margin: 0 10%;
  background: #ffffff;
  height: 8vh;
  border-radius: 13px;
}
.sh-container {
  position: absolute;
  top: -15%;
  width: 100%;
}
@media screen and (max-width: 600px) {
  .sh-container {
    position: absolute;
    top: -3em;
    width: 90% !important;
  }
  .hide-xs {
    display: none !important;
  }
}
</style>
