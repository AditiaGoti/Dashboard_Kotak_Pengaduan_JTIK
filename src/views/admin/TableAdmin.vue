<template>
  <div class="flex flex-wrap mt-4">
    <div class="w-full mb-12 px-4">
      <card-table-admin />
    </div>
  </div>
</template>
<script>
import CardTableAdmin from "@/components/Cards/CardTableAdmin.vue";

export default {
  components: {
    CardTableAdmin
  },
};
</script>