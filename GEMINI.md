# Hướng Dẫn & Quy Tắc Dự Án: Practice-English-Daily

Dự án này phục vụ việc học và luyện thi IELTS hàng ngày (Listening, Reading, Writing, Vocab, Flashcards).

---

## 1. Quyền Thực Thi Tự Động & Phạm Vi Kích Hoạt (Autonomous Execution & Scope)

Agent được quyền thực thi các công cụ và lệnh terminal phục vụ học tập, tra cứu và xử lý tài liệu mà không cần hỏi xác nhận trước:
- **Thao tác tra cứu & đọc**: `git status`, `git diff`, `git log`, `ls`, `cat`, `grep`, `find`, `view_file`, `python3`, `curl`, `pdftotext`, `yt-dlp`.
- **Thao tác ghi file & Git commit/push**: **CHỈ THỰC HIỆN KHI NGƯỜI DÙNG YÊU CẦU CỤ THỂ** (ví dụ: *"lưu vào file"*, *"thêm vào ghi chú"*, *"commit cho tôi"*,...):
  - Tuyệt đối **KHÔNG tự ý ghi vào file** hoặc **tự ý commit/push** khi người dùng chỉ gửi câu/cụm từ để hỏi nghĩa hoặc học. Khi đó chỉ phân tích theo Mục 4.
  - Khi đã có yêu cầu cập nhật/lưu từ người dùng, Agent tự động thực hiện `write_to_file`, `replace_file_content`, `git add`, `git commit`, `git push` theo đúng quy chuẩn mà không cần hỏi lại từng bước.

> ⚠️ **Chỉ hỏi xác nhận khi**: Thực hiện các thao tác phá hủy dữ liệu (như `rm -rf`, `git reset --hard`, `git push --force`).

## 2. Quy Cách Đặt Thông Điệp Commit Git (Git Commit Convention)

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
6. **Đồng bộ từ xa (Git Push)**:
   - Sau khi hoàn thành các commit riêng lẻ, tự động thực hiện `git push` để đồng bộ lên remote repository.

---

## 3. Quy Cách Phân Tích Câu / Cụm Tiếng Anh (English Analysis Convention)

Mỗi khi người dùng gửi một câu, cụm từ hoặc đoạn văn tiếng Anh để hỏi nghĩa hoặc học:
> 💡 **Phạm vi phản hồi**: Phân tích trực tiếp trong đoạn chat theo các mục bên dưới. **Tuyệt đối KHÔNG tự ý ghi vào file, KHÔNG commit/push** trừ khi người dùng yêu cầu rõ ràng.

1. **Dịch nghĩa tổng thể theo ngữ cảnh**:
   - Dịch mượt mà, tự nhiên và bám sát đúng văn cảnh (giao tiếp đời sống, anime/rom-com, tin tức báo chí, học thuật IELTS,...).
2. **Bóc tách các cụm từ & cấu trúc "đắt giá" (Key Takeaways)**:
   - **Cụm từ cốt lõi / Phrasal Verbs / Idioms / Collocations**: Nêu rõ nghĩa tiếng Việt, định nghĩa tiếng Anh súc tích, sắc thái và ngữ cảnh sử dụng (ví dụ: thường đi với phủ định, mức độ thân mật hay trang trọng).
   - **Cấu trúc ngữ pháp hay**: Bóc tách dạng công thức mẫu câu (ví dụ: `[Noun] + after + [Noun]`, `not all that + adj`, `cause someone to do something`).
   - **Từ vựng quan trọng**: Phiên âm IPA (nếu từ dễ đọc sai/dễ nhầm), từ loại, từ đồng nghĩa hoặc cụm liên quan để paraphrase.
3. **Ví dụ minh họa mở rộng**:
   - Cung cấp 1-2 câu ví dụ thực tế kèm bản dịch để người học dễ ghi nhớ và ứng dụng vào Speaking/Writing.
4. **Hình thức trình bày**:
   - Rõ ràng, trực quan, phân mục rành mạch, in đậm từ khóa, súc tích và dễ nhớ.
