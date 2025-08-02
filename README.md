Hướng Dẫn Sử Dụng Karaoke Player trên GitHub
Chào mừng bạn đến với Karaoke Player, một trình phát nhạc karaoke với hiệu ứng lời bài hát (lyrics) đồng bộ và giao diện thân thiện! Dự án này được thiết kế để chạy trên trình duyệt, hỗ trợ phát nhạc, hiển thị lời bài hát theo thời gian thực và cung cấp các tính năng điều khiển như phát/tạm dừng, chuyển bài, lặp lại, ngẫu nhiên, và điều chỉnh âm lượng. Dưới đây là hướng dẫn chi tiết để triển khai và sử dụng dự án trên GitHub.

1. Tổng Quan Dự Án
Karaoke Player là một ứng dụng web sử dụng HTML, CSS và JavaScript để:

Phát nhạc MP3 từ danh sách bài hát được định nghĩa sẵn.
Hiển thị lời bài hát (định dạng .lrc) với hiệu ứng highlight từng ký tự theo thời gian thực.
Cung cấp giao diện đẹp mắt với hình nền mờ (blur) dựa trên ảnh bìa bài hát.
Hỗ trợ các tính năng như phát ngẫu nhiên, lặp bài, điều chỉnh âm lượng, và tải bài hát về.


2. Yêu Cầu

Trình duyệt web: Chrome, Firefox, Edge, hoặc bất kỳ trình duyệt hiện đại nào.
Môi trường lưu trữ: Bạn có thể chạy trực tiếp trên máy cục bộ hoặc triển khai trên GitHub Pages.
File âm thanh và lời bài hát: Đảm bảo các liên kết đến file MP3 và file .lrc trong danh sách audioList (trong mã JavaScript) hoạt động. Các file này cần được lưu trữ trên một máy chủ có hỗ trợ CORS (như Dropbox, Google Drive, hoặc Archive.org).


3. Cài Đặt và Triển Khai trên GitHub
Bước 1: Tạo Repository trên GitHub

Đăng nhập vào tài khoản GitHub của bạn.
Tạo một repository mới (ví dụ: karaoke-player).
Tải mã nguồn từ đoạn code HTML đã cung cấp và lưu vào tệp index.html.

Bước 2: Tải Mã Nguồn Lên Repository

Tạo tệp index.html trong repository của bạn và sao chép toàn bộ mã HTML/CSS/JavaScript từ đoạn code đã cung cấp.
Commit và push tệp lên repository:
bashgit add index.html
git commit -m "Thêm Karaoke Player"
git push origin main


Bước 3: Kích Hoạt GitHub Pages

