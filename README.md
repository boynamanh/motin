# Website Motin

Trang giới thiệu một trang của **CÔNG TY TNHH CÔNG NGHỆ VÀ TRUYỀN THÔNG MOTIN** (MST 0111623521).
HTML + CSS thuần, không JavaScript, không cần build — đẩy thẳng lên GitHub Pages là chạy.

## Cấu trúc

```
index.html          Trang tiếng Anh (mặc định)
vi/index.html       Trang tiếng Việt
assets/style.css    Giao diện dùng chung — màu, cỡ chữ, khoảng cách khai báo ở đầu file
assets/favicon.svg  Biểu tượng trên tab trình duyệt
.nojekyll           Báo GitHub Pages phục vụ file nguyên trạng
```

Nút **VI / EN** trên thanh đầu trang chuyển qua lại giữa hai ngôn ngữ.

## Xem thử trên máy

Mở `index.html` bằng trình duyệt, hoặc chạy server tĩnh rồi vào http://localhost:8000:

```bash
python3 -m http.server 8000
```

## Đưa lên GitHub Pages

1. Tạo repository mới trên GitHub (ví dụ `motin-web`), chế độ **Public**.
2. Trong thư mục này, chạy:

   ```bash
   git init
   git add .
   git commit -m "Website Motin"
   git branch -M main
   git remote add origin https://github.com/<tai-khoan>/motin-web.git
   git push -u origin main
   ```

3. Trên GitHub: **Settings → Pages → Build and deployment** — Source: *Deploy from a branch*, Branch: `main`, thư mục `/ (root)` → **Save**.
4. Sau 1–2 phút web chạy tại `https://<tai-khoan>.github.io/motin-web/` (bản tiếng Việt ở `.../motin-web/vi/`).

**Tên miền riêng (tuỳ chọn):** vào Settings → Pages → Custom domain, nhập tên miền (ví dụ `motin.vn`), rồi tạo bản ghi DNS theo hướng dẫn của GitHub.

## Sửa nội dung

Nội dung nằm trực tiếp trong hai file HTML — sửa câu chữ thì nhớ sửa **cả hai ngôn ngữ**.

| Muốn đổi | Tìm trong `index.html` và `vi/index.html` |
|---|---|
| Số điện thoại | `0334005508`, `334 005 508` |
| Email | `adat.technology@gmail.com` |
| Địa chỉ | `Duy Tan` / `Duy Tân` |
| Màu, cỡ chữ, khoảng cách | khối `:root` đầu file `assets/style.css` |

Thông tin doanh nghiệp (tên, MST, ngày đăng ký, nơi cấp, trụ sở, ngành nghề) lấy từ Giấy chứng nhận đăng ký doanh nghiệp đăng ký lần đầu ngày 07/09/2026.
