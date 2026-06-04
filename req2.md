Chào bạn, tôi đã tổng hợp danh sách 20 lỗ hổng và sự cố phần mềm (Software Defects/Bugs) được công bố trong giai đoạn 2022-2026 để bạn hoàn thành Requirement 2. Như bạn đã yêu cầu, tôi đã bỏ qua phần phân tích AI Bias/Hallucination để bạn có thể tự kiểm chứng dựa trên kết quả thô.

Dưới đây là tài liệu nghiên cứu chi tiết với các nguồn dẫn đầy đủ, phân chia rõ ràng giữa 5 lỗi liên quan đến AI/LLM và 15 lỗi phần mềm/IT truyền thống.

Phần A: Lỗi phần mềm liên quan đến AI/LLM (5 Lỗi)

1. Air Canada Chatbot Hallucination (Tháng 2/2024)

Nguồn: CBS News - Air Canada chatbot costs airline, BCCRT - Moffatt v. Air Canada

Mô tả: Chatbot hỗ trợ khách hàng của Air Canada đã "ảo giác" (hallucinate) và tự bịa ra chính sách hoàn tiền vé máy bay không có thật dành cho khách hàng chịu tang.

Mức độ nghiêm trọng: Cao (Pháp lý & Danh tiếng).

Hậu quả: Khách hàng khởi kiện và Tòa án dân sự tại Canada phán quyết hãng hàng không phải chịu trách nhiệm bồi thường cho thông tin sai lệch từ chatbot. Đây là án lệ lịch sử về trách nhiệm pháp lý của doanh nghiệp đối với AI.

Giải pháp: Hãng vô hiệu hóa chatbot, bồi thường thiệt hại và phải cập nhật lại chính sách rào chắn (guardrails) cũng như các dòng cảnh báo pháp lý trên website.

2. Google Gemini Image Generation Bias (Tháng 2/2024)

Nguồn: The Guardian - 'We definitely messed up', arXiv - Agonistic Image Generation

Mô tả: Thuật toán tạo ảnh của Gemini mắc lỗi thiên vị ngược (over-correcting bias). Khi cố gắng đảm bảo tính đa dạng sắc tộc, model đã bỏ qua tính chính xác lịch sử (ví dụ: tạo ảnh người lính Đức Quốc xã hay các vị vua với các sắc tộc không chính xác).

Mức độ nghiêm trọng: Cao.

Hậu quả: Gây ra làn sóng chỉ trích mạnh mẽ trên mạng xã hội, cổ phiếu công ty sụt giảm và ban lãnh đạo Google phải lên tiếng xin lỗi công khai.

Giải pháp: Google lập tức tạm dừng tính năng tạo hình ảnh con người để tinh chỉnh lại trọng số (weights) của prompt nội bộ và tối ưu lại cơ chế can thiệp đa dạng hóa của model.

3. Lộ mã nguồn qua Samsung ChatGPT (Tháng 4/2023)

Nguồn: Datafence - Samsung ChatGPT Ban, AuthenTech AI

Mô tả: Các kỹ sư thiết kế chất bán dẫn của Samsung đã đưa mã nguồn nội bộ (source code) và file ghi âm các cuộc họp mật vào ChatGPT để tìm bug và nhờ tóm tắt nội dung.

Mức độ nghiêm trọng: Rất Cao (Bảo mật Dữ liệu cốt lõi).

Hậu quả: Dữ liệu bí mật thương mại trị giá hàng tỷ USD của bộ phận R&D bị đưa ra ngoài và lưu trữ trên server của OpenAI, có rủi ro bị dùng để train model.

Giải pháp: Samsung ban hành lệnh cấm sử dụng toàn bộ các công cụ AI tạo sinh công cộng trên thiết bị công ty và đầu tư phát triển hệ thống LLM nội bộ (Samsung Gauss) với quyền kiểm soát dữ liệu hoàn toàn.

4. NYC MyCity Chatbot cho lời khuyên phạm pháp (Tháng 3/2024)

Nguồn: The Markup - NYC AI Chatbot Tells Businesses to Break the Law

