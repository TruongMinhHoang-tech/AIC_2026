# 🏆 Hệ Thống Xử Lý OCR & Smart Search Tiếng Việt (Video Keyframes)

Dự án này là giải pháp toàn diện để trích xuất văn bản từ hình ảnh/keyframes (OCR) và xây dựng công cụ tìm kiếm nội dung video dựa trên văn bản. Hệ thống được thiết kế tối ưu cho tiếng Việt, phục vụ quá trình truy xuất dữ liệu trong các kỳ thi AI / Xử lý Dữ liệu lớn.

## ✨ Tính năng nổi bật
* **Song kiếm hợp bích (Hybrid OCR):** Sử dụng **PaddleOCR** để dò tìm khung chữ/đọc số siêu tốc và **VietOCR (Transformer)** để xử lý các dấu câu tiếng Việt phức tạp.
* **Tiền xử lý ảnh thông minh:** Tích hợp bộ lọc OpenCV (Grayscale + CLAHE) giúp đọc chuẩn xác cả những keyframe bị mờ, tối hoặc nhiễu.
* **Smart Search (Tìm kiếm mờ):** Bộ máy tìm kiếm có khả năng chấm điểm độ khớp (%), tự động bỏ qua lỗi chính tả nhỏ của OCR hoặc lỗi thiếu dấu.
* **Kháng lỗi đứt mạng:** Code được thiết kế để lưu thẳng vào ổ cứng (Flush) và có khả năng tự động chạy tiếp (Resume) các frame còn dang dở nếu hệ thống bị treo.
* **Chuẩn hóa Dữ liệu:** Xuất file CSV định dạng `UTF-8-SIG` giúp Ban Giám Khảo mở file bằng Microsoft Excel không bao giờ bị lỗi font tiếng Việt.

---

## ⚙️ Hướng dẫn Cài đặt (Tránh lỗi thư viện)

Để hệ thống chạy mượt mà nhất (đặc biệt là trên Google Colab hoặc máy ảo), vui lòng cài đặt các thư viện theo đúng thứ tự sau:

**Bước 1: Cài đặt các thư viện lõi từ file requirements**
```bash
pip install -r requirements.txt