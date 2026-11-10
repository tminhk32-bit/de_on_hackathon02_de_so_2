# ĐỀ LUYỆN TẬP ÔN THI HACKATHON 02
- **Mã đề:** 02
- **Họ tên:** Đào Tuấn Minh
- **Lớp:** CNTT3
- **Link repository:**
- **Hệ điều hành (Windows/macOS):** Windows

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```Powershell
1.pwd
2.ls -force
3.mv .\bien_ban_ban_giao.txt .\docs
4.mkdir backup
5.cp .\data\ban_ve_thang_11.xlsx .\backup
6.rm .\cache_991.tmp
7.cd .\logs
8.ls
9.cd..
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text

    Directory: D:\rap-phim-website
Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        11/10/2026   8:59 AM                backup
d-----        11/10/2026   9:23 AM                data
d-----        11/10/2026   8:58 AM                docs
d-----        11/10/2026   8:42 AM                evidence
d-----        11/10/2026   9:27 AM                logs
d-----        11/10/2026   8:39 AM                web
-a----        11/10/2026   8:39 AM             82 .env
-a----        11/10/2026   8:44 AM           2611 bai_lam.md
-a----        11/10/2026   9:26 AM            363 tong_hop.ps1
```

## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng ERROR

```Powershell
Get-Content .\logs\server.log | Select-String "ERROR" >> .\logs\loi_error.txt
```

### 2 dòng đầu tiên trong logs/loi_error.txt

```text
2026-11-01 09:25:40 ERROR POST /api/mua-ve
2026-11-01 09:29:11 ERROR POST /api/thanh-toan-qr
```

### b) Lệnh đếm số dòng WARNING và kết quả

```Powershell
(Get-Content .\logs\server.log | Select-String "WARNING").count >> .\logs\loi_error.txt
```

```text
5
```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```Powershell
1.Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
2. .\tong_hop.ps1
```

### Nội dung file logs/tong_hop.txt

```text
=== BAO CAO SU CO WEBSITE ===

2026-11-01 09:08:10 WARNING GET /phim-sap-chieu-cu
2026-11-01 09:15:30 WARNING GET /uu-dai-thang-9
2026-11-01 09:36:50 WARNING GET /images/phong-imax.jpg
2026-11-01 10:01:20 WARNING GET /voucher-het-han
2026-11-01 10:12:55 WARNING GET /combo-bap-nuoc

6
```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] README.md: Heading 1, mô tả có **in đậm** và _in nghiêng_, bảng, code block, task list, blockquote
- [ ] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | -------------------------- | --------------------------- | -------------- |
| 1   |                            |                             |                |
| 2   |                            |                             |                |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:**
- **Expected:**
- **Actual:**
- **Log:**

### Câu tìm kiếm Google

```text
(Ghi câu tìm kiếm vào đây – xoá dòng này)

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/ban_ve_thang_11.xlsx`, không cần ghi vào đây.

