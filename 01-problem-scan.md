# 🔍 Phase 1 — SCAN (Cá nhân, 20 min)

| # | Subsidiary (VinFast/Xanh SM...) | Lens             | Mô tả ngắn bài toán                                                                   |
| - | ------------------------------- | ---------------- | ------------------------------------------------------------------------------------------ |
| 1 | VinMec                          | Repetitive       | Tóm tắt hồ sơ bệnh án & hội chẩn đa chuyên khoa vẫn tốn rất nhiều thời gian |
| 2 | VinMec                          | Time-consuming   | Chăm sóc hậu điều trị & follow-up bệnh nhân còn thủ công                        |
| 3 | VinBus                          | Stakeholder Pain | Điều phối xe Bus không tốt làm 1 xe thì đông người, xe còn lại thì ít       |
| 4 | VinHomes                        | AI-upgrade       | Camera an ninh phụ thuộc người giám sát, không thể theo dõi hàng trăm camera   |
| 5 | Xanh SM                         | AI-upgrade       | Tối ưu dispact xe Xanh/SM theo constrains về pin, trạm sạc thay vì chỉ vị trí.    |

---

# 🃏 Phase 2 — QUICK-ASSESS (Cá nhân, 30 min)

```


┌─────────────────────────────────────────────────────────────┐
│ QUICK PROBLEM CARD #1                                     │
│                                                             │
│ Bài toán (1 câu): Tóm tắt hồ sơ bệnh án & hội chẩn 			      │
│ Công ty thành viên: [ ] VinFast  [ ] Xanh SM  [ ] Vinhomes  │
│                     [V] Vinmec   [ ] Khác (Ghi rõ)_______   │
│                                                             │
│ Ai đang đau (Actor)? Bác sĩ, khách hàng______________________ │
│                                                             │
│ Workflow thủ công hiện tại (3-5 bước):                      │
│   1. Khách hàng được khám, chụp chiếu ──> 2. Kết quả tổng hợp ở hồ sơ ──> 3. Bác sĩ đọc hồ sơ để chuẩn đoán ──> 4. Chuấn đoán gửi về cho khách hàng                   │
│                                                             │
│ Bước nào tốn thời gian/lỗi nhất? Bác sĩ đọc hồ sơ để chuẩn đoán(⏱ 10 phút/lượt)      │
│ AI có thể nhảy vào hỗ trợ ở bước nào? Đọc hồ sơ hộ bác sĩ│
│                                                             │
│ Đo thành công bằng gì (Metric có số)? Thời gian chuẩn đoán so với bác sĩ, số bệnh chuẩn đoán đúng││
│                                                             │
│ Quick Architecture: [ ] No AI  [ ] Rule  [V] LLM  [ ] Agent │
└─────────────────────────────────────────────────────────────┘
```

┌─────────────────────────────────────────────────────────────┐
│ QUICK PROBLEM CARD #2                                     │
│                                                             │
│ Bài toán (1 câu): Camera giám sát 			      │
│ Công ty thành viên: [ ] VinFast  [ ] Xanh SM  [V] Vinhomes  │
│                     [ ] Vinmec   [ ] Khác (Ghi rõ)_______   │
│                                                             │
│ Ai đang đau (Actor)? Bảo vệ______________________ │
│                                                             │
│ Workflow thủ công hiện tại (3-5 bước):                      │
│   1. Camera thu hình ──> 2. Bảo vệ giám sát qua camera ──> 3. Nếu có điều không ổn, bảo vệ thông báo với an ninh  │               │
│                                                             │
│ Bước nào tốn thời gian/lỗi nhất?: Bảo vệ giám sát qua camera, 1 người xem hơn chục camera sẽ có thể có sai sót, bỏ lỡ sự việc│
│ AI có thể nhảy vào hỗ trợ ở bước nào? Giám sát hộ bảo vệ │
│                                                             │
│ Đo thành công bằng gì (Metric có số)? Bắt được đúng hơn bao nhiêu tính huống│
│                                                             │
│ Quick Architecture: [ ] No AI  [V] Rule  [ ] LLM  [ ] Agent │
└─────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────┐
│ QUICK PROBLEM CARD #3                                     │
│                                                             │
│ Bài toán (1 câu): Tối ưu dispact xe Xanh/SM theo constrains về pin, trạm sạc thay vì chỉ vị trí.		      │
│ Công ty thành viên: [ ] VinFast  [V] Xanh SM  [ ] Vinhomes  │
│                     [ ] Vinmec   [ ] Khác (Ghi rõ)_______   │
│                                                             │
│ Ai đang đau (Actor)? Bộ tài chính______________________ │
│                                                             │
│ Workflow thủ công hiện tại (3-5 bước):                      │
│   1. Khách hàng gửi yêu cầu xe ──> 2. Nhân viên nhìn vị trí xe nào gần nhất, pin đủ không ──> 3. Nhân viên dispact xe hợp lý nhất                 │
│                                                             │
│ Bước nào tốn thời gian/lỗi nhất? 2 (⏱ 4 phút/lượt)      │
│ AI có thể nhảy vào hỗ trợ ở bước nào? Xem xét xe phù hợp cho nhân viên│
│                                                             │
│ Đo thành công bằng gì (Metric có số)? Thời gian di chuyển tất cả các xe trong 1 giai đoạn (1 buổi, 1 ngày) có tối ưu không│
│                                                             │
│ Quick Architecture: [ ] No AI  [ V] Rule  [ ] LLM  [ ] Agent │
└─────────────────────────────────────────────────────────────┘
