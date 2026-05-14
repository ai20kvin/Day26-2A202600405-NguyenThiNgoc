---
artifact: analysis-report — Báo cáo phân tích 2 sản phẩm AI (nhóm)
bai-tap: 2 — Phân tích 2 sản phẩm AI (nhóm 2 học viên)
phase: Phase 3 — Dựng slide deck (15 phút)
time: 10 phút outline + 5 phút build slide
input: 1-research-notes.md + 2-comparison-table.md + screenshots/ + prompts/08-analysis-report.md
nop-cuoi: Có — analysis-report.pdf (deliverable bắt buộc)
---

# Analysis Report — Outline đầy đủ S1 → S5

Sản phẩm A: NotebookLM (Google) | Sản phẩm B: Consensus
Ngành: D — Nghiên cứu | Nhiệm vụ test: Tổng hợp tài liệu AI agent (500 từ, có dẫn nguồn)
Thành viên: Ngọc (NotebookLM) + Quang (Consensus)

---

## S1 — Product Moment (slide 1-2)

Mục đích: định danh rõ 2 sản phẩm, nhiệm vụ chung, điểm gặp đầu (entry point).

### S1.1 — Bảng so sánh nhanh

| Yếu tố | Sản phẩm A — NotebookLM | Sản phẩm B — Consensus |
|---|---|---|
| Tên + URL | NotebookLM — https://notebooklm.google.com | Consensus — https://consensus.app |
| Entry point (trang đầu nhìn thấy gì) | Giao diện Google Material Design, danh sách notebook đã tạo, sample notebook sẵn để demo | Thanh tìm kiếm lớn ở giữa, tagline "Search Engine for Research", sample searches sẵn |
| Ý định người dùng (vào để làm gì) | Upload tài liệu → tạo notebook → hỏi đáp / tổng hợp / tạo audio overview | Tìm kiếm câu hỏi nghiên cứu → xem tổng hợp từ các bài báo khoa học |
| Surface chính (chat / form / canvas / IDE / khác) | Chat-style QA + notebook viewer + source citation panel | Search bar + results list + Consensus Meter + snippet cards |
| Có cần đăng nhập / paywall ngay không | Cần đăng nhập Google; không có paywall ngay | Có thể dùng không đăng nhập cho search cơ bản; đăng nhập để lưu lịch sử |

### S1.2 — Bằng chứng (ảnh tham chiếu)

- `screenshots/product-A-1-entry.png` — Trang đầu NotebookLM hiển thị danh sách notebook và sample guide
- `screenshots/product-B-1-entry.png` — Trang đầu Consensus với search bar trung tâm và sample queries

### S1.3 — Nhận định so sánh entry point (2-3 câu)

NotebookLM tạo first impression "workspace" hơn là "search engine" — người dùng cảm giác đang vào một môi trường làm việc với tài liệu của riêng mình. Consensus tạo first impression giống Google Search nhưng chuyên biệt cho research — lập tức cho phép người dùng gõ câu hỏi mà không cần upload hay setup gì. Nếu ý định là "tìm nhanh câu trả lời từ literature", Consensus thắng ở tốc độ tiếp cận; nếu ý định là "đào sâu vào một chủ đề với tài liệu riêng", NotebookLM thắng ở tính cá nhân hóa.

---

## S2 — Workflow Evidence (slide 3-4)

Mục đích: hiển thị luồng người dùng + 3 friction areas (Lens 3).

### S2.1 — Luồng người dùng (trước / trong / sau khi dùng AI)

