<template>
  <div class="bottom-0">
    <div class="w-full bg-black flex text-white text-center bottom-0">
      <!-- <h1 class="text-light-50">this is the footer</h1> -->
      <div class="w-1/3">
        <h1 class="font-400 text-3xl text-center py-1 tracking-1px">
          Sản phẩm
        </h1>
        <div class="flex justify-center">
          <ul class="text-white px-4 py-4 w-2/5">
            <li class="hover:text-red-400 py-2 flex">
              <Bigger class="pt-1" />
              <nuxt-link to="#option1">
                <h1>Piano Upright</h1>
              </nuxt-link>
            </li>
            <li class="hover:text-red-400 py-2 flex">
              <Bigger class="pt-1" />
              <nuxt-link to="#option2"> Piano Grand </nuxt-link>
            </li>
            <li class="hover:text-red-400 py-2 flex">
              <Bigger class="pt-1" />
              <nuxt-link to="#option3"> Piano Electric</nuxt-link>
            </li>
          </ul>
        </div>
      </div>
      <div class="w-1/3">
        <h1 class="font-400 text-3xl text-center py-1 tracking-1px">
          Liên hệ với chúng tôi
        </h1>
        <div class="flex hover:text-red-500">
          <Address class="mt-2 w-1/6" />
          <nuxt-link class="p-1 w-5/6 hover:text-red-500 text-xl" to="#"
            >P4.02, Cao ốc căn hộ Thái An, 2290 Quốc Lộ 1A, Phường Trung Mỹ Tây,
            Quận 12, Tp. Hồ Chí Minh</nuxt-link
          >
        </div>
        <div class="flex hover:text-red-500">
          <Email class="mt-1 w-1/6" />
          <nuxt-link class="p-1 w-5/6 hover:text-red-500 text-xl" to="#"
            >Minhgiap.artist@gmail.com</nuxt-link
          >
        </div>
        <div class="flex hover:text-red-500">
          <Phone class="mt-1 w-1/6" />

          <nuxt-link class="p-1 w-5/6 hover:text-red-500 text-2xl" to="#"
            >0937053688</nuxt-link
          >
        </div>
      </div>
      <div class="w-1/3">
        <h1 class="font-400 text-3xl text-center py-1 tracking-1px">
          Theo dõi chúng tôi
        </h1>
        <div class="flex justify-center">
          <nuxt-link class="mx-2 hover:text-blue-500" to="">
            <fb />
          </nuxt-link>
          <nuxt-link class="mx-2 hover:text-purple-500" to="">
            <Tiktok />
          </nuxt-link>
          <nuxt-link class="mx-2 hover:text-red-500" to="">
            <Youtube />
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Address from "~/components/icons/address.vue";
import Bigger from "./icons/bigger.vue";
import Email from "./icons/email.vue";
import Fb from "./icons/fb.vue";
import Phone from "./icons/phone.vue";
import Tiktok from "./icons/tiktok.vue";
import Youtube from "./icons/youtube.vue";
export default {
  components: { Address, Phone, Email, Fb, Tiktok, Youtube, Bigger },
};
</script>