Mô tả: Chatbot AI (sử dụng công nghệ của Microsoft) do thành phố New York triển khai để tư vấn cho doanh nghiệp đã liên tục đưa ra các lời khuyên trái luật (ví dụ: khuyên chủ doanh nghiệp có quyền tịch thu tiền tip của nhân viên).

Mức độ nghiêm trọng: Cao.

Hậu quả: Gây ảnh hưởng uy tín nghiêm trọng cho chính quyền thành phố, đe dọa trực tiếp tới quyền lợi của người lao động nếu các doanh nghiệp làm theo lời chatbot.

Giải pháp: Bổ sung ngay lập tức các dòng cảnh báo "không sử dụng chatbot làm tư vấn pháp lý" và siết chặt lại bộ dữ liệu Retrieval-Augmented Generation (RAG).

5. Prompt Injection trên Chatbot Chevrolet Watsonville (Tháng 12/2023)

Nguồn: Medium - The AI hack that convinced a chatbot

Mô tả: Một người dùng đã thực hiện kỹ thuật Prompt Injection thành công, ép chatbot bán hàng của đại lý Chevrolet đồng ý bán một chiếc Chevy Tahoe đời mới với giá 1 USD và ép bot khẳng định đó là "ràng buộc pháp lý không được hoàn tác".

Mức độ nghiêm trọng: Trung bình (Thiệt hại danh tiếng là chủ yếu, không có hợp đồng thực tế).

Hậu quả: Bức ảnh chụp màn hình đạt hơn 20 triệu lượt xem, trở thành một cuộc khủng hoảng PR, cho thấy AI thiếu đi các quy tắc an toàn cơ bản (system prompts lỏng lẻo).

Giải pháp: Đại lý vô hiệu hóa hệ thống chatbot lập tức và các đơn vị cung cấp AI phải vá lại system prompt, cấm AI được quyền thay mặt đại lý xác nhận giao dịch tài chính.

Phần B: Lỗi phần mềm truyền thống (15 Lỗi) 6. Sự cố Màn hình xanh toàn cầu CrowdStrike Falcon (Tháng 7/2024)

Nguồn: CrowdStrike Root Cause Analysis

Mô tả: Bản cập nhật file cấu hình (Channel File 291) cho phần mềm Falcon Sensor chứa lỗi cấp phát bộ nhớ (out-of-bounds read). Bộ diễn dịch nội dung của Windows sập ngay lập tức khi đọc file này.

Mức độ nghiêm trọng: Cực kỳ Nghiêm trọng.

Hậu quả: Đánh sập 8.5 triệu thiết bị Windows, làm tê liệt các hãng hàng không, ngân hàng, bệnh viện và hạ tầng toàn thế giới. Thiệt hại ước tính hàng tỷ USD.

Giải pháp: Người dùng phải khởi động máy tính vào Safe Mode và xóa tệp lỗi thủ công. CrowdStrike thay đổi kiến trúc test và áp dụng quy trình phát hành từ từ (Staged rollout).

7. Lỗi Parser Hệ thống Không lưu Anh Quốc NATS (Tháng 8/2023)

Nguồn: Incident.io - UK Airspace Bug

Mô tả: Phần mềm phân tích hệ thống không lưu gặp một "edge case". Một lịch trình bay hoàn toàn hợp lệ nhưng chứa 2 mã trạm không lưu (waypoint) trùng tên ngẫu nhiên đã gây ra lỗi ngoại lệ chưa từng có, làm sập tiến trình xử lý.

Mức độ nghiêm trọng: Rất Cao.

Hậu quả: Mất khả năng xử lý bay tự động, hơn 1.500 chuyến bay bị hủy/hoãn trong kỳ nghỉ lễ tại Anh, thiệt hại lên tới hơn 100 triệu Bảng Anh.

Giải pháp: Vá lỗi xử lý logic trùng lặp (duplicates) trong parser và nâng cấp cơ chế failover (chuyển đổi dự phòng) để không khóa toàn bộ hệ thống khi một module crash.

