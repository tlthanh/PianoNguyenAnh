<template>
  <div class="h-auto bg-gray-200">
    <div class="fixed w-full">
      <NuxtNavbar />
    </div>
    <div class="w-11/12 mx-auto pt-32">
      <h1 class="text-center font-600 text-4xl tracking-2px">
        SẢN PHẨM CỦA CHÚNG TÔI
      </h1>
      <div class="">
        <div class="my-10">
          <div class="inline-flex" v-for="item in dataProduct" :key="item.id">
            <div class="w-1/4 text-center mx-2">
              <button @click="Seedetails(item.id)" class="w-70">
                <img class="w-70 h-70" :src="item.image" alt="giảm giá" />
                <h1>{{ item.piano_name }}</h1>
                <h1>{{ item.price }}</h1>
              </button>
            </div>
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
      dataProduct: [],
      dataGrand: [],
      dataUpright: [],
      dataElectric: [],
    };
  },
  async fetch() {
    await axios.get("http://127.0.0.1:3006/products").then((res) => {
      this.dataProduct = res.data;
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
