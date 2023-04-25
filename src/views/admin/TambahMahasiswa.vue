<template>
  <div class="flex flex-wrap">
    <div class="w-full lg:w-8/12 px-4">
      <CardTambahMahasiswa />
    </div>
  </div>
</template>
<script>
import CardTambahMahasiswa from "@/components/Cards/CardTambahMahasiswa.vue";

export default {
  components: {
    CardTambahMahasiswa,
  },
};
</script>
