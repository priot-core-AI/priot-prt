# P.riot Prt 1.0.0

Ứng dụng chụp và chỉnh sửa ảnh màn hình cho Windows.

## Tải Và Chạy

1. Tải `P.riot.Prt-1.0.0-win-portable.zip` tại [GitHub Releases](https://github.com/priot-core-AI/priot-prt/releases/latest).
2. Giải nén toàn bộ ZIP vào thư mục có quyền ghi, chẳng hạn thư mục trong Documents. Không chạy trực tiếp bên trong ZIP.
3. Mở `P.riot Prt.exe`. Giữ `screenshot-app-icon.png` cùng thư mục với chương trình.

Yêu cầu Windows có .NET Framework 4.5 trở lên; khuyến nghị .NET Framework 4.8. Bản portable không cần trình cài đặt. Chương trình chưa được ký số nên Windows có thể hiện cảnh báo nhà phát hành không xác định.

## Chức Năng

- Chụp vùng hoặc toàn màn hình, điều chỉnh vùng bằng các điểm neo.
- Phiên chụp nhiều ảnh trong thư mục có tên riêng.
- Xem ảnh với các nút Lưu, Copy, Sửa và Gửi AI.
- Thêm chữ, ghi chú, bút vẽ, đánh dấu, mũi tên, khung và hình elip.
- Chọn đối tượng để di chuyển, chỉnh thuộc tính hoặc xóa. Mũi tên có thể kéo hai đầu để đổi hướng và độ dài.
- Thanh thuộc tính chỉ hiện khi chọn đối tượng; hỗ trợ hoàn tác và làm lại.
- Gửi AI tạo ảnh PNG gồm ảnh chụp và vùng prompt tiếng Việt phía dưới, để lưu hoặc copy sang dịch vụ AI. Không gửi dữ liệu ZIP thô.
- Tích hợp Gemini bằng API key của người dùng để hỏi về ảnh hoặc soạn prompt.
- Cài đặt phím gọi ứng dụng, khởi động cùng Windows, thư mục lưu và thời gian thông báo; mặc định 4 giây.

## Phím Tắt

| Phím | Thao tác |
| --- | --- |
| Ctrl+Shift+PrintScreen | Gọi chụp vùng, có thể đổi trong cài đặt |
| Ctrl+S | Lưu ảnh PNG |
| Ctrl+C | Copy ảnh |
| Ctrl+Shift+A | Tạo ảnh kèm prompt cho AI |
| Enter | Vào chỉnh sửa nâng cao từ màn hình xem ảnh; sửa nội dung chữ đang chọn khi vùng ảnh có tiêu điểm |
| Delete | Xóa đối tượng đang chọn |
| Ctrl+Z / Ctrl+Y | Hoàn tác / làm lại |
| Ctrl+B / Ctrl+I | Đậm / nghiêng chữ đang chọn khi vùng ảnh có tiêu điểm |
| Escape | Bỏ chọn đối tượng; nếu không còn đối tượng được chọn thì về xem ảnh; hủy khi đang chọn vùng chụp |

## Lưu Trữ Và Riêng Tư

Ảnh mặc định nằm trong thư mục `Captures` cạnh chương trình. Cài đặt nằm ở `%LOCALAPPDATA%\P.riot Prt\settings.json`. API key Gemini được mã hóa bằng Windows DPAPI cho tài khoản Windows hiện tại, không nằm trong bản phát hành.

Ảnh chỉ được gửi tới Google khi bạn dùng chức năng Hỏi AI. Chức năng AI viết prompt gửi mô tả bạn nhập. Việc tạo ảnh kèm prompt không tự tải ảnh lên dịch vụ AI.

Đóng cửa sổ sẽ thu ứng dụng xuống khay hệ thống. Để tắt hoàn toàn, chọn Thoát trong menu biểu tượng ở khay hệ thống.

## Cập Nhật

Vào Cài đặt → Cập nhật. Kho mặc định là `priot-core-AI/priot-prt`. Nút Kiểm tra cập nhật mở trang tải nếu có bản mới; chương trình chưa tự tải và cài đặt cập nhật.

Khi thay bản mới, thoát chương trình, thay các tệp ứng dụng và giữ thư mục `Captures`. Cài đặt trong LocalAppData được giữ nguyên.

PNG lưu ra là ảnh đã ghép; mở lại PNG không khôi phục các đối tượng chỉnh sửa. Chỉ chạy một phiên ứng dụng để tránh tranh chấp phím tắt toàn hệ thống.

Kho này phân phối bản chạy và hướng dẫn. Mã nguồn không được công khai trong bản phát hành này.

