---
artifact: 2 — Bảng so sánh 2 sản phẩm theo 5 mục
bai-tap: 2 — Phân tích 2 sản phẩm AI (nhóm 2 học viên)
phase: Chuyển giao Phase 2 → Phase 3 (5 phút)
time: 5 phút
input: 1-research-notes.md + screenshots/
nop-cuoi: Không — file trung gian (đầu vào cho `3-FINAL-analysis-outline.md`)
---

# 2 — Bảng so sánh 2 sản phẩm theo 5 mục slide deck

Mục tiêu: gộp toàn bộ quan sát ở Bước 1 thành **một bảng so sánh nén** — cùng cấu trúc 5 mục mà slide deck cuối sẽ dùng. Sau bước này, nhóm có "khung xương" của slide deck.

Lý do làm bước này: nhảy thẳng từ log sang slide deck dễ bị bỏ sót mục. Bảng so sánh ép nhóm trả lời từng mục cho cả 2 sản phẩm song song — phát hiện ngay nếu mục nào còn thiếu bằng chứng.

Quy tắc: mỗi ô của bảng dài tối đa 2 câu. Nếu ô nào để trống → quay lại `1-research-notes.md` đào thêm trước khi sang Bước 3.

## Quy trình 5 phút

```text
3 phút  — Điền bảng so sánh 5 mục (5 dòng × 2 cột)
1 phút  — Đánh dấu ô nào còn thiếu bằng chứng
1 phút  — Quyết định: cần test thêm hay đủ để sang slide?
```

---

## Phần A — Bảng so sánh 5 mục

| Mục | Sản phẩm A | Sản phẩm B |
|---|---|---|
| **S1 — Product Moment**<br><sup>Entry point + ý định người dùng + surface chính (chat / form / canvas / IDE)</sup> | Giao diện workspace cá nhân, cần đăng nhập Google. Người dùng muốn upload tài liệu riêng để AI tổng hợp qua chat QA. | Giao diện thanh tìm kiếm trung tâm, dùng được ngay không cần login. Người dùng muốn tìm câu trả lời nhanh từ các bài báo khoa học. |
| **S2 — Workflow Evidence**<br><sup>Trước / trong / sau khi dùng AI. Friction chính (số click, tab, copy-paste, load mental)</sup> | Phải qua bước chuẩn bị (upload PDF, chờ index) nên physical load cao. Bù lại cognitive burden thấp vì AI giữ ngữ cảnh tốt. | Không cần upload, gõ trực tiếp vào thanh search nên physical load rất thấp. Tuy nhiên, mỗi query độc lập nên cognitive burden ở mức trung bình. |
| **S3 — Output &amp; Trust**<br><sup>Chất lượng output + dẫn nguồn + disclaimer + control cho người dùng</sup> | Output đầy đủ, đúng yêu cầu 500 từ. Citation chính xác đến từng đoạn văn trong tài liệu upload, có disclaimer rõ ràng. | Output trả về từng snippets ngắn thay vì bài tổng hợp dài. Trích dẫn DOI khoa học minh bạch, có Consensus Meter trực quan. |
| **S4 — Business Signal**<br><sup>Pricing + giới hạn / paywall + định vị Cost-Capability-Speed (rẻ-nhanh hay mạnh-đắt)</sup> | Định vị Cân bằng: miễn phí cho tính năng cơ bản, gói Plus $20/tháng, tốc độ trung bình, capability cao. | Định vị Mạnh-đắt: freemium giới hạn search, gói Premium $10-12/tháng, tập trung vào research chuyên sâu. |
| **S5 — Product Judgment**<br><sup>Verdict 1 dòng: Strong / Promising / Weak / At Risk + lý do</sup> | **Promising** — Chất lượng cao, miễn phí nhưng chưa có hướng đi monetization độc lập rõ ràng. | **Strong** — Niche nghiên cứu rõ ràng, data moat mạnh mẽ (200M+ papers) và mô hình doanh thu thực tế. |

---

## Phần B — Đối chiếu 3 friction areas (nén từ Lens 3)

Đây là cột trụ của mục S2 trong slide deck. Mỗi friction area trả lời 1 câu so sánh:

