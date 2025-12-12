# Công cụ tính vay (Excel → HTML)

Repo này chuyển đổi hoàn toàn logic tính toán từ file Excel `Cong_cu_tinh_vay_full_mau_thu_phi_thu_gui_khach.xlsx` sang một ứng dụng web (`index.html`) chạy trực tiếp trên trình duyệt. Công cụ này giúp người dùng nhập các thông số vay, tính toán lịch trả nợ và xem kết quả ngay trên web.

## Tính năng chính

- **Nhập thông tin khoản vay**:
  - **B13 – Ngày trả lần 1:** chọn ngày bắt đầu trả (kỳ đầu tiên).
  - **B9 – Số tiền vay (VNĐ):** số tiền gốc vay.
  - **B10 – Kỳ hạn vay:** số tháng vay.
  - **Lãi suất ưu đãi:** người dùng có thể nhập lãi suất ưu đãi theo năm.
  - **Lãi suất sau ưu đãi:** lãi suất áp dụng sau thời gian ưu đãi.

- **Tính toán lịch trả nợ**:
  - Xác định số tiền gốc phải trả mỗi kỳ, làm tròn đến hàng nghìn đồng, ngoại trừ kỳ cuối.
  - Tính toán số tiền lãi phải trả theo lãi suất ưu đãi và lãi suất sau ưu đãi.
  - Hiển thị bảng chi tiết từng kỳ trả nợ: số kỳ, ngày trả, gốc, lãi, tổng tiền phải trả và dư nợ còn lại.
  - Cho phép điều chỉnh kỳ đóng lãi linh hoạt (ví dụ: kỳ đầu tiên là ngày 25/12/2025).

- **Tính phí trả nợ trước hạn** (sheet bổ sung):
  - Nhập ngày vay và ngày trả nợ dự kiến.
  - Tính dư nợ tại ngày trả nợ dự kiến dựa trên lịch trả nợ.
  - Áp dụng tỷ lệ phí theo quy định:
    - <= 24 tháng: **2,0%**
    - > 24 tháng và <= 36 tháng: **1,5%**
    - > 36 tháng và <= 60 tháng: **1,0%**
    - > 60 tháng: không thu phí
  - Tính số tiền phí = Dư nợ tại ngày trả nợ dự kiến × Tỷ lệ phí.
  - Sinh bảng gửi thông tin tính phí cho khách hàng.

- **Triển khai dễ dàng**:
  - Chỉ cần mở `index.html` để sử dụng công cụ trên trình duyệt.
  - Có thể deploy công cụ này lên GitHub Pages để sử dụng trực tuyến hoặc chia sẻ nội bộ.

## Cách sử dụng

1. Mở file `index.html` trong trình duyệt (hoặc truy cập trang GitHub Pages sau khi deploy).
2. Nhập các thông tin:
   - Số tiền vay (B9)
   - Kỳ hạn vay (B10 – số tháng)
   - Lãi suất ưu đãi và lãi suất sau ưu đãi (nếu có)
   - Ngày trả lần 1 (B13)
3. Nhấn **Tính toán** để xem lịch trả nợ và tổng kết khoản vay.
4. (Tùy chọn) Tính phí trả nợ trước hạn bằng cách nhập ngày vay và ngày trả dự kiến trong sheet tính phí.

## Phát triển thêm

- Bổ sung khả năng xuất lịch trả nợ ra file PDF hoặc Excel.
- Tích hợp thêm biểu đồ trực quan hóa dòng tiền trả nợ.
- Cho phép nhập nhiều khoản vay khác nhau và so sánh phương án trả nợ.
- Thêm tùy chọn lãi suất thả nổi theo thị trường.

## Đóng góp

Nếu bạn muốn đóng góp cải tiến hoặc phát hiện lỗi, hãy mở issue hoặc gửi pull request cho repo này.

---

Công cụ này được thiết kế để hỗ trợ người vay và nhân viên ngân hàng tính toán khoản vay nhanh chóng, minh bạch và chính xác. Hy vọng sẽ giúp ích cho công việc và học tập của bạn!
