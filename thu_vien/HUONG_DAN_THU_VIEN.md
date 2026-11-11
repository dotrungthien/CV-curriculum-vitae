HƯỚNG DẪN THƯ VIỆN (bản 11/11/2026 15:40; tách từ xương sống 7.3–7.4 bản 11/11 15:20, giữ nguyên nội dung)
Đặt ở `thu_vien/HUONG_DAN_THU_VIEN.md` trong mọi kho dự án; đổi thì chép sang mọi kho cùng ngày.

1. Đất dự án = THƯ VIỆN TRONG KHO
- `CLAUDE.md` ở gốc kho: agent tự đọc mỗi lần mở; ghi chỉ dẫn của cành, cấu trúc kho, đọc gì trước.
- Thư mục `thu_vien/`:
  - Bản sao xương sống (dòng đầu ghi bản).
  - TRẠNG THÁI: < 50 KB, thay cả tệp, khối "Cập nhật" đầu tệp, thêm một bỏ một, có mục 6.4 ("Chưa thử trên đồ thật").
  - LỊCH SỬ đánh số: chỉ tạo mới, không sửa cũ; một lịch sử = một đầu việc = một chat; có 2 dòng 6.5 và "Học sau" chưa mở.
  - Thiết kế, sơ đồ phối hợp.
- Dữ liệu đồ thật (hộp đen, log) trong kho cạnh mã.
- Project trên claude.ai chỉ giữ một tệp chỉ đường tới kho.
- Kho có chuyện riêng thì để riêng tư (Private); không để bí mật trong kho (mật khẩu, token, mã, số tài khoản).
- Xương sống đổi thì chép bản đầy đủ sang mọi kho cùng ngày.
- Đầu chat: gắn kho, đọc trọn trạng thái và lịch sử mới nhất; tệp bị cắt thì dừng, không ghi đè.
- Trước khi đổi quyết định đã chốt, đọc lịch sử nơi chốt nó.

2. Ghi tệp ("ghi giai đoạn N", "cập nhật trạng thái")
soạn .md → gửi đính kèm cho Thiên xem → ghi vào `thu_vien/` bằng commit (agent làm, hoặc chat nếu có quyền ghi kho) → Thiên push → đọc lại bản trong kho, so dòng đầu, chỗ đổi, dòng cuối → báo ≤ 6 dòng. Nội dung dài luôn gửi bằng tệp.
