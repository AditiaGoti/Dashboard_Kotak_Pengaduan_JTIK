<template>
  <div>
    <sidebar />
    <div class="relative md:ml-64 bg-blueGray-100">
      <Header/>
      <div class="px-4 md:px-10 mx-auto w-full -m-24">
        <router-view />
        <footer-admin />
      </div>
    </div>
  </div>
</template>
<script>
import Sidebar from "@/components/Sidebar/Sidebar.vue";
import FooterAdmin from "@/components/Footers/FooterAdmin.vue";
import Header from '../components/Headers/Header.vue';
export default {
  name: "admin-layout",
  components: {
    Sidebar,
    FooterAdmin,
    Header
    },
};
</script>
