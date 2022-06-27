<template>
  <div>
    <div class="bg-blue-400 h-screen">
      <div class="flex justify-center">
        <div class="w-1/3"></div>
        <div class="w-1/3 place-items-center">
          <img src="./logo.png" alt="" class="w-50 ml-30" />
          <div class="bg-white rounded-md">
            <div class="h-5"></div>
            <h1 class="uppercase text-3xl text-center text-bold">Đăng nhập</h1>
            <div class="pb-10">
              <input
                class="bg-gray-200 appearance-none border-2 border-gray-200 rounded-2xl mt-5 ml-10 w-4/5 py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
                type="text"
                placeholder="Tên đăng nhập"
                required="Đừng có để trống"
              />
              <input
                class="bg-gray-200 appearance-none border-2 border-gray-200 rounded-2xl mt-5 ml-10 w-4/5 py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
                type="password"
                placeholder="Mật Khẩu"
                required="Đừng có để trống"
              />
            </div>
            <div>
              <button
                class="shadow bg-green-500 hover:bg-green-400 focus:shadow-outline focus:outline-none text-white font-bold ml-37 py-2 px-4 rounded"
              >
                ĐĂNG NHẬP
              </button>
              <div class="h-10"></div>
            </div>
          </div>
        </div>
        <div class="w-1/3"></div>
      </div>
    </div>
  </div>
</template>
