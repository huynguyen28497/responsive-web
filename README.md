<p align="center">
  <a href="" rel="noopener">
 <img width=200px height=200px src="https://i.imgur.com/OXKLK5y.png" alt="Project logo" /></a>
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
<img width=200px height=200px src="https://i.imgur.com/Dj1TFtf.png" alt="Project logo" />

Cột và hàng
- Để chia grid thành các cột và các hàng, chúng ta sẽ sử dụng 2 thuộc tính grid-template-columns và grid-template-rows.
```
.wrapper {
  grid-template-columns: <track-size>...;
  grid-template-rows: <track-size>...;
}
```
Trong đó:
```
Số giá trị trong thuộc tính grid-template-columns sẽ tương ứng với số cột, các giá trị sẽ tương ứng với chiều rộng của các cột lần lượt từ trái sang phải.
Số giá trị trong thuộc tính grid-template-rows sẽ tương ứng số hàng, các giá trị sẽ tương ứng với chiều cao của các hàng lần lượt từ trên xuống dưới.
```
VD: Để tạo một grid kích thước 3x2, bạn có thể viết như sau:
```
.wrapper {
    display: grid;
    grid-template-columns: 200px 200px 200px;
    grid-template-rows: 100px 100px;
}
```
```
Trong đoạn code trên, chúng ta đưa cho thuộc tính grid-template-columns 3 giá trị, như vậy, grid của chúng ta sẽ có 3 cột, mỗi cột đều có chiều rộng là 200px. Tương tự, thuộc tính grid-template-rows có 2 giá trị, tương ứng với 2 hàng, mỗi hàng có chiều cao là 100px.
```
<img width=200px height=200px src="https://i.imgur.com/Bgv6U15.png" alt="Project logo" />
Grid gaps
- Khoảng cách giữa các cột trong grid được gọi là column-gap, còn khoảng cách giữa các hàng trong grid được gọi là row-gap. Để thay đổi khoảng cách giữa các cột và các hàng, chúng ta sẽ sử dụng grid-column-gap và grid-row-gap.

```
.wrapper {
  grid-column-gap: <line-size>;
  grid-row-gap: <line-size>;
}
```
Trong đó: 
```
<line-size> là một giá trị chiều dài

```
Để viết ngắn gọn hơn, ta dùng grid-gap. Giá trị thứ nhất sẽ tương ứng với grid-column-gap, còn giá trị thứ hai sẽ tương ứng với grid-row-gap.
VD: 
```
.wrapper {
    display: grid;
    grid-gap: 50px 25px;
}
```
<img width=200px height=200px src="https://i.imgur.com/F74FKWM.png" alt="Project logo" />
Sắp xếp các item trong grid

- Với mỗi item, để thay đổi kích thước cũng như vị trí, chúng ta sẽ thay đổi thuộc tính grid-column và grid-row.
```
.item1 {
    grid-column-start: 1;
    grid-column-end: 4;
}
```
Với code trên thì item bắt đầu ở cột 1 và kết thúc ở cột 4 
<img width=200px height=200px src="https://i.imgur.com/tcs9Hpo.png" alt="Project logo" />
Viết ngắn gọn
```
.item1 {
    grid-column: 1 / 4;
}
```

### Flex  <a name = "Flex"></a>

Flexbox là khi chúng ta căn theo 2 trục x y
Sử dụng
```
display: flex;
```
Hướng của trục chính được xác định bởi thuộc tính flex-direction có thể có bốn giá trị:
```
flex-direction: row; – trục chính chạy từ trái sang phải (mặc định)
flex-direction: row-reverse; – trục chính chạy từ phải sang trái
flex-direction: column; – trục chính chạy từ trên xuống dưới
flex-direction: column-reverse; – trục chính chạy từ dưới lên trên
```
Left to Right: row
- Hướng flex mặc định là row; nếu bạn không thiết lập gì khác thì đây sẽ là giá trị được sử dụng. Như bạn có thể thấy bên dưới, tôi chỉ thêm các thuộc tính liên quan đến flexbox vào thùng chứa flex. Các phần tử flex đã áp dụng một số thuộc  tính với mục đích trang trí:
Right to Left: column
Một trò chơi để học full flex

```
https://flexboxfroggy.com/#vi
```


## 🔧 Media Query <a name = "Media-Query"></a>

Media Query là một trong những module mới được thêm vào trong CSS3. Nó là một sự cải thiện của Media Type đã có từ CSS2, bằng việc thêm vào những cú pháp query để ta có thể đáp ứng được cho nhiều device với nhiều kích cỡ màn hình khác nhau.
Media Type
Tất cả các giá trị của Media Type bao gồm

- All: Dùng cho tất cả các loại Media Type
- Aural: Dùng cho speech and sound synthesizers
- Braille: Dùng cho các devices liên quan đến chữ nổi (braille)
- Embossed: Dùng cho các loại máy in các trang braille
- Handheld: Dùng cho các thiết bị nhỏ, thiết bị cầm tay
- Print: Dùng cho máy in
- Projection: Dùng cho các loại máy chiếu
- Screen: Dùng cho computer screen
- Tty: Dùng cho các thiết bị sử dụng fixed-pitch character grid
- Tv: Dùng cho các loại TV
Ta có thể sử dụng Media Type theo cú pháp sau đây:
```
@media media_type {rules}
```
Một số breakpoint quan trọng khi responsive
<img width=200px height=200px src="https://i.imgur.com/jfIofW3.png" alt="Project logo" />
Mobile First - Desktop First 
Mobile first
- Nói theo nghĩa của nó thì chúng ta sẽ code một giao diện từ thiết bị nhỏ cho tới thiết bị to, từ mobile tới tablet rồi tới laptop và các màn hình lớn như Retina.
Desktop first
- Ngược lại với mobile first thì chúng ta sẽ code các giao diện từ lớn đến bé từ Retina cho tới laptop, rồi tới tablet và cuối cùng là các thiết bị mobile
Tùy vào từng dự án ta sẽ chọn type phù hợp 
VD:
```
@media (max-width: 900px) { body {font-size: 16px;} }
/*Áp dụng cho những browser có chiều rộng >= 600px*/
@media (min-width: 600px) { body {font-size: 14px;} }
/*Áp dụng cho những browser có chiều rộng >= 800px*/
@media (min-width: 800px) { body {font-size: 15px;} }
/*Áp dụng cho những browser có chiều rộng <= 700px*/
@media (max-width: 700px) { body {font-size: 13px;} }
```
Như ở trên trang web mẫu
Khi screen thay đổi, gridview cũng thay đổi số lượng cột hàng tương ứng
```
.grid-container {
  display: grid;
  grid-template-columns: auto auto auto auto;
  padding: 10px;
}
@media screen and (max-width: 768px) {
  .grid-container {
    display: grid;
    grid-template-columns: auto auto;
    margin: 10px;
  }
}
```
Hoặc thay vì flex chia đôi thì một bên sẽ ẩn, một bên sẽ width 100%
```
.content-left {
  background-color: beige;
  margin: 1%;
  margin-right: 0%;
  width: 20%;
}
.content-right {
  padding: 1%;
  width: 80%;
}
@media screen and (max-width: 768px) {
  .content-left {
    display: none;
  }
  .content-right {
    width: 100%;
  }
 }
```

### Tổng kết <a name = "Tổng_Kết"></a>

Trên đây là hng dẫn học responsive cơ bản nhất. Mong mọi người bổ sung và góp ý thêm


## ✍️ Authors <a name = "authors"></a>

DU21 - NDHUY



