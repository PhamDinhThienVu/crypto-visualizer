# 📌 Bước tiếp theo nên làm - Hoàn thiện Frontend cơ bản (Giai đoạn 01)

## Hoàn thiện frontend cơ bản
- Tạo component nhập text (textarea + button).

- Viết logic encode/decode Base64 ngay trong frontend bằng TypeScript.

- Hiển thị kết quả rõ ràng (ví dụ: ô kết quả bên dưới).

- Commit và push branch feature/base64-visualization.

👉 Đây sẽ là milestone đầu tiên để có một demo chạy được.

## 2. Viết test nhỏ cho frontend
- Dùng Jest hoặc Vitest để test hàm encode/decode.

- Đảm bảo input → output đúng, tránh bug khi mở rộng sau này.

## 3. Bổ sung docs
- Trong thư mục docs/walkthrough_project/, viết file hướng dẫn chi tiết cách chạy frontend.

- Ví dụ: 001_base64_frontend.md mô tả cách nhập text, encode/decode, và kết quả mong đợi.

## 4. Chuẩn bị cho Giai đoạn 2 (Visualization)
- Nghĩ cách hiển thị step-by-step:

- Chia input thành bytes.

- Mapping sang bảng Base64.

- Render từng bước bằng bảng hoặc animation.

- Có thể dùng thư viện visualization (D3.js, Chart.js, hoặc React Flow).

5. Workflow Git
- Sau khi hoàn thành Giai đoạn 1, tạo Pull Request từ branch feature/base64-visualization sang main.

- Review, merge, rồi tiếp tục tạo branch mới cho Giai đoạn 2 (feature/base64-steps-visualization).