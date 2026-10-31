# GegeTeam — Blox Fruits Rate Website

Trang báo giá thu mua item Blox Fruits của GegeTeam (Nhà Cáo): 46 item (trái gốc, đột biến, skin limited/chromatic, item limited khác). Người chơi chọn item và số lượng, trang tính tổng tiền bằng VND và USDT rồi sao chép phiếu để gửi qua Zalo.

Mở `index.html` để xem trang.

## Sửa giá

Mọi dữ liệu nằm đầu thẻ `<script>` trong `index.html`, sau này nạp từ database thì thay các giá trị này:

- `ITEMS[].rate`: số trong bảng giá của team, `null` nếu chưa có giá.
- `VND_PER_RATE`: 1 rate bằng bao nhiêu VND.
- `VND_PER_USDT`: 1 USDT bằng bao nhiêu VND.

## Ngôn ngữ

Trang có tiếng Việt và tiếng Anh. Tiếng Việt hiện giá VND kèm USDT, tiếng Anh chỉ hiện USDT. Tiếng Việt nằm trong HTML, tiếng Anh nằm trong `EN_HTML`, `TEXT`, `CATEGORIES[].en` và `ITEMS[].noteEn`.

## Tài khoản

Đăng nhập không bắt buộc. Chưa có backend nên tài khoản chỉ lưu trong localStorage của từng trình duyệt (mật khẩu băm PBKDF2), khi có database thì đổi object `AUTH` sang gọi API.
