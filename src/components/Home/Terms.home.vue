<template>
  <div id="terms" class="terms-container">
    <v-img
      eager
      src="../../assets/images/wave-1.svg"
      max-width="120"
      class="wave-1"
    ></v-img>
    <p class="font-7 weight-600 mb-0">KOMAT 2023</p>
    <h2 class="font-2 weight-600 d-none d-sm-flex">Persyaratan umum</h2>
    <p class="font-6">Syarat dan Ketentuan Umum Peserta</p>
    <ol>
      <li v-for="(item, idx) in terms" :key="idx">
        {{ item }}
      </li>
    </ol>
    <v-img
      eager
      src="../../assets/images/wave-1.svg"
      max-width="120"
      class="mt-5"
    ></v-img>
  </div>
</template>

<script>
export default {
  name: "Terms",
  data() {
    return {
      terms: [
        `Peserta Kompetisi Matematika Universitas Katolik Parahyangan 2023 adalah
        siswa/i yang terdaftar sebagai pelajar SMA/sederajat atau SMP/sederajat
        pada tahun ajaran 2023/2024 di Indonesia.`,
        `Peserta Kompetisi Matematika UNPAR 2023 belum pernah menjadi juara
        1,2,atau 3 KOMAT UNPAR di tahun 2022 untuk tingkat yang sama.`,
        `Peserta wajib melakukan registrasi dengan data yang benar dan sesuai,
        serta membayar biaya registrasi kompetisi sejumlah yang sudah
        ditentukan.`,
        `Lomba bersifat individual.`,
        `Keputusan juri tidak dapat diganggu gugat.`,
        `Panitia berhak mendiskualifikasikan peserta yang melakukan pelanggaran
        atau kecurangan.`,
        `Peserta bersedia ke Bandung untuk melaksanakan babak semifinal-final
        secara offline 8. Peserta membaca dan memahami Booklet Informasi Peserta.`,
        `Penjelasan alur pendaftaran`,
      ],
    };
  },
};
</script>

<style>
.terms-container {
  padding: 4%;
}
.wave-1 {
  margin-left: auto;
}
</style>