```text
TRƯỚC khi gặp AI:
- Người dùng đang có 3-5 bài báo/PDF về AI agent cần tổng hợp thành 1 bài viết 500 từ có dẫn nguồn

TRONG khi dùng Sản phẩm A (NotebookLM):
1. Upload 5 PDF vào notebook mới
2. Đợi indexing (tự động phân tích nguồn)
3. Gõ prompt: "Tổng hợp bài viết 500 từ về AI agent trong doanh nghiệp..."
4. Nhận output có citation [1], [2]... click được về đoạn trong tài liệu gốc
5. Có thể chuyển thành Audio Overview hoặc export

TRONG khi dùng Sản phẩm B (Consensus):
1. Gõ câu hỏi trực tiếp vào search bar (không cần upload)
2. Đợi "Searching 200M+ papers..."
3. Xem Consensus Meter + snippet từ các bài báo liên quan
4. Click vào từng paper để xem abstract / full text
5. Có thể save vào library hoặc export citation

SAU khi dùng AI:
- NotebookLM: copy output, share link notebook, tạo audio overview, hoặc export ra Google Docs
- Consensus: copy snippet, save paper vào library, export citation sang Zotero, hoặc share link
```

### S2.2 — 3 Friction Areas (Lens 3)

| Friction | Sản phẩm A — NotebookLM | Sản phẩm B — Consensus |
|---|---|---|
| **Physical load** (số click, tab, copy-paste) | Cao hơn — cần upload tài liệu trước, đợi indexing, nhiều bước setup | Thấp hơn — chỉ cần gõ search query, không cần upload gì |
| **Cognitive burden** (cần học prompt eng. / nhớ ngữ cảnh giữa lượt chat) | Thấp — AI nhớ ngữ cảnh trong notebook; gợi ý câu hỏi tiếp theo | Trung bình — không có ngữ cảnh liên tục như chat; mỗi search là独立的 |
| **User workarounds** (nhóm phải tự làm gì để bù yếu điểm) | Nếu tài liệu không đủ đa dạng, phải tự tìm thêm PDF để upload | Nếu cần tổng hợp từ tài liệu riêng (không public), phải chuyển sang công cụ khác |

### S2.3 — Bằng chứng

- `screenshots/product-A-2-input.png` + `screenshots/product-A-3-output.png` — Hiển thị quá trình gõ prompt và nhận output có citation trong NotebookLM
- `screenshots/product-B-2-input.png` + `screenshots/product-B-3-output.png` — Hiển thị search query và kết quả với Consensus Meter

### S2.4 — Nhận định: sản phẩm nào giảm friction tốt hơn? Tại sao? (3-4 câu)

Consensus giảm friction tốt hơn cho use case "tìm nhanh câu trả lời từ literature" vì không yêu cầu upload hay đăng nhập. Tuy nhiên, NotebookLM giảm friction tốt hơn cho use case "tổng hợp từ tài liệu riêng" vì AI nhớ ngữ cảnh toàn bộ notebook và citation chính xác đến từng đoạn trong tài liệu đã upload. Friction chính của NotebookLM nằm ở bước upload và indexing; friction chính của Consensus nằm ở việc không thể dùng tài liệu private và output thường ngắn hơn yêu cầu 500 từ.

---

## S3 — Output & Trust (slide 5-6)

Mục đích: đánh giá chất lượng output + 6 tín hiệu đáng tin.

### S3.1 — Chất lượng output

- **Sản phẩm A — NotebookLM**:
  - Output có **trả lời đúng câu hỏi** chính không? **Có** — trả lời đủ 3 yêu cầu: định nghĩa, 3 use case, 2 rủi ro
  - Output có **bịa thông tin** không (hallucination)? **Không rõ** — dựa trên tài liệu đã upload, nhưng cần verify từng citation
  - Output có **đầy đủ** hay nửa vời? **Đầy đủ** — đạt ~500 từ, có cấu trúc rõ ràng

- **Sản phẩm B — Consensus**:
  - Output có **trả lời đúng câu hỏi** chính không? **Một phần** — trả về các snippet từ papers liên quan nhưng không tổng hợp thành 1 bài viết liền mạch
  - Output có **bịa thông tin** không? **Thấp** — mỗi snippet gắn với DOI/paper cụ thể, dễ verify
  - Output có **đầy đủ** hay nửa vời? **Nửa vời** — output là danh sách snippet, không phải 1 bài viết 500 từ như yêu cầu

