Chào bạn, dưới đây là bộ 15 test cases được thiết kế dành cho thiết bị máy lạnh Toshiba (dàn lạnh model RAS-H10Z2KCVG-V) dựa trên thông tin từ tem nhãn bạn đã cung cấp.

Vì mình là AI nên không thể thao tác vật lý để quay video hay trực tiếp tìm ra 5 defects (lỗi) trên thiết bị của bạn. Tuy nhiên, mình đã thiết kế sẵn format chuẩn, tập trung vào các chức năng thực tế của máy lạnh và các thông tin trên tem. Bạn có thể dùng bảng này làm tài liệu, chọn ra ít nhất 5 cases để tự thực thi (execute), quay video, và ghi nhận kết quả vào cột **Actual** và **Verdict** nhé.

### Test Specification: Toshiba Air Conditioner (RAS-H10Z2KCVG-V)

| ID       | Objective                                     | Input                                     | Steps                                 | Expected Result | Actual Result | Verdict |
| -------- | --------------------------------------------- | ----------------------------------------- | ------------------------------------- | --------------- | ------------- | ------- |
| **TC01** | Kiểm tra chức năng Bật/Tắt nguồn bằng Remote. | Remote có pin, máy lạnh đã được cấp điện. | 1. Hướng remote về phía dàn lạnh.<br> |

<br>2. Nhấn nút Nguồn (Power). | Dàn lạnh phát tiếng "bíp", cánh đảo gió mở ra, đèn LED sáng và quạt bắt đầu thổi gió. | _(Điền khi test thực tế)_ | _(Pass/Fail)_ |
| **TC02** | Kiểm tra chế độ làm lạnh (Cool Mode). | Remote ở chế độ Cool. | 1. Bật máy.<br>

<br>2. Chọn Mode: Cool.<br>

<br>3. Chỉnh nhiệt độ xuống 18°C. | Sau khoảng 3-5 phút, block ngoài trời hoạt động, dàn lạnh thổi ra hơi lạnh rõ rệt. | | |
| **TC03** | Kiểm tra chức năng thay đổi nhiệt độ. | Máy đang ở chế độ Cool. | 1. Nhấn nút Temp [^] lên 30°C.<br>

<br>2. Nhấn nút Temp [v] xuống 18°C. | Nhiệt độ trên remote (và màn hình LED dàn lạnh nếu có) phản hồi đúng số vừa chỉnh. | | |
| **TC04** | Kiểm tra các cấp độ quạt gió (Fan Speed). | Máy đang chạy, Mode: Cool/Fan. | 1. Nhấn nút Fan Speed lần lượt: Low, Med, High, Auto. | Tốc độ và tiếng ồn của luồng gió thay đổi tương ứng theo từng cấp độ được chọn. | | |
| **TC05** | Kiểm tra chức năng cánh đảo gió (Swing). | Máy đang chạy. | 1. Nhấn nút Swing (Lên/Xuống).<br>

<br>2. Nhấn lại để dừng cánh đảo gió. | Cánh đảo gió di chuyển mượt mà lên/xuống. Khi nhấn dừng, cánh đứng yên tại vị trí hiện tại. | | |
| **TC06** | Kiểm tra quét mã QR Bảo hành điện tử trên tem. | Smartphone có kết nối Internet, ứng dụng Camera. | 1. Mở camera điện thoại.<br>

<br>2. Quét mã QR nằm ở góc phải dưới của tem dàn lạnh. | Trình duyệt mở ra đúng trang web bảo hành chính hãng của Toshiba. | | |
| **TC07** | Kiểm tra kết nối Hotline trên tem (18001529). | Điện thoại di động có sóng. | 1. Bấm số 18001529.<br>

<br>2. Nhấn phím gọi. | Kết nối thành công đến tổng đài CSKH Toshiba và không bị tính cước phí (Điện thoại miễn phí). | | |
| **TC08** | Kiểm tra chế độ Hút ẩm (Dry Mode). | Máy đang chạy. | 1. Nhấn nút Mode chuyển sang Dry. | Quạt chạy ở tốc độ thấp, hơi lạnh tỏa ra nhẹ nhàng, độ ẩm trong phòng giảm dần. | | |
| **TC09** | Kiểm tra chế độ Quạt (Fan Only). | Máy đang chạy. | 1. Nhấn nút Mode chuyển sang Fan. | Dàn lạnh chỉ thổi gió, không phả ra hơi lạnh (dàn nóng không hoạt động). | | |
| **TC10** | Kiểm tra chức năng Hẹn giờ tắt máy (Timer Off). | Máy đang hoạt động. | 1. Nhấn nút Timer Off.<br>

<br>2. Cài đặt thời gian tắt là 0.5 giờ (30 phút). | Đèn báo hẹn giờ sáng. Máy tự động tắt hoàn toàn sau đúng 30 phút. | | |
| **TC11** | Kiểm tra chức năng Hẹn giờ bật máy (Timer On). | Máy đang ở trạng thái Tắt (nhưng có điện). | 1. Nhấn nút Timer On.<br>

<br>2. Cài đặt thời gian bật là 0.5 giờ (30 phút). | Đèn báo hẹn giờ sáng. Máy tự động bật và làm mát sau đúng 30 phút. | | |
| **TC12** | Kiểm tra chức năng Làm lạnh nhanh (Hi-Power / Turbo). | Máy đang chạy. | 1. Nhấn nút Hi-Power / Turbo trên remote. | Quạt gió lập tức chuyển lên mức công suất tối đa, tiếng ồn lớn nhất để làm lạnh phòng nhanh. | | |
| **TC13** | Kiểm tra khả năng tự khởi động lại khi cúp điện (Auto-Restart). | Máy đang chạy ở chế độ Cool, 25°C. | 1. Rút phích cắm điện (hoặc sập CB) đột ngột.<br>

<br>2. Đợi 1 phút, cắm điện lại (mở CB). | Máy tự động bật lại, giữ nguyên trạng thái Cool và mức nhiệt độ 25°C trước khi mất điện. | | |
| **TC14** | Kiểm tra độ phản hồi của Remote khi bị che khuất. | Remote, vật cản (cuốn tập/bàn tay). | 1. Lấy tay che kín mắt hồng ngoại của remote.<br>

<br>2. Nhấn nút thay đổi nhiệt độ. | Máy lạnh không nhận tín hiệu, không phát tiếng "bíp" (test xử lý ngoại lệ). | | |
| **TC15** | Kiểm tra cơ chế tháo lắp lưới lọc bụi. | Dàn lạnh RAS-H10Z2KCVG-V đang tắt. | 1. Dùng tay nhấc nắp mặt nạ phía trước dàn lạnh.<br>

<br>2. Rút 2 tấm lưới lọc bụi ra.<br>

<br>3. Lắp lại vào ngàm. | Mặt nạ mở dễ dàng không bị kẹt. Lưới lọc rút ra và gắn vào khớp mượt mà, không lỏng lẻo. | | |

**Mẹo để tìm Defects (Lỗi) trong quá trình quay video:**

- **UI/Hardware Defects:** Kiểm tra xem cánh đảo gió có phát ra tiếng kêu "cót két" khi quay không (rất hay gặp ở máy dùng lâu). Ngàm nắp nhựa của lưới lọc (TC15) có bị lỏng hoặc khó khép kín không.
- **Functional Defects:** Thử bấm remote liên tục và nhanh xem dàn lạnh có bị "miss" tín hiệu không. Hoặc quét mã QR (TC06) xem link có bị lỗi 404 (do hãng đổi đường dẫn) hay không.
