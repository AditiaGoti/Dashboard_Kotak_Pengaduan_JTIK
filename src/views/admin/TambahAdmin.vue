<template>
  <div class="flex flex-wrap">
    <div class="w-full lg:w-8/12 px-4">
      <CardTambahAdmin />
    </div>
    <div class="w-full lg:w-4/12 px-4">
    </div>
  </div>
</template>
<script>
import CardTambahAdmin from "@/components/Cards/CardTambahAdmin.vue";

export default {
  components: {
    CardTambahAdmin,
  },
};
</script>
