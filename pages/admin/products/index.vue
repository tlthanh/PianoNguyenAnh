<template>
  <div>
    <AdminNavbar />

    <div class="w-4/5 absolute right-0 p-10">
      <div class="my-5">
        <nuxt-link
          class="shadow bg-blue-500 hover:bg-blue-400 focus:shadow-outline focus:outline-none text-white font-bold mx-5 py-2 px-4 rounded"
          to="/admin/products/create"
          >Thêm sản phẩm</nuxt-link
        >
      </div>
      <div>
        <!-- {{ data }} -->
      </div>
      <table
        class="border-solid-2 border-solid-black border-collapse-2 border-collapse-black w-4/5"
      >
        <thead>
          <tr>
            <th>STT</th>
            <th>TÊN SẢN PHẨM</th>
            <th>MÃ SẢN PHẨM</th>
            <th></th>
          </tr>
        </thead>
        <tbody
          class="text-center table-row-group table-auto border-collapse py-3"
          v-for="(item, index) in data"
          :key="item.index"
        >
          <tr>
            <td>{{ index + 1 }}</td>
            <td>{{ item.piano_name }}</td>
            <td>{{ item.piano_code }}</td>
            <td>
              <button
                class="shadow bg-yellow-500 hover:bg-yellow-400 focus:shadow-outline focus:outline-none text-white font-bold mx-5 py-2 px-4 rounded"
                @click="Seedetails(item.id)"
              >
                Sửa
              </button>
              <button
                class="shadow bg-red-500 hover:bg-red-400 focus:shadow-outline focus:outline-none text-white font-bold mx-5 py-2 px-4 rounded"
              >
                Xóa
              </button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      data: [],
    };
  },
  async fetch() {
    await axios.get("http://127.0.0.1:3006/products").then((res) => {
      this.data = res.data;
    });
  },
  created() {},

  methods: {
    Seedetails(id) {
      this.$router.push("/admin/products/" + id);
    },
  },
};
</script>
