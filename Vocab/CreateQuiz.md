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

unwitting : vô tình, không biết (not aware of the full facts; not intended or planned)

close call : suýt toang (a situation in which a dangerous or undesirable outcome is narrowly avoided)

heartthrob : người trong mộng (a person, often a celebrity, who is very attractive and admired by many people)

assertive : quyết đoán, tự tin (having or showing a confident and forceful personality; able to express oneself effectively)

doesn't seem all that different : dường như không khác biệt lắm (appearing to be similar or not significantly distinct from something else)

possessive emotions : cảm xúc chiếm hữu (feelings of jealousy or desire to control someone or something, often in a romantic context)

unknowingly : vô tình, không biết (without being aware of the facts or consequences; unintentionally)

something after something : hết cái này đến cái khác (a sequence of repeated people, events, or things occurring one after another)

make a move on someone : chủ động tiếp cận, tán tỉnh ai (to take action to initiate a romantic or sexual relationship with someone)

makeup caked on : lớp trang điểm dày cộp (makeup that has been applied in excessive amounts, often resulting in a heavy or unnatural appearance)

a sheen of sweat : một lớp mồ hôi (a thin layer of perspiration on the skin, often indicating physical exertion or nervousness)

seep through : thấm qua, rỉ ra (to pass slowly through small openings or pores; to leak or ooze out)

agonize over something : đau khổ, dằn vặt, trăn trở về điều gì (to suffer mentally or emotionally over a difficult decision or situation)

countermeasure : biện pháp đối phó, biện pháp phòng ngừa (an action taken to counteract or prevent a negative effect or threat)

slip past : lẻn qua, lách qua (to move quietly and quickly past someone or something without being noticed)

on the verge of : trên bờ vực, sắp sửa (very close to experiencing or achieving something, often implying a critical or dangerous point)

let out a grunt : kêu hự một tiếng, phát ra tiếng hừ/thở hắt ra (to make a low, guttural sound, often expressing physical impact, discomfort, or exertion)

charge into : lao vào, xông vào (to rush forward aggressively or with determination, often into a situation or conflict)

be harder than it looks to me: khó hơn tôi tưởng (to perceive something as more difficult than it appears to others)

shorts : quần đùi, quần soóc (a garment worn on the lower body that covers the hips and upper legs, typically ending above the knee)

skew / skewed :  chênh lệch (to distort or make uneven; unevenly balanced, e.g. a skewed gender ratio)

run into situations : gặp phải tình huống (to encounter or experience situations, often unexpectedly or by chance)
