<template>
  <div>
    <div class="w-full bg-blue-500 h-15 items-end flex">
      <div class="w-1/3"></div>
      <div class="w-1/3"></div>
      <div class="w-1/3">
        <button
          class="shadow bg-gray-500 hover:bg-gray-400 focus:shadow-outline focus:outline-none text-white font-bold ml-37 py-2 px-4 rounded ml-80"
        >
          ĐĂNG XUẤT
        </button>
      </div>
    </div>
    <div class="absolute top-0 w-1/5 h-screen bg-gray-700">
      <div class="w-35 p-3 text-center">
        <nuxt-link to="/" class="bg-white">
          <img src="../assets/logo.png" alt="hình ảnh logo" />
        </nuxt-link>
      </div>
      <div class="py-5 w-full">
        <div
          class="my-1 text-center font-bold text-xl hover:bg-indigo-800 cursor-pointer"
        >
          <nuxt-link class="block py-5 w-full text-white" to="/admin/products"
            >QUẢN LÝ SẢN PHẨM</nuxt-link
          >
        </div>
        <div
          class="my-1 text-center font-bold text-xl hover:bg-indigo-800 cursor-pointer"
        >
          <nuxt-link class="block py-5 w-full text-white" to="/admin/orders"
            >QUẢN LÝ ĐƠN HÀNG</nuxt-link
          >
        </div>
        <div
          class="my-1 text-center font-bold text-xl hover:bg-indigo-800 cursor-pointer"
        >
          <nuxt-link class="block py-5 w-full text-white" to="/admin/categories"
            >QUẢN LÝ HÓA ĐƠN</nuxt-link
          >
        </div>
      </div>
    </div>
  </div>
</template>
