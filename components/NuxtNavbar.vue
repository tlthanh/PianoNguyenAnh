<template>
  <div class="">
    <div class="bg-gray-500 border-black-500 sm:px-4 py-2.5 dark:bg-gray-800">
      <nav>
        <div class="flex justify-between items-center">
          <div class="w-1/5">
            <div class="w-20">
              <nuxt-link to="/">
                <img src="../assets/logo.png" alt="hình ảnh logo" />
              </nuxt-link>
            </div>
          </div>
          <div class="container w-auto">
            <ul
              class="flex flex-col text-white px-4 mt-4 md:flex-row md:space-x-8 md:mt-0 md:text-lg sm:text-lg md:font-semibold sm:font-bold"
            >
              <li class="hover:text-red-400">
                <nuxt-link to="/">TRANG CHỦ</nuxt-link>
              </li>
              <li class="hover:text-red-400">
                <nuxt-link to="/introduce">GIỚI THIỆU</nuxt-link>
              </li>
              <!-- hi -->
              <li class="dropdownn hover:text-red-400">
                <nuxt-link class="flex" to="/products">
                  <div>SẢN PHẨM</div>
                  <svg
                    class="h-5 w-5 mt-1"
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  >
                    <polyline points="6 9 12 15 18 9" />
                  </svg>
                </nuxt-link>
                <div class="">
                  <ul
                    class="flex flex-col bg-gray-900 bg-opacity-80 dropdown-menu absolute hidden text-white px-4 py-4 transform -translate-x-1/7 ease-linear delay-1000"
                  >
                    <li class="hover:text-red-400 py-2">
                      <nuxt-link to="/products/PianoUpright">
                        Piano Upright</nuxt-link
                      >
                    </li>
                    <li class="hover:text-red-400 py-2">
                      <nuxt-link to="/products/PianoGrand"
                        >Piano Grand</nuxt-link
                      >
                    </li>
                    <li class="hover:text-red-400 py-2">
                      <nuxt-link to="/products/PianoElectric"
                        >Piano Electric</nuxt-link
                      >
                    </li>
                  </ul>
                </div>
              </li>

              <li class="hover:text-red-400">
                <nuxt-link to="/policy">CHÍNH SÁCH</nuxt-link>
              </li>
              <li class="hover:text-red-400">
                <nuxt-link to="/contact">LIÊN HỆ</nuxt-link>
              </li>
            </ul>
          </div>

          <!-- search -->
          <div class="w-1/5 flex">
            <div class="pr-2">
              <!-- giỏ hàng -->

              <button
                id="viewCart"
                class="w-full px-2 pt-3 hover:text-red-400 animate-bounce"
                @click="ViewCart()"
              >
                <Cart />
                dsadsa
              </button>
            </div>
            <input
              class="placeholder:italic placeholder:text-slate-400 block bg-white w-full border border-slate-300 rounded-md py-2 pl-9 pr-3 shadow-sm focus:outline-none focus:border-sky-500 focus:ring-sky-500 focus:ring-1 sm:text-sm"
              placeholder="Search for piano..."
              type="text"
              name="search"
            />
          </div>
        </div>
      </nav>
    </div>

    <!-- slide bar -->
    <div
      v-if="slidebar"
      class="absolute top-0 w-full h-screen bg-black bg-opacity-40"
    >
      <div
        class="absolute rounded -right-1 w-1/3 h-screen bg-gray-100 top-0 shadow-blue-500 p-5 overflow-scroll"
      >
        <div
          class="absolute right-0 hover:bg-red-500 top-0 cursor-pointer p-1"
          @click="ViewCart()"
        >
          <CloseCart />
        </div>
        <!-- {{ cartId }} -->
        <h1 class="text-center text-3xl">GIỎ HÀNG</h1>

        <h1 class="text-center pb-5">_________________</h1>
        <div class="px-5">
          <div class="border-solid-2 border-gray-200">
            <div class="py-2 flex justify-between">
              {{ cart }}
              <img
                class="w-1/6"
                src="https://vietthuong.vn/upload/content/images/tuvan/piano/dan-piano-upright-la-gi-ma-hang-van-nguoi-tin-dung2.jpg"
                alt="piano"
              />

              <nuxt-link class="w-4/6 px-2" to="#pianosanpham"
                >APOLLO SR5301
              </nuxt-link>
              <button class="w-1/6 p-3 hover:text-gray-300">
                <delete-item />
              </button>
            </div>
            <h1 class="text-center">
              57.500.000 <span class="underline">VNĐ</span>
            </h1>
          </div>

          <div class="text-center">
            <h1>_______________________</h1>
          </div>

          <div
            @click="ViewCart()"
            class="my-3 container mx-auto text-center -right-1/2 my-5"
          >
            <nuxt-link
              class="text-center font-semibold text-xl bg-red-500 p-2 px-10 rounded-md hover:bg-red-400"
              to="/order"
              @click="OrderProduct()"
              >TIẾN HÀNH ĐẶT HÀNG</nuxt-link
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Fb from "./icons/fb.vue";
import Cart from "./icons/cart.vue";
import DeleteItem from "./icons/DeleteItem.vue";
import CloseCart from "./icons/CloseCart.vue";

export default {
  props: {},
  data() {
    return {
      slidebar: false,
      hihihi: "xin chào",
    };
  },
  methods: {
    ViewCart() {
      //console.log("click close");
      this.slidebar = !this.slidebar;
    },
    OrderProduct() {
      console.log("đặt hàng");
    },
  },
  components: { Fb, Cart, DeleteItem, CloseCart },
};
</script>

<style>
.dropdownn:hover .dropdown-menu {
  display: block;
}
</style>
