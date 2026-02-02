# Crypto Visualizer Project

Dự án nghiên cứu và trực quan hóa các thuật toán mã hóa thông tin.  

Trước mắt, ứng dụng sẽ hỗ trợ **mã hóa/giải mã Base64** và hiển thị từng bước xử lý.


- **Giai đoạn 1**: Frontend cơ bản (TypeScript + React/Vue) → nhập text, encode/decode Base64, hiển thị kết quả.

- **Giai đoạn 2**: Thêm visualization step-by-step cho Base64.

- **Giai đoạn 3**: Cho phép upload file và hiển thị nội dung.

- **Giai đoạn 4**: Tích hợp backend Python để parse/validate và xuất JSON.

- **Giai đoạn 5**: Mở rộng sang các thuật toán khác (AES, RSA, SHA).

**Công nghệ sử dụng**
- Frontend: TypeScript (React/Vue)

- Backend (optional): Python (Flask/FastAPI)

---

## 🚀 Quy trình làm việc với Git

### 1. Tạo repository mới trên GitHub
1. Truy cập [GitHub](https://github.com).
2. Chọn **New Repository**.
3. Đặt tên repo, ví dụ: `crypto-visualizer`.
4. Chọn public/private tùy nhu cầu.
5. Nhấn **Create Repository**.

### 2. Clone project về máy
Sau khi tạo repo, copy đường dẫn HTTPS hoặc SSH.  
Ví dụ:
```bash
git clone https://github.com/PhamDinhThienVu/crypto-visualizer.git
```

### 3. Kiểm tra trạng thái của repo
Giúp kiểm tra các file đã thay đổi, thêm mới hoặc chưa commit.
```bash
cd crypto-visualizer
git status
```

### 4. Thêm các file hoặc thay đổi 

- Thêm đường dẫn tới profile của bạn ở cuối file README.md chẳng hạn
- Sau khi có thay đổi về nội dung hoặc thêm file. Add vào repo local

```bash
git add .
```

Sau đó kiểm tra:
```bash
git status 
```

```bash
git commit -m "Add README.md with project description, docs|walkthrough_project folder, algorithm_explaination folder"
```

### 5. Push code lên GitHub

```bash
git push origin main
```

### 6. Pull code từ GitHub về máy
Khi có thay đổi trên GitHub (ví dụ đồng đội đã commit):
```bash
git pull origin main
```

### 7. Quy trình làm việc nhóm (Workflow)
- Pull trước khi làm việc: luôn chạy git pull origin main để đồng bộ code mới nhất.
- Tạo branch riêng: mỗi tính năng nên phát triển trên một branch riêng để tránh xung đột.
- Ví dụ: 
```bash
git checkout -b feature/base64-visualization
```
- Commit nhỏ gọn, rõ ràng: mỗi commit chỉ nên giải quyết một vấn đề.
- Merge qua Pull Request (PR): khi hoàn thành tính năng, tạo PR để review trước khi merge vào main.


### 8. Cấu trúc thư mục dự kiến
crypto-visualizer/
|
├── README.md
├── docs/                  # Tài liệu hướng dẫn, walkthrough
├── walkthrough_project/   # Các bước triển khai chi tiết
├── algorithm_explaination/ # Giải thích thuật toán (Base64, AES, RSA...)
├── frontend/              # Code TypeScript (React/Vue)
└── backend/               # Code Python (Flask/FastAPI, optional)


### 9. Thiết lập môi trường
**Frontend (TypeScript + React/Vue)**
1. Cài đặt [Node.js](https://nodejs.org/en/download). Lưu ý bổ sung enviroment path vào máy, các tùy chọn khi cài đặt.
2. Khởi tạo project React/Vue:
```bash
npm init vue@latest frontend
```

3. Chạy ứng dụng
```bash
cd frontend
npm install
npm run dev
```

**Backend (Python - optional)**
1. Cài đặt Python (>= 3.10).

2. Tạo virtual environment
```bash
python -m venv venv
```
3. Kích hoạt python venv khi chạy backend
```bash
source venv/bin/activate   # Linux/Mac

venv\Scripts\activate      # Windows
```

4. Cài đặt Flask
```bash
pip install flask fastapi uvicorn
```

5. Lưu lại dependency vào file requirements.txt
```bash
pip freeze > requirements.txt
```

6. Khi clone repo, để download hết dependencies
```bash
pip install -r requirements.txt
```


### 10. Bổ sung .gitignore để tránh commit những file không cần thiết

```gitignore
# Node.js / Frontend
node_modules/
dist/
build/
*.log
.env.local

# Python / Backend
__pycache__/
*.pyc
*.pyo
*.pyd
venv/
env/
.venv/
backend/.env

# IDE / Editor
.vscode/
.idea/
*.swp
*.swo

# OS / Misc
.DS_Store
Thumbs.db

```

### 11. Quy ước commit (Commit convention)

Để dễ quản lý lịch sử commit, bạn có thể áp dụng quy tắc như sau:

- feat: thêm tính năng mới

- fix: sửa lỗi

- docs: cập nhật tài liệu

- style: chỉnh sửa format/code style

- refactor: cải tổ code không thêm tính năng

- test: thêm hoặc sửa test

- chore: việc lặt vặt (update dependency, config)

```bash
git commit -m "feat(frontend): add base64 encode/decode component"
```

### 12. Hướng dẫn chạy project

**Frontend**
```bash
cd frontend 
npm install 
npm run dev
```

**Backend**
```bash
cd backend
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
pip install -r requirements.txt
python app.py
```