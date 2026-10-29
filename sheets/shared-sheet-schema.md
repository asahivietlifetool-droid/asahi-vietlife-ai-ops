# Google Sheet chung "Asahi AI Ops" – cấu trúc 6 tab

Tạo 1 Google Sheet (hoặc mở `asahi-ai-ops-sheet.xlsx` bằng WPS rồi tải lên Drive → "Lưu dạng Google Sheets"). Chia sẻ cho: chủ (chỉnh sửa), nhân viên (chỉnh sửa), Claude qua connector Google Drive (đọc + ghi tab CEO_REPORT). Hàng 1 = tiêu đề, không đổi tên cột (AI đọc theo tên).

| Tab | Cột | Ai ghi |
|---|---|---|
| TASKS | ID, Việc, Doanh nghiệp (Asahi/Yume/Chung), Người phụ trách, Hạn (yyyy-mm-dd), Trạng thái (Chưa/Đang/Chờ duyệt/Done), Ghi chú | chủ, nhân viên, AI đề xuất |
| YUME_LEGAL | ID, Dịch vụ/Việc, Luật, Yêu cầu, Người xác nhận, Hạn, Trạng thái (Chưa/Đang/Xong), Ghi chú | vai trò 02 tạo, nhân viên cập nhật |
| CONTENT | ID, Ngày đăng dự kiến, Doanh nghiệp, Nền tảng (IG/FB/TikTok/LINE), Chủ đề, Ngôn ngữ, Link file, Trạng thái (Nháp/Chờ duyệt/Đã duyệt/Đã đăng), Kết quả (lượt xem/tin nhắn) | AI tạo, chủ duyệt, nhân viên đăng |
| BOOKINGS | Mã, Ngày, Giờ, Dịch vụ, Thời lượng, Nhân viên, Kênh (LINE/Tel/FB), Trạng thái (Đặt/Đến/Hủy/No-show), Khách quay lại (Y/N) | nhân viên (KHÔNG ghi tên/SĐT khách – chỉ mã) |
| ASAHI_B2B | ID, Công ty, Website, Thị trường, Bán tour Nhật (Y/N + link), Kênh liên hệ công khai, Điểm 0–100, Lý do, Ngày tra cứu, Trạng thái (Mới/Chủ chọn/Đã gửi/Phản hồi/Hợp tác), Ghi chú | vai trò 05 tạo, nhân viên cập nhật |
| CEO_REPORT | Ngày, Spa: lịch hôm nay, Việc quá hạn, Nội dung chờ duyệt, B2B mới, Quyết định đã hỏi, Quyết định của chủ, Giờ chủ tiết kiệm (ước) | vai trò 01 ghi 1 dòng/ngày |

Quy tắc dữ liệu: tên/SĐT/LINE ID của khách chỉ nằm trong Google Calendar và sổ của nhân viên, **không** vào Sheet này (Sheet này AI đọc được).
