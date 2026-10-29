# Asahi VietLife – AI Ops (hệ thống nhân sự AI)

Bộ "nhân viên AI" vận hành **Asahi VietLife LLC** (du lịch inbound, Adachi, Tokyo) và **Yume Spa** (Takenotsuka, khai trương 12/2026),
chạy trên các gói đã trả tiền (Claude + ChatGPT) và một Google Sheet chung. **Không dựng hạ tầng mới, không server, 0 đồng phần mềm.**

Nguyên tắc (chốt sau đối chất Claude ↔ ChatGPT ngày 29/10/2026, xem `docs/decisions-2026-10-29.md`):
1. AI chỉ **nghiên cứu, soạn nháp, nhắc việc, tóm tắt**. Mọi thứ ra ngoài (bài đăng, email, tin LINE, báo giá, lịch hẹn) **người duyệt**.
2. AI **không báo giá tour** ngoài App báo giá hiện có; **không nhận dữ liệu khách** (hộ chiếu, lịch sử da) trên công cụ free-tier.
3. Mọi chữ về spa đi qua `legal/forbidden-words.md` trước khi đăng.
4. Đo thành công bằng **giờ chủ tiết kiệm được / tuần**, không đếm số agent.

## Sơ đồ 9 vai trò
| # | Vai trò | Chạy trên | Lịch | File |
|---|---|---|---|---|
| 1 | Trợ lý điều hành (brief sáng) | Claude scheduled task | 07:30 T2–T7 | `agents/01-executive-assistant.md` |
| 2 | Pháp lý & khai trương spa | Claude | tuần 1, rồi T2 hàng tuần | `agents/02-spa-legal-opening.md` |
| 3 | Nội dung spa JP/VI/EN | Claude / ChatGPT | T2 hàng tuần | `agents/03-spa-content.md` |
| 4 | Đặt lịch spa (người + LINE + Calendar) | người | theo khách | `agents/04-spa-booking-sop.md` |
| 5 | Hiện diện & đối tác du lịch | Claude | T4 hàng tuần | `agents/05-travel-presence-partners.md` |
| 6 | Điều phối yêu cầu tour | Claude theo yêu cầu | khi có inquiry | `agents/06-travel-inquiry-coordinator.md` |
| 7 | Fanpage du lịch | ChatGPT task đã có | hàng tuần | `agents/07-travel-fanpage-chatgpt.md` |
| 8 | Kịch bản & caption media | Claude / ChatGPT | trước buổi quay | `agents/08-media-script-caption.md` |
| 9 | Quay – dựng – đăng (người) | điện thoại + CapCut + Canva | 1 buổi/tuần | `agents/09-media-production-sop.md` |

## Thư mục
- `agents/` – prompt + đầu vào/đầu ra + điều kiện dừng của từng vai trò. Dán nguyên prompt vào Claude/ChatGPT.
- `legal/` – từ cấm (薬機法・景表法・あん摩法), checklist giấy phép spa, ghi chú 旅行業法.
- `sheets/` – cấu trúc Google Sheet chung (6 tab) + CSV mẫu + `asahi-ai-ops-sheet.xlsx` (mở bằng WPS).
- `schedules/` – lịch chạy và cách tạo scheduled task trong Claude.
- `docs/` – quyết định, biên bản đối chất với ChatGPT, lộ trình 5 tuần.

## Cách dùng trong 1 ngày
1. 07:30 Claude gửi brief (vai trò 1) → bạn đọc 5 phút, trả lời "OK / sửa" ngay trong Claude.
2. Nhân viên cập nhật Sheet (TASKS, BOOKINGS, CONTENT) trong ngày.
3. Tối: nếu có bài/email cần duyệt, bạn duyệt trên điện thoại (15 phút).

Website Yume Spa: repo riêng `yume-spa-website`.
