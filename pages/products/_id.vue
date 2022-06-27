<template>
  <div>
    <div class="fixed w-full">
      <NuxtNavbar />
    </div>
    <div class="w-11/12 mx-auto pt-32">
      <h1 class="text-center font-600 text-4xl tracking-2px">
        SẢN PHẨM CỦA CHÚNG TÔI
      </h1>
      <div class="">
        <h1 class="uppercase font-400 text-2xl">
          lOẠI: <span class="text-red-500"> {{ this.$route.params.id }}</span>
        </h1>
        <div class="my-10">
          <div class="inline-flex" v-for="item in product" :key="item.id">
            <div class="w-1/5 text-center mx-2">
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
import NuxtNavbar from "~/components/NuxtNavbar.vue";
export default {
  data() {
    return {
      product: [],
      //   short_des: [],
    };
  },
  async axios() {
    await this.getproduct(this.$route.params.id);
  },
  created() {
    this.getproduct();
  },
  methods: {
    getproduct() {
      this.product = [];
      axios
        .get("http://127.0.0.1:3006/productType/" + this.$route.params.id)
        .then((product) => {
          this.product = product.data;
          console.log("product", this.product);
        });
    },
    Seedetails(id) {
      this.$router.push("/" + id);
    },
  },
  components: { NuxtNavbar },
};
</script>
