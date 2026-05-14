---
artifact: 1 — Ghi chú nghiên cứu khi test 2 sản phẩm AI
bai-tap: 2 — Phân tích 2 sản phẩm AI (nhóm 2 học viên)
phase: Phase 2 — Thử nghiệm + chụp ảnh + research (20 phút)
time: 20 phút
input: group-members.md (nhóm đã chốt ngành + 2 sản phẩm + nhiệm vụ chung)
nop-cuoi: Không — file trung gian (đầu vào cho `2-comparison-table.md`)
---

# 1 — Ghi chú nghiên cứu khi test 2 sản phẩm AI

Mục tiêu: trong 20 phút thử nghiệm, 2 thành viên cùng test 2 sản phẩm AI với 1 nhiệm vụ chung. File này ghi lại **quan sát thật** (không phải đánh giá tổng kết).

Quy tắc: **không có ảnh chụp / log = không có quan sát**.

## Quy trình 20 phút

```text
2 phút   — Ghi setup chung (nhiệm vụ + câu prompt + tài khoản dùng)
8 phút   — Test Sản phẩm A: chụp 3-5 ảnh + ghi log
8 phút   — Test Sản phẩm B: chụp 3-5 ảnh + ghi log
2 phút   — First impressions: ghi 3 quan sát nổi nhất cho mỗi sản phẩm
```

---

## Phần A — Setup chung (2 phút)

- **Nhiệm vụ chung**: Tổng hợp tài liệu nghiên cứu: upload 3-5 PDF/bài báo về chủ đề "AI agent" hoặc "Vietnam fintech regulation 2024", yêu cầu AI tổng hợp bài viết 500 từ có dẫn nguồn.
- **Câu prompt chính xác**: "Tôi upload 5 tài liệu về AI agent trong doanh nghiệp. Tổng hợp giúp tôi 1 bài viết 500 từ gồm: (1) định nghĩa AI agent, (2) 3 use case chính cho doanh nghiệp, (3) 2 rủi ro cần lưu ý. Yêu cầu dẫn nguồn cụ thể từ các tài liệu đã upload."
- **Loại tài khoản dùng**:
  - Sản phẩm A (NotebookLM): Tài khoản Google cá nhân (miễn phí)
  - Sản phẩm B (Consensus): Tài khoản miễn phí (giới hạn Pro Analysis)
- **Trình duyệt + thời gian test**: Chrome / Edge — 2026-05-14

---

## Phần B — Log Sản phẩm A: NotebookLM (8 phút)

**Tên sản phẩm A**: NotebookLM (Google)
**URL**: https://notebooklm.google.com
**Model dưới mui xe**: Gemini 1.5 Pro (hiển thị trong settings)

### B.1 — Entry point + lần chạm đầu

- Trang đầu hiển thị giao diện Google Material Design, danh sách notebook đã tạo (nếu có).
- Có sample notebook sẵn để demo (vd: "NotebookLM Guide").
- Cần đăng nhập Google trước khi dùng; không có paywall ngay.
- **Ảnh đã chụp**: `screenshots/product-A-1-entry.png`

### B.2 — Khi gõ prompt + nhận output

- Thời gian phản hồi: ~8 giây
- Có hiển thị "Đang tạo ghi chú..." / streaming từng đoạn.
- Output dài: ~520 từ (kiểm tra đủ 500 từ không: Có, vượt yêu cầu).
- Output có dẫn nguồn: **Có** — hiển thị số citation [1], [2]... click được đến đoạn trong tài liệu gốc.
- Có hiển thị disclaimer: "Câu trả lời dựa trên các nguồn bạn đã upload".
- **Ảnh đã chụp**: `screenshots/product-A-1-entry.png` + `screenshots/product-A-2-input.png` + `screenshots/product-A-3-output.png` + `screenshots/product-A-4-source.png` (citation check) + `screenshots/product-A-5-pricing.png` (giá gói Plus)

### B.3 — Phản hồi sau khi nhận output

- Có nút "Chuyển thành Hướng dẫn nghiên cứu" / "Tạo Audio Overview" không? [Có]
- Có nút copy / export ra format khác không? [Có — copy, share link]
- Có gợi ý câu hỏi tiếp theo không? [Có — 3 suggested questions]
- Có lưu lịch sử để truy lại không? [Có — trong notebook]
- Có thumb up / thumb down để feedback không? [Có]

### B.4 — Quan sát nổi (3 quan sát)

1. Giao diện dạng workspace, tập trung sâu vào cá nhân hóa tài liệu thay vì tìm kiếm web rộng rãi.
2. Output bám cực sát vào tài liệu đã upload, trích dẫn chính xác đến từng đoạn văn trong file PDF.
3. Tính năng chuyển đổi thành Audio Overview (dạng podcast) rất mượt và hữu ích để nghe lại.