### S3.2 — 6 Tín hiệu đáng tin (đối chiếu)

| Tín hiệu | Sản phẩm A — NotebookLM | Sản phẩm B — Consensus |
|---|---|---|
| 1. Dẫn nguồn (citation mở được, đúng nội dung) | Có — citation [1], [2] click được đến đoạn trong tài liệu gốc | Có — hiển thị DOI, tên paper, năm; click đến source |
| 2. Disclaimer khi không chắc | Có — "Câu trả lời dựa trên các nguồn bạn đã upload" | Có — hiển thị mức độ confidence và số lượng papers |
| 3. Fallback / dừng lại khi out-of-scope | Có — từ chối trả lời nếu câu hỏi ngoài tài liệu upload | Một phần — giới hạn trong literature đã index |
| 4. Consistency (chạy 2 lần cùng prompt) | Cao — cùng 1 notebook, cùng tài liệu → output nhất quán | Trung bình — kết quả có thể thay đổi theo papers mới được index |
| 5. User control (sửa, dừng, regenerate, undo) | Có — regenerate, copy, share, tạo audio overview | Có — save, export citation, share link |
| 6. Explanation (giải thích "vì sao AI nói thế") | Một phần — citation link nhưng không giải thích reasoning | Có — Consensus Meter giải thích tỷ lệ ủng hộ/phản đối |

### S3.3 — Nhận định: sản phẩm nào tạo trust mạnh hơn? Vì sao? (3-4 câu)

Consensus tạo trust mạnh hơn ở khía cạnh "transparency" vì hiển thị rõ từng snippet gắn với paper cụ thể, có Consensus Meter cho biết mức độ đồng thuận trong literature. NotebookLM tạo trust ở khía cạnh "personalization" — citation chính xác đến từng đoạn trong tài liệu của người dùng, nhưng người dùng phải tin tưởng tài liệu họ upload là đúng. Tổng thể, Consensus đáng tin hơn cho việc "khám phá literature mới" vì source độc lập; NotebookLM đáng tin hơn cho việc "đào sâu tài liệu đã có".

---

## S4 — Business Signal (slide 7)

Mục đích: định vị 2 sản phẩm trên Cost-Capability-Speed + pricing pattern.

### S4.1 — Định vị tam giác (cho mỗi sản phẩm)

- **Sản phẩm A — NotebookLM**: **Cân bằng** — model dưới mui xe: Gemini 1.5 Pro — lý do định vị 1 câu: Miễn phí cho cơ bản, trả phí cho nâng cao (Plus), tốc độ trung bình (phải đợi indexing), capability cao (tổng hợp dài, audio overview)
- **Sản phẩm B — Consensus**: **Mạnh-đắt (ở tier cao)** — model dưới mui xe: Không hiển thị rõ (có thể GPT-4 hoặc custom model) — lý do định vị 1 câu: Freemium hạn chế, Premium mới unlock full analysis; tốc độ nhanh (search 200M+ papers), capability chuyên biệt cho research

### S4.2 — Pricing pattern

| Yếu tố | Sản phẩm A — NotebookLM | Sản phẩm B — Consensus |
|---|---|---|
| Mô hình giá | Freemium — Free tier đủ dùng cho cá nhân; Plus cho nâng cao | Freemium — Free giới hạn số lượng searches; Premium cho unlimited + Pro Analysis |
| Giá entry (free tier giới hạn gì) | Free: tạo notebook, upload tài liệu, hỏi đáp cơ bản, audio overview | Free: ~20 searches/tháng, không có Consensus Meter đầy đủ, không export |
| Giá trả phí (gói chính + giá) | NotebookLM Plus: ~$20/tháng (tích hợp Google One AI Premium) | Premium: ~$10-12/tháng; Pro/Enterprise: custom pricing |
| Paywall xuất hiện ở đâu (khi hết quota / tính năng nâng cao / etc.) | Khi cần nhiều notebook hơn, audio overview dài hơn, hoặc tích hợp Google Workspace | Khi hết quota searches, cần Consensus Meter đầy đủ, hoặc export sang reference manager |

