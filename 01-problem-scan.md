# 01 Problem Scan — Lab 02: AI Product Scoping

**Student:** Nguyễn Anh Kiệt  
**Scope:** Vin Smart Future — AI opportunity scan across Vingroup subsidiaries

---

# Phase 1 — SCAN

## 4 Lenses

1. **Lặp lại (Repetitive):** Tác vụ lặp đi lặp lại nhiều lần hằng ngày.
2. **Tốn thời gian (Time-consuming):** Tác vụ ngốn thời gian xử lý thủ công của nhân viên.
3. **AI có thể tốt hơn (AI-upgrade):** Dịch vụ hiện tại chậm, rập khuôn hoặc thiếu cá nhân hóa.
4. **Pain từ người khác (Stakeholder Pain):** Bottleneck khiến khách hàng, nhân viên hoặc đối tác phàn nàn.

## List bài toán của tôi

| # | Subsidiary | Lens | Mô tả ngắn bài toán |
|---|------------|------|---------------------|
| 1 | Xanh SM | Tốn thời gian | Điều phối viên xử lý thủ công các ca tài xế xe điện báo pin yếu giữa chuyến: tra vị trí xe, tra trạm sạc, kiểm tra khoảng cách an toàn và soạn hướng dẫn cho tài xế. |
| 2 | Vinhomes | AI-upgrade | Nhân viên CSKH mất nhiều thời gian đọc, phân loại và chuyển tuyến phản ánh cư dân trên app như thang máy hỏng, tiếng ồn, an ninh, vệ sinh, phí dịch vụ. |
| 3 | VinFast | Lặp lại | Đội vận hành phải đối chiếu hóa đơn sạc điện, log trạm sạc và lịch sử xe thủ công để phát hiện sai lệch chi phí hoặc giao dịch bất thường. |
| 4 | Vinmec | Tốn thời gian | Bác sĩ mất 20-30 phút/bệnh nhân để viết tóm tắt xuất viện, hướng dẫn uống thuốc, lịch tái khám và dấu hiệu cần quay lại bệnh viện. |
| 5 | Vinpearl / VinWonders | Stakeholder Pain | Nhân viên chăm sóc khách hàng phải trả lời lặp lại câu hỏi về vé, giờ mở cửa, lịch show, chính sách hoàn/hủy và ưu đãi, làm khách chờ lâu vào mùa cao điểm. |

---

# 🃏 Phase 2 — QUICK-ASSESS

Tôi chọn 3 bài toán tiềm năng nhất để đánh giá nhanh:

1. **Xanh SM:** Xử lý tài xế báo pin yếu giữa chuyến.
2. **Vinhomes:** Phân loại và chuyển tuyến phản ánh cư dân.
3. **Vinmec:** Soạn tóm tắt xuất viện và hướng dẫn chăm sóc sau điều trị.

---

## Quick Problem Card #1 — Xanh SM Low-Battery Dispatcher

**Bài toán (1 câu):** Điều phối viên Xanh SM xử lý chậm các ca tài xế báo pin yếu hoặc gần hết pin giữa chuyến.

**Công ty thành viên:** [ ] VinFast  [x] Xanh SM  [ ] Vinhomes  [ ] Vinmec  [ ] Khác

**Actor / Operator đang đau:** Tài xế Xanh SM, điều phối viên trung tâm vận hành, khách hàng đang chờ chuyến.

**Workflow thủ công hiện tại:**

1. Tài xế gọi hoặc nhắn tổng đài báo mức pin thấp và vị trí hiện tại.
2. Điều phối viên mở bản đồ nội bộ để xác định vị trí xe.
3. Điều phối viên tra thủ công trạm sạc VinFast gần nhất và tình trạng trụ sạc.
4. Điều phối viên soạn tin nhắn hướng dẫn tài xế đi tới trạm sạc hoặc gọi đội hỗ trợ.
5. Nếu pin quá thấp, điều phối viên chuyển ca sang đội cứu hộ hoặc xe sạc di động.

**Bước tốn thời gian/lỗi nhất:** Bước 3-4, khoảng **10-12 phút/lượt**. Lỗi thường gặp là chọn trạm quá xa so với mức pin hoặc soạn hướng dẫn thiếu rõ ràng trong tình huống gấp.

**AI có thể hỗ trợ ở bước nào:** Bước 3-4. AI nhận đầu vào gồm vị trí xe, mức pin, khoảng cách trạm sạc và tình trạng trụ sạc, sau đó tạo bản nháp hướng dẫn an toàn cho điều phối viên duyệt.

**Metric thành công có số:** Giảm thời gian xử lý từ **15 phút/lượt xuống dưới 3 phút/lượt**; ít nhất **95%** hướng dẫn tuân thủ ranh giới an toàn, ví dụ pin dưới 5% không được đề xuất trạm xa hơn 5km.

**Quick Architecture:** [ ] No AI  [ ] Rule  [x] LLM  [ ] Agent

**Lý do chọn kiến trúc:** LLM phù hợp vì cần tạo hướng dẫn ngôn ngữ tự nhiên cho tài xế, nhưng vẫn phải có rule cứng và human-in-the-loop để kiểm soát an toàn.

---

## Quick Problem Card #2 — Vinhomes Resident Ticket Router

**Bài toán (1 câu):** Vinhomes CSKH phân loại và chuyển tuyến phản ánh cư dân còn chậm, dễ gửi sai bộ phận xử lý.

**Công ty thành viên:** [ ] VinFast  [ ] Xanh SM  [x] Vinhomes  [ ] Vinmec  [ ] Khác

