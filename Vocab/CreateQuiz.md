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
     * `example` (Ví dụ): 1 câu ví dụ tiếng Anh tự nhiên, sinh động, chuẩn ngữ pháp, gắn với ngữ cảnh đời sống/học tập/công việc thực tế, không áp dụng quá nhiều từ vựng chuyên ngành, ví dụ đơn giản dễ hiểu có liên quan trực tiếp đến thuật ngữ.
     * `synonyms` (Từ đồng nghĩa / Cụm diễn đạt tương đương): Mảng chứa 1-2 từ hoặc **cụm paraphrase tiếng Anh có nghĩa tương đương** (đặc biệt đối với Idiom, Phrasal verb hoặc thuật ngữ khó: luôn tìm cụm từ tiếng Anh giải nghĩa/thay thế tương đương, ví dụ: `bite the bullet` ➔ `["face the challenge", "endure difficulties"]`). Bắt buộc luôn có 1-2 phần tử tiếng Anh, KHÔNG được để mảng rỗng.
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
    }
  ]
}

TIÊU CHÍ CHẤT LƯỢNG NỘI DUNG:
- **Đầy đủ**: Làm đúng và đủ tất cả các từ trong danh sách được cung cấp.
- **Thuật ngữ**: Giữ đúng từ/cụm từ gốc (phần trước dấu 2 chấm).
- **Văn phong**: Giải thích và ví dụ phải dễ hiểu, trực quan cho người học mọi độ tuổi, tránh dịch máy thô cứng.

BƯỚC TỰ KIỂM TRA TRƯỚC KHI XUẤT KẾT QUẢ (SELF-CHECK):
- [ ] Mảng `synonyms` đã có 1-2 từ/cụm paraphrase 100% bằng tiếng Anh chưa? (Tuyệt đối không để trống và không có tiếng Việt).
- [ ] Root JSON chỉ có `"title"` và `"words"`, tuyệt đối không có trường `"description"` chứ?
- [ ] Cú pháp JSON hợp lệ, không có dấu phẩy thừa (trailing comma)?
- [ ] Đã bao gồm đầy đủ 100% các từ trong danh sách cung cấp chưa?
---

itch / itchy : cảm giác ngứa / ngứa ngáy (an unpleasant feeling on your skin that makes you want to scratch; causing an itch)

scratch : gãi ngứa (to rub your nails back and forth against the skin to relieve an itch)

itchy jumper : áo len gây ngứa ngáy (a knitted sweater that causes an uncomfortable, prickly sensation on the skin)

loads and loads : rất nhiều, vô số (a large amount or number of something, used informally for emphasis)

hairy : rậm lông, có nhiều lông/tóc (covered with a lot of hair)

unpack : giải thích chi tiết, làm rõ (to explain an idea, concept, or complex topic in clear detail)

parasite : ký sinh trùng (an animal or plant that lives on or inside another organism and feeds on it)


catch a scratch : bị "lây" phản xạ gãi ngứa (to pick up or develop the urge to scratch after seeing or hearing someone else scratch, similar to catching an illness)

scalp : da đầu (the skin covering the head, usually covered with hair)

be spot on : hoàn toàn chính xác, chuẩn xác (to be completely accurate or correct)
