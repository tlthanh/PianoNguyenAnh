<template>
  <div>
    <AdminNavbar />
    <div class="w-4/5 absolute right-0 p-5">
      <h1 class="font-600 text-3xl tracking-2px">Thêm mới sản phẩm</h1>
      <form method="POST">
        <div class="flex">
          <div class="w-3/5 mx-2">
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              v-model="piano_name"
              placeholder="Tên sản phẩm"
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              v-model="piano_code"
              placeholder="Mã sản phẩm"
              required="Đừng có để trống"
            />
            <label for="">Loại sản phẩm </label>
            <select
              class="bg-white border border-gray-400 hover:bg-gray-200 px-4 py-2 rounded shadow leading-tight focus:outline-none focus:shadow-outline mt-3"
              v-model="piano_type"
            >
              <option value="PianoUpright">Piano Upright</option>
              <option value="PianoGrand">Piano Grand</option>
              <option value="PianoElectric">Piano Electric</option>
            </select>
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              v-model="price"
              placeholder="Giá sản phẩm"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              v-model="discount"
              placeholder="Giá khuyến mãi"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              v-model="image"
              placeholder="Link ảnh sản phẩm"
              required="Đừng có để trống"
            />
            <textarea
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              placeholder="Mô tả sản phẩm"
              v-model="descriptions"
              required="Đừng có để trống"
            />
          </div>
          <div class="w-2/5 mx-4">
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              v-model="origin"
              placeholder="Xuất xứ"
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              v-model="manufacturer"
              placeholder="Hãng sản xuất"
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              v-model="keys"
              placeholder="Keys"
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              v-model="weight"
              placeholder="Khối lượng"
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              v-model="size"
              placeholder="Kích thước "
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              v-model="pedals"
              placeholder="Pedals"
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              v-model="warranty"
              placeholder="Bảo hành"
              required="Đừng có để trống"
            />
            <input
              class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
              type="text"
              v-model="service"
              placeholder="Dịch vụ đi kèm"
              required="Đừng có để trống"
            />
          </div>
        </div>
        <nuxt-link to="/admin/products">
          <el-button type="danger"> HỦY</el-button>
        </nuxt-link>

        <el-button type="primary" @click="CreateProduct()">
          THÊM SẢN PHẨM
        </el-button>

        <!-- <el-button type="text" @click="centerDialogVisible = true"
          >Click to open the Dialog</el-button
        >

        <el-dialog
          title="Warning"
          :visible.sync="centerDialogVisible"
          width="30%"
          center
        >
          <span
            >It should be noted that the content will not be aligned in center
            by default</span
          >
          <span slot="footer" class="dialog-footer">
            <el-button @click="centerDialogVisible = false">Cancel</el-button>
            <el-button type="primary" @click="centerDialogVisible = false"
              >Confirm</el-button
            >
          </span> -->
        <!-- </el-dialog> -->
      </form>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      dialogStatus: "",
      piano_name: null,
      piano_code: null,
      piano_type: null,
      price: null,
      discount: null,
      origin: null,
      manufacturer: null,
      keys: null,
      weight: null,
      size: null,
      pedals: null,
      warranty: null,
      service: null,
      image: null,
      descriptions: null,
    };
  },
  methods: {
    CreateProduct() {
      axios({
        method: "POST",
        url: "http://127.0.0.1:3006/product",
        data: {
          piano_name: this.piano_name,
          piano_code: this.piano_code,
          piano_type: this.piano_type,
          price: this.price,
          discount: this.discount,
          short_des: [
            {
              origin: this.origin,
              manufacturer: this.manufacturer,
              keys: this.keys,
              weight: this.weight,
              size: this.size,
              pedals: this.pedals,
              warranty: this.warranty,
              service: this.service,
            },
          ],

          image: this.image,
          long_des: [
            {
              descriptions: this.descriptions,
            },
          ],
        },
      })
        .then(() => {
          this.$router.push("/admin/products");
          this.$notify({
            title: "Success",
            message: "Tạo Mới Sản Phẩm Thành Công",
            type: "success",
            duration: 2000,
          });
        })
        .catch((error) => {
          console.log(error);
          this.$notify({
            title: "Không Thành Công",
            message: "Tạo Mới Sản Phẩm Không Thành Công",
            type: "error",
            duration: 2000,
          });
        });
    },
  },
};
</script>