**Actor / Operator đang đau:** Cư dân, nhân viên CSKH, đội vận hành tòa nhà như kỹ thuật, an ninh, vệ sinh, ban quản lý.

**Workflow thủ công hiện tại:**

1. Cư dân gửi phản ánh trên app hoặc hotline.
2. Nhân viên CSKH đọc nội dung, ảnh đính kèm và lịch sử phản ánh.
3. Nhân viên xác định loại vấn đề: kỹ thuật, vệ sinh, an ninh, phí, tiện ích hoặc khiếu nại.
4. Nhân viên tạo ticket, chọn mức ưu tiên và chuyển sang đội phụ trách.
5. Đội vận hành phản hồi tình trạng xử lý; CSKH cập nhật lại cho cư dân.

**Bước tốn thời gian/lỗi nhất:** Bước 2-4, khoảng **8-10 phút/ticket**. Với phản ánh dài hoặc giọng điệu bức xúc, nhân viên dễ bỏ sót thông tin hoặc chọn sai nhóm xử lý.

**AI có thể hỗ trợ ở bước nào:** Bước 2-4. AI tóm tắt phản ánh, phân loại ticket, gợi ý mức độ ưu tiên, phát hiện sentiment tiêu cực và draft phản hồi ban đầu.

**Metric thành công có số:** **85%** ticket được phân loại trong dưới **30 giây**; giảm tỷ lệ chuyển sai bộ phận từ **12% xuống dưới 4%**; giảm thời gian phản hồi đầu tiên từ **2 giờ xuống dưới 15 phút**.

**Quick Architecture:** [ ] No AI  [ ] Rule  [x] LLM  [ ] Agent

**Lý do chọn kiến trúc:** LLM tốt cho phân loại nội dung tự nhiên và tóm tắt phản ánh. Tuy nhiên, bước gán đội xử lý cuối cùng nên dùng rule mapping và cho CSKH duyệt để tránh sai quy trình.

---

## Quick Problem Card #3 — Vinmec Discharge Summary Assistant

**Bài toán (1 câu):** Vinmec mất nhiều thời gian soạn tóm tắt xuất viện và hướng dẫn chăm sóc sau điều trị cho bệnh nhân.

**Công ty thành viên:** [ ] VinFast  [ ] Xanh SM  [ ] Vinhomes  [x] Vinmec  [ ] Khác

**Actor / Operator đang đau:** Bác sĩ điều trị, điều dưỡng, bệnh nhân và người nhà bệnh nhân.

**Workflow thủ công hiện tại:**

1. Bác sĩ đọc lại hồ sơ bệnh án, kết quả xét nghiệm, chẩn đoán, thuốc đã dùng và diễn biến điều trị.
2. Bác sĩ viết tóm tắt quá trình điều trị.
3. Bác sĩ soạn hướng dẫn uống thuốc, tái khám, ăn uống, vận động và dấu hiệu nguy hiểm.
4. Điều dưỡng in giấy tờ và giải thích lại cho bệnh nhân.
5. Bệnh nhân hoặc người nhà hỏi thêm nếu nội dung khó hiểu.

**Bước tốn thời gian/lỗi nhất:** Bước 2-3, khoảng **20-30 phút/bệnh nhân**. Nội dung dễ bị quá chuyên môn, thiếu phần giải thích dễ hiểu cho bệnh nhân.

**AI có thể hỗ trợ ở bước nào:** Bước 2-3. AI tạo bản nháp tóm tắt xuất viện và hướng dẫn chăm sóc bằng ngôn ngữ rõ ràng, sau đó bác sĩ bắt buộc kiểm tra, chỉnh sửa và ký duyệt.

**Metric thành công có số:** Giảm thời gian soạn hồ sơ từ **25 phút xuống 8 phút/bệnh nhân**; **100%** bản nháp phải có bác sĩ duyệt trước khi gửi; ít nhất **90%** bệnh nhân đánh giá hướng dẫn dễ hiểu.

**Quick Architecture:** [ ] No AI  [ ] Rule  [x] LLM  [ ] Agent

**Lý do chọn kiến trúc:** LLM phù hợp để tóm tắt và chuyển đổi ngôn ngữ chuyên môn sang hướng dẫn dễ hiểu. Không chọn Agent vì rủi ro y tế cao, AI không được tự quyết định chẩn đoán hoặc phác đồ.

---

# Quyết định ưu tiên

Tôi chọn **Quick Problem Card #1 — Xanh SM Low-Battery Dispatcher** để đi tiếp vào prototype.

**Lý do chọn:**

1. Workflow hiện tại rõ ràng, có đầu vào/đầu ra dễ mô phỏng trong prototype.
2. Metric đo được: thời gian xử lý, khoảng cách trạm sạc, mức pin, tỷ lệ cần dispatcher duyệt.
3. Rủi ro an toàn có thể đặt thành ranh giới vận hành cụ thể: nếu pin dưới 5%, không đề xuất trạm sạc xa hơn 5km và phải gọi xe sạc di động.
4. Bài toán phù hợp với file `starter-code/prompt_prototype.py`, vì prototype đang kiểm tra hai boundary quan trọng: tag `[DRAFT_ONLY]` và xử lý pin dưới 5%.

**Kết luận cá nhân:** Đây là bài toán nên được thử nghiệm ở mức prototype hẹp trước. AI chỉ nên đóng vai trò co-pilot tạo bản nháp và đề xuất hành động, không được tự gửi tin nhắn hoặc tự điều phối cứu hộ nếu chưa có con người duyệt.
