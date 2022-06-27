<template>
  <div>
    <AdminNavbar />
    <div class="w-4/5 absolute right-0 p-5">
      <h1 class="font-600 text-3xl tracking-2px">SỬA THÔNG TIN SẢN PHẨM</h1>
      <form method="POST">
        <div class="flex">
          <div class="w-3/5 mx-2">
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              :value="product.piano_name"
              placeholder="Tên sản phẩm"
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              :value="product.piano_name"
              placeholder="Mã sản phẩm"
              required="Đừng có để trống"
            />
            <label for="">Loại sản phẩm </label>
            <select
              class="bg-white border border-gray-400 hover:bg-gray-200 px-4 py-2 rounded shadow leading-tight focus:outline-none focus:shadow-outline mt-3"
              :value="product.piano_type"
            >
              <option value="PianoUpright">Piano Upright</option>
              <option value="PianoGrand">Piano Grand</option>
              <option value="PianoElectric">Piano Electric</option>
            </select>
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              :value="product.price"
              placeholder="Giá sản phẩm"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              :value="product.discount"
              placeholder="Giá khuyến mãi"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              :value="product.image"
              placeholder="Link ảnh sản phẩm"
              required="Đừng có để trống"
            />
            <textarea
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              placeholder="Mô tả sản phẩm"
              :value="product.descriptions"
              required="Đừng có để trống"
            />
          </div>
          <div class="w-2/5 mx-4">
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              :value="short_des.origin"
              placeholder="Xuất xứ"
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              :value="short_des.manufacturer"
              placeholder="Hãng sản xuất"
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              :value="short_des.keys"
              placeholder="Keys"
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              :value="short_des.weight"
              placeholder="Khối lượng"
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              :value="short_des.size"
              placeholder="Kích thước "
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              :value="short_des.pedals"
              placeholder="Pedals"
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              :value="short_des.warranty"
              placeholder="Bảo hành"
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              :value="short_des.service"
              placeholder="Dịch vụ đi kèm"
              required="Đừng có để trống"
            />
          </div>
        </div>
        <nuxt-link
          class="shadow bg-gray-500 hover:bg-gray-400 focus:shadow-outline focus:outline-none text-white font-bold mx-5 py-2 px-4 rounded"
          to="/admin/products"
        >
          HỦY
        </nuxt-link>
        <button
          class="shadow bg-green-500 hover:bg-green-400 focus:shadow-outline focus:outline-none text-white font-bold mx-5 py-2 px-4 rounded"
          @click="CreateProduct()"
        >
          THÊM SẢN PHẨM
        </button>
      </form>
    </div>
  </div>
</template>
<script>
import axios from "axios";
export default {
  data() {
    return {
      product: [],
      short_des: [],
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
        .get("http://127.0.0.1:3006/product/" + this.$route.params.id)
        .then((product) => {
          this.product = product.data;
          this.short_des = product.data.short_des;
          console.log("product", this.product);
          console.log("product", this.short_des);
        });
    },
  },
};
</script>
