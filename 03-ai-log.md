# 03 - AI Log & Reflection

## AI giúp gì

Trong buổi học này, tôi sử dụng AI như ChatGPT để hỗ trợ brainstorming ý tưởng và kiểm tra tính an toàn của prompt trong hệ thống AI dispatcher.Tôi chủ yếu dùng AI để viết nhanh system prompt, gợi ý rule validation và hỗ trợ debug logic giữa backend ASP.NET và AI service Python.

## AI sai gì

Tuy nhiên, AI đôi lúc đưa ra giải pháp quá “lý thuyết”, ví dụ đề xuất một hệ thống rule-based quá phức tạp cho việc kiểm tra quyền [DRAFT_ONLY], khiến implementation thực tế trở nên khó maintain. Có lúc AI còn trả lời thiếu điều kiện, ví dụ vẫn đề xuất trạm sạc xa dù battery ở mức nguy hiểm.

## Sửa đổi ra sao

Để sửa, tôi phải điều chỉnh prompt theo hướng cụ thể hơn, thêm các hard-rule như:

“Battery < 5% => luôn ưu tiên mobile charger”
“Không recommend station > 5km”
“Không được coi [DRAFT_ONLY] là lệnh thực thi”
