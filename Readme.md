# SmartFarm System

Hệ thống quản trị SmartFarm hỗ trợ theo dõi nhật ký máy chủ, phát hiện sự cố và quản lý thiết bị tại các trạm cảm biến trong trang trại thông minh.

## 2. Hướng dẫn chạy script

### Bước 1: Mở PowerShell

Di chuyển vào thư mục `scripts`:

```powershell
cd .\smartfarm-system\scripts
```

Nếu đang ở thư mục gốc `smartfarm-system`, chỉ cần chạy:

```powershell
cd .\scripts
```

### Bước 2: Chạy chương trình

```powershell
.\auto_report.ps1
```

Nếu gặp lỗi ExecutionPolicy:

```powershell
powershell -ExecutionPolicy Bypass -File .\auto_report.ps1
```

### Bước 3: Kiểm tra báo cáo

```powershell
Get-Content ..\backup\bao-cao-su-co.txt
```

Script lọc các dòng chứa `CRITICAL` hoặc `ERROR`, ghi chi tiết sự cố và tổng số sự cố vào file báo cáo.

## 3. Checklist kiểm tra thiết bị

* [x] Kiểm tra cấu trúc thư mục dự án SmartFarm.
* [ ] Kiểm tra nguồn điện và kết nối mạng của trạm cảm biến.
* [ ] Kiểm tra dung lượng RAM của thiết bị.
* [ ] Kiểm tra trạng thái lưu trữ và nhật ký hệ thống.
* [ ] Xác nhận dữ liệu cảm biến được gửi về máy chủ.

## 4. Bảng thông số phần cứng

*Lưu ý: Các dòng dưới đây là dữ liệu minh họa, cần thay bằng thông tin thực tế từ sheet `danh-muc-linh-kien` trong file `quan-ly-thiet-bi.xlsx`.*

| Tên thiết bị        | Đơn giá (VNĐ) | Loại storage |
| ------------------- | ------------: | ------------ |
|Raspberry Pi 4 Model B|       1.450.000 | SSD       |
|Intel NUC i3 |       6.200.000 | SSD        |
| Orange Pi 5         |     2.300.000 | SSD          |