Vào Settings của repository.
Cuộn xuống phần Pages trong mục Code and automation.
Trong mục Branch, chọn nhánh main (hoặc nhánh chứa index.html) và thư mục gốc (/root).
Nhấn Save. GitHub sẽ cung cấp một URL (ví dụ: https://username.github.io/karaoke-player).
Truy cập URL này để xem trình phát karaoke chạy trên trình duyệt.

Bước 4: Tùy Chỉnh Danh Sách Bài Hát (Tùy Chọn)

Mở tệp index.html và tìm phần audioList trong đoạn mã JavaScript:
javascriptconst audioList = [
  {
    name: 'Tên Bài Hát',
    artist: 'Tên Nghệ Sĩ',
    url: 'URL_đến_file_MP3',
    cover: 'URL_đến_ảnh_bìa',
    lrc: 'URL_đến_file_LRC'
  },
  // Thêm các bài hát khác
];

Thay đổi các giá trị name, artist, url, cover, và lrc để thêm bài hát mới. Đảm bảo:

File MP3 và .lrc được lưu trữ ở nơi hỗ trợ truy cập trực tiếp (như Dropbox hoặc Archive.org).
File .lrc có định dạng chuẩn (ví dụ: [mm:ss.ss] Lời bài hát).


Commit và push lại để cập nhật.


4. Cách Sử Dụng Karaoke Player
Sau khi triển khai, truy cập URL của GitHub Pages để sử dụng trình phát. Dưới đây là các tính năng và cách sử dụng:
Giao Diện Chính

Ảnh bìa và thông tin bài hát: Hiển thị ở góc trên bên trái, bao gồm ảnh bìa, tên bài hát, và tên nghệ sĩ.
Lời bài hát: Hiển thị ở trung tâm với hiệu ứng highlight từng ký tự theo thời gian thực.
Thanh tiến trình: Cho biết thời gian hiện tại và tổng thời gian bài hát.
Danh sách phát: Hiển thị danh sách bài hát ở dưới cùng.

Các Nút Điều Khiển

Phát/Tạm dừng (▶/⏸): Nhấn để phát hoặc tạm dừng bài hát.
Bài trước (⏮): Chuyển đến bài hát trước đó trong danh sách (hoặc bài ngẫu nhiên nếu bật chế độ ngẫu nhiên).
Bài tiếp theo (⏭): Chuyển đến bài hát tiếp theo.
Ngẫu nhiên (⇄): Bật/tắt chế độ phát ngẫu nhiên. Khi bật, bài hát tiếp theo sẽ được chọn ngẫu nhiên.
Lặp lại (↻): Chuyển đổi giữa các chế độ:

Không lặp (↻̶): Phát lần lượt và dừng khi hết danh sách.
Lặp một bài (↻₁): Lặp lại bài hiện tại.
Lặp vòng (↻): Lặp lại toàn bộ danh sách.


Thanh âm lượng: Điều chỉnh âm lượng bằng cách kéo thanh trượt hoặc nhấn vào biểu tượng loa để bật/tắt âm thanh.
Thanh tiến trình: Nhấn vào thanh tiến trình để nhảy đến thời điểm cụ thể trong bài hát.

Danh Sách Phát

Nhấn vào một bài hát trong danh sách để phát ngay lập tức.
Nhấn vào biểu tượng tải xuống (⬇) để tải file MP3 về máy.


5. Tùy Chỉnh Nâng Cao

Thay đổi giao diện: Chỉnh sửa CSS trong phần <style> để thay đổi màu sắc, kích thước, hoặc bố cục giao diện.
Thêm hiệu ứng: Điều chỉnh các thuộc tính transition hoặc animation trong CSS để thay đổi hiệu ứng highlight lời bài hát.
Thêm bài hát: Cập nhật audioList với nhiều bài hát hơn, đảm bảo các URL hợp lệ.
Lưu trữ cục bộ: Nếu không muốn dùng URL bên ngoài, bạn có thể lưu file MP3 và .lrc trong cùng repository và tham chiếu bằng đường dẫn tương đối (ví dụ: ./assets/song.mp3).


6. Lưu Ý

CORS: Nếu file MP3 hoặc .lrc không tải được, kiểm tra xem máy chủ lưu trữ có bật CORS không. Bạn có thể sử dụng dịch vụ như Dropbox hoặc Archive.org để lưu trữ file.
Hiệu suất: Nếu danh sách bài hát dài, hãy đảm bảo tối ưu hóa các file MP3 và ảnh bìa để giảm thời gian tải.
Hỗ trợ di động: Giao diện đã được tối ưu cho thiết bị di động (responsive), nhưng hãy kiểm tra trên các thiết bị để đảm bảo trải nghiệm tốt nhất.


7. Báo Cáo Lỗi
Nếu gặp vấn đề (ví dụ: lời bài hát không đồng bộ, file không tải được), hãy:

Kiểm tra console của trình duyệt (F12 > Console) để xem lỗi.
Đảm bảo các URL trong audioList hoạt động.
Tạo issue trên repository GitHub để báo cáo lỗi hoặc đề xuất cải tiến.


8. Đóng Góp
Nếu bạn muốn đóng góp:

Fork repository.
Tạo nhánh mới (git checkout -b feature/ten-tinh-nang).
Commit thay đổi (git commit -m "Mô tả thay đổi").
Push lên nhánh (git push origin feature/ten-tinh-nang).
Tạo Pull Request trên GitHub.


Cảm ơn bạn đã sử dụng Karaoke Player! Chúc bạn có những giây phút thư giãn với âm nhạc và lời bài hát đồng bộ! 🎤🎵
