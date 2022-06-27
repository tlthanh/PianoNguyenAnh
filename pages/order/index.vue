<template>
  <div class="h-auto bg-gray-200">
    <div class="fixed w-full">
      <NuxtNavbar />
    </div>

    <div class="w-11/12 mx-auto bg-gray-50 pt-23">
      <div class="flex justify-bettwen w-full my-10">
        <!-- info Cus -->
        <div class="container w-2/5 mx-5">
          <form action="">
            <h1 class="font-semibold text-2xl">THÔNG TIN ĐẶT HÀNG</h1>
            <table class="w-full">
              <tr>
                <th>Họ tên</th>
                <td>
                  <input
                    class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
                    type="text"
                    placeholder="Họ tên"
                    required="Đừng có để trống"
                  />
                </td>
              </tr>
              <tr>
                <th>Số điện thoại</th>
                <td>
                  <input
                    class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
                    type="text"
                    placeholder="Số điện thoại"
                    required="Đừng có để trống"
                  />
                </td>
              </tr>
              <tr>
                <th>Email</th>
                <td>
                  <input
                    class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
                    type="text"
                    placeholder="Email"
                    required="Đừng có để trống"
                  />
                </td>
              </tr>
              <tr>
                <th>Tỉnh/Thành phố</th>
                <td>
                  <input
                    class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
                    type="text"
                    placeholder="Tỉnh/Thành phố"
                    required="Đừng có để trống"
                  />
                </td>
              </tr>
              <tr>
                <th>Quận/Huyện</th>
                <td>
                  <input
                    class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
                    type="text"
                    placeholder="Quận/Huyện"
                    required="Đừng có để trống"
                  />
                </td>
              </tr>
              <tr>
                <th>Xã/Phường</th>
                <td>
                  <input
                    class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
                    type="text"
                    placeholder="Xã/Phường"
                    required="Đừng có để trống"
                  />
                </td>
              </tr>
              <tr>
                <th>Địa chỉ cụ thể</th>
                <td>
                  <input
                    class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
                    type="text"
                    placeholder="Địa chỉ cụ thể"
                    required="Đừng có để trống"
                  />
                </td>
              </tr>
              <tr>
                <th>Ghi chú</th>
                <td>
                  <input
                    class="bg-gray-200 appearance-none border-2 border-gray-200 rounded mt-5 w-full py-4 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-purple-500"
                    type="text"
                    placeholder="Ghi chú"
                    required="Đừng có để trống"
                  />
                </td>
              </tr>
            </table>
          </form>
        </div>
        <!-- info order -->
        <div class="w-3/5 mx-5 my-10">
          <div class="border-solid-1 border-gray-500">
            <h1 class="font-semibold text-2xl">ĐƠN HÀNG CỦA BẠN</h1>
            <div class="my-5">
              <table class="border-solid-2 border-gray-500">
                <tr>
                  <th>Hình ảnh</th>
                  <th>Tên Sản Phẩm</th>
                  <th>Giá (VNĐ)</th>
                </tr>
                <tr>
                  <td class="w-2/6">
                    <img
                      src="https://vietthuong.vn/upload/content/images/tuvan/piano/dan-piano-upright-la-gi-ma-hang-van-nguoi-tin-dung2.jpg"
                      alt=""
                    />
                  </td>
                  <td class="font-semibold text-2xl text-center">
                    APOLO SR5301
                  </td>
                  <td class="font-semibold text-2xl text-center">57.500.000</td>
                </tr>
                <tr class="my-20 border-solid-2 border-gray-500">
                  <td class="py-10 font-semibold text-2xl text-center">Tổng</td>
                  <td></td>
                  <td class="font-semibold text-2xl text-center">57.500.000</td>
                </tr>
              </table>
            </div>
            <button
              class="shadow bg-blue-500 hover:bg-blue-400 focus:shadow-outline focus:outline-none text-white font-bold mx-5 py-2 px-4 rounded"
            >
              ĐẶT HÀNG
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
