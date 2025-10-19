# Court Order Calendar Integration

⚖️ **Tự động tạo lịch Google Calendar từ các lệnh tòa án**

## Mô tả

Ứng dụng web này giúp bạn tự động trích xuất các deadline từ file PDF lệnh tòa án và tạo các sự kiện trong Google Calendar. Sử dụng công nghệ AI để phân tích nội dung văn bản và tự động tạo lịch nhắc nhở.

## Tính năng

- 📄 **Upload PDF**: Hỗ trợ drag & drop hoặc chọn file PDF lệnh tòa án
- 🤖 **AI Analysis**: Sử dụng Ollama AI để trích xuất thông tin deadline
- 📅 **Google Calendar**: Tự động tạo sự kiện trong Google Calendar
- 🔗 **Direct Links**: Cung cấp link trực tiếp đến từng sự kiện calendar
- 📊 **Summary Dashboard**: Hiển thị tổng quan các deadline và thống kê
- 🎨 **Modern UI**: Giao diện đẹp, responsive và dễ sử dụng

## Công nghệ sử dụng

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Backend**: n8n Workflow Automation
- **AI**: Ollama (Qwen3:32b model)
- **Calendar**: Google Calendar API
- **PDF Processing**: n8n Extract from File node

## Cách sử dụng

1. **Truy cập trang web**: [Court Order Calendar Integration](https://your-username.github.io/court-order-calendar)

2. **Cấu hình Webhook URL**: 
   - Nhập URL webhook của n8n workflow
   - Mặc định: `https://nhaquachne.app.n8n.cloud/webhook/court-order-upload`

3. **Upload file PDF**:
   - Kéo thả file PDF vào vùng upload
   - Hoặc click "Choose File" để chọn file

4. **Xem kết quả**:
   - Hệ thống sẽ tự động phân tích PDF
   - Hiển thị danh sách các deadline
   - Tạo sự kiện Google Calendar
   - Cung cấp link trực tiếp đến từng sự kiện

## Cài đặt n8n Workflow

Để sử dụng ứng dụng này, bạn cần:

1. **n8n Instance**: Cài đặt n8n (cloud hoặc self-hosted)
2. **Google Calendar Credentials**: Cấu hình OAuth2 cho Google Calendar
3. **Ollama Server**: Cài đặt Ollama với model Qwen3:32b
4. **Import Workflow**: Import file `court-order-workflow.json`

## Cấu trúc dự án

```
court-order-calendar/
├── index.html              # Trang chính (GitHub Pages)
├── Court_order.html         # File gốc
├── court-order-workflow.json # n8n workflow
├── test_frontend.html       # File test
└── README.md               # Tài liệu này
```

## Demo

🔗 **Live Demo**: [https://your-username.github.io/court-order-calendar](https://your-username.github.io/court-order-calendar)

## Screenshots

### Upload Interface
- Giao diện upload file PDF với drag & drop
- Cấu hình webhook URL

### Results Dashboard
- Hiển thị thống kê tổng quan
- Bảng danh sách các deadline
- Link trực tiếp đến Google Calendar

## Hỗ trợ

Nếu bạn gặp vấn đề:

1. **Kiểm tra Webhook URL**: Đảm bảo n8n workflow đang chạy
2. **Kiểm tra file PDF**: File phải có text (không phải scan)
3. **Kiểm tra Google Calendar**: Đảm bảo credentials được cấu hình đúng

## Phát triển

### Yêu cầu
- n8n (latest version)
- Ollama với model Qwen3:32b
- Google Calendar API access
- Modern web browser

### Local Development
```bash
# Clone repository
git clone https://github.com/your-username/court-order-calendar.git

# Serve locally
python3 -m http.server 8000

# Truy cập http://localhost:8000
```

## License

MIT License - Xem file LICENSE để biết thêm chi tiết.

## Đóng góp

Mọi đóng góp đều được chào đón! Vui lòng tạo issue hoặc pull request.

---

**Lưu ý**: Ứng dụng này được thiết kế cho mục đích giáo dục và hỗ trợ. Vui lòng kiểm tra kỹ các thông tin trước khi sử dụng trong môi trường production.