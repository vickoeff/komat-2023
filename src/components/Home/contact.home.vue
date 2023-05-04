<template>
  <div class="contact-container" id="about">
    <v-row align="center" justify="center">
      <v-col cols="12" xl="6" lg="6" class="" style="position: relative">
        <p class="font-2 weight-600 d-flex d-sm-none text-center">
          Tentang KOMAT 2023
        </p>

        <v-img eager src="../../assets/images/logo-2023.png"></v-img>
      </v-col>
      <v-col cols="12" xl="6" lg="6" class="">
        <h2 class="font-2 weight-600 d-none d-sm-flex">Tentang KOMAT 2023</h2>
        <p class="font-7 font-weight-light">
          Diadakan sejak (tahun awal komat), KOMAT merupakan suatu kompetisi
          matematika yang diadakan oleh Himpunan Mahasiswa dan Program Studi
          Matematika Universitas Katolik Parahyangan untuk pelajar SMP dan SMA.
          Harapannya, KOMAT dapat meningkatkan minat terhadap matematika dan
          juga menjadi wadah belajar sekaligus berkompetisi bagi para peserta.
        </p>
        <br />
        <h2 class="font-5 weight-600 d-none d-sm-flex">Tema: Horizon</h2>
        <p class="font-7 font-weight-light">
          Horizon adalah istilah untuk garis semu antara laut dan langit yang
          seakan menjadi pembatas ketika kita melihatnya dari pantai. Karena
          horizon tadi, seakan laut berhenti di sana dan langit menjadi sangat
          dekat. Namun nyatanya, laut tetap luas dan langit tetap tinggi di
          atas. Hal ini sama seperti Matematika.
        </p>
        <p class="font-7 font-weight-light">
          Masih banyak stigma yang seakan-akan menyederhanakan Matematika
          sebagai ilmu yang terbatas pada hitung-hitungan. Padahal, Matematika
          lebih luas dan dalam seperti lautan serta tinggi dan jauh seperti
          langit. Matematika memerlukan logika, berpikir kritis, daya imajinasi,
          hingga kemampuan analisis.
        </p>
        <p class="font-7 font-weight-light">
          Lewat tema ini, KOMAT 2023 hadir bagi siswa-siswi SMP dan SMA untuk
          menjadi salah satu sarana memperdalam minat dan mengasah kemampuan
          mereka dalam bidang Matematika.
        </p>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {};
</script>

<style>
.contact-container {
  padding: 4%;
}
.box {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  height: 13vh;
  min-width: 100px;
  width: 150px;
  border-radius: 25px !important;
  position: absolute;
  background: white;
  padding-top: 2%;
}
.box-1 {
  top: 15%;
  right: -5%;
}
.box-2 {
  top: 85%;
  right: -5%;
}
.box-3 {
  top: 75%;
  left: -5%;
}
@media screen and (max-width: 600px) {
  .contact-container {
    padding: 10%;
  }
  .box {
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    height: 7vh;
    min-width: 100px;
    width: 100px;
    border-radius: 20px !important;
    position: absolute;
    background: white;
    padding-top: 2.5%;
  }
  .box-1 {
    top: 35%;
    right: -5%;
  }
  .box-2 {
    top: 80%;
    right: -5%;
  }
  .box-3 {
    top: 75%;
    left: -5%;
  }
}
</style>
