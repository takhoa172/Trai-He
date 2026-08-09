# Buổi 1 - Tổng Quan Git & 4 Vùng Làm Việc

> 📅 Ngày hoàn thành: ____________
> 💬 Ghi chú nhanh: _________________________________

---

## 📝 Bài Tập 1: Khám Phá Repo Của Bạn

| Bước | Lệnh | Kết quả quan sát của tôi | Đáp án đúng | Kết quả |
| :--: | :--- | :----------------------- | :---------- | :-----: |
|  1   | `git status` | | `On branch git-learning...` | |
|  2   | `git log --oneline` | | dòng commit mới nhất `dd60a83 Khởi tạo lộ trình học Git...` | |
|  3   | `git remote -v` | | `https://github.com/takhoa172/Trai-He.git` | |
|  4   | `git branch` | | `* git-learning`, `main` | |

=> **Kết quả:** ... /4 đúng

**Câu hỏi suy ngẫm:**
| # | Câu trả lời của tôi | Đáp án đúng |
|---|---|---|
| Tài khoản GitHub? | | `takhoa172` |
| Nhánh hiện tại? | | `git-learning` |

---

## 🔬 Bài 2: Chứng Minh "Git Chỉ Theo Dõi File"

| Bước | Lệnh | Kết quả quan sát của tôi | Đáp án đúng |
| :--: | :--- | :----------------------- | :---------- |
| 1 | `git ls-files Git/` | | `Git/Git-Kung-Fu.md` |
| 2 | `git status` | | `Git/Practice/`, `Git/Theory/` hiện untracked gọn theo thư mục |

**Trả lời câu hỏi:**

| # | Câu trả lời của tôi | Đáp án đúng | Kết quả |
|---|---|---|---|
| 1 | `ls-files` trả ra gì? Chứng minh điều gì? | | Nó trả ra file `Git/Git-Kung-Fu.md` — Git theo dõi file, không theo dõi thư mục |
| 2 | Vì sao `Git/` không hiện trong status? | | Vì file trong đó đã commit sạch, không còn thay đổi mới |
| 3 | Thư mục trống `test-empty/` hiện không? | | Không — Git bỏ qua thư mục trống |

---

## 🖊️ Bài 3: Vẽ Lại Sơ Đồ 4 Vùng Từ Trí Nhớ

| STT | Vùng tôi điền | Đáp án đúng | Kết quả |
| :-: | :--------- | :-------- | :-----: |
| 1 | | `Working Directory` | |
| 2 | | `Staging Area` | |
| 3 | | `Local Repository` | |
| 4 | | `Remote Repository` | |

=> **Kết quả:** ... /4 đúng

---

## 📒 Bài 4: Bảng Ghi Chú Thực Hành Cá Nhân

| Lệnh đã chạy | Điều học được |
| :------- | :---------- |
| `git status` |  |
| `git log --oneline` |  |
| `git remote -v` |  |
| `git branch` |  |

---

## ✅ Kiểm Tra Nhanh Cuối Buổi

| # | Câu trả lời của tôi | Đáp án đúng | Kết quả |
|---|---|---|---|
| 1 | Git ≠ GitHub: khác nhau chỗ cốt nhất? |  | Git là công cụ chạy trên máy (quản lý phiên bản); GitHub là nơi lưu trữ trên internet | |
| 2 | Kể 4 vùng theo thứ tự dữ liệu đi qua | | Working → Staging → Local → Remote |
| 3 | Lệnh nào chỉ "chốt giữ" mà chưa lưu lịch sử? | | `git add` |

---

## 📝 Tự Đánh Giá

- **Phần dễ nhất:** _________________________________
- **Phần khó nhất:** _________________________________
- **Điều rút ra được:** _________________________________

---

## ✅ Checklist Hoàn Thành

- [ ] Bài 1 - Khám phá repo
- [ ] Bài 2 - Chứng minh Git theo dõi file
- [ ] Bài 3 - Vẽ sơ đồ 4 từ trí nhớ
- [ ] Bài 4 - Bảng ghi chú cá nhân
- [ ] Kiểm tra nhanh cuối buổi