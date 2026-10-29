# Quyết định 29/10/2026 – sau đối chất Claude ↔ ChatGPT ("Ý tưởng AI táo bạo")

## Bỏ
- Kiến trúc "ASAHI AI OS" 12 agent, n8n (cloud hay tự host/Docker), Supabase, dashboard riêng, OpenAI Agents SDK: tốn 12–25 giờ setup + bảo trì, máy phải bật; không hợp người không có thời gian.
- B2B Hunter đọc RSS tin tức: không tìm được khách thật.
- Booking Concierge / Client Retention / Sales Coordinator bằng AI free-tier: không khả thi vì không được đưa dữ liệu khách vào Gemini free (Google dùng dữ liệu để cải thiện sản phẩm).

## Giữ
- 3 cấp quyền: AI tự làm (nghiên cứu, nháp, nhắc) / người duyệt (mọi thứ ra ngoài) / không giao AI (tiền, hợp đồng, giấy phép, bảng giá gốc).
- AI không báo giá tour ngoài App báo giá Asahi.
- Tách dữ liệu du lịch – spa; đo "giờ chủ tiết kiệm".

## Thứ tự 5 tuần đến khai trương (ChatGPT đề xuất, Claude đồng ý)
1. 29/10–5/11: pháp lý Yume (保健所), LINE công式, chốt dịch vụ.
2. 2–8/11: menu, giá, Google Business Profile, website (đã có bản v0.1).
3. 5–15/11: quay video thật, 10–15 nội dung teaser, lịch đăng.
4. 10–22/11: quy trình đặt lịch, chạy thử.
5. 23/11–khai trương: tổng duyệt vận hành.
Song song: website Asahi mới (task khác), hồ sơ công khai công ty.

## Điểm ChatGPT không đồng ý với Claude
1. "Asahi không có website công khai" – ChatGPT đúng: asahijapantours.com đang chuyển hướng về asahivietlife.tokyo/en/ (WordPress, 160 tour, giá USD). Chủ xác nhận web mới đang làm ở task khác; web cũ chỉ tham khảo.
2. "Có số đăng ký 第20990号 trên catalog = đã xác minh pháp lý" – ChatGPT đúng: cần đối chiếu bản gốc; 旅行サービス手配業 không cho bán tour lẻ. Chủ xác nhận và sẽ lên 第3種.

## Kiểm chứng số liệu (Claude)
- LINE công式: Communication 0円/200 tin; Light 5.000円/5.000 tin; Standard 15.000円/30.000 tin (lycbiz.com).
- Phí kiểm tra 美容所: 24.000円 (目黒区, 杉並区, 文京区, 町田市 – mức chung Tokyo).
- Gemini API free tier: dữ liệu dùng để cải thiện sản phẩm (ai.google.dev/gemini-api/docs/billing).
- ChatGPT còn ~8% hạn mức sử dụng lúc 23:40 29/10 → ưu tiên Claude cho các task lặp.