---

## Phần C — Log Sản phẩm B: Consensus (8 phút)

**Tên sản phẩm B**: Consensus
**URL**: https://consensus.app
**Model dưới mui xe**: Không hiển thị rõ (có thể GPT-4 hoặc custom model)

### C.1 — Entry point + lần chạm đầu

- Trang đầu hiển thị thanh tìm kiếm lớn + tagline "Search Engine for Research".
- Có sample searches sẵn (vd: "Does creatine improve cognition?").
- Có thể dùng không đăng nhập cho search cơ bản; đăng nhập để lưu lịch sử.
- **Ảnh đã chụp**: `screenshots/product-B-1-entry.png`

### C.2 — Khi gõ prompt + nhận output

- Thời gian phản hồi: ~4 giây
- Có hiển thị "Searching 200M+ papers..." rồi trả kết quả.
- Output dài: ~250 từ (có đủ 500 từ không? Không, Consensus thường trả về ngắn hơn, chủ yếu là các snippets).
- Output có dẫn nguồn: **Có** — hiển thị DOI, tên paper, năm.
- Có hiển thị "Consensus Meter" (tỷ lệ ủng hộ/phản đối/trung lập).
- **Ảnh đã chụp**: `screenshots/product-B-1-entry.png` + `screenshots/product-B-2-input.png` + `screenshots/product-B-3-output.png` + `screenshots/product-B-5-pricing.png` (giá Premium)

### C.3 — Phản hồi sau khi nhận output

- Có nút "Save to Library" / "Export to Zotero" không? [Có — Save, Export citation]
- Có nút copy / share không? [Có]
- Có gợi ý câu hỏi tiếp theo không? [Có — Related questions]
- Có lưu lịch sử để truy lại không? [Có — nếu đăng nhập]
- Có thumb up / thumb down để feedback không? [Có]

### C.4 — Quan sát nổi (3 quan sát)

1. Tốc độ tìm kiếm qua hàng trăm triệu bài báo khoa học rất ấn tượng, không cần upload hay setup gì.
2. Tính năng Consensus Meter rất trực quan để xem mức độ đồng thuận của giới khoa học về một chủ đề.
3. Output trả về theo dạng danh sách các trích đoạn (snippets) độc lập chứ không phải một bài tổng hợp liền mạch dài.

---

## Phần D — First impressions (2 phút)

1. **Sản phẩm nào "cảm giác" dễ dùng hơn lần đầu? Tại sao?**
   - Consensus dễ tiếp cận hơn cho lần đầu sử dụng vì giao diện giống Google Search truyền thống — gõ là ra, không cần đăng nhập hay thao tác upload tài liệu phức tạp.

2. **Sản phẩm nào "cảm giác" cho output đáng tin hơn? Tại sao?**
   - Về mặt học thuật và khách quan, Consensus đáng tin hơn do nguồn trích dẫn từ 200M+ bài báo khoa học. Nhưng về mặt kiểm soát nguồn, NotebookLM an toàn hơn vì chỉ dựa trên đúng các file mình chủ động upload.

3. **Câu hỏi mà nhóm CHƯA trả lời được sau 20 phút test:**
   - Liệu Google có dùng gián tiếp hành vi đọc/tổng hợp tài liệu trên NotebookLM để tối ưu hóa thuật toán chung không? Consensus dùng model nền tảng nào (GPT-4 hay custom) để tạo ra các snippets tổng hợp?

> Đây là first impressions — chưa phải nhận định. Khi sang `2-comparison-table.md` sẽ đối chiếu chéo với số liệu cụ thể.

---

## Bảng kiểm trước khi sang Bước 2

- [x] Câu prompt giống y hệt cho cả 2 sản phẩm.
- [x] Đã chụp tối thiểu 3 ảnh cho mỗi sản phẩm (entry + input + output).
- [x] NotebookLM: 5 ảnh (entry, input, output, source, pricing).
- [x] Consensus: 4 ảnh (entry, input, output, pricing).
- [x] Mỗi quan sát có ảnh / log tham chiếu.
- [x] Mỗi quan sát có ảnh / log tham chiếu.
- [x] First impressions ghi rõ — không dùng từ chung chung như "hay hơn", "tốt hơn" mà không kèm lý do.
- [x] Đã trả lời 5 câu trong `group-members.md` về phân chia trách nhiệm.

Sang `2-comparison-table.md` để dựng bảng so sánh 2 sản phẩm theo 5 mục của slide deck.
