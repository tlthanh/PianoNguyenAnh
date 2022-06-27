<template>
  <div class="h-auto bg-gray-100">
    <div class="fixed w-full">
      <NuxtNavbar />
    </div>
    <div class="w-11/12 mx-auto pt-32">
      <div class="flex">
        <div class="w-2/5 inline-flex justify-center">
          <img alt="" :src="product.image" class="inline-flex w-100 h-100" />
        </div>
        <div class="w-1/3">
          <h1 class="uppercase text-2xl my-1">{{ product.piano_name }}</h1>
          <h1 class="font-bold text-xl text-red-600 my-1">
            {{ product.price }}
          </h1>
          <h1>MÃ SẢN PHẨM: {{ product.piano_code }}</h1>
          <h1>THÔNG SỐ</h1>
          <div v-for="item in product.short_des" :key="item.id">
            <table class="w-5/6 text-left border-solid">
              <tr class="">
                <th>Xuất xứ</th>
                <td>{{ item.origin }}</td>
              </tr>
              <tr>
                <th>Hãng sản xuất</th>
                <td>{{ item.manufacturer }}</td>
              </tr>
              <tr>
                <th>Key</th>
                <td>{{ item.keys }}</td>
              </tr>
              <tr>
                <th>Khối Lượng</th>
                <td>{{ item.weight }}</td>
              </tr>
              <tr>
                <th>Kích Thước</th>
                <td>{{ item.size }}</td>
              </tr>
              <tr>
                <th>Pedals</th>
                <td>{{ item.pedals }}</td>
              </tr>
              <tr>
                <th>Bảo Hành</th>
                <td>{{ item.warranty }}</td>
              </tr>
              <tr>
                <th>Dịch Vụ Đi Kèm</th>
                <td>{{ item.service }}</td>
              </tr>
            </table>
            <div class="mt-10 mb-20 inline-flex">
              <button
                class="shadow bg-yellow-500 hover:bg-yellow-400 focus:shadow-outline focus:outline-none text-white font-bold mx-3 py-2 px-2 rounded"
                @click="pushCart(item)"
              >
                THÊM VÀO GIỎ HÀNG
              </button>
            </div>
          </div>
        </div>
        <div class="w-1/4">
          <h1>Sản phẩm đang giảm giá</h1>
          <div v-for="(item, index) in dataDiscout" :key="item.index">
            <div v-if="index < 4" class="w-11/12 text-center mx-2 my-5">
              <button @click="Seedetails(item.id)" class="w-full inline-flex">
                <img class="w-1/3" :src="item.image" alt="giảm giá" />
                <div>
                  <h1 class="uppercase text-2xl my-1">{{ item.piano_name }}</h1>
                  <h1 class="font-bold text-red-600 my-1">
                    {{ item.price }} VNĐ
                  </h1>
                </div>
              </button>
            </div>
          </div>
        </div>
      </div>
      <div v-for="item in product.long_des" :key="item.index" class="my-20">
        <h1>MÔ TẢ SẢN PHẨM</h1>
        <h1>{{ item.descriptions }}"</h1>
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
      dataDiscout: [],
      // cartId: [],
    };
  },
  computed: {
    cart() {
      return this.$store.state.cart.list;
    },
  },
  async axios() {
    await this.getproduct(this.$route.params.id);
  },
  async fetch() {
    await axios
      .get("http://127.0.0.1:3006/productDiscount")
      .then((resDiscount) => {
        this.dataDiscout = resDiscount.data;
      });
  },
  created() {
    this.getproduct();
  },
  methods: {
    getproduct() {
      this.product = [];
      axios
        .get("http://127.0.0.1:3006/product/" + this.$route.params.id)
        .then((product) => {
          this.product = product.data;
          //   this.short_des = product.short_des;
          // console.log("product", this.product);
          //   console.log("product haha", this.product.short_des);
        });
    },
    Seedetails(id) {
      this.$router.push("/" + id);
    },
    pushCart(item) {
      console.log("this.$store.commit", this.$store.commit("cart/add", item));
      this.$store.commit("cart/add", item);
    },
  },

  components: { NuxtNavbar },
};
</script>
