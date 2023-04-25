<template>
  <!-- Header -->
  <div class="relative bg-emerald-600 md:pt-32 pb-32 pt-12">
    <div class="px-4 md:px-10 mx-auto w-full">
      <div>
        <!-- Card stats -->
        <div class="flex flex-wrap">
          <div class="w-full lg:w-6/12 xl:w-3/12 px-4">
            <card-stats
              statSubtitle="TOTAL MAHASISWA"
              statTitle="0"
              statIconName="fas fa-users"
              statIconColor="bg-orange-500"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import CardStats from "@/components/Cards/CardStats.vue";

export default {
  components: {
    CardStats,
  },
};
</script>
