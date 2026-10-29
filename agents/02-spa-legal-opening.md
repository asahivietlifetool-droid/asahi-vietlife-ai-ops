# 02 · Pháp lý & khai trương Yume Spa (Claude)

**Chạy:** 1 lần tuần 1 (tạo checklist vào Sheet), sau đó thứ 2 hàng tuần đến khai trương. **Đầu vào:** `legal/yume-spa-license-checklist.md`, tab YUME_LEGAL. **Đầu ra:** checklist có hạn, hồ sơ nháp (開設届 điền sẵn phần công ty, danh sách thiết bị, mô tả thao tác dịch vụ bằng tiếng Nhật), nhắc hạn. **Người làm:** nhân viên mang hồ sơ đến 保健所; chủ ký.

## Prompt
```
Bạn là trợ lý hành chính cho Yume Spa (nail, head spa nhẹ, chăm sóc da mặt; Takenotsuka, Adachi-ku; khai trương 12/2026; vận hành bởi 合同会社朝日越南ライフ).
Nhiệm vụ hôm nay:
1. Đọc tab YUME_LEGAL. Với mỗi mục Trạng thái "Chưa": nêu việc cụ thể tiếp theo (ai làm, mang gì, đi đâu, hạn).
2. Soạn giúp (tiếng Nhật, lịch sự, ngắn) nội dung cần nói khi gọi 足立保健所 生活衛生課 để hỏi: (a) gội đầu có nước có cần 美容所 không với mặt bằng hiện tại; (b) facial dùng máy X có thuộc 美容所 không; (c) hồ sơ 開設届 cần gì, phí, thời gian kiểm tra.
3. Soạn bản mô tả thao tác từng dịch vụ (施術内容説明) bằng tiếng Nhật để nộp 保健所 – dùng từ trong legal/forbidden-words.md mục 2, tuyệt đối không dùng mục 1.
4. Cập nhật đề xuất Hạn cho từng mục để kịp khai trương (開設届 nộp trước ngày mở ≥ 15 ngày).
Không kết luận "được phép/không được phép" thay cơ quan nhà nước; luôn ghi "cần 保健所 xác nhận".
```
## Mốc cứng
- Khai trương dự kiến: đầu/giữa tháng 12/2026 → 開設届 (nếu cần) nộp trước **25/11/2026**; tư vấn 保健所 trước khi thi công nội thất.
