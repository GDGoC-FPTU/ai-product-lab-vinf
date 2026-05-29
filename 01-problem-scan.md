# 01-problem-scan — AI Product Scoping cho Vin Smart Future / Vingroup

> **Mục tiêu:** Tổng hợp các use case AI ấn tượng dựa trên thông tin công khai, ưu tiên nguồn chính thức và gần-chính-thức. File này bám format Lab 02: Phase 1 SCAN và Phase 2 QUICK-ASSESS.
>
> **Lưu ý phạm vi:** “Vin Green” trong tài liệu này được hiểu là mảng **V-GREEN / hạ tầng trạm sạc xe điện** liên quan hệ sinh thái VinFast. “Vinsoc” chưa thấy là pháp nhân/thương hiệu chính thức phổ biến trong nguồn công khai; do đó tôi diễn giải gần nhất là **Vinschool** nếu người học muốn làm mảng giáo dục.

---

## Phase 1 — SCAN: Tìm kiếm cơ hội AI

### Nguồn chính thức / gần chính thức đã dùng

| Nhóm | Factual hook từ nguồn | Nguồn |
|---|---|---|
| VinFast | VinFast App có các luồng số hóa: đăng nhập bảo mật, kết nối xe, quản lý nhiều xe, gọi khẩn cấp/SOS, tìm trạm sạc gần nhất, cảnh báo trộm, theo dõi sửa chữa/bảo dưỡng, đặt lịch bảo dưỡng/cứu hộ. | [VinFast — Ứng dụng VinFast](https://vinfastauto.com/vn_vi/ung-dung-vinfast) |
| VinFast / V-GREEN | Trang pin & trạm sạc của VinFast công bố luồng giá sạc, phí quá giờ sau khi pin đầy, thông tin sạc tại nhà và hệ thống trạm sạc. | [VinFast — Hệ thống trạm sạc](https://vinfastauto.com/vn_vi/he-thong-tram-sac) |
| Vinhomes | Vinhomes Resident cho cư dân đặt tiện ích công cộng, thanh toán hóa đơn, gửi yêu cầu hỗ trợ dịch vụ tòa nhà, phản ánh/góp ý với BQL, nhận thông tin PCCC/intercom/chỉ số môi trường. | [Google Play — Vinhomes Resident](https://play.google.com/store/apps/details?id=com.vinhomes.resident&hl=vi) |
| Vinmec | Vinmec là hệ thống bệnh viện/phòng khám lớn; các trang công khai về VinBrain/DrAid và hợp tác Vinmec–VinBrain thường nhắc AI hỗ trợ y tế/chẩn đoán hình ảnh. Cần xác minh lại bằng nguồn nội bộ nếu chọn làm bài chính thức. | [Vinmec](https://www.vinmec.com/) và [VinBrain](https://www.vinbrain.net/) |
| Vinschool | Vinschool triển khai Chương trình giáo dục Trí tuệ nhân tạo từ năm học 2025–2026 cho học sinh 5–18 tuổi toàn hệ thống; nội dung gồm hiểu AI, nhận diện AI, sử dụng AI có trách nhiệm; tích hợp liên môn. | [Vinschool — Chương trình giáo dục Trí tuệ nhân tạo](https://vinschool.edu.vn/chuong-trinh-giao-duc/chuong-trinh-giao-duc-tri-tue-nhan-tao/) |

---

### 📝 List bài toán của tôi

| # | Subsidiary | Lens | Mô tả ngắn bài toán |
|---|------------|------|---------------------|
| 1 | **VinFast / V-GREEN** | Stakeholder Pain | Chủ xe cần quyết định “sạc ở đâu, khi nào, trong bao lâu” nhưng phải tự kết hợp pin hiện tại, khoảng cách, loại trụ, phí quá giờ, lịch trình và tình trạng trạm. |
| 2 | **VinFast** | Tốn thời gian | Khi xe gặp sự cố, người dùng bấm SOS/gọi cứu hộ nhưng nhân viên hỗ trợ vẫn phải tổng hợp thủ công: xe nào, lỗi gì, pin/lốp/động cơ, vị trí, lịch sử bảo dưỡng, hướng xử lý. |
| 3 | **Vinhomes** | AI-upgrade | Cư dân gửi phản ánh/góp ý và yêu cầu dịch vụ tòa nhà qua app; BQL phải phân loại, hỏi lại thông tin thiếu, route cho kỹ thuật/an ninh/lễ tân và soạn phản hồi. |
| 4 | **Vinhomes** | Lặp lại | Đặt tiện ích công cộng, đăng ký khách, intercom/mở cửa/phân tầng thang máy tạo nhiều tác vụ xác nhận lặp lại; dễ phát sinh hàng đợi vào giờ cao điểm hoặc sự kiện. |
| 5 | **Vinmec** | Tốn thời gian | Bác sĩ/điều dưỡng phải tóm tắt hồ sơ, kết quả xét nghiệm, chỉ định và hướng dẫn sau khám/xuất viện thành văn bản dễ hiểu cho bệnh nhân. |
| 6 | **Vinmec** | AI-upgrade | Kết quả chẩn đoán hình ảnh/khám chuyên khoa cần được giải thích bằng ngôn ngữ bệnh nhân hiểu được, nhưng vẫn không được thay thế kết luận bác sĩ. |
| 7 | **Vinschool** | AI-upgrade | Chương trình AI 5–18 tuổi cần cá nhân hóa bài tập, rubric, phản hồi và cảnh báo misuse theo cấp lớp; giáo viên khó tự thiết kế nhanh cho toàn bộ học sinh. |
| 8 | **Vinschool** | Stakeholder Pain | Phụ huynh cần hiểu tiến bộ năng lực AI/digital literacy của con theo ngôn ngữ dễ hiểu, không chỉ điểm số; giáo viên mất thời gian viết nhận xét cá nhân hóa. |
| 9 | **Vin Smart Future / liên hệ sinh thái** | AI-upgrade | Khách hàng sống ở Vinhomes, lái VinFast, khám Vinmec, có con học Vinschool đang có nhiều app/điểm chạm rời rạc; chưa có “life-event concierge” xuyên hệ sinh thái. |
| 10 | **VinFast / V-GREEN / Vinhomes** | Repetitive + AI-upgrade | Quản trị sạc tại khu đô thị: cư dân VinFast muốn đặt lịch sạc gần nhà, tránh phí quá giờ và tránh quá tải điện cục bộ; BQL cần điều phối công bằng, minh bạch. |

---

## 🃏 Phase 2 — QUICK-ASSESS: 3 Quick Problem Cards

### Card #1 — VinFast / V-GREEN: Smart Charging Concierge

```text
┌─────────────────────────────────────────────────────────────┐
│ QUICK PROBLEM CARD #1                                       │
│                                                             │
│ Bài toán: Chủ xe VinFast cần trợ lý quyết định sạc tối ưu   │
│ theo pin, lịch trình, trạm gần nhất và phí quá giờ.         │
│ Công ty thành viên: [x] VinFast / V-GREEN                   │
│                                                             │
│ Ai đang đau? Chủ xe EV; CSKH VinFast; vận hành trạm sạc.    │
│                                                             │
│ Workflow thủ công hiện tại (5 bước):                        │
│   1. Chủ xe mở app xem pin/xe                               │
│   → 2. Tìm trạm sạc gần nhất                                │
│   → 3. Tự ước lượng thời gian đến/trạng thái sạc             │
│   → 4. Tự nhớ phí quá giờ và lịch cá nhân                    │
│   → 5. Tự đi/đợi/sạc, dễ phát sinh quá giờ hoặc đổi trạm     │
│                                                             │
│ Bước tốn/lỗi nhất? Bước 2-4 (⏱ 5-10 phút/lần quyết định)    │
│ AI hỗ trợ ở đâu? Bước 2-4: gợi ý kế hoạch sạc + nhắc rời trụ │
│                                                             │
│ Metric có số: Giảm thời gian chọn phương án sạc từ 8 phút   │
│ xuống dưới 60 giây; giảm 30% phiên bị phí quá giờ.          │
│                                                             │
│ Quick Architecture: [x] Agentic Loop có HITL                │
└─────────────────────────────────────────────────────────────┘
```

**Vì sao ấn tượng:** Đây là bài toán “AI + operations + behavior design”, không chỉ chatbot. Nó tận dụng dữ liệu xe, vị trí, trạm sạc, biểu phí, lịch người dùng và có thể mở rộng sang đặt chỗ sạc tại Vinhomes.

**Caveat:** Cần API thời gian thực về tình trạng trạm, loại cổng/trụ, SOC/pin, ETA và quy tắc phí. Nếu chưa có dữ liệu realtime, scope MVP chỉ nên là “draft recommendation”, không tự động điều phối.

---

### Card #2 — Vinhomes: AI Resident Ops Router

```text
┌─────────────────────────────────────────────────────────────┐
│ QUICK PROBLEM CARD #2                                       │
│                                                             │
│ Bài toán: Cư dân gửi phản ánh/yêu cầu dịch vụ tòa nhà qua   │
│ app nhưng BQL phải đọc, phân loại, hỏi thêm, route thủ công.│
│ Công ty thành viên: [x] Vinhomes                            │
│                                                             │
│ Ai đang đau? Cư dân; BQL; kỹ thuật tòa nhà; an ninh/lễ tân. │
│                                                             │
│ Workflow thủ công hiện tại (5 bước):                        │
│   1. Cư dân gửi yêu cầu/phản ánh trên app                    │
│   → 2. BQL đọc nội dung tự do                                │
│   → 3. Hỏi lại nếu thiếu ảnh/vị trí/mã căn hộ/thời gian      │
│   → 4. Route sang kỹ thuật/an ninh/lễ tân/kế toán            │
│   → 5. Soạn phản hồi và cập nhật trạng thái                  │
│                                                             │
│ Bước tốn/lỗi nhất? Bước 2-4 (⏱ 6-12 phút/ticket)            │
│ AI hỗ trợ ở đâu? Tự phân loại, hỏi thiếu thông tin, draft   │
│ phản hồi, đề xuất SLA và đội xử lý.                         │
│                                                             │
│ Metric có số: 85% ticket được phân loại dưới 10 giây;       │
│ giảm thời gian triage từ 8 phút xuống dưới 90 giây.         │
│                                                             │
│ Quick Architecture: [x] LLM Feature + Rule Router           │
└─────────────────────────────────────────────────────────────┘
```

**Vì sao ấn tượng:** Bài toán có dữ liệu ngôn ngữ tự nhiên, ảnh, mức độ khẩn cấp và routing đa bộ phận. AI tạo giá trị rõ nhưng vẫn kiểm soát được bằng rule/SLA.

**Caveat:** Không để AI tự kết luận tranh chấp phí/quy định pháp lý; các trường hợp tiền bạc, an ninh, PCCC, xung đột cư dân phải chuyển HITL.

---

### Card #3 — Vinschool: AI Curriculum Copilot cho giáo viên

```text
┌─────────────────────────────────────────────────────────────┐
│ QUICK PROBLEM CARD #3                                       │
│                                                             │
│ Bài toán: Vinschool triển khai chương trình AI 5-18 tuổi;   │
│ giáo viên cần cá nhân hóa hoạt động, rubric và phản hồi     │
│ theo cấp lớp nhưng không thể soạn thủ công cho mọi lớp.     │
│ Công ty thành viên: [x] Vinschool                           │
│                                                             │
│ Ai đang đau? Giáo viên; học sinh; phụ huynh; tổ chuyên môn. │
│                                                             │
│ Workflow thủ công hiện tại (5 bước):                        │
│   1. Giáo viên đọc khung chương trình AI theo cấp lớp        │
│   → 2. Tự chuyển thành bài học liên môn                      │
│   → 3. Tự viết rubric, ví dụ, bài tập và cảnh báo đạo đức    │
│   → 4. Chấm/nhận xét từng nhóm học sinh                      │
│   → 5. Viết cập nhật cho phụ huynh                           │
│                                                             │
│ Bước tốn/lỗi nhất? Bước 2-4 (⏱ 45-90 phút/lesson pack)      │
│ AI hỗ trợ ở đâu? Sinh lesson pack theo chuẩn khung năng lực, │
│ rubric, bài tập phân tầng, feedback cá nhân hóa.            │
│                                                             │
│ Metric có số: Giảm thời gian chuẩn bị lesson pack từ 60     │
│ phút xuống dưới 15 phút; 90% rubric đạt chuẩn tổ chuyên môn.│
│                                                             │
│ Quick Architecture: [x] LLM Feature + RAG curriculum guard  │
└─────────────────────────────────────────────────────────────┘
```

Bài toán khớp trực tiếp với chương trình AI toàn hệ thống, tạo năng lực “AI-native education” thay vì chỉ dạy lý thuyết. Có thể demo nhanh bằng RAG trên curriculum + generator rubric.

Không để AI chấm điểm cuối cùng hay gán nhãn năng lực/hành vi của học sinh; giáo viên duyệt toàn bộ phản hồi trước khi gửi phụ huynh.

---

## 🗳️ Đề xuất chọn bài toán Deep-Dive

Đề xuất chọn **Card #1 — VinFast / V-GREEN Smart Charging Concierge** làm bài Deep-Dive vì có đủ ba yếu tố: pain thực tế của EV, dữ liệu số hóa đã tồn tại trong VinFast App/trạm sạc, và khả năng mở rộng sang Vinhomes để tạo use case xuyên hệ sinh thái.

Lý do chưa chọn hai card còn lại: **Vinhomes Resident Ops Router** rất khả thi nhưng dễ giống bài toán ticket-routing phổ biến; nên dùng làm phương án dự phòng nếu nhóm muốn scope chắc. **Vinschool Curriculum Copilot** ấn tượng về giáo dục nhưng phụ thuộc nhiều vào dữ liệu nội bộ/curriculum chi tiết và guardrail cho học sinh, nên cần thiết kế an toàn kỹ hơn.
