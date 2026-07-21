# 📖 Markdown Formatting Guide

> Hướng dẫn toàn diện về cú pháp Markdown và Obsidian — dành cho người mới bắt đầu.
> Mỗi phần có: **Cú pháp** → **Ví dụ** → **Kết quả** → **Ghi chú**.

---

## Mục Lục

1. [Text Formatting — Định dạng chữ](#1-text-formatting--định-dạng-chữ)
2. [Headings — Tiêu đề](#2-headings--tiêu-đề)
3. [Lists — Danh sách](#3-lists--danh-sách)
4. [Tables — Bảng biểu](#4-tables--bảng-biểu)
5. [Links & Navigation — Liên kết & Điều hướng](#5-links--navigation--liên-kết--điều-hướng)
6. [Code — Mã lệnh](#6-code--mã-lệnh)
7. [Blockquotes & Dividers — Trích dẫn & Dòng kẻ](#7-blockquotes--dividers--trích-dẫn--dòng-kẻ)
8. [Callouts — Obsidian Blocks](#8-callouts--obsidian-blocks)
9. [Obsidian Nâng Cao](#9-obsidian-nâng-cao)
10. [Làm Đẹp & Tips Visual](#10-làm-đẹp--tips-visual)
11. [Quick Reference Card — Bảng tra nhanh](#11-quick-reference-card--bảng-tra-nhanh)

---

## 1. Text Formatting — Định dạng chữ

### 1.1 Các cú pháp cơ bản

| Cú pháp               | Kết quả              | Dùng khi nào?                |
| --------------------- | -------------------- | ---------------------------- |
| `**text**`            | **text**             | Nhấn mạnh, tiêu đề nhỏ       |
| `*text*`              | *text*               | Tên sách, nghiêng nhẹ        |
| `~~text~~`            | ~~text~~             | Nội dung sai/cần xóa         |
| `==text==`            | ==text==             | Highlight từ khóa (Obsidian) |
| `` `text` ``          | `text`               | Code inline, cú pháp         |
| `<u>text</u>`         | <u>text</u>          | Gạch chân (dùng HTML)        |
| `<mark>text</mark>`   | <mark>text</mark>    | Tô màu vàng                  |
| `<small>text</small>` | <small>text</small>  | Chữ nhỏ, phụ chú             |
| `<kbd>F5</kbd>`       | <kbd>F5</kbd>        | Phím tắt bàn phím            |
| `^text^`              | Super<sup>text</sup> | Chỉ số trên (ex: E=mc^2^)    |
| `~text~`              | Sub<sub>text</sub>   | Chỉ số dưới (ex: H~2~O)      |

### 1.2 HTML tags bổ sung

```html
<span style="color:red">Chữ đỏ</span>
<span style="background:yellow">Tô nền vàng</span>
<span style="font-size:24px">Chữ to</span>

<p align="center"><b>Căn giữa</b></p>
<br>           → xuống dòng
&nbsp;         → 1 khoảng trắng
&emsp;         → 1 tab
```

### 1.3 Escape — Gõ ký tự đặc biệt

Dùng dấu `\` để gõ các ký tự Markdown mà không bị hiểu là cú pháp:

| Cú pháp | Kết quả |
|---------|---------|
| `\*` | \* (dấu sao, không phải in nghiêng) |
| `\#` | \# (dấu thăng, không phải heading) |
| `\[` | \[ (mở ngoặc, không phải link) |
| `` \` `` | \` (backtick, không phải code) |
| `\|` | \| (gạch dọc, không phải table) |
| `\-` | \- (dấu trừ, không phải list) |

### 1.4 Line Break — Xuống dòng

| Cách | Cú pháp |
|------|---------|
| Xuống dòng nhưng không tách paragraph | Kết thúc dòng bằng **2 spaces** + Enter |
| Xuống dòng cứng | `<br>` |
| Tách paragraph | Enter 2 lần (dòng trắng) |

> 💡 **Mẹo:** Dùng `<br>` dễ nhớ hơn 2 spaces cuối dòng.

---

## 2. Headings — Tiêu đề

### 2.1 ATX Headings (phổ biến)

| Cú pháp | Mức | Ví dụ kết quả |
|---------|:---:|---------------|
| `# text` | H1 | # Tiêu đề lớn |
| `## text` | H2 | ## Chương chính |
| `### text` | H3 | ### Mục nhỏ |
| `#### text` | H4 | #### Tiểu mục |
| `##### text` | H5 | ##### Ghi chú |
| `###### text` | H6 | ###### Chú thích nhỏ |

### 2.2 Setext Headings (ít dùng hơn)

```
Heading 1
=========

Heading 2
---------
```

### 2.3 Quy tắc

> ✅ **Nên nhớ:**
> - **1 file chỉ có 1 H1** — đó là tên tài liệu
> - **Không bỏ cấp:** `#` → `##` → `###` (đúng), `#` → `###` (sai)
> - **Có dòng trắng** trước và sau heading
> - **Có thể thêm emoji:** `## 📖 Nội Dung`

> ❌ **Sai:**
> ```
> # Tài liệu
> ### Mục con (thiếu ##)
> ```
> ✅ **Đúng:**
> ```
> # Tài liệu
> ## Mục con
> ### Tiểu mục
> ```

---

## 3. Lists — Danh sách

### 3.1 Bullet list

```
- Cấp 1
  - Cấp 2 (thụt 2 spaces)
    - Cấp 3 (thụt thêm 2 spaces)
      - Cấp 4
```

Kết quả:
- Cấp 1
  - Cấp 2
    - Cấp 3
      - Cấp 4

> 💡 **Mẹo:** Dùng `-`, `+`, hoặc `*` đều được — nên chọn `-` cho nhất quán.

### 3.2 Numbered list

```
1. Bước 1
2. Bước 2
   1. Bước 2a (thụt 3 spaces)
   2. Bước 2b
3. Bước 3
```

Kết quả:
1. Bước 1
2. Bước 2
   1. Bước 2a
   2. Bước 2b
3. Bước 3

> 💡 **Mẹo:** Có thể dùng toàn bộ `1.` — Markdown tự động đánh số đúng.

### 3.3 Task list (Checkbox) — Click được trong Obsidian

```
- [ ] Chưa làm
- [x] Đã làm xong
- [ ] Còn dang dở
- [x] Đã hoàn thành
```

Kết quả:
- [ ] Chưa làm
- [x] Đã làm xong
- [ ] Còn dang dở
- [x] Đã hoàn thành

> ⚠️ **Lưu ý:** Task list chỉ click được trong Obsidian (Reading/Live Preview). Trên PDF là hình tĩnh.

### 3.4 Nâng cao — List kèm mô tả

```
- **Tên sách** — Tác giả
  Mô tả ngắn về nội dung cuốn sách này.
  
- **Tên phim** — Đạo diễn
  Thể loại, năm sản xuất, đánh giá.
```

### 3.5 Mix emoji phân loại

```
- ✅ Đã hoàn thành
- ⏳ Đang xử lý
- 🔄 Đang review
- ❌ Tạm dừng
- 📝 Cần bổ sung
- 🆕 Mới thêm
- 🎯 Mục tiêu quan trọng
```

---

## 4. Tables — Bảng biểu

### 4.1 Cú pháp cơ bản

```
| Cột 1 | Cột 2 | Cột 3 |
|-------|-------|-------|
| A     | B     | C     |
| D     | E     | F     |
```

| Cột 1 | Cột 2 | Cột 3 |
|-------|-------|-------|
| A     | B     | C     |
| D     | E     | F     |

### 4.2 Căn lề

| Cú pháp | Căn |
|---------|:---:|
| `:---` | Trái |
| `:---:` | Giữa |
| `---:` | Phải |

```
| Trái      | Giữa       | Phải |
|:----------|:----------:|-----:|
| text      | text       | text |
```

| Trái      | Giữa       | Phải |
|:----------|:----------:|-----:|
| text      | text       | text |

### 4.3 Định dạng trong bảng

Có thể dùng **bold**, *italic*, `code`, [link](), v.v. trong ô:

```
| Mục | Ví dụ |
|-----|-------|
| **Quan trọng** | Nhấn mạnh `code` |
| [Xem thêm](https://...) | *ghi chú* |
```

| Mục | Ví dụ |
|-----|-------|
| **Quan trọng** | Nhấn mạnh `code` |
| [Xem thêm](https://google.com) | *ghi chú* |

### 4.4 Xuống dòng trong bảng

Dùng `<br>` để có nhiều dòng trong 1 ô:

```
| Tên | Mô tả |
|-----|-------|
| Markdown | Định dạng văn bản<br>Dễ học, dễ dùng<br>Phổ biến |
| Obsidian | Ghi chú cá nhân<br>Hỗ trợ plugin<br>Đồng bộ đa nền tảng |
```

| Tên | Mô tả |
|-----|-------|
| Markdown | Định dạng văn bản<br>Dễ học, dễ dùng<br>Phổ biến |
| Obsidian | Ghi chú cá nhân<br>Hỗ trợ plugin<br>Đồng bộ đa nền tảng |

### 4.5 Bảng với emoji

```
| 🟢 Dễ | 🟡 Trung bình | 🔴 Khó |
|:-----:|:-------------:|:-----:|
| Cơ bản | Nâng cao | Chuyên sâu |
```

| 🟢 Dễ | 🟡 Trung bình | 🔴 Khó |
|:-----:|:-------------:|:-----:|
| Cơ bản | Nâng cao | Chuyên sâu |

### 4.6 Bảng rỗng

Để ô trống bằng ` ` hoặc không ghi gì:

```
| Cột 1 | Cột 2 | Cột 3 |
|-------|-------|-------|
| A     |       | C     |
|       | B     |       |
```

| Cột 1 | Cột 2 | Cột 3 |
|-------|-------|-------|
| A     |       | C     |
|       | B     |       |

---

## 5. Links & Navigation — Liên kết & Điều hướng

### 5.1 Obsidian Internal Links (Link nội bộ)

```
[[file-name]]                        → Link tới file
[[file-name|Tên hiển thị]]           → Link có alias
[[file-name#tiêu-đề]]               → Link tới heading
[[file-name#^anchor]]               → Link tới anchor

# Ngắn gọn:
[[file]] → tự động hiện tên file
[[file|Xem thêm]] → hiện "Xem thêm"
```

### 5.2 External Links (Link web)

```
[Google](https://google.com)
[Email](mailto:abc@example.com)
[Xem thêm](https://example.com "Tooltip")

Có thể viết gọn URL:
<https://google.com> → https://google.com
<abc@example.com> → abc@example.com
```

### 5.3 Reference-Style Links

Dùng khi muốn gom link xuống cuối file:

```
[Google][google-ref]
[Wikipedia][wiki-ref]

[google-ref]: https://google.com "Google"
[wiki-ref]: https://wikipedia.org "Wikipedia"
```

Kết quả: [Google][google-ref] — [Wikipedia][wiki-ref]

[google-ref]: https://google.com "Google"
[wiki-ref]: https://wikipedia.org "Wikipedia"

### 5.4 Anchor — Đánh dấu vị trí

```
^muc-quan-trong             → đánh dấu ở dòng muốn link đến
[[file#^muc-quan-trong]]    → link tới dòng đó
```

> **Cách dùng:** Đặt `^ten` ở đầu dòng. Chỉ Obsidian mới hỗ trợ.

### 5.5 Embed — Nhúng nội dung

```
![[file-name]]                 → nhúng toàn bộ file
![[file-name#heading]]        → nhúng 1 phần
![[file.pdf]]                 → xem PDF (Obsidian)
![[audio.mp3]]                → nghe audio
![[video.mp4]]                → xem video
![[image.png]]                → xem ảnh
```

### 5.6 Obsidian URI

Dùng khi cần mở Obsidian từ bên ngoài:

```
obsidian://open?vault=TênVault&file=path/to/note
obsidian://new?vault=TênVault&name=Ghi+chú+mới
```

---

## 6. Code — Mã lệnh

### 6.1 Inline code

```
Dùng lệnh `git status` để kiểm tra.
Nhấn `Ctrl + S` để lưu file.
Biến `$name` chứa tên người dùng.
```

Kết quả: Dùng lệnh `git status` để kiểm tra.

### 6.2 Code block

```
Đây là code block không tô màu
```
print("Hello World")
```
```

### 6.3 Code block với syntax highlighting

Thêm tên ngôn ngữ sau 3 backticks:

\```python
def hello():
    print("Hello, World!")
\```

\```javascript
function hello() {
    console.log("Hello!");
}
\```

\```html
<div class="container">
  <p>Hello</p>
</div>
\```

\```css
body {
    background: #f0f0f0;
    font-size: 14px;
}
\```

\```bash
npm install opencode
```

\```sql
SELECT * FROM users WHERE active = 1;
```

\```json
{
  "name": "John",
  "age": 30
}
```

### 6.4 Diff — Hiện thay đổi

\```diff
- dòng xóa
+ dòng thêm
  dòng giữ nguyên
```

### 6.5 Ký tự đặc biệt trong code

```
Nếu trong code có 3 backticks, dùng 4:
````
```python
print("code lồng nhau")
```
````
```

> 💡 **Mẹo:** Luôn chỉ định ngôn ngữ cho code block để có màu sắc đẹp hơn.

---

## 7. Blockquotes & Dividers — Trích dẫn & Dòng kẻ

### 7.1 Blockquotes — Trích dẫn

```
> Cấp 1
>> Cấp 2
>>> Cấp 3
```

Kết quả:
> Cấp 1
>> Cấp 2
>>> Cấp 3

```
> 💡 **Mẹo:** Thêm emoji vào đầu blockquote để phân loại:

> 💡 Mẹo vặt
> ⚠️ Cảnh báo
> 📝 Ghi chú
> ✅ Lưu ý quan trọng
> 🎯 Mục tiêu
```

> 💡 **Mẹo:** Thêm emoji vào đầu blockquote để phân loại

### 7.2 Dividers — Dòng kẻ ngang

Dùng để phân cách các phần:

```
Nội dung phía trên
---
Nội dung phía dưới
```

Kết quả:

---
---

Có 3 cú pháp tương đương:

| Cú pháp | Ghi chú |
|---------|---------|
| `---` | Phổ biến nhất |
| `***` | Dấu sao |
| `___` | Dấu gạch dưới |

> ⚠️ **Luôn có dòng trắng** trước và sau divider.

---

## 8. Callouts — Obsidian Blocks

### 8.1 Các loại Callouts

Obsidian hỗ trợ 12 loại callout tích hợp:

```
> [!note]-
> [!abstract]-
> [!info]-
> [!tip]-
> [!success]-
> [!question]-
> [!warning]-
> [!failure]-
> [!danger]-
> [!bug]-
> [!example]-
> [!quote]-
```

### 8.2 Collapse (thu gọn)

```
> [!note]- Title  (dấu - → mặc định đóng)
Content ẩn

> [!note]+ Title  (dấu + → mặc định mở)
Content hiện
```

### 8.3 Ví dụ cụ thể

```
> [!note]- 📝 Ghi chú
> Đây là ghi chú chung, thông tin cơ bản.

> [!tip]- 💡 Mẹo nhỏ
> Dùng callout để phân loại nội dung trong ghi chú.

> [!warning]- ⚠️ Lưu ý
> Không làm điều này nếu chưa hiểu rõ.

> [!success]- ✅ Hoàn thành
> Nội dung đã được xác nhận.

> [!question]- ❓ Câu hỏi
> Bạn có thắc mắc gì không?
```

Kết quả (trong Obsidian):

> [!note]- 📝 Ghi chú
> Đây là ghi chú chung.

> [!tip]- 💡 Mẹo nhỏ
> Dùng callout để phân loại nội dung.

> [!warning]- ⚠️ Lưu ý
> Không làm điều này nếu chưa hiểu rõ.

> [!success]- ✅ Hoàn thành
> Nội dung đã được xác nhận.

> [!question]- ❓ Câu hỏi
> Bạn có thắc mắc gì không?

> [!danger]-
> Cảnh báo nguy hiểm — cẩn thận!

> [!example]-
> Đây là ví dụ minh họa.

> [!quote]-
> Trích dẫn nguồn tham khảo.

### 8.4 Lồng callout

```
> [!question]- Câu hỏi
> Nội dung câu hỏi
>
> > [!success]- Đáp án
> > Nội dung đáp án
```

> [!question]- Câu hỏi
> Nội dung câu hỏi
>
> > [!success]- Đáp án
> > Nội dung đáp án

### 8.5 Lưu ý quan trọng

> ⚠️ **HTML `<details>` KHÔNG hoạt động trong Obsidian Live Preview**, chỉ chạy trong Reading View. Dùng Callouts thay thế để tương thích mọi chế độ.
>
> ❌ `<details><summary>Title</summary>content</details>` — **không nên dùng**
> ✅ `> [!note]- Title` content — **nên dùng**

---

## 9. Obsidian Nâng Cao

### 9.1 YAML Frontmatter — Metadata file

Đặt ở **đầu file**, giữa 2 dấu `---`:

```yaml
---
created: 2024-07-21
updated: 2024-07-22
tags: [tutorial, markdown]
aliases: [formatting-guide, cheat-sheet]
status: draft
author: Your Name
---
```

| Trường | Dùng để |
|--------|---------|
| `created` | Ngày tạo file |
| `updated` | Ngày sửa gần nhất |
| `tags` | Gắn nhãn phân loại |
| `aliases` | Tên khác của file (để link dễ hơn) |
| `status` | Trạng thái: draft/complete/archived |

### 9.2 Properties (Obsidian 1.4+)

Từ Obsidian 1.4, properties được hiển thị dưới dạng UI:

```yaml
---
title: 
tags:
  - markdown
  - tutorial
status: draft
---
```

Có thể thêm/sửa Properties qua giao diện (Ctrl+; hoặc nút Properties).

### 9.3 Tags — Gắn nhãn

```
#tutorial                  → tag đơn
#tutorial/markdown         → tag phân cấp (cha/con)
#project/active            → trạng thái dự án
```

> **Cách dùng:** Tags giúp tìm kiếm và nhóm file theo chủ đề trong Obsidian.

### 9.4 Comments — Ẩn nội dung

```
%% Đây là comment, chỉ thấy khi Edit %%
%% Không hiện trong Reading View hay Live Preview %%
```

> 💡 **Dùng để:** Ghi chú nội bộ, nhắc nhở bản thân, ghi chú không muốn hiển thị khi export.

### 9.5 Aliases — Tên khác

Đặt trong YAML frontmatter:

```yaml
---
aliases: [tên-gọn, tên-khác]
---
```

> Khi gõ `[[tên-gọn]]`, Obsidian tự động gợi ý file.

### 9.6 Templates — Mẫu (cần plugin Templates)

Dùng trong template file:

```
{{title}}           → Tên file
{{date}}            → Ngày hiện tại
{{date:YYYY-MM-DD}} → Ngày format tùy chỉnh
{{time}}            → Giờ hiện tại
{{time:HH:mm}}      → Giờ format tùy chỉnh
```

### 9.7 Math — Công thức toán (cần bật plugin)

```
Công thức inline: $E = mc^2$

Công thức block:
$$
\sum_{i=1}^{n} i = \frac{n(n+1)}{2}
$$
```

### 9.8 Mermaid — Sơ đồ (cần bật plugin)

```
\```mermaid
graph TD
    A[Start] --> B{Decision}
    B -->|Yes| C[Action 1]
    B -->|No| D[Action 2]
    C --> E[End]
    D --> E
\```

\```mermaid
sequenceDiagram
    A->>B: Hello
    B->>A: Hi!
\```

\```mermaid
gantt
    title Project Timeline
    section Phase 1
    Task A: 2024-01-01, 30d
```
```

### 9.9 Footnote — Chú thích cuối

```
Đây là câu có footnote[^1].

[^1]: Nội dung footnote ở cuối file.

Hoặc viết liền:
Đây là footnote[^inline-note] có tên.

[^inline-note]: Nội dung inline.
```

### 9.10 Dataview — Truy vấn dữ liệu (cần plugin)

Dùng để tạo bảng từ metadata:

```
\```dataview
TABLE created, status
FROM "folder"
SORT created DESC
\```
```

> ⚠️ **Cần cài plugin Dataview từ Community Plugins.**

### 9.11 Command Palette

```
Ctrl+P    → mở Command Palette
Ctrl+O    → Quick Switch (mở file nhanh)
Ctrl+F    → Tìm kiếm trong file
Ctrl+E    → Toggle Edit/Preview
```

---

## 10. Làm Đẹp & Tips Visual

### 10.1 Emoji trong Heading

```
# 📚 Tổng Quan
## ✨ Tính Năng Chính
### 🎯 Mục Tiêu
#### 📝 Chi Tiết
```

```markdown
## 📖 Nội Dung Chính    (sách, tài liệu)
## ⚙️ Cài Đặt           (technical)
## 🚀 Bắt Đầu           (hướng dẫn)
## 🧪 Thực Hành         (bài tập)
## ✅ Kiểm Tra          (review)
```

### 10.2 Badge-style — Huy hiệu phân loại

```
- 🔴 **Quan trọng:** Cần làm gấp
- 🟡 **Cảnh báo:** Lưu ý khi dùng
- 🟢 **Hoàn thành:** Đã xong
- 🔵 **Đang làm:** Đang tiến hành
- ⚪ **Bỏ qua:** Tạm gác lại
- 🟣 **Nâng cao:** Dành cho người đã biết
```

### 10.3 Căn giữa (dùng HTML)

```html
<p align="center">
  <b>Chữ đậm ở giữa</b><br>
  <i>Chữ nghiêng ở giữa</i><br>
  <small>Chữ nhỏ ở giữa</small>
</p>
```

> ⚠️ HTML chỉ hoạt động trong Reading View Obsidian, không hoạt động trong Live Preview.

### 10.4 Tô màu chữ (dùng HTML)

```html
<span style="color:red">Chữ đỏ</span>
<span style="color:#ff6600">Chữ cam</span>
<span style="color:blue">Chữ xanh dương</span>
<span style="color:green">Chữ xanh lá</span>
<span style="color:purple">Chữ tím</span>
<span style="color:gray">Chữ xám</span>
```

### 10.5 Tô nền (dùng HTML)

```html
<span style="background:#ffff00">Nền vàng</span>
<span style="background:#ffcccc">Nền hồng nhạt</span>
<span style="background:#ccffcc">Nền xanh nhạt</span>
<span style="background:#ccccff">Nền xanh dương nhạt</span>
```

### 10.6 Spacing — Khoảng cách

```
---               → dòng kẻ (phân cách mạnh)

<br>              → xuống dòng đơn

&nbsp;            → 1 space (giữa 2 dòng ko bị collapse)

> Dòng cách biệt  → blockquote tạo khoảng cách
```

### 10.7 Horizontal Rule nâng cao

```
───────────────────

═══════════════════

░▒▓█▓▒░░▒▓█▓▒░
```

Dùng ký tự Unicode để tạo divider đẹp hơn (chép từ ký tự đặc biệt).

### 10.8 Grid/Columns (thủ công)

Dùng table để tạo layout dạng cột:

```
| 🎯 **Mục A** | 🎯 **Mục B** |
|:------------:|:------------:|
| Nội dung A    | Nội dung B    |
```

### 10.9 HTML Details — Cảnh báo

```
❌ Không nên dùng trong Obsidian Live Preview:
<details><summary>Title</summary>content</details>

✅ Dùng Callout thay thế:
> [!note]- Title
> content
```

---

## 11. Quick Reference Card — Bảng tra nhanh

```
╔══════════════════════════════════════════════╗
║         📋 BẢNG TRA NHANH MARKDOWN           ║
╚══════════════════════════════════════════════╝

─── ĐỊNH DẠNG CHỮ ─────────────────────────────
  **bold**       *italic*       ~~gạch ngang~~
  ==highlight==  `code`         <u>gạch chân</u>
  ^super^       ~sub~          <kbd>phím</kbd>

─── TIÊU ĐỀ ────────────────────────────────────
  #      → H1 (chỉ 1/file)
  ##     → H2
  ###    → H3
  ####   → H4
  #####  → H5
  ###### → H6

─── DANH SÁCH ──────────────────────────────────
  - item          → bullet
  1. item         → số
  - [ ] checkbox  → chưa làm
  - [x] checkbox  → đã làm

─── BẢNG ──────────────────────────────────────
  | a | b |       → table cơ bản
  |:---|:---:|---:| → align: trái | giữa | phải

─── LINKS ──────────────────────────────────────
  [[file]]           → internal link
  [[file|name]]      → alias
  [text](url)        → external link
  ![[file]]          → embed
  ^anchor            → anchor

─── BLOCKQUOTE ─────────────────────────────────
  > text             → quote cấp 1
  >> text            → quote cấp 2

─── CALLOUT ────────────────────────────────────
  > [!note]- Title    → collapsed
  > [!tip]+ Title     → expanded

─── CODE ──────────────────────────────────────
  `code`             → inline
  ``` ```language```   → block (có highlight)

─── OBSIDIAN ───────────────────────────────────
  %% comment %%      → ẩn nội dung
  #tag               → tag
  {{date}}           → template
  $math$             → công thức
  Ctrl+P             → Command Palette

─── DIVIDER ────────────────────────────────────
  ---                → dòng kẻ ngang

─── HTML ───────────────────────────────────────
  <br>               → xuống dòng
  &nbsp;             → space
  <span style="">    → tô màu
```

---

> 💡 **Mẹo cuối cùng:** Cách học Markdown nhanh nhất là **mở 2 cửa sổ Obsidian**: 1 bên Edit, 1 bên Preview. Gõ cú pháp ở bên trái → xem kết quả bên phải.

---

*Happy Note-Taking! 🚀*
