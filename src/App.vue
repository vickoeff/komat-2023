<template>
  <v-app class="animate__animated animate__fadeIn animate__slow">
    <v-app-bar
      :color="color"
      id="nav-bar"
      class=""
      fixed
      dark
      style="padding: 0 5%"
      flat
    >
      <v-spacer></v-spacer>

      <div class="d-none d-sm-flex">
        <div class="d-flex align-center">
          <v-btn
            href="#about"
            style="text-transform: none"
            class="font-7"
            text
            plain
            >Tentang</v-btn
          >
          <v-btn
            href="#timeline"
            style="text-transform: none"
            class="font-7"
            text
            plain
            >Timeline</v-btn
          >
          <v-btn
            href="#terms"
            style="text-transform: none"
            class="font-7"
            text
            plain
            >Persyaratan</v-btn
          >
          <v-btn
            href="#prize"
            style="text-transform: none"
            class="font-7"
            text
            plain
            >Hadiah</v-btn
          >
          <v-btn
            href="#footer"
            style="text-transform: none"
            class="font-7"
            text
            plain
            >Kontak</v-btn
          >
        </div>
      </div>

      <v-menu left bottom>
        <template v-slot:activator="{ on, attrs }">
          <v-btn icon v-bind="attrs" v-on="on" class="d-block d-sm-none">
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item>
            <v-btn
              href="#about"
              style="text-transform: none"
              class="font-7"
              text
              plain
              >Tentang</v-btn
            >
          </v-list-item>
          <v-list-item>
            <v-btn
              href="#timeline"
              style="text-transform: none"
              class="font-7"
              text
              plain
              >Timeline</v-btn
            >
          </v-list-item>
          <v-list-item>
            <v-btn
              href="#terms"
              style="text-transform: none"
              class="font-7"
              text
              plain
              >Persyaratan</v-btn
            >
          </v-list-item>
          <v-list-item>
            <v-btn
              href="#prize"
              style="text-transform: none"
              class="font-7"
              text
              plain
              >Hadiah</v-btn
            >
          </v-list-item>
          <v-list-item>
            <v-btn
              href="#footer"
              style="text-transform: none"
              class="font-7"
              text
              plain
              >Kontak</v-btn
            >
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>

    <v-footer id="footer">
      <v-container>
        <v-row style="justify-content: space-between; align-items: end">
          <v-col class="col-12 col-md-4 order-2 order-sm-1 mt-4 mt-sm-0">
            <v-row>
              <v-col class="col-4">
                <v-img src="../src/assets/images/logo-2023.png"></v-img>
              </v-col>
              <v-col class="col-4">
                <v-img src="../src/assets/images/logo-HMPSMa.png"></v-img>
              </v-col>
              <v-col class="col-4">
                <v-img src="../src/assets/images/logo-UNPAR.png"></v-img>
              </v-col>
            </v-row>
          </v-col>

          <v-col class="col-12 col-md-4 order-1 order-sm-2 contact-wrapper">
            <h2 class="font-2">Kontak Kami</h2>
            <ul class="contact">
              <li class="phone-contact">
                <v-img
                  max-width="24"
                  src="../src/assets/images/phone-call.png"
                ></v-img>
                <p class="font-6">Cicil: 087748360496</p>
              </li>
              <li class="phone-contact mb-5">
                <v-img
                  max-width="24"
                  src="../src/assets/images/phone-call.png"
                ></v-img>
                <p class="font-6">Patricia: 081312479007</p>
              </li>
              <li class="sosmed-wrapper">
                <a
                  class="sosmed"
                  href="https:/instagram.com/komatunpar"
                  target="_blank"
                  ><v-img src="../src/assets/images/instagram.png"></v-img
                ></a>
              </li>
            </ul>
          </v-col>
        </v-row>
        <div class="d-sm-none d-md-flex">
          <v-row
            no-gutters
            style="align-items: center"
            class="footer d-none d-sm-flex"
          >
            <p class="font-7 mt-5 copyright">
              Developed by <a href="https://sibiti.co.id">sibiti.co.id</a> with
              ❤️
            </p>
            <v-spacer></v-spacer>
            <div class="jst" style="display: flex">
              <v-btn
                href="#about"
                style="text-transform: none"
                class="font-7"
                text
                plain
                >Tentang</v-btn
              >
              <v-btn
                href="#timeline"
                style="text-transform: none"
                class="font-7"
                text
                plain
                >Timeline</v-btn
              >
              <v-btn
                href="#terms"
                style="text-transform: none"
                class="font-7"
                text
                plain
                >Persyaratan</v-btn
              >
              <v-btn
                href="#prize"
                style="text-transform: none"
                class="font-7"
                text
                plain
                >Hadiah</v-btn
              >
              <v-btn
                href="#footer"
                style="text-transform: none"
                class="font-7"
                text
                plain
                >Kontak</v-btn
              >
            </div>
          </v-row>
        </div>
        <v-row
          no-gutters
          style="width: 100%"
          class="footer d-flex d-sm-none d-none d-sm-flex d-md-none"
        >
          <v-spacer></v-spacer>
          <div>
            <p class="font-7 text-center mt-5 copyright">
              Developed by <a href="https://sibiti.co.id">sibiti.co.id</a> with
              ❤️
            </p>
          </div>
          <v-spacer></v-spacer>
        </v-row>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
import "./css/fonts.css";
export default {
  name: "App",

  data: () => ({
    color: "transparent",
    colo: "white",
  }),
  mounted() {
    const navbar = document.getElementById("nav-bar");
    window.addEventListener("scroll", () => {
      if (window.scrollY > 20) {
        this.color = "whitesmoke";
        this.colo = "grey";
        navbar.classList.add("scale-in-center");
      } else {
        this.color = "transparent";
        this.colo = "white";
        navbar.classList.remove("scale-in-center");
        navbar.classList.add("scale-out-center");
      }
    });
  },
};
</script>
<style scoped>
#nav-bar {
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 3% !important;
}
#nav-bar.theme--dark.v-app-bar.v-toolbar.v-sheet.v-app-bar.v-app-bar--fixed.v-app-bar--is-scrolled {
  max-width: unset;
  margin: unset;
  background-color: #0b3c43;
}
.contact-wrapper {
  color: white !important;
}
.contact-wrapper h2 {
  color: #e9d7a5 !important;
}
.contact {
  list-style: none;
  padding-left: unset !important;
}
.copyright {
  color: white;
}
#footer {
  min-height: 50vh;
  background-image: linear-gradient(180deg, #005f73, #36aca7, #e9d7a5);
  padding-top: 300px;
}
.sosmed {
  display: block;
  width: 40px;
  height: 40px;
  background: #fff;
  border-radius: 100%;
  padding: 8px;
}
.phone-contact {
  display: flex;
  align-items: center;
  margin-bottom: 8px;
}
.phone-contact p {
  margin-left: 8px;
  margin-bottom: 0;
}
.footer {
  padding-top: 4%;
  padding-bottom: 4%;
}
@media screen and (max-width: 600px) {
  .footer {
    padding: 10%;
  }

  .contact-wrapper {
    margin-bottom: 4rem;
  }
  .contact-wrapper h2 {
    text-align: center;
    margin-bottom: 1rem;
  }
  .phone-contact {
    justify-content: center;
  }
  .sosmed {
    margin: 0 auto;
  }
}
</style>
