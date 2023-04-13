<template>
  <div class="flex flex-wrap mt-4">
    <div class="w-full mb-12 px-4">
      <card-table-mahasiswa />
    </div>
  </div>
</template>
<script>
import CardTableMahasiswa from "@/components/Cards/CardTableMahasiswa.vue";

export default {
  components: {
    CardTableMahasiswa
  },
};
</script>