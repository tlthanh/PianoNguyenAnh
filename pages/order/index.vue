<template>
  <div>
    <div class="fixed w-full">
      <NuxtNavbar />
    </div>

    <div class="w-11/12 mx-auto bg-gray-50 pt-23">
      <div class="flex justify-bettwen w-full my-10">
        <!-- info Cus -->
        <div class="container w-3/5 mx-5">
          <h1 class="w-full">đây là khu vực điền thông tin khách hàng</h1>
          <form action="">
            <h1>THÔNG TIN THANH TOÁN</h1>
            <table class="w-full border-solid-2 border-red-500">
              <tr>
                <th>Họ tên</th>
                <td>
                  <input class="w-full" type="text" placeholder="xin chào" />
                </td>
              </tr>
              <tr>
                <th>Số điện thoại</th>
                <td><input type="text" placeholder="xin chào" /></td>
              </tr>
              <tr>
                <th>Email</th>
                <td><input type="text" placeholder="xin chào" /></td>
              </tr>
              <tr>
                <th>Tỉnh/Thành phố</th>
                <td><input type="text" placeholder="xin chào" /></td>
              </tr>
              <tr>
                <th>Quận/Huyện</th>
                <td><input type="text" placeholder="xin chào" /></td>
              </tr>
              <tr>
                <th>Xã/Phường</th>
                <td><input type="text" placeholder="xin chào" /></td>
              </tr>
              <tr>
                <th>Địa chỉ cụ thể</th>
                <td><input type="text" placeholder="xin chào" /></td>
              </tr>
              <tr>
                <th>Ghi chú</th>
                <td><input type="text" placeholder="xin chào" /></td>
              </tr>
            </table>
          </form>
        </div>
        <!-- info order -->
        <div class="w-2/5 mx-5">
          <h1>đây là khu hiển thị thông tin đơn hàng</h1>
        </div>
      </div>
    </div>
    <div class="bottom-0">
      <NuxtFooter />
    </div>
  </div>
</template>
