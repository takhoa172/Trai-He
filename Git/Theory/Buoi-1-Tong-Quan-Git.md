# 🥋 Buổi 1: Tổng Quan Git & 4 Vùng Làm Việc

> *"Hiểu được dữ liệu đi tới đâu, bạn sẽ điều khiển được cả thế giới Git."*

---

## 🎯 Mục Tiêu Buổi Học

Sau buổi này, bạn sẽ có thể:

- [x] Hiểu **Git là gì** và phân biệt được Git vs GitHub
- [x] Vẽ lại được **bức tranh 4 vùng làm việc** của Git
- [x] Giải thích được vì sao dữ liệu đi theo quy trình `Working → Staging → Local → Remote`
- [x] Giải thích được vì **Git chỉ theo dõi file, không theo dõi thư mục**
- [x] Đọc được `git status` để biết file đang "ở đâu" trong cỗ máy

---

## 🧠 Phần 1: Git Là Gì?

### Câu chuyện mở đầu

Bạn từng lưu file thành nhiều bản thế này chưa?

```
bai-tap-cuoi.doc
bai-tap-cuoi-final.doc
bai-tap-cuoi-final-that-su.doc
bai-tap-cuoi-FINAL-LAN-2.doc
```

Nhìn quen quen phải không? 😅 Git sinh ra để giải quyết chính cái rối này.

### Version Control là gì?

- **Version control** (quản lý phiên bản) là cách theo dõi mọi thay đổi của file theo thời gian
- Bạn lưu **mỗi lần sửa** thành một "mốc thời gian" gọi là **commit**
- Muốn quay lại bất kỳ lúc nào trong quá khứ? Git làm được ngay

### Git ≠ GitHub

| | Git | GitHub |
|---|---|---|
| Là gì | Công cụ quản lý phiên bản chạy trên máy bạn | Dịch vụ lưu trữ Git trên internet |
| Chạy ở | Máy tính của bạn (terminal) | Website github.com |
| Cần không | **Có, bắt buộc** — phần trí tuệ này mới quan trọng | Không bắt buộc — chỉ cần khi muốn lưu trữ & chia sẻ |
| Đây là | Cái não | Cái tủ trên mây |

> 💡 **Mẹo ghi nhớ:** Git là "trí não" hoạt động trên máy bạn. GitHub chỉ là "nơi chứa" trên internet. Bạn dùng Git mà không cần GitHub, nhưng không thể dùng GitHub mà không có Git bên dưới.

---

## 🌊 Phần 2: Bức Tranh 4 Vùng Làm Việc (Trọng Tâm)

### Ví dụ: Nhà hàng nấu món ăn 🍳

Hãy tưởng tượng Git là một **nhà hàng**, còn bạn là đầu bếp:

| | Trong Nhà Hàng | Trong Git |
|---|---|---|
| **Nhà bếp** | Nơi bạn cắt rau, nấu nướng | **Working Directory** — nơi bạn sửa file thật |
| **Bàn đợi trước quầy** | Món làm xong, chờ phục vụ | **Staging Area** — vùng chờ, chỉ những gì `git add` mới lên đây |
| **Đóng hộp có nhãn** | Món chính thức thành sản phẩm "món ngày X" | **Local Repository** — commit có message |
| **Giá bán** | Đưa món ra cho khách khắp nơi | **Remote Repository** — GitHub |

### Sơ đồ 4 vùng (hãy ghi nhớ nó!)

```
[Nhà Bếp — Working Directory]
          │
          │  git add  (đưa món lên bàn đợi)
          ▼
[Bàn Đợi — Staging Area]
          │
          │  git commit  (đóng hộp, ghi nhãn "món ngày X")
          ▼
[Kho Nhà — Local Repository]
          │
          │  git push  (giao ra thế giới bên ngoài)
          ▼
[Giá Bán — Remote Repository trên GitHub]
```

### 3 điểm mấu chốt phải nhớ

