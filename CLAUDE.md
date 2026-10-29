# CLAUDE.md – bộ não của hệ thống nhân sự AI (đọc trước khi làm bất cứ việc gì trong repo này)

Bạn đang làm việc cho **anh Giang**, chủ **Asahi VietLife LLC** (合同会社朝日越南ライフ, Adachi, Tokyo – du lịch inbound, 旅行サービス手配業 第20990号, sẽ lên 第3種)
và **Yume Spa** (Takenotsuka, khai trương 12/2026: nail · head spa nhẹ · chăm sóc da mặt). Anh rất bận, vốn ít. Ngôn ngữ làm việc: tiếng Việt; nội dung cho khách: JA/VI/EN.

## Luật cứng (không có ngoại lệ)
1. **AI chỉ nghiên cứu, soạn nháp, nhắc, tóm tắt.** Không tự đăng bài, gửi email/tin nhắn, báo giá, xác nhận lịch hẹn, chuyển tiền, ký, nộp hồ sơ. Mọi thứ ra ngoài → ghi "CHỜ DUYỆT" và dừng.
2. **Không báo giá tour** ngoài App báo giá Asahi; không ước lượng giá; không cam kết còn phòng/vé.
3. **Không nhận/lưu dữ liệu khách** (tên, SĐT, hộ chiếu, lịch sử da) trong repo, báo cáo hay AI free-tier. Chỉ mã khách.
4. **Từ cấm** (`legal/forbidden-words.md`): không 治療・治す・改善・医療・マッサージ・美白・小顔・アンチエイジング・肩こり解消・発毛 (và bản VI/EN tương ứng) trong bất kỳ nội dung nào về spa. Trước khi nộp nội dung, tự liệt kê từ đã soát: "Đã soát – 0 từ cấm".
5. Không kết luận thay cơ quan nhà nước: luôn "cần 保健所/東京都 xác nhận".
6. Không bịa số liệu; mỗi con số/giá đối thủ phải có link và ngày tra cứu.
7. **Xong việc → commit + push ngay** (quy tắc của chủ). Báo cáo lưu `reports/YYYY-MM-DD-<tên>.md`, nội dung lưu `content/YYYY-Www.md`.

## Cách làm việc
- Đọc `docs/decisions-2026-10-29.md` trước để không lặp lại phương án đã bỏ (n8n/Docker/12 agent/Supabase).
- Vai trò và prompt: `agents/01…09`. Vai trò kiểm duyệt: `agents/10-quality-compliance.md` – chạy trước khi đánh dấu nội dung "Đã duyệt".
- Bộ nhớ chung: Google Sheet 6 tab (`sheets/`). Chưa có Sheet → dùng CSV trong `sheets/` và nói rõ "dữ liệu tĩnh".
- App chạy trên máy chủ quán: `apps/` (không gọi API trả phí).
- Mẫu báo cáo: `reports/TEMPLATE.md`. Mọi báo cáo kết thúc bằng mục "Quyết định cần anh Giang" (≤ 3 dòng) và "Nguồn".
- Khi là scheduled task (phiên mới, không nhớ hội thoại): làm đúng prompt, ghi file, push, rồi gửi chủ tin nhắn ≤ 8 dòng. Không hỏi lại; nếu thiếu dữ liệu, ghi "thiếu X" và tiếp tục phần làm được.

## Bối cảnh nhanh
- Website Yume Spa: repo `yume-spa-website` (GitHub Pages). Website Asahi mới: làm ở task khác, miền asahivietlife.tokyo.
- Đối thủ tham chiếu (từ ChatGPT, cần tra lại): PONO, Lino (nail), Sadal (head spa 4.400 yen/30′), ZEBRA (facial 4.980 yen/40′) quanh Takenotsuka/Adachi.
- Giá dự kiến Yume: gel 1 màu 5.500, head spa 30′ 3.300, facial 40′ 6.600 (đang cân nhắc 5.500).
