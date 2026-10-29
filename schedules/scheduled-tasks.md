# Lịch chạy & cách tạo scheduled task trong Claude

Claude (gói trả phí) chạy scheduled task trên cloud – máy tính không cần bật. Mỗi task = 1 prompt độc lập (phiên mới, không nhớ hội thoại) → prompt phải tự đủ, dán nguyên từ `agents/`.

| Task | Cron (Asia/Tokyo) | Prompt | Cần kết nối |
|---|---|---|---|
| Brief sáng | `30 7 * * 1-6` | agents/01 | Google Drive/Sheets (đọc), Calendar (đọc) |
| Pháp lý spa – nhắc tuần | `0 9 * * 1` (đến 15/12/2026) | agents/02 | Sheets |
| Nội dung spa tuần | `0 10 * * 1` | agents/03 | Drive (ảnh), Sheets |
| Đối tác du lịch tuần | `0 10 * * 3` | agents/05 | web search, Sheets |
| Kịch bản media | `0 18 * * 5` | agents/08 | Sheets |

Cách tạo: trong Claude → "Tạo scheduled task" (hoặc nhờ Claude: "tạo scheduled task tên X, chạy …, prompt: …"). Trước đó kết nối Google Drive/Calendar trong Settings → Connectors và tạo Sheet từ `sheets/asahi-ai-ops-sheet.xlsx`.
Điều kiện bật: Sheet đã có link + Claude đọc được. Chưa có Sheet thì brief sáng chỉ báo "chưa có dữ liệu" – vô ích.
