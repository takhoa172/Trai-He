# 🥋 Buổi 1 — Bài Tập Thực Hành: Tổng Quan Git & 4 Vùng Làm Việc

> 📌 **HƯỚNG DẪN:** Mỗi bài tập, bạn hãy **chạy lệnh thật**, **quan sát kết quả**, rồi **ghi lại** vào các phần có sẵn bên dưới. Buổi này chỉ quan sát và ghi chú — **chưa commit gì cả**.

---

## 📝 Bài Tập 1: Khám Phá Repo Của Bạn

**Mở terminal tại `D:\Trai-He` rồi chạy từng lệnh, ghi kết quả vào bảng:**

| Bước | Lệnh cần chạy | Kết quả quan sát (chép vào đây) |
|---|---|---|
| 1 | `git status` | |
| 2 | `git log --oneline` | |
| 3 | `git remote -v` | |
| 4 | `git branch` | |

**Câu hỏi suy ngẫm (trả lời vào chỗ trống):**
- Với `git remote -v`, URL hiện ra tên tài khoản gì?
  → _________________________________
- Nhánh hiện tại bạn đang đứng là gì?
  → _________________________________

---

## 🔬 Bài Tập 2: Chứng Minh "Git Chỉ Theo Dõi File"

**Thực hiện tuần tự rồi ghi lại:**

| Bước | Lệnh | Kết quả quan sát |
|---|---|---|
| 1 | `git ls-files Git/` | |
| 2 | `git status` | |

**Trả lời các câu hỏi:**
1. `git ls-files Git/` trả ra gì? Điều đó chứng minh điều gì?
   → ________________________________________________________________
2. Vì sao thư mục `Git/` không xuất hiện trong `git status` hiện tại?
   → ________________________________________________________________
3. Nếu bạn tạo một thư mục **trống** tên `test-empty/`, rồi chạy `git status` — bạn nghĩ Git có hiện không? Vì sao?
   → _________________________________

---

## 🖊️ Bài Tập 3: Vẽ Lại Bức Tranh 4 Vùng Từ Trí Nhớ

Trong khung dưới đây, hãy **tự viết** tên 4 vùng và **3 lệnh** (add / commit / push) vào đúng vị trí:

```
[                    ]
          │
          │  git add
          ▼
[                    ]
          │
          │  git ________ (đóng hộp)
          ▼
[                    ]
          │
          │  git ________ (giao ra ngoài)
          ▼
[                    ]
```

**Sau khi điền xong, so sánh với sơ đồ trong file lý thuyết. Bạn điền đúng bao nhiêu vùng? (1/4, 2/4, ...)**
→ _________________________________

---

## 4. Bảng Ghi Chú Thực Hành Cá Nhân

> Ghi lại **mọi lệnh** bạn đã chạy trong buổi này và rút ra bài học cho riêng mình:

| Lệnh đã chạy | Kết quả quan sát | Điều học được |
|---|---|---|
| `git status` | | |
| `git log --oneline` | | |
| `git remote -v` | | |
| `git branch` | | |
| | | |
| | | |

---

## ✅ Kiểm Tra Nhanh Cuối Buổi

Trả lời nhanh (không nhìn lại lý thuyết):

1. Git ≠ GitHub. Khác nhau chỗ nào cốt nhất?
   → _________________________________
2. Kể tên 4 vùng làm việc theo thứ tự dữ liệu đi qua.
   → _________________________________
3. Lệnh nào chỉ "chốt" giữ chỗ file mà chưa chính thức lưu lịch sử?
   → _________________________________

---

## 🏁 Hoàn Thành Buổi 1

Chúc mừng! Bạn vừa hoàn thành:

- [ ] Bài tập 1 — Khám phá repo
- [ ] Bài tập 2 — Chứng minh Git chỉ theo dõi file
- [ ] Bài tập 3 — Vẽ lại sơ đồ 4 vùng từ trí nhớ
- [ ] Bài tập 4 — Bảng ghi chú cá nhân
- [ ] Kiểm tra nhanh cuối buổi

Khi bạn đã đánh dấu đủ, hãy **quay lại `Theory/Buoi-1-Tong-Quan-Git.md`** và tích vào các mục tiêu tương ứng!

> 💡 *Việc ghi chú và tự trả lời mới là phần quý nhất — nó biến kiến thức từ "đã đọc" thành "đã hiểu".*