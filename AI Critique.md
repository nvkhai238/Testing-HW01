# Đánh giá công cụ AI (AI Critique)

**MSSV:** 23127060  
**Họ và tên:** Ninh Văn Khải  
**Ngày nộp:** 4/6/2026

Trong quá trình hoàn thành bài tập về nhà này, em đã hợp tác với các công cụ AI như Gemini 3 Pro và Claude Sonnet 4.6 để lên ý tưởng cho các test case và nghiên cứu các lỗi phần mềm (software defects). Mặc dù AI giúp đẩy nhanh đáng kể quá trình dự thảo ban đầu, nó lại bộc lộ những thiếu sót rõ rệt trong việc nhận thức ngữ cảnh và các trường hợp biên (edge cases) đặc thù của lĩnh vực. Ví dụ, khi tạo các test case cho máy điều hòa Toshiba, AI đã đề xuất kiểm tra chức năng "Hẹn giờ bật" (Timer On) và "gọi đến đường dây nóng bên ngoài" (trong test case của Chế độ khô - Dry Mode). AI đã không nhận ra rằng mẫu điều hòa cụ thể này không có chức năng "Hẹn giờ bật", đồng thời tự suy diễn (hallucinated) ra một test case về đường dây nóng thay vì tập trung nghiêm ngặt vào các chức năng vật lý của thiết bị. AI mắc lỗi này vì nó dựa trên kiến thức chung về các loại máy điều hòa "tiêu chuẩn" thay vì các giới hạn vật lý của mẫu máy cụ thể đang được kiểm tra.

Hơn nữa, khi được yêu cầu giải thích các lỗi phần mềm, AI thường xuyên thể hiện sự thiên vị (bias) và ảo tưởng (hallucination), chẳng hạn như tự bịa ra các quy định pháp lý không tồn tại hoặc quy kết sai lệch nguyên nhân và kết quả (ví dụ: tuyên bố rằng lỗi hệ thống POS của Target là một chiêu trò tiếp thị). Điều này xảy ra do các mô hình ngôn ngữ lớn (LLM) thường cố gắng tạo ra một câu chuyện mạch lạc ngay cả khi thiếu dữ liệu thực tế, dẫn đến những tuyên bố nghe có vẻ hợp lý nhưng hoàn toàn là bịa đặt.

Nguyên tắc cốt lõi mà em rút ra được khi làm việc với AI trong lĩnh vực QA/QC là **AI là một trợ lý đắc lực cho việc tạo nội dung, nhưng sự kiểm chứng của con người là bắt buộc để xác thực**. AI thiếu trực giác vật lý và sự gắn kết với thực tế. Với tư cách là một sinh viên học QA, em phải coi kết quả đầu ra của AI như những bản nháp thô chưa đáng tin cậy, xem xét kỹ lưỡng chúng đối chiếu với các thực tế vật lý, và áp dụng kiến thức chuyên ngành (như các nguyên lý ISTQB) để lọc bỏ các ảo tưởng cũng như tinh chỉnh các trường hợp biên.