8. Lỗi tràn dung lượng đĩa cơ sở dữ liệu Toyota (Tháng 8/2023)

Nguồn: PCMag - Toyota Stops Assembly Lines

Mô tả: Kịch bản cấu hình bảo trì định kỳ cơ sở dữ liệu đặt sai thông số, yêu cầu phân bổ không gian trống vượt quá dung lượng vật lý thực tế của đĩa cứng. Sự kiện này làm sập cả server chính lẫn backup.

Mức độ nghiêm trọng: Rất Cao.

Hậu quả: Đóng băng 14 nhà máy lắp ráp của Toyota tại Nhật Bản, buộc họ phải tạm ngưng sản xuất 13.000 xe ô tô.

Giải pháp: Di chuyển toàn bộ dữ liệu qua cụm máy chủ mới có dung lượng đĩa lớn hơn, viết lại tập lệnh (script) tự động dọn dẹp log hệ thống.

9. Hệ thống Cảnh báo Hàng không Mỹ FAA NOTAM (Tháng 1/2023)

Nguồn: FAA NOTAM Statement

Mô tả: Lỗi đồng bộ hóa phần mềm đã làm một file database cốt lõi bị hỏng (corrupt). Tệp bị lỗi vô tình được sao chép thẳng sang hệ thống dự phòng, gây sập toàn bộ mạng lưới NOTAM.

Mức độ nghiêm trọng: Rất Cao.

Hậu quả: Sự kiện lần đầu tiên kể từ 11/9 khiến mọi chuyến bay khởi hành tại Mỹ (hơn 10.000 chuyến) bị lệnh hạ cánh (Ground stop) trong nhiều giờ.

Giải pháp: Khôi phục cơ sở dữ liệu từ bản sao lưu trước đó, FAA sau đó yêu cầu Quốc hội cấp vốn khẩn cấp để thiết kế lại hoàn toàn cấu trúc IT cũ kỹ của mình.

10. Meltdown phần mềm xếp lịch Southwest Airlines (Tháng 12/2022)

Nguồn: CNN - Southwest Airlines operational meltdown

Mô tả: Hệ thống phần mềm xếp lịch tự động cũ kỹ "SkySolver" không được lập trình để xử lý lượng hủy chuyến khổng lồ do bão mùa đông, dẫn đến tắc nghẽn dữ liệu (bottleneck) và sập mạng.

Mức độ nghiêm trọng: Cao.

Hậu quả: Hơn 16.000 chuyến bay bị hủy trong dịp lễ, hành lý thất lạc khắp nơi, thiệt hại khoảng 800 triệu USD.

Giải pháp: Nâng cấp khẩn cấp mô-đun phần mềm lõi và cam kết chi 1,3 tỷ USD để đại tu nền tảng IT.

11. Lỗ hổng API của Hãng viễn thông Optus (Tháng 9/2022)

Nguồn: Reuters - Optus data breach

Mô tả: Optus đã để mở một endpoint API dạng RESTful mà không có bất kỳ cơ chế xác thực nào (unauthenticated), cho phép hacker tạo tập lệnh truy vấn hàng loạt dữ liệu dễ dàng.

Mức độ nghiêm trọng: Nghiêm trọng.

Hậu quả: Lộ lọt dữ liệu cá nhân của 9.8 triệu công dân Úc (passport, bằng lái xe). Công ty phải chi trả hàng chục triệu đô để cấp lại giấy tờ cho nạn nhân.

Giải pháp: Đóng API vĩnh viễn, thuê đơn vị kiểm toán bảo mật độc lập và thay đổi toàn bộ vòng đời phát triển phần mềm an toàn (SSDLC).

12. Đợt tắt mạng di động AT&T do lỗi Script (Tháng 2/2024)

Nguồn: CNN - AT&T Outage Software Error

Mô tả: Lỗi cấu hình phần mềm xảy ra trong một quy trình thực thi sai (incorrect process execution) khi mở rộng hạ tầng mạng, làm gián đoạn bảng định tuyến của hệ thống lõi.

