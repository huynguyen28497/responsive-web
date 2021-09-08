<p align="center">
  <a href="" rel="noopener">
 <img width=200px height=200px src="https://i.imgur.com/OXKLK5y.png" alt="Project logo"></a>
</p>

<h3 align="center">Responsive Web</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/kylelobo/The-Documentation-Compendium.svg)](https://github.com/huynguyen28497/responsive-web/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/kylelobo/The-Documentation-Compendium.svg)](https://github.com/huynguyen28497/responsive-web/pulls)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

</div>

---

<p align="center"> Hướng dẫn Responsive Website cơ bản
    <br> 
</p>

## 📝 Table of Contents

- [Responsive Web là gì](#about)
- [Viewport](#viewport)
- [Gridview](#gridview)
- [Flex](#Flex)
- [Media-Query](#Media-Query)
- [Tổng kết](#Tổng_Kết)
- [Authors](#authors)

## 🧐 Responsive Web là gì? <a name = "about"></a>

Responsive Web hay còn gọi là Thiết kế Web đáp ứng là cách tiếp cận tập trung vào môi trường của người dùng trang web.
Môi trường của người dùng sẽ phụ thuộc vào thiết bị họ đã kết nối với internet.
Có nhiều đặc điểm môi trường tác động đến việc này bao gồm:
```
 - Kết nối mạng
 - Kích thước màn hình
 - Loại tương tác (Màn hình cảm ứng, track pad)
 - Độ phân giải đồ họa
```
Trước khi web responsive được phổ biến, nhiều công ty có tiền, họ đầu tư làm riêng 1 giao diện cho di động, 1 giao diện cho máy tính để bàn
Nó là 2 bản mã nguồn được lập trình khác nhau, quản lý khác nhau.
Nhưng trong cách responsive web, máy chủ luôn gửi cùng một bộ code HTML đến tất cả các thiết bị và chỉ sử dụng CSS để thay đổi cách hiển thị của trang trên các thiết bị khác nhau.


## 🏁 Viewport <a name = "viewport"></a>

```
Viewport là khung hình người dùng nhìn thấy trên thiết bị của họ khi vào một trang web bất kì. Với mỗi thiết khác nhau lại có viewport khác nhau. Nếu trang web cố định kích thước thì trình duyệt sẽ tự động thu nhỏ nội dung khi chuyển từ màn hình máy tính qua smartphone - điều này tạo nên trải nghiệm không tốt cho người dùng.
```
Chúng ta cần thêm Viewport để responsive website
```
<meta name="viewport" content="width=device-width, initial-scale=1">
```
- Thẻ <meta> viewport thiết lập cho trang web hiển thị tương ứng với kích thước của từng thiết bị khác nhau.
- Thuộc tính width=device-width đặt chiều rộng của trang web theo chiều rộng màn hình của thiết bị.
- Thuộc tính initial-scale=1.0 thiết lập mức độ phóng ban đầu khi trang được trình duyệt tải lần đầu tiên, người dùng sẽ không thể zoom khi thuộc tính này có giá trị bằng 1.

### Gridview <a name = "gridview"></a>

Một grid sẽ bao gồm hai thành phần chính: wrapper đóng vai trò grid container, và các item con là thành phần của grid.

```
<div class="wrapper">
  <div class="item item1">1</div>
  <div class="item item2">2</div>
  <div class="item item3">3</div>
  <div class="item item4">4</div>
  <div class="item item5">5</div>
  <div class="item item6">6</div>
</div>
```
Để chuyển wrapper thành grid, chúng ta chỉ cần thay đổi thuộc tính display:
```
.wrapper {
  display: grid; /* hoặc inline-grid | subgrid */
}
```

### Flex  <a name = "Flex"></a>

A step by step series of examples that tell you how to get a development env running.

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo.

## 🔧 Media Query <a name = "Media-Query"></a>

Explain how to run the automated tests for this system.

### Tổng kết <a name = "Tổng_Kết"></a>

Explain what these tests test and why

```
Give an example
```



## ✍️ Authors <a name = "authors"></a>

DU21 - NDHUY