### S4.3 — Nhận định: chiến lược kinh doanh của 2 sản phẩm khác nhau thế nào? (2-3 câu)

NotebookLM đi theo chiến lược "ecosystem lock-in" của Google — miễn phí để thu hút người dùng Google ecosystem, trả phí qua Google One AI Premium bundle. Consensus đi theo chiến lược "vertical SaaS for researchers" — freemium hạn chế để upsell sang Premium cho sinh viên/nhà nghiên cứu, và Enterprise cho institutions. NotebookLM không cần monetize trực tiếp sản phẩm vì Google hưởng lợi từ data và ecosystem; Consensus cần monetize trực tiếp vì là startup độc lập.

---

## S5 — Product Judgment (slide 8-12 — phần đậm nhất)

Mục đích: ra verdict + vận dụng 4 Lens + Spark/Loop/System + Niche/Feature Map + liên hệ Lab 1.

S5 mở rộng thành 8 sub-mục — bắt buộc xong **S5.1, S5.6, S5.7, S5.8**. Nhóm khá phải hoàn thành cả 8 sub-mục.

### S5.1 — Verdict (BẮT BUỘC)

- **Sản phẩm A — NotebookLM**: **Promising** — Lý do: Sản phẩm miễn phí chất lượng cao, tích hợp sâu vào Google ecosystem, nhưng vẫn đang tìm product-market fit rõ ràng và chưa có đường monetization độc lập.
- **Sản phẩm B — Consensus**: **Strong** — Lý do: Niche rõ ràng (search engine for research), moat từ data (200M+ papers), monetization rõ ràng (Premium + Enterprise), và đang tăng trưởng nhanh trong cộng đồng học thuật.

### S5.2 — User base + tăng trưởng

- **Sản phẩm A — NotebookLM**: Không có số liệu MAU/DAU công khai sau khi tra TechCrunch, The Verge, Google Blog. Google không công bố số liệu riêng cho NotebookLM. Ước tính: hàng triệu người dùng Google Workspace tiềm năng.
- **Sản phẩm B — Consensus**: Không có số liệu MAU/DAU chính xác công khai sau khi tra Crunchbase, Product Hunt, Consensus Blog. Được sử dụng bởi 1M+ researchers theo marketing materials (chưa verify độc lập).

### S5.3 — Doanh thu / pricing power

- **Sản phẩm A — NotebookLM**: Không có ARR/MRR công khai — là sản phẩm nội bộ Google, không báo cáo riêng. Chiến lược pricing: Freemium → upsell Google One AI Premium bundle ($20/tháng bao gồm Gemini Advanced, 2TB storage, và các tính năng AI khác).
- **Sản phẩm B — Consensus**: Không có ARR/MRR chính xác công khai — là startup private. Đã raise funding (Series A/B chưa công bố chi tiết). Chiến lược pricing: Freemium → Premium ($10-12/tháng) → Enterprise/Institution (custom pricing).

### S5.4 — Moat phân tích (5 loại)