Mức độ nghiêm trọng: Cao.

Hậu quả: Hàng triệu khách hàng tại Mỹ mất hoàn toàn sóng điện thoại và không thể gọi các dịch vụ khẩn cấp 911 trong nhiều giờ.

Giải pháp: Khôi phục về (Rollback) bản cấu hình phần mềm trước đó, hãng viễn thông đền bù 5 USD/khách hàng ảnh hưởng.

13. Lỗi cấu hình hệ thống POS toàn cầu của McDonald's (Tháng 3/2024)

Nguồn: BBC - McDonald's global IT outage

Mô tả: Một bản cập nhật cấu hình phần mềm bị lỗi do nhà cung cấp bên thứ 3 đẩy xuống đã làm hỏng tính năng đồng bộ giao dịch.

Mức độ nghiêm trọng: Cao.

Hậu quả: Các cửa hàng trên toàn thế giới (Anh, Nhật Bản, Úc, New Zealand...) không thể nhận đơn hàng qua máy tự phục vụ (Kiosks), ứng dụng di động hay tại quầy.

Giải pháp: Tạm ngừng nhận cập nhật từ bên thứ ba, cấu hình lại máy POS cục bộ và tái khởi động toàn hệ thống.

14. Lỗ hổng Change Healthcare API thiếu MFA (Tháng 2/2024)

Nguồn: Wired - Change Healthcare Ransomware Attack

Mô tả: Hệ thống portal công nghệ cũ không được cấu hình bắt buộc Xác thực hai bước (MFA), cho phép phần mềm tống tiền ALPHV/BlackCat đột nhập qua thông tin đăng nhập rò rỉ.

Mức độ nghiêm trọng: Cực kỳ Nghiêm trọng.

Hậu quả: Hệ thống xử lý bảo hiểm y tế và thanh toán lớn nhất nước Mỹ tê liệt, hàng chục ngàn nhà thuốc và bệnh viện không thể thanh toán viện phí trong hàng tuần liền.

Giải pháp: Xây dựng lại hệ thống mới hoàn toàn sạch, bắt buộc chuẩn FIDO2/MFA cho bất kỳ phần mềm truy cập nào.

15. Hacker đánh cắp Mã nguồn (Source Code) của AnyDesk (Tháng 1/2024)

Nguồn: BleepingComputer - AnyDesk hack

Mô tả: Lỗi quản lý quyền truy cập hệ thống (Access Control Bug) cho phép hacker đánh cắp kho lưu trữ mã nguồn và chứng chỉ ký phần mềm (code signing certificates) của AnyDesk.

Mức độ nghiêm trọng: Nghiêm trọng.

Hậu quả: Dấy lên nguy cơ khủng khiếp về việc hacker có thể đính kèm mã độc vào các bản cập nhật phần mềm AnyDesk tương lai.

Giải pháp: Thu hồi mọi chứng chỉ kỹ thuật số cũ, buộc mọi người dùng trên thế giới tải và xác thực phần mềm bằng chứng chỉ mới, đồng thời ép toàn bộ tài khoản đặt lại mật khẩu.

16. Lỗi Firmware ICM của Honda Accord Hybrid (Triệu hồi 2025)

Nguồn: NHTSA / Honda Recall Service

Mô tả: Code xử lý trong Mô-đun Điều khiển Tích hợp (ICM) hiểu sai các luồng dữ liệu liên lạc nội bộ thông thường là "lỗi kỹ thuật", kích hoạt chế độ tự khởi động lại phần mềm khi xe đang chạy.

Mức độ nghiêm trọng: Cao (Rủi ro tính mạng).

Hậu quả: Hệ thống Hybrid bị tắt tạm thời dẫn đến mất lực kéo đột ngột hoặc giảm tốc không báo trước, gây nguy cơ tai nạn nghiêm trọng.

Giải pháp: Triệu hồi hàng trăm ngàn xe sản xuất từ 2023-2025 để nạp lại bản Firmware phần mềm sửa lỗi miễn phí tại đại lý.

