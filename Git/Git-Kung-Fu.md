# 🥋 Git Kung Fu

### Hành trình luyện Git & GitHub từ số 0

> *"Give a man a fish and you feed him for a day; teach a man to fish and you feed him for a lifetime."*
> *(Cho một người con cá, anh ta ăn được một ngày; dạy người đó cách câu cá, anh ta ăn được cả đời.)*

**Với Git cũng vậy** — mục tiêu không chỉ là biết gõ lệnh, mà là **hiểu bản chất** để tự mình giải quyết mọi vấn đề.

---

## 🥷 Giới Thiệu

Xin chào! Đây là hành trình cá nhân của mình để **chinh phục Git và GitHub**.

Mình từng chỉ biết máy móc bốn lệnh:

- `git status` — xem trạng thái
- `git add` — thêm file
- `git commit -m` — commit
- `git push` — đẩy lên GitHub

Nhưng mình **không thật sự hiểu** chuyện gì đang diễn ra bên trong. File này ra đời để ghi lại hành trình từ "biết gõ lệnh" đến "hiểu bản chất".

---

## 🎯 Mục Tiêu

| Cấp Độ | Mục Tiêu |
|--------|----------|
| 🥉 **Sơ Cấp** | Dùng thành thạo: status, add, commit, push, pull |
| 🥈 **Trung Cấp** | Branch, merge, giải quyết conflict khi gộp nhánh |
| 🥇 **Cao Cấp** | Restore, reset, stash, .gitignore, workflow chuẩn lập trình viên |

---

## 🗺️ Lộ Trình 7 Buổi

| Buổi | Nội Dung | Thành Quả |
|------|----------|-----------|
| 🥋 **Buổi 1** | Tổng quan Git & 4 vùng làm việc | Vẽ được bức tranh dữ liệu đi qua đâu |
| 🥋 **Buổi 2** | Đọc hiểu `git status` | Phân biệt được 3 trạng thái của file |
| 🥋 **Buổi 3** | `add` & `commit` | Viết commit rõ ràng, gọn gàng |
| 🥋 **Buổi 4** | Remote, push, pull, clone | Kết nối thành thạo với GitHub |
| 🥋 **Buổi 5** | Branch & Merge | Làm việc nhiều nhánh không sợ lạc |
| 🥋 **Buổi 6** | Sửa lỗi & phục hồi | Không còn sợ làm sai nữa |
| 🥋 **Buổi 7** | `.gitignore` & tổng kết | Dọn dẹp repo chuyên nghiệp |

---

## 🗂️ Cấu Trúc Thư Mục

```
Git/
├── Git-Kung-Fu.md           ← File bạn đang đọc
├── Theory/                  ← Lý thuyết từng buổi
│   ├── Buoi-1-Tong-Quan-Git.md
│   └── Buoi-2-Doc-Hieu-Status.md
└── Exercise/                ← Bài tập thực hành
    ├── Buoi-1-Bai-Tap-Tong-Quan.md
    └── Buoi-2-Bai-Tap-Status.md
```

- **`Theory/`**: Nơi lưu kiến thức lý thuyết theo từng buổi
- **`Practice/`**: Nơi ghi lại quá trình tự thực hành theo từng bước

---

## 🤝 Quy Ước Làm Việc

1. Toàn bộ nội dung học nằm ở nhánh `git-learning`
2. Nhánh `main` giữ lộ trình tiếng Anh — **không được động vào**
3. Mỗi buổi học xong → `commit` + `push` gọn gàng
4. Khi hoàn thành toàn bộ lộ trình → gộp `git-learning` về `main`

**Quy ước commit message:**

| Loại | Cú Pháp | Ví Dụ |
|------|---------|-------|
| Khởi tạo | `Khoi tao...` | `Khoi tao Git-Kung-Fu` |
| Thêm nội dung | `Them...` | `Them buoi 1 - Tong quan Git` |
| Sửa lỗi | `Fix: ...` | `Fix: sai danh may buoi 3` |

---

## ✅ Checklist

- [ ] Buổi 1: Tổng quan & 4 vùng
- [ ] Buổi 2: `git status`
- [ ] Buổi 3: `add` & `commit`
- [ ] Buổi 4: Remote + push/pull
- [ ] Buổi 5: Branch & merge
- [ ] Buổi 6: Sửa lỗi & phục hồi
- [ ] Buổi 7: `.gitignore` + tổng kết
- [ ] 🎓 **Hoàn thành! Gộp `git-learning` vào `main`**

---

## 📚 Tham Khảo

- 📖 Git chính thức: [git-scm.com](https://git-scm.com/doc)
- 🐙 GitHub Docs: [docs.github.com](https://docs.github.com)
- 🎮 Luyện tập vui: [learngitbranching.js.org](https://learngitbranching.js.org)

---

## 📝 Changelog

| Ngày | Nội dung thay đổi |
|------|-------------------|
| 2026-08-08 | Khởi tạo lộ trình Git Kung Fu |