| Moat | Sản phẩm A — NotebookLM | Sản phẩm B — Consensus |
|---|---|---|
| Data (proprietary data flywheel) | Trung bình — dữ liệu từ tài liệu người dùng upload, nhưng không exclusive (Google có nhiều nguồn data khác) | Mạnh — 200M+ scientific papers, relationships giữa papers, citation graph |
| Network effects | Yếu — không có network effect rõ ràng; value chủ yếu từ individual usage | Trung bình — value tăng khi nhiều researchers dùng (more citations, more reviews), nhưng không mạnh như social network |
| Switching cost (chi phí đổi sang sản phẩm khác) | Trung bình — tài liệu đã upload và notebook đã tạo tạo switching cost nhẹ | Trung bình — library và saved papers tạo switching cost; nhưng dễ export citation sang Zotero/Mendeley |
| Brand | Mạnh — thương hiệu Google, trust từ billions người dùng | Trung bình — known trong cộng đồng học thuật và research, nhưng chưa mainstream |
| Distribution (kênh tiếp cận user) | Mạnh — tích hợp vào Google Workspace, Google Drive, Google One AI Premium | Trung bình — organic growth từ academia, word-of-mouth, Product Hunt, partnerships với universities |

### S5.5 — Data flywheel + feedback loop

- **Sản phẩm A — NotebookLM**: Người dùng upload tài liệu → AI tổng hợp → người dùng đọc output, click citation, thumbs up/down → feedback này có thể cải thiện model. Tuy nhiên, loop không rõ ràng vì Google không công bố cách dùng feedback từ NotebookLM để train model. Compounding yếu vì value chủ yếu đến từ tài liệu của từng người dùng riêng lẻ, không phải từ aggregate data.
- **Sản phẩm B — Consensus**: Người dùng search → click vào papers → save papers → export citations → feedback này cải thiện ranking và relevance của search results. Loop mạnh hơn vì mỗi lần dùng đều feed vào understanding của hệ thống về "paper nào relevant với query nào". Compounding mạnh hơn vì càng nhiều researchers dùng → càng nhiều behavioral data → search càng chính xác.

### S5.6 — Niche Down + AI Feature Map (BẮT BUỘC)

- **Sản phẩm A — NotebookLM**:
  - Niche cụ thể (đối tượng người dùng + use case): Học sinh, sinh viên, nhà nghiên cứu, và knowledge workers cần tổng hợp tài liệu dài thành nội dung dễ tiêu thụ (notes, audio, Q&A). Use case chính: "đọc hiểu và tổng hợp tài liệu của bản thân".
  - AI Feature Map (User Value × User Alignment × Business Value):
    - User Value: **Cao** — tổng hợp dài → ngắn, audio overview, Q&A chính xác từ tài liệu riêng
    - User Alignment: **Cao** — không bán data, không quảng cáo trong output, privacy-first (tài liệu private không dùng train model theo Google)
    - Business Value: **Trung bình** — miễn phí cho hầu hết users, monetization qua Google One bundle, không phải standalone revenue driver

- **Sản phẩm B — Consensus**:
  - Niche cụ thể: Nhà nghiên cứu, sinh viên graduate, medical professionals, và policy makers cần tìm nhanh evidence từ scientific literature. Use case chính: "tìm kiếm và đánh giá evidence quality từ 200M+ papers".
  - AI Feature Map:
    - User Value: **Cao** — trả lời câu hỏi research bằng evidence từ literature, Consensus Meter cho biết mức độ đồng thuận
    - User Alignment: **Cao** — không bịa kết quả, mỗi claim gắn với paper cụ thể, transparency cao
    - Business Value: **Cao** — monetization rõ ràng (Premium + Enterprise), high willingness-to-pay từ researchers và institutions

### S5.7 — Spark → Loop → System (BẮT BUỘC)