17. Bug chuyển đổi dự phòng (Failover) hệ thống làm mát DBS Bank (Tháng 10/2023)

Nguồn: CNA - DBS banking disruption

Mô tả: Phần mềm giám sát nhiệt độ của Equinix (trung tâm dữ liệu của DBS) gặp lỗi logic khi xử lý tiến trình ngắt mạng, khiến các tín hiệu Failover (chuyển đổi máy chủ dự phòng) không kích hoạt chính xác.

Mức độ nghiêm trọng: Cao.

Hậu quả: Ngân hàng số lớn nhất Đông Nam Á bị sập hoàn toàn ATM, thẻ tín dụng và ứng dụng ngân hàng suốt một ngày. DBS bị cơ quan quản lý nhà nước phạt giới hạn kinh doanh trong 6 tháng.

Giải pháp: Chuyển đổi định tuyến dữ liệu thủ công, cập nhật mã nguồn phần mềm để khắc phục nút thắt cổ chai tín hiệu báo động nhiệt độ.

18. Lỗ hổng mạng VPN Viasat KA-SAT (Tháng 2/2022)

Nguồn: Reuters - Viasat satellite hack

Mô tả: Lỗ hổng cấu hình trong phần mềm quản lý VPN của Viasat. Hacker xâm nhập mạng quản lý và đẩy một phần mềm độc hại (AcidRain) xuống để xóa sạch (wipe) bộ nhớ flash của mọi modem.

Mức độ nghiêm trọng: Rất Cao.

Hậu quả: Hàng chục ngàn modem vệ tinh tại Châu Âu (bao gồm mạng lưới chỉ huy quân đội Ukraine và 5.800 tuabin gió ở Đức) biến thành cục gạch.

Giải pháp: Vì modem đã mất hệ điều hành cốt lõi và không thể nâng cấp Firmware OTA, Viasat bắt buộc phải giao hàng chục ngàn modem mới tinh (phần cứng vật lý) đến từng khách hàng.

19. Lỗ hổng mạng ảo Nissan Australia (Tháng 12/2023)

Nguồn: ABC News - Nissan data breach

Mô tả: Thiết lập phần mềm VPN từ xa chưa được vá lỗ hổng Zero-day, cho phép nhóm tin tặc Akira truy cập và mã hóa các hệ thống mạng quan trọng.

Mức độ nghiêm trọng: Cao.

Hậu quả: 100.000 khách hàng tại Úc và New Zealand bị rò rỉ dữ liệu cá nhân, một số hệ thống hoạt động bị khóa chặt.

Giải pháp: Ngắt toàn bộ hệ thống ngoại vi, xây dựng lại tường lửa bảo mật, báo cáo lên cơ quan không gian mạng Úc.

20. Phần mềm Quản trị dữ liệu British Library thiếu bảo vệ (Tháng 10/2023)

Nguồn: British Library Cyber Incident Report

Mô tả: Hệ thống phần mềm quản lý kho lưu trữ dữ liệu cũ (legacy system) của Thư viện Anh không hỗ trợ mã hóa bảo mật hiện đại và xác thực đa luồng, bị hacker Rhysida đột nhập phá hoại hoàn toàn cấu trúc dữ liệu.

Mức độ nghiêm trọng: Cao.

Hậu quả: Thư viện bị mất hàng loạt mục lục trực tuyến lịch sử quý giá, website và mạng nội bộ sập suốt nhiều tháng. Ước tính chi phí xây dựng lại mạng lưới lên tới 7 triệu Bảng.

Giải pháp: Loại bỏ hoàn toàn hệ thống phần mềm cũ, xây dựng hệ thống quản lý dữ liệu đám mây (Cloud) hoàn toàn mới dưới các tiêu chuẩn an toàn hiện đại.

Hy vọng danh sách này đã cung cấp đầy đủ dữ kiện, đường link tin cậy và cấu trúc rõ ràng để bạn có thể hoàn thành xuất sắc yêu cầu của môn học QA/QC. Chúc bạn phân tích các lỗi AI (Bias/Hallucination) thành công nhé!
