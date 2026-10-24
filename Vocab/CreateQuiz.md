Tôi sẽ gửi LIST TỪ VỰNG IELTS. Hãy chuyển đổi danh sách này thành chuỗi JSON chuẩn hóa để import trực tiếp vào thẻ Flashcard theo đúng cấu trúc bên dưới.

QUY TẮC ĐỊNH DẠNG (BẮT BUỘC):
1. ĐẦU RA: Chỉ xuất ra DUY NHẤT 1 block JSON hợp lệ (Valid JSON). TUYỆT ĐỐI KHÔNG thêm văn bản giải thích ngoài JSON.
2. CẤU TRÚC JSON CỐ ĐỊNH (STRICT SCHEMA - CẤM TỰ Ý THÊM TRƯỜNG):
   - Cấp cao nhất (Root) CHỈ ĐƯỢC CHỨA ĐÚNG 2 KEY: `"title"` và `"words"`. TUYỆT ĐỐI KHÔNG thêm `"description"` hay bất kỳ trường nào khác.
   - Mỗi item trong `"words"` CHỈ ĐƯỢC CHỨA ĐÚNG 6 KEY sau:
     * `term`: Từ/cụm từ tiếng Anh gốc (giữ nguyên không đổi).
     * `definition`: Lấy định nghĩa tiếng Anh kèm nghĩa tiếng Việt theo đúng cấu trúc: `<Định nghĩa tiếng Anh>. (<Nghĩa tiếng Việt>)`.
       - Bắt buộc có dấu chấm `.` kết thúc câu tiếng Anh trước khi mở ngoặc `(<Nghĩa tiếng Việt>)`.
       - **NGUYÊN TẮC BẮT BUỘC CHO NGHĨA TIẾNG VIỆT**: Phần nghĩa tiếng Việt trong ngoặc `(...)` PHẢI giữ CHÍNH XÁC NGUYÊN VĂN 100% từ bản ghi chú của người dùng (phần nằm ngay sau dấu `:`). TUYỆT ĐỐI KHÔNG tự ý suy diễn, dịch lại, viết thêm từ ngữ hay diễn giải dài dòng (Ví dụ: note ghi `đóng sách` thì phải để `(Đóng sách)`, note ghi `gấp và may` thì để `(Gấp và may)`, TUYỆT ĐỐI KHÔNG tự bôi thêm thành `(Gấp và may các tờ giấy lại với nhau trong nghề đóng sách)`).
     * `pronounce`: Phiên âm IPA chuẩn quốc tế.
     * `word_type`: Từ loại tiếng Anh (e.g. "noun", "verb", "adjective", "noun phrase", "verb phrase", "adjective phrase", "idiom",...).
     * `example`: 1 câu ví dụ tiếng Anh tự nhiên, sinh động, chuẩn ngữ pháp (100% TIẾNG ANH), gắn với ngữ cảnh đời sống/học tập/công việc thực tế. BẮT BUỘC câu ví dụ phải minh họa ĐÚNG nét nghĩa đã nêu ở `definition`. Đối với từ đa nghĩa (polysemous words), tuyệt đối không được viết ví dụ sang nét nghĩa khác.
     * `synonyms`: **100% TIẾNG ANH (ENGLISH ONLY)**. Mảng chứa 1-2 từ hoặc cụm paraphrase bằng TIẾNG ANH có nghĩa tương đương (ví dụ: `bite the bullet` -> `["face the challenge", "endure difficulties"]`). 
       NGUYÊN TẮC BẤT DI BẤT DỊCH: Giá trị trong `synonyms` PHẢI HOÀN TOÀN LÀ TIẾNG ANH. TUYỆT ĐỐI KHÔNG ĐƯA TỪ/CỤM TIẾNG VIỆT VÀO MẢNG NÀY.
3. CHUẨN CÚ PHÁP JSON (VALID JSON SYNTAX):
   - Tuyệt đối KHÔNG để dấu phẩy thừa ở phần tử cuối cùng (No trailing commas) tránh làm lỗi trình parse JSON.

VÍ DỤ MẪU JSON CHUẨN FLASHCARD:
{
  "title": "IELTS Vocabulary Flashcards",
  "words": [
    {
      "term": "staple food",
      "definition": "A food that makes up the main part of a person's regular diet. (Lương thực chính, thực phẩm thiết yếu hàng ngày)",
      "pronounce": "/ˈsteɪpl fuːd/",
      "word_type": "noun phrase",
      "example": "Rice is the primary staple food for more than half of the world's population.",
      "synonyms": ["basic food", "dietary staple"]
    }
  ]
}

---