- **Sản phẩm A — NotebookLM**: **Loop** — Lý do: Đã vượt qua giai đoạn Spark (không còn là experiment đơn thuần), đã có user base ổn định, tích hợp vào Google ecosystem, nhưng chưa đạt System vì chưa có network effects mạnh, chưa có compounding loop rõ ràng, và đang tìm kiếm product-market fit rõ ràng hơn. Dự báo 12 tháng tới: Google sẽ tích hợp sâu hơn vào Google Workspace for Education, thêm collaboration features (share notebook giữa nhiều người), và có thể rebrand hoặc merge vài Gemini ecosystem.
- **Sản phẩm B — Consensus**: **Loop** — Lý do: Đã có product-market fit rõ ràng trong niche research, đang mở rộng từ individual researchers sang institutions và enterprises, nhưng chưa đạt System vì chưa có network effects dominant hay switching cost quá cao. Dự báo 12 tháng tới: Ra mắt Enterprise tier với admin dashboard, partnerships với major universities, mở rộng sang medical/legal research verticals, và có thể raise thêm funding hoặc bị acquire bởi major publisher (Elsevier, Springer) hoặc AI company.

### S5.8 — Liên hệ Lab 1 (BẮT BUỘC)

Đối chiếu 2 sản phẩm với case bigtech-disruption mỗi thành viên đã làm ở Lab 1:

- Sản phẩm A (NotebookLM) có rủi ro disruption tương tự case nào của nhóm? **Tương tự case Google Bard / Gemini disrupt các standalone AI writing tools** — NotebookLM là sản phẩm bigtech (Google) miễn phí/tích hợp ecosystem có thể disrupt các công cụ tổng hợp tài liệu nhỏ hơn như Scholarcy, SummarizeBot, hoặc các startup làm "AI research assistant".
- Sản phẩm B (Consensus) có rủi ro disruption tương tự case nào của nhóm? **Tương tự case ChatGPT / Perplexity disrupt traditional search** — Consensus đang ở vị thế "startup vertical search" có nguy cơ bị bigtech (Google Scholar + Gemini, Microsoft Academic + Copilot) copy feature hoặc undercut pricing.
- Bài học rút từ Lab 1 áp dụng được cho 2 sản phẩm này thế nào? (2-3 câu):
  1. **Moat từ data không đủ nếu bigtech có distribution**: Consensus mạnh ở data (200M papers) nhưng nếu Google Scholar tích hợp Gemini để làm tương tự, distribution của Google sẽ là lợi thế áp đảo.
  2. **Ecosystem integration là double-edged sword**: NotebookLM hưởng lợi từ Google ecosystem nhưng cũng bị ràng buộc bởi roadmap và priorities của Google — có thể bị deprecate hoặc merge vào sản phẩm khác bất cứ lúc nào.
  3. **Niche rõ ràng là cách sống sót**: Consensus chọn niche research rõ ràng thay vì "AI search for everything" — đây là chiến lược đúng để tránh đối đầu trực tiếp với Perplexity hay Google trong short term.

---

## Bảng kiểm trước khi build slide

- [x] S1 → S4 đã điền đầy đủ.
- [x] S5.1 + S5.6 + S5.7 + S5.8 đã hoàn thành (4 sub-mục bắt buộc).
- [x] S5.2 → S5.5 đã hoàn thành (hoặc đã ghi rõ "không có nguồn công khai" cho ô trống).
- [x] Mỗi nhận định nối được về ảnh / log / số liệu cụ thể.
- [x] Verdict ở S5.1 nhất quán với phân tích moat ở S5.4 và giai đoạn ở S5.7.
- [x] 2 thành viên cùng đồng ý với toàn bộ outline.

---

## Sau khi xong outline

1. Mở pptx / Keynote / Google Slides / Figma.
2. Tạo 12-15 slide bám theo cấu trúc S1 → S5 ở trên (mỗi mục 1-3 slide).
3. **Mỗi slide có ít nhất 1 ảnh tham chiếu** (từ `screenshots/`).
4. Export PDF → lưu thành `analysis-report.pdf` trong cùng folder này.
5. Nếu dùng Google Slides công khai, lưu link vào `analysis-report-link.md` (tuỳ chọn).
6. 2 thành viên cùng copy `analysis-report.pdf` + `group-member.md` về repo cá nhân của mình.

> Tham khảo `prompts/08-analysis-report.md` nếu cần AI hỗ trợ build slide từ outline này.