- **Physical load** (số click / tab / lần copy-paste): NotebookLM có physical load cao hơn vì yêu cầu upload tài liệu trước, trong khi Consensus chỉ cần gõ trực tiếp câu hỏi.
- **Cognitive burden** (cần học prompt engineering / có hint sẵn / có nhớ ngữ cảnh giữa lượt chat):
  - NotebookLM có cognitive burden thấp hơn vì AI nhớ toàn bộ ngữ cảnh trong notebook, Consensus yêu cầu gõ lại query rõ ràng cho mỗi lần tìm.
- **User workarounds** (nhóm phải tự làm gì để bù yếu điểm — vd: prompt lại 3 lần, copy sang công cụ khác):
  - Với NotebookLM phải tự đi tìm thêm PDF nếu tài liệu thiếu, với Consensus phải tự ghép các snippets thành bài viết hoàn chỉnh.

---

## Phần C — Đối chiếu 6 trust signals (nén cho mục S3)

Đánh dấu mỗi sản phẩm có / không / một phần:

| Tín hiệu đáng tin | Sản phẩm A | Sản phẩm B |
|---|---|---|
| 1. Dẫn nguồn (citation) — link mở được, đúng nội dung | Có — trỏ về đoạn PDF | Có — hiển thị DOI / link paper |
| 2. Disclaimer khi không chắc ("không tìm được", "có thể sai") | Có — "Dựa trên nguồn upload" | Có — Hiển thị mức độ confidence |
| 3. Fallback / dừng lại khi out-of-scope | Có — từ chối nếu ngoài tài liệu | Một phần — giới hạn trong literature |
| 4. Consistency — chạy 2 lần cùng prompt, output có giống không | Cao — cùng notebook ra output giống | Trung bình — kết quả thay đổi theo index |
| 5. User control — sửa lại, dừng, regenerate, undo | Có — regenerate, audio overview | Có — save, export citation |
| 6. Explanation — giải thích "tại sao AI nói thế" (nếu có) | Một phần — link citation nhưng không giải thích | Có — Consensus Meter giải thích tỷ lệ |

---

## Phần D — Định vị 2 sản phẩm trên Cost-Capability-Speed (cho mục S4)

Mỗi sản phẩm chọn **1** trong 3 góc tam giác (vẽ hình tay nếu cần — sẽ dán vào slide S4):

- **Sản phẩm A nghiêng về**: cân bằng — lý do 1 câu: Miễn phí cho cơ bản, gói Plus, tốc độ trung bình do chờ index, nhưng capability tổng hợp sâu rất cao.
- **Sản phẩm B nghiêng về**: mạnh-đắt — lý do 1 câu: Freemium rất hạn chế, phải mua Premium để unlock full analysis, capability chuyên biệt cho research từ data độc quyền.

---

## Phần E — Verdict sơ bộ (cho mục S5.1)

Đặt verdict 1 dòng cho mỗi sản phẩm (sẽ tinh chỉnh lại ở Bước 3 sau khi vận dụng 4 Lens + Spark/Loop/System):

- **Sản phẩm A — verdict sơ bộ**: Promising
  - Lý do 1 câu: Sản phẩm tuyệt vời, miễn phí, hệ sinh thái Google nhưng vẫn đang đi tìm business model rõ ràng.
- **Sản phẩm B — verdict sơ bộ**: Strong
  - Lý do 1 câu: Chọn đúng niche research, kho dữ liệu 200 triệu bài báo tạo thành moat mạnh và user có willingness-to-pay cao.

---

## Bảng kiểm trước khi sang Bước 3

- [x] Mỗi ô của bảng so sánh 5 mục có ít nhất 1-2 câu, không trống.
- [x] Mỗi nhận định đều có thể chỉ về ảnh / log trong `1-research-notes.md` làm bằng chứng.
- [x] Đã định vị cả 2 sản phẩm trên Cost-Capability-Speed.
- [x] Đã có verdict sơ bộ cho cả 2 sản phẩm.
- [x] Còn ô nào thiếu bằng chứng → đã đánh dấu để Phase 3 đào thêm.

Sang `3-FINAL-analysis-outline.md` để dựng outline 5 mục đầy đủ (với S5 mở rộng 8 sub-mục) trước khi build slide.