1. **Phải `git add` trước rồi mới `git commit`** — Git không cho bạn đóng hộp khi món chưa lên bàn đợi
2. **`git status` là camera quan sát** — giúp bạn biết từng món đang "đứng" ở đâu
3. **File chỉ có thể coi "xong" khi vào Local Repo** — push là để chia sẻ ra ngoài, không bắt buộc phải làm ngay

---

## 📋 Phần 3: Chi Tiết 4 Vùng

| Vùng | Là gì | Nằm ở đâu | Lệnh dẫn vào |
|---|---|---|---|
| **Working Directory** | File bạn đang mở sửa thật, là nơi làm việc hằng ngày | Thư mục dự án trên máy | (tự nhiên khi bạn sửa) |
| **Staging Area** | Vùng chọn lựa — chỉ những thay đổi được "chốt" mới vào commit | File ẩn `.git/index` | `git add` |
| **Local Repository** | Kho commit trên máy — lịch sử đầy đủ | Thư mục ẩn `.git` | `git commit` |
| **Remote Repository** | Bản sao dự án trên GitHub | Máy chủ GitHub | `git push` |

> ⚠️ **Lưu ý quan trọng:** Dữ liệu chỉ chính thức "an toàn & có lịch sử" khi nằm trong **Local Repository** (đã commit). Working và Staging vẫn nằm trong "vùng tạm", dễ bị mất.

---

## 🔍 Phần 4: Đối Chiếu Với Repo Thật Của Bạn

Mình xem thực trạng repo `Trai-He` của bạn:

| Vùng | Dữ liệu đang ở đó |
|---|---|
| **Working Directory** (untracked) | `.obsidian/`, `C##/`, `Java/`, `LapTrinh/`, `wikilink.md` |
| **Local Repo** | `Git/Git-Kung-Fu.md` và các file tiếng Anh đã commit |
| **Remote** | Toàn bộ đã push lên nhánh `git-learning` & `main` |

**Tại sao `git status` không thấy `Git/`?**
Vì `Git/Git-Kung-Fu.md` đã **commit sạch** — không còn thay đổi mới để report. Còn `Java/`, `.obsidian/`... chưa từng commit, nên Git "báo" bạn chúng còn mới (untracked).

### Thí nghiệm nhỏ để tự tin hơn
Nếu bạn **sửa một chữ** trong `Git/Git-Kung-Fu.md` rồi chạy `git status`, `Git/` sẽ bắt đầu xuất hiện với ký hiệu ` M` (modified) — đúng như... một món đã chạm tay!

---

## ✅ Tóm Tắt & Câu Hỏi Tự Kiểm Tra

### Bảng tổng kết nhanh
| Muốn làm | Bạn dùng lệnh | Dữ liệu chuyển |
|---|---|---|
| Chọn thay đổi để đưa vào commit | `git add` | Working → Staging |
| Lưu lại lịch sử trên máy | `git commit` | Staging → Local |
| Đưa lên GitHub | `git push` | Local → Remote |

---

### ❓ 5 Câu Trắc Nghiệm (tự trả lời trước khi xem đáp án cuối file)

1. Lệnh nào đưa file từ Working vào Staging?
2. `git commit` di chuyển dữ liệu từ đâu đến đâu?
3. Vùng nào nằm trong thư mục ẩn `.git`?
4. Lệnh nào đưa dữ liệu từ Local lên GitHub?
5. Thư mục trống có được Git theo dõi không?

> [!success]- 👀 Xem Đáp Án
> 1. `git add`
> 2. Staging → Local (commit)
> 3. Staging Area (`.git/index`) và Local Repository (`.git/`)
> 4. `git push`
> 5. Không — Git chỉ theo dõi file, thư mục trống bị bỏ qua

---

## 🗺️ Chuyển Sang Buổi 2

Buổi 2 ta sẽ học cách "đọc vị" `git status` — từng ký hiệu ` M`, `A`, `??` mang ý nghĩa gì để biết file đang ở vùng nào.

*Hãy nhấn "Checklist trống" ✏️ ✔  phần mục tiêu sau khi bạn thực sự làm xong bài tập nhé!*