# Công cụ tính vay (Excel → HTML) — B13 & B9

Repo này chuyển logic chính từ file Excel `Cong_cu_tinh_vay` sang một web tính (`index.html`) chạy trực tiếp trên trình duyệt và có thể deploy bằng GitHub Pages.

## Tính năng

- Nhập thông tin khoản vay:
  - **B13**: Ngày trả lần 1 (kỳ đầu tiên) – Date.
  - **B9**: Số tiền vay (VNĐ).
  - **B10**: Số tháng vay.

- Tính toán lịch trả nợ chi tiết bao gồm:
  - Số tiền gốc và lãi cho tỻng kỳ trả.
  - Điều chỉnh lãi suất ưu đãi và lãi suất sau ưu đãi.
  - Tính toán các khoản thanh toán lãi và gốc vào ngày đầu và các ngày sau đó.
  - Làm tròn tiền gốc trả hàng tháng tới nghìn đồng (ngoại trừ kỳ cuối).

- Hiển thị bảng lịch trả nợ trên trang web.

## Triển khai

Chỉ cần mở file `index.html` trong trình duyệt để sử dụng công cụ tính vay. Bạn có thể deploy repo này bằng GitHub Pages để truy cập trực tuyến.
