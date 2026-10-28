# 🎄 Merry Christmas – Christmas Tree Animation

Trang web tương tác chào đón Giáng sinh với cây thông lấp lánh, tuyết rơi, ông già Noel bay ngang bầu trời, quà rơi có thể bấm để nhận lời chúc, pháo hoa và nhạc nền. Dự án được xây dựng hoàn toàn bằng **HTML, CSS và JavaScript thuần** (không dùng framework), chỉ dùng [Parcel](https://parceljs.org/) để chạy dev server và build.

## ✨ Tính năng

- 🎄 **Cây thông tương tác** – bấm vào cây để cây rung lên và chuông reo
- 💡 **Đèn nhấp nháy, quả châu và chuông** trang trí ngẫu nhiên trên cây
- ⭐ **Ngôi sao lấp lánh** trên nền trời đêm
- ❄️ **Tuyết rơi** với kích thước, tốc độ và độ mờ ngẫu nhiên
- ☁️ **Mây trôi** chuyển động liên tục
- 🎅 **Ông già Noel bay** ngang màn hình
- 🎁 **Quà rơi từ trên xuống** – bấm vào hộp quà để hiện lời chúc ngẫu nhiên
- 🎆 **Pháo hoa** nổ ra tại vị trí bạn bấm chuột
- ✨ **Hạt sáng theo con trỏ chuột**
- ⏳ **Đồng hồ đếm ngược** đến ngày 25/12 (ngày, giờ, phút, giây)
- 🎵 **Nhạc nền** có nút bật/tắt (🔊 / 🔈)

## 🛠️ Công nghệ sử dụng

| Thành phần | Chi tiết |
| --- | --- |
| Giao diện | HTML5, CSS3 (keyframes animation) |
| Logic | JavaScript (ES Modules) |
| Font | [Mountains of Christmas](https://fonts.google.com/specimen/Mountains+of+Christmas) (Google Fonts) |
| Công cụ build | Parcel `^2.13.2` |

## 📁 Cấu trúc thư mục

```
Merry-Christmas/
├── index.html        # Cấu trúc trang
├── style.css         # Toàn bộ style và animation
├── script.js         # Logic hiệu ứng và tương tác
├── final.mp3         # Nhạc nền
├── favicon.ico       # Biểu tượng tab trình duyệt
├── package.json      # Scripts và dependencies
└── README.md
```

## 🚀 Cài đặt và chạy

### Yêu cầu

- [Node.js](https://nodejs.org/) (khuyến nghị bản LTS)
- Kết nối Internet (hình cây thông, mây, ông già Noel và font được tải từ CDN)

### Các bước

```bash
# 1. Clone dự án
git clone https://github.com/TranHoc123/Merry-Christmas.git
cd Merry-Christmas

# 2. Cài đặt dependencies
npm install

# 3. Chạy môi trường phát triển
npm start
```

Mở trình duyệt tại địa chỉ Parcel hiển thị trong terminal (mặc định `http://localhost:1234`).

### Build bản production

```bash
npm run build
```

File sau khi build nằm trong thư mục `dist/`.

> 💡 `script.js` được nạp dưới dạng `type="module"`, vì vậy hãy chạy qua `npm start` (hoặc một server cục bộ như Live Server) thay vì mở trực tiếp file `index.html` bằng đường dẫn `file://`.

## 🎮 Cách sử dụng

1. Mở trang web và bấm nút **🔊** ở góc màn hình để bật nhạc (trình duyệt thường chặn tự phát âm thanh cho đến khi người dùng tương tác).
2. **Bấm vào cây thông** để xem cây rung và chuông reo.
3. **Bấm vào các hộp quà** đang rơi để nhận lời chúc Giáng sinh ngẫu nhiên.
4. **Bấm bất kỳ đâu** trên màn hình để bắn pháo hoa, **di chuột** để tạo hạt sáng.
5. Theo dõi đồng hồ đếm ngược đến Giáng sinh ở cuối trang.

## 🎨 Tùy chỉnh

| Muốn thay đổi | Chỉnh ở đâu |
| --- | --- |
| Nhạc nền | Thay file `final.mp3` (hoặc sửa `src` trong thẻ `<audio>` ở `index.html`) |
| Lời chúc khi mở quà | Mảng `messages` trong hàm `createGift()` – `script.js` |
| Tần suất tuyết rơi | `setInterval(createSnow, 200)` – `script.js` |
| Tần suất quà rơi | `setInterval(createGift, 1000)` – `script.js` |
| Số lượng ngôi sao | Biến `numberOfStars` trong hàm `createStars()` |
| Màu pháo hoa | Mảng `colors` trong hàm `createFirework()` |
| Ngày đếm ngược | Hàm `updateCountdown()` (mặc định là 25/12 của năm hiện tại) |

## 📝 Ghi chú

- Hình ảnh cây thông, mây và ông già Noel được tải từ Firebase Storage; nếu mất mạng hoặc đường dẫn hết hiệu lực, các hình này sẽ không hiển thị.
- Hiệu ứng âm thanh khi mở quà tham chiếu tới file `unwrap.mp3`. Hãy thêm file này vào thư mục gốc nếu muốn có tiếng mở quà.

## 👤 Tác giả

**TranHoc123** – [GitHub](https://github.com/TranHoc123)

---

🎅 *Chúc bạn một mùa Giáng sinh an lành và ấm áp!*