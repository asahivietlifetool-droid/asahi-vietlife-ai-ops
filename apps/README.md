# Apps chạy trên máy (không cài đặt, không tốn tiền)

Mỗi app là **một file HTML**. Tải về máy → nhấp đúp → mở trong Edge/Chrome → dùng được ngay, kể cả không có mạng.
Dữ liệu lưu trong trình duyệt của máy đó (localStorage). Mỗi tuần bấm **Sao lưu JSON** để giữ bản sao.

| App | Dùng cho | Làm được gì |
|---|---|---|
| `yume-ops-desk.html` | Yume Spa – chủ + nhân viên | **Hôm nay**: brief sáng tự tạo từ dữ liệu trong máy (không cần AI) · **Lịch hẹn**: sổ hẹn theo giờ, chống trùng nhân viên, tuần này, in lịch ngày, xuất CSV cho tab BOOKINGS (chỉ mã khách) · **Việc cần làm**: nạp sẵn 12 việc khai trương, báo quá hạn · **Nội dung**: lịch đăng, trạng thái duyệt · **Soát từ cấm**: tô đỏ từ vi phạm 薬機法/あん摩法 (JA/VI/EN) + gợi ý thay · **Trợ lý AI**: chọn vai trò → tạo prompt → dán vào Claude/ChatGPT · **Cài đặt**: dịch vụ/giá, nhân viên, giờ, từ cấm, sao lưu/khôi phục |
| `asahi-inquiry-desk.html` | Asahi VietLife – điều phối tour | Nhập yêu cầu khách/đại lý → phiếu yêu cầu chuẩn (dán vào App báo giá) + nháp thư trả lời VI/EN/JA **không có giá** + danh sách theo dõi, xuất CSV |

## Cách tải về máy
1. Mở file trên GitHub → nút **Raw** → Ctrl+S (lưu dạng "Webpage, HTML only") vào `Documents\YumeSpa\`.
2. Hoặc tải cả repo: nút **Code → Download ZIP**, giải nén, vào thư mục `apps`.
3. Tạo lối tắt ra Desktop. Mở bằng Edge/Chrome (không mở bằng WPS).

## Tại sao là HTML một file, không phải .exe
- Chạy trên Windows/Mac/điện thoại, không cần cài, không bị Windows chặn như .exe lạ, dễ sửa (mở bằng Notepad).
- Không gọi API trả phí: phần "AI" là prompt dán vào Claude/ChatGPT đã trả tiền. Khi có ngân sách, có thể nối API Claude vào nút "Tạo brief" (đã để sẵn chỗ).

## Giới hạn
- Dữ liệu nằm trên **một** máy. Dùng chung nhiều máy → xuất CSV lên Google Sheet (tab cùng tên) hoặc sao lưu JSON qua Drive.
- Không thay thế luật sư/保健所: Soát từ cấm chỉ bắt từ trong danh sách; người vẫn phải đọc lại ý.
