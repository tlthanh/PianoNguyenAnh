<template>
  <div>
    <div class="fixed w-full block">
      <NuxtNavbar />
    </div>
    <div class="w-11/12 mx-auto bg-gray-50 pt-32">
      <h1 class="text-center font-600 text-4xl tracking-2px">
        PIANO NGUYÊN ANH
      </h1>
      <div class="flex justify-between w-4/5 mx-auto py-10">
        <div class="w-1/3">
          <h1 class="font-400 text-3xl text-center py-1 tracking-1px">
            ĐỊA CHỈ
          </h1>
          <div class="flex hover:text-red-500">
            <Address class="mt-2 w-1/6" />
            <a
              class="p-1 w-5/6 hover:text-red-500 text-xl"
              href="https://www.google.com/maps/place/Piano+Nguy%C3%AAn+Anh/@10.8491132,106.6242452,21z/data=!4m12!1m6!3m5!1s0x31752a266eb397a9:0x3dc5e2db8f0b8d61!2zQ2h1bmcgQ8awIFRow6FpIEFu!8m2!3d10.8495915!4d106.6244231!3m4!1s0x31752bdb59552cf5:0x5e181ad3790d3e9e!8m2!3d10.8491291!4d106.6243523"
            >
              P4.02, Cao ốc căn hộ Thái An, 2290 Quốc Lộ 1A, Phường Trung Mỹ
              Tây, Quận 12, Tp. Hồ Chí Minh
            </a>
          </div>
        </div>
        <div class="w-1/3">
          <h1 class="font-400 text-3xl text-center py-1 tracking-1px">EMAIL</h1>
          <div class="flex hover:text-red-500">
            <email class="mt-1 w-1/6" />
            <nuxt-link class="p-1 w-5/6 hover:text-red-500 text-xl" to="#"
              >Minhgiap.artist@gmail.com</nuxt-link
            >
          </div>
        </div>
        <div class="w-1/3">
          <h1 class="font-400 text-3xl text-center py-1 tracking-1px">
            HOTLINE 24/7
          </h1>
          <div class="flex justify-center hover:text-red-500">
            <Phone class="mt-1 w-1/6" />

            <nuxt-link class="p-1 w-2/3 hover:text-red-500 text-2xl" to="#"
              >0937053688</nuxt-link
            >
          </div>
        </div>
      </div>
      <div class="flex justify-center">
        <a href="https://www.google.com/maps">
          <img
            src="https://cdn.tgdd.vn/Files/2020/11/10/1305861/googlemap_1280x720-800-resize.jpg"
            alt="googlemap"
        /></a>
      </div>
    </div>
    <NuxtFooter />
  </div>
</template>
<script>
import Address from "~/components/icons/address.vue";
import email from "~/components/icons/email.vue";
import Phone from "~/components/icons/phone.vue";

import NuxtFooter from "~/components/NuxtFooter.vue";
export default {
  components: { email, Address, Phone, NuxtFooter },
};
</script>
