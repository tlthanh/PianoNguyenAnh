<template>
  <div>
    <AdminNavbar />
    <div class="w-4/5 absolute right-0 p-10">
      <div class="my-5">
        <h1 class="text-center font-600 text-4xl tracking-2px">
          QUẢN LÝ ĐƠN ĐẶT HÀNG
        </h1>
      </div>
      <div></div>
      <table
        class="border-solid-2 border-solid-black border-collapse-2 border-collapse-black w-full"
      >
        <thead>
          <tr>
            <th class="w-1/12">STT</th>
            <th class="w-1/6">KHÁCH HÀNG</th>
            <th>SỐ ĐIỆN THOẠI</th>
            <!-- <th>EMAIL</th> -->
            <th>TÊN SẢN PHẨM</th>
            <th>GIÁ</th>
            <th>TRẠNG THÁI</th>
            <th class="w-1/6">GHI CHÚ</th>
            <th class="w-1/12"></th>
          </tr>
        </thead>
        <tbody
          class="text-center table-row-group table-auto border-collapse py-3"
        >
          <tr class="mt-2">
            <td>1</td>
            <td>Trần Long Thành</td>
            <td>0339022885</td>
            <!-- <td>Kiutjvj@gmail.com</td> -->
            <td>APOLO SR5301</td>
            <td>57.500.000</td>
            <td>Đang Xử Lý</td>
            <td>Giao hàng vào buổi chiều</td>
            <td>
              <button
                class="shadow bg-yellow-500 hover:bg-yellow-400 focus:shadow-outline focus:outline-none text-white font-bold mx-5 py-2 px-4 rounded"
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
          <tr>
            <td class="pt-5"></td>
            <td></td>
            <td></td>
            <td></td>
          </tr>
          <tr>
            <td>2</td>
            <td>Nguyễn Văn Long</td>
            <td>0969338865</td>
            <!-- <td>Kiutjvj@gmail.com</td> -->
            <td>Piano Behning DX-1</td>
            <td>48.500.000</td>
            <td>Đang Xử Lý</td>
            <td>Giao hàng ban đêm</td>
            <td>
              <button
                class="shadow bg-yellow-500 hover:bg-yellow-400 focus:shadow-outline focus:outline-none text-white font-bold mx-5 py-2 px-4 rounded"
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
export default {};
</script>
