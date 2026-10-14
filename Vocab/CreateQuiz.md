Tôi sẽ gửi LIST TỪ VỰNG IELTS. Hãy chuyển đổi danh sách này thành chuỗi JSON chuẩn hóa để import trực tiếp vào thẻ Flashcard theo đúng cấu trúc bên dưới.

QUY TẮC ĐỊNH DẠNG (BẮT BUỘC):
1. ĐẦU RA: Chỉ xuất ra DUY NHẤT 1 block JSON hợp lệ (Valid JSON). TUYỆT ĐỐI KHÔNG thêm văn bản giải thích ngoài JSON.
2. CẤU TRÚC JSON CỐ ĐỊNH (STRICT SCHEMA - CẤM TỰ Ý THÊM TRƯỜNG):
   - Cấp cao nhất (Root) CHỈ ĐƯỢC CHỨA ĐÚNG 2 KEY: `"title"` và `"words"`. TUYỆT ĐỐI KHÔNG thêm các trường ngoài lề (như `"description"`, `"category"`, `"id"`, v.v.).
   - Mỗi item trong `"words"` CHỈ ĐƯỢC CHỨA ĐÚNG 6 KEY sau:
     * `term` (Thuật ngữ): Từ/cụm từ tiếng Anh gốc (giữ nguyên không đổi).
     * `definition` (Định nghĩa): Định nghĩa tiếng Anh súc tích kèm nghĩa tiếng Việt theo đúng cấu trúc: `<Định nghĩa tiếng Anh>. (<Nghĩa tiếng Việt lấy đúng theo note>)`. Bắt buộc có dấu chấm `.` kết thúc câu tiếng Anh trước khi mở ngoặc `(<Nghĩa tiếng Việt>)`.
     * `pronounce` (Phát âm): Phiên âm IPA chuẩn quốc tế.
     * `word_type` (Loại từ): Từ loại tiếng Anh (e.g. "noun", "verb", "adjective", "noun phrase", "verb phrase", "adjective phrase", "idiom",...).
     * `example` (Ví dụ): 1 câu ví dụ tiếng Anh tự nhiên, sinh động, chuẩn ngữ pháp, gắn với ngữ cảnh đời sống/học tập/công việc thực tế. BẮT BUỘC câu ví dụ phải minh họa ĐÚNG nét nghĩa đã nêu ở `definition`. Đối với từ đa nghĩa (polysemous words), tuyệt đối không được viết ví dụ sang nét nghĩa khác (ví dụ: nếu `conservatory` có nghĩa "nhà kính/phòng kính trồng cây" thì ví dụ phải nói về cây cối/ánh nắng/nhà cửa, tuyệt đối không viết ngữ cảnh "nhạc viện/âm nhạc").
     * `synonyms` (Từ đồng nghĩa / Cụm diễn đạt tương đương): Mảng chứa 1-2 từ hoặc **cụm paraphrase tiếng Anh có nghĩa tương đương** (đặc biệt đối với Idiom, Phrasal verb hoặc thuật ngữ khó: luôn tìm cụm từ tiếng Anh giải nghĩa/thay thế tương đương, ví dụ: `bite the bullet` ➔ `["face the challenge", "endure difficulties"]`). Bắt buộc luôn có 1-2 phần tử tiếng Anh, KHÔNG được để mảng rỗng. Bắt buộc phải đồng nhất 100% với đúng nét nghĩa được chỉ định.
       CẤM TUYỆT ĐỐI: KHÔNG DÙNG TIẾNG VIỆT TRONG MẢNG `synonyms`.
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
    },
  ]
}

TIÊU CHÍ CHẤT LƯỢNG NỘI DUNG:
- **Đầy đủ**: Làm đúng và đủ tất cả các từ trong danh sách được cung cấp.
- **Thuật ngữ**: Giữ đúng từ/cụm từ gốc (phần trước dấu 2 chấm).
- **Văn phong**: Giải thích và ví dụ phải dễ hiểu, trực quan cho người học mọi độ tuổi, tránh dịch máy thô cứng.
- **Nhất quán ngữ nghĩa (Strict Semantic Consistency)**: `definition`, `example` và `synonyms` bắt buộc phải khóa chặt vào DUY NHẤT một nét nghĩa được chỉ định theo nghĩa tiếng Việt cung cấp. Tuyệt đối không để xảy ra tình trạng "định nghĩa nghĩa A nhưng câu ví dụ hay từ đồng nghĩa lại minh họa cho nghĩa B" của từ đa nghĩa.

BƯỚC TỰ KIỂM TRA TRƯỚC KHI XUẤT KẾT QUẢ (SELF-CHECK):
- [ ] Tính nhất quán ngữ nghĩa: `example` và `synonyms` đã khớp hoàn toàn 100% với nét nghĩa tiếng Việt được chỉ định chưa? Có bị lẫn sang nét nghĩa khác của từ đa nghĩa không?
- [ ] Mảng `synonyms` đã có 1-2 từ/cụm paraphrase 100% bằng tiếng Anh chưa? (Tuyệt đối không để trống và không có tiếng Việt).
- [ ] Root JSON chỉ có `"title"` và `"words"`, tuyệt đối không có trường `"description"` chứ?
- [ ] Cú pháp JSON hợp lệ, không có dấu phẩy thừa (trailing comma)?
- [ ] Đã bao gồm đầy đủ 100% các từ trong danh sách cung cấp chưa?
---

slender : mảnh mai, thon thả (having a thin, graceful, or delicate form or shape, often indicating elegance or attractiveness)

have a light perm : uốn tóc nhẹ (to have hair that has been styled with a gentle wave or curl, often indicating a soft or natural look)

or rather : hay đúng hơn là (used to correct or clarify a previous statement, often indicating a more accurate description or explanation)

that very same something :  chính cái gì đó (the exact same thing being referred to, often indicating emphasis or specificity)

in no time : ngay lập tức, trong chớp mắt (very quickly or immediately; without delay, often indicating rapid action or response)


