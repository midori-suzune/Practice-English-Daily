# Hướng Dẫn & Quy Tắc Dự Án: Practice-English-Daily

Dự án này phục vụ việc học và luyện thi IELTS hàng ngày (Listening, Reading, Writing, Vocab, Flashcards).

---

## 1. Quyền Thực Thi Tự Động (Autonomous Execution)

Agent được toàn quyền **tự động thực thi ngay lập tức** các công cụ và lệnh terminal phục vụ học tập, tra cứu và chỉnh sửa tài liệu mà **KHÔNG CẦN HỎI XÁC NHẬN TRƯỚC**:
- **Thao tác Git an toàn**: `git status`, `git diff`, `git log`, `git add`, `git commit`
- **Thao tác đọc & kiểm tra file/thư mục**: `ls`, `cat`, `grep`, `find`, `head`, `tail`, `view_file`
- **Thao tác chỉnh sửa & tạo file**: `write_to_file`, `replace_file_content`
- **Công cụ hỗ trợ tra cứu bài học & trích xuất transcript**: `python3`, `curl`, `pdftotext`, `yt-dlp`

> ⚠️ **Chỉ hỏi xác nhận khi**: Thực hiện các thao tác phá hủy dữ liệu (như `rm -rf`, `git reset --hard`, `git push --force`).

---

## 2. Quy Cách Ghi Chép Từ Vựng (`Watching Daily/`, `Review Listening Test/`,...)

Mỗi khi hỗ trợ kiểm tra hoặc tạo ghi chú từ vựng mới:
1. **Định dạng mỗi dòng**:
   ```text
   term : <nghĩa tiếng Việt chính xác theo ngữ cảnh> (<định nghĩa tiếng Anh súc tích, chuẩn ngữ cảnh>)
   ```
2. **Độ chính xác ngữ cảnh**:
   - Đối chiếu với bài nghe/đọc gốc (BBC 6 Minute English, IELTS Listening Test,...).
   - Dịch đúng sắc thái văn cảnh bài học (ví dụ: `visceral pain` là cơn đau nội tạng / đau thắt tâm can; `skip` là thùng chứa phế thải xây dựng; `hose down` là xịt rửa bằng vòi nước).
3. **Kiểm tra chính tả**: Rà soát kỹ chính tả tiếng Việt (dấu thanh, bộ gõ telex) và tiếng Anh trước khi hoàn tất.

---



## 3. Quy Cách Đặt Thông Điệp Commit Git (Git Commit Convention)

Khi thực hiện commit các thay đổi trong kho lưu trữ, tuân thủ đúng định dạng chuẩn trong lịch sử Git của dự án:

### Cấu trúc:
```text
<action>: <Thư mục> - <Tên bài/tập tin>
```

### Chi tiết thành phần:
1. **`<action>`** (viết thường, có dấu hai chấm và khoảng trắng `: ` phía sau):
   - `add`: Khi thêm bài học, file mới.
     - *Ví dụ:* `add: Watching Daily - Rude emails`
     - *Ví dụ:* `add: Review Listening Test - Winterbourne Wetlands`
     - *Ví dụ:* `add: Review Reading Test - Dark chocolate's health-giving benefits`
   - `update`: Khi chỉnh sửa, cập nhật nội dung bài đã có.
     - *Ví dụ:* `update: Vocab - CreateQuiz`
     - *Ví dụ:* `update: Watching Daily - Why does heartbreak hurt so much?`
     - *Ví dụ:* `update: Review Reading Test - Synaesthesia`
   - `remove`: Khi xóa file hoặc bài học.
     - *Ví dụ:* `remove: Watching Daily - RealityQuest-1`
2. **`<Thư mục>`**: Tên thư mục chứa file (không cần đường dẫn dài).
   - *Ví dụ:* `Watching Daily`, `Review Listening Test`, `Review Reading Test`, `Vocab`, `Crunchyroll`, `Writing daily`,...
3. **`<Tên bài/tập tin>`**: Tên bài viết hoặc tệp tin **bỏ phần mở rộng `.md`**.
4. **Dấu nối**: Giữa `<Thư mục>` và `<Tên bài>` ngăn cách bởi dấu gạch ngang có khoảng trắng 2 bên: ` - `.
5. **Quy tắc Commit riêng lẻ (BẮT BUỘC)**:
   - **TUYỆT ĐỐI KHÔNG commit chung nhiều file** trong một lần commit.
   - Mỗi file/bài học phải được commit riêng biệt bằng `git add "<file>"` và đi kèm commit message chuẩn đúng tên bài đó.
