<template>
  <div
    class="relative flex flex-col min-w-0 break-words w-full mb-6 shadow-lg rounded"
    :class="[color === 'light' ? 'bg-white' : 'bg-emerald-900 text-white']"
  >
    <div class="rounded-t mb-0 px-4 py-3 border-0">
      <div class="flex flex-wrap items-center">
        <div class="relative w-full px-4 max-w-full flex-grow flex-1">
          <h3
            class="font-semibold text-lg"
            :class="[color === 'light' ? 'text-blueGray-700' : 'text-white']"
          >
            Tabel Moderasi Keluhan
          </h3>
        </div>
      </div>
    </div>
    <div class="block w-full overflow-x-auto">
      <!-- Projects table -->
      <table class="items-center w-full bg-transparent border-collapse">
        <thead>
          <tr>
            <th
              class="px-6 align-middle border border-solid py-3 text-xs uppercase border-l-0 border-r-0 whitespace-nowrap font-semibold text-left"
              :class="[
                color === 'light'
                  ? 'bg-blueGray-50 text-blueGray-500 border-blueGray-100'
                  : 'bg-emerald-800 text-emerald-300 border-emerald-700',
              ]"
            >
              Judul Keluhan
            </th>
            <th
              class="px-6 align-middle border border-solid py-3 text-xs uppercase border-l-0 border-r-0 whitespace-nowrap font-semibold text-left"
              :class="[
                color === 'light'
                  ? 'bg-blueGray-50 text-blueGray-500 border-blueGray-100'
                  : 'bg-emerald-800 text-emerald-300 border-emerald-700',
              ]"
            >
              Pembuat Keluhan
            </th>
            <th
              class="px-6 align-middle border border-solid py-3 text-xs uppercase border-l-0 border-r-0 whitespace-nowrap font-semibold text-left"
              :class="[
                color === 'light'
                  ? 'bg-blueGray-50 text-blueGray-500 border-blueGray-100'
                  : 'bg-emerald-800 text-emerald-300 border-emerald-700',
              ]"
            >
              Tujuan
            </th>
            <th
              class="px-6 align-middle border border-solid py-3 text-xs uppercase border-l-0 border-r-0 whitespace-nowrap font-semibold text-left"
              :class="[
                color === 'light'
                  ? 'bg-blueGray-50 text-blueGray-500 border-blueGray-100'
                  : 'bg-emerald-800 text-emerald-300 border-emerald-700',
              ]"
            >
              Kategori
            </th>
            <th
              class="px-6 align-middle border border-solid py-3 text-xs uppercase border-l-0 border-r-0 whitespace-nowrap font-semibold text-left"
              :class="[
                color === 'light'
                  ? 'bg-blueGray-50 text-blueGray-500 border-blueGray-100'
                  : 'bg-emerald-800 text-emerald-300 border-emerald-700',
              ]"
            >
              Waktu
            </th>
            <th
              class="px-6 align-middle border border-solid py-3 text-xs uppercase border-l-0 border-r-0 whitespace-nowrap font-semibold text-left"
              :class="[
                color === 'light'
                  ? 'bg-blueGray-50 text-blueGray-500 border-blueGray-100'
                  : 'bg-emerald-800 text-emerald-300 border-emerald-700',
              ]"
            >
              Aksi
            </th>
            <th
              class="px-6 align-middle border border-solid py-3 text-xs uppercase border-l-0 border-r-0 whitespace-nowrap font-semibold text-left"
              :class="[
                color === 'light'
                  ? 'bg-blueGray-50 text-blueGray-500 border-blueGray-100'
                  : 'bg-emerald-800 text-emerald-300 border-emerald-700',
              ]"
            ></th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th
              class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4 text-left flex items-center"
            >
              <span
                class="font-bold"
                :class="[
                  color === 'light' ? 'text-blueGray-600' : 'text-white',
                ]"
              >
                Susah dalam menyampaikan pendapat
              </span>
            </th>
            <td
              class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
            >
              anonim
            </td>
            <td
              class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
            >
              <i></i> JTIK
            </td>
            <td
              class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
            >
              <i></i> Fasilitas/ Layanan
            </td>
            <td
              class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
            >
              04-12-2023, 11:10
            </td>
            <td
              class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
            >
              <div class="flex items-center mouse-pointer" @click="showModal = true">
                <span class="mr-2 moderasi">Moderasi</span>
                <div v-if="showModal">
                <div class="modal-backdrop"></div>
                <div class="modal">
                  <div class="flex flex-row justify-between">
                  <p class="text-xl font-bold	text-red-500 mb-6">Moderasi Keluhan</p>
                  <div>
                          <img
                            :src="close"
                            class="h-8 w-8 cursor-pointer"
                            alt="..."
                            @click="closeModal"
                          />
                  </div>
                  </div>  
                <div class="grid grid-cols-2 mb-4" >
                    <div class="flex flex-col">
                      <div class="mr-4">
                      <p class="align-middle text-xs uppercase whitespace-nowrap font-semibold text-left"> Judul Keluhan </p>
                        <p class="text-md mt-1 break-words whitespace-normal mb-5 "> Tidak Bisa Menyampaikan Keluhan </p>
                        <p class="align-middle text-xs uppercase whitespace-nowrap font-semibold text-left"> Isi Keluhan </p>
                        <p class="text-md mt-1 break-words whitespace-normal">Lorem ipsum dolor sit amet, 
                          consectetur adipiscing elit. Faucibus velit, adipiscing senectus
                           eget semper id. Pretium venenatis ridiculus ornare nec a, arcu aenean. 
                            at scelerisque porta etiam consectetur varius. Arcu, quis sed dictum libero. 
                            Nulla eu commodo in odio aenean sit amet mattis. Purus massa velit sapien 
                            fermentum non amet, amet ac. Magnis mattis egestas lobortis elementum elit 
                            ut rhoncus. Viverra vivamus condimentum nisl erat lobortis dictum risus
                             scelerisque. Dapibus semper eu est et non neque, sed. Massa, id nunc lectus 
                             , tortor. Non a, eget imperdiet proin turpis placerat. Sagittis donec 
                              feugiat orci dolor. </p>
                      </div>
                    </div>
                    <div class="flex flex-col">
                        <p class="align-middle text-xs uppercase whitespace-nowrap font-semibold text-left"> Kategori Keluhan </p>
                        <p class="text-md mt-1 mb-5 break-words whitespace-normal">Fasilitas/Layanan</p>
                        <p class="align-middle text-xs uppercase whitespace-nowrap font-semibold text-left"> Tujuan </p>
                        <p class="text-md mt-1 mb-5">JTIK</p>
                        <p class="align-middle text-xs uppercase whitespace-nowrap font-semibold text-left"> Waktu Pembuatan </p>
                        <p class="text-md mt-1">13-04-2023, 11:59</p>
                    </div>
                </div>
                <hr class="mb-5 "/>
                <footer className="bg-white flex flex-row-reverse">
            <button class="w-fit
        py-3
        pl-4
        pr-4	
        text-l
        font-semibold
        mx-4
        rounded-md
        bg-emerald-600	
        text-white
        hover:bg-pink-500"> 
              Publikasikan Keluhan
            </button>
            <button class="w-fit
        py-3
        pl-4
        pr-4	
        text-l
        font-semibold
        rounded-md
        bg-red-500
        text-white
        hover:bg-pink-500">
              Tolak Keluhan
            </button>
          </footer>
                  <!-- <div @click="showModal = false">Tutup Modal</div> -->
                </div>
              </div>
              </div>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<script>

import bootstrap from "@/assets/img/bootstrap.jpg";
import close from "@/assets/img/x.svg";


export default {
  data() {
    return {
      bootstrap,
      close,
      showModal: false,
    };
  },
  components: {
    
  },
  props: {
    color: {
      default: "light",
      validator: function (value) {
        // The value must match one of these strings
        return ["light", "dark"].indexOf(value) !== -1;
      },
    },
  },
};
</script>
<style>
.modal-backdrop {
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}

.modal {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: white;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.3);
}
td:hover .moderasi {
  color: blue;
  cursor: pointer;
}
</style>