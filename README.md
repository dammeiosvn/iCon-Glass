# iCon Glass

Webclip độc lập để vẽ icon kính trên iPhone, xuất PNG, đóng bộ, hoặc cài thẳng bằng hồ sơ `.mobileconfig`.

Sáng tối theo hệ thống. Nút viên thuốc kính. Xem trước nằm góc trái. Bố cục tự chia theo điện thoại, máy tính bảng và màn hình lớn.

[**Dùng ngay:**](https://dammeiosvn.github.io/iCon-Glass/)

## Làm được gì

- Hình kính có khối: hoa, thư, thư mục, danh sách, bánh răng, chữ G
- Chữ hoặc emoji riêng, tải PNG/SVG thành lớp
- Độ đục, viền sáng, óng ánh, bo góc, cỡ hình
- Ba kiểu bóng: tiếp xúc, mềm, nổi
- Tấm nền kem hoặc nền trong
- Xuất 180 và 1024, gói ZIP kèm đoạn `apple-touch-icon`
- Lưu mẫu trên máy
- Tải hồ sơ webclip: toàn màn hình, icon gắn sẵn, gỡ được

## Cài lên màn hình chính

Safari → mở site → Chia sẻ → Thêm vào Màn hình chính.

Hoặc trong app, mục Xuất: dán URL site, bấm Hồ sơ, cài file `.mobileconfig`. iOS sẽ hỏi xác nhận vì hồ sơ chưa ký.

## Bật GitHub Pages

Repo này đã để file ở gốc, có `.nojekyll`.

1. Settings → Pages
2. Build and deployment → Deploy from a branch
3. Branch `main`, folder `/ (root)`
4. Save

Site: `https://dammeiosvn.github.io/iCon-Glass/`

## Cấu trúc

```
index.html              app
manifest.webmanifest    PWA, standalone
sw.js                   cache offline cho webclip
apple-touch-icon.png    icon 180
icons/                  192 và 512
.nojekyll               Pages không qua Jekyll
```

Trang khai báo `apple-mobile-web-app-capable`, `apple-touch-icon`, `theme-color` theo sáng tối, và `display: standalone`.

## PNG xuất ra dùng ở đâu

- Webclip khác: gắn file 180 vào `apple-touch-icon`
- App đổi icon: dùng file 1024
- Hồ sơ: app nhúng icon 180 vào payload `com.apple.webClip.managed`

iOS vẫn bo squircle lên ảnh. Bóng, viền và kính nằm sẵn trong PNG.
