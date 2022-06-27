<template>
  <div class="h-auto bg-gray-100">
    <div class="fixed w-full">
      <NuxtNavbar />
    </div>

    <div class="w-11/12 mx-auto pt-25">
      <div>
        <img
          src="https://cdn.pixabay.com/photo/2015/11/10/08/31/banner-1036482_960_720.jpg"
          alt="Ảnh banner"
          class="w-full"
        />
        <!-- <img src="../assets/banner.jpg" alt="Ảnh banner" class="w-full" /> -->
      </div>

      <div class="my-10">
        <h1 class="text-center uppercase text-2xl font-bold">
          Các sản phẩm được giảm giá
        </h1>
        <h1 class="text-color-blue-200 text-center">
          ___________________________________________
        </h1>
        <div
          class="inline-flex mt-5"
          v-for="(item, index) in dataDiscout"
          :key="item.index"
        >
          <div v-if="index < 4" class="w-1/4 text-center mx-2">
            <button @click="Seedetails(item.id)" class="w-70">
              <img class="w-70 h-70" :src="item.image" alt="giảm giá" />
              <h1 class="uppercase text-2xl my-1">{{ item.piano_name }}</h1>
              <h1 class="font-bold text-red-600 my-1">{{ item.price }} VNĐ</h1>
            </button>
          </div>
        </div>
      </div>

      <div class="my-10">
        <h1 class="text-center uppercase text-2xl font-bold">
          Đàn piano grand
        </h1>
        <h1 class="text-color-blue-200 text-center">
          ___________________________________________
        </h1>
        <div
          class="inline-flex mt-5"
          v-for="(item, index) in dataGrand"
          :key="item.index"
        >
          <div v-if="index < 4" class="w-1/4 text-center mx-2">
            <button @click="Seedetails(item.id)" class="w-70">
              <img class="w-70 h-70" :src="item.image" alt="giảm giá" />
              <h1 class="uppercase text-2xl my-1">{{ item.piano_name }}</h1>
              <h1 class="font-bold text-red-600 my-1">{{ item.price }} VNĐ</h1>
            </button>
          </div>
        </div>
      </div>

      <div class="my-10">
        <h1 class="text-center uppercase text-2xl font-bold">
          Đàn piano upright
        </h1>
        <h1 class="text-color-blue-200 text-center">
          ___________________________________________
        </h1>
        <div
          class="inline-flex mt-5"
          v-for="(item, index) in dataUpright"
          :key="item.index"
        >
          <div v-if="index < 4" class="w-1/4 text-center mx-2">
            <button @click="Seedetails(item.id)" class="w-70">
              <img class="w-70 h-70" :src="item.image" alt="giảm giá" />
              <h1 class="uppercase text-2xl my-1">{{ item.piano_name }}</h1>
              <h1 class="font-bold text-red-600 my-1">{{ item.price }} VNĐ</h1>
            </button>
          </div>
        </div>
      </div>

      <div class="my-10">
        <h1 class="text-center uppercase text-2xl font-bold">Đàn piano Điện</h1>
        <h1 class="text-color-blue-200 text-center">
          ___________________________________________
        </h1>
        <div
          class="inline-flex mt-5"
          v-for="(item, index) in dataElectric"
          :key="item.index"
        >
          <div v-if="index < 4" class="w-1/4 text-center mx-2">
            <button @click="Seedetails(item.id)" class="w-70">
              <img class="w-70 h-70" :src="item.image" alt="giảm giá" />
              <h1 class="uppercase text-2xl my-1">{{ item.piano_name }}</h1>
              <h1 class="font-bold text-red-600 my-1">{{ item.price }} VNĐ</h1>
            </button>
          </div>
        </div>
      </div>
    </div>
    <div class="bottom-0">
      <NuxtFooter />
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      dataDiscout: [],
      dataGrand: [],
      dataUpright: [],
      dataElectric: [],
    };
  },
  async fetch() {
    await axios
      .get("http://127.0.0.1:3006/productDiscount")
      .then((resDiscount) => {
        this.dataDiscout = resDiscount.data;
        // console.log("res.dataDiscou", resDiscount.dataDiscout);
        // console.log("this.dataDiscout", this.dataDiscout);
      });
    await axios.get("http://127.0.0.1:3006/productGrand").then((resGrand) => {
      this.dataGrand = resGrand.data;
    });
    await axios
      .get("http://127.0.0.1:3006/productUpright")
      .then((resUpright) => {
        this.dataUpright = resUpright.data;
      });
    await axios
      .get("http://127.0.0.1:3006/productElectric")
      .then((resElectric) => {
        this.dataElectric = resElectric.data;
      });
  },
  created() {
    //  GetData() {
    //   axios.get("http://127.0.0.1:3006/products").then((res) => {
    //     this.data = res.data;
    //   });
  },

  methods: {
    Seedetails(id) {
      this.$router.push("/" + id);
    },
  },
};
</script>
