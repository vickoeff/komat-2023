<template>
  <div id="region" class="region-wrapper">
    <h2 class="font-2 weight-600 text-center mb-5">Kompetisi Nasional</h2>
    <v-img eager src="../../assets/images/map.png"></v-img>
    <p class="text-center mt-5">Cabang lomba untuk SMP dan SMA</p>
  </div>
</template>

<script>
export default {
  name: "region",
};
</script>

<style>
.region-wrapper {
  padding: 4rem 1.5rem;
  padding-top: 260px;
  background-image: linear-gradient(180deg, #005f73, #36aca7, #e9d7a5);
}
.region-wrapper h2 {
  color: white;
}
</style>
