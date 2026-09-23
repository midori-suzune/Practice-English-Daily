Tôi sẽ gửi LIST TỪ VỰNG IELTS. Hãy chuyển đổi danh sách này thành chuỗi JSON chuẩn hóa để import trực tiếp vào thẻ Flashcard theo đúng cấu trúc bên dưới.

QUY TẮC ĐỊNH DẠNG (BẮT BUỘC):
1. ĐẦU RA: Chỉ xuất ra DUY NHẤT 1 block JSON hợp lệ (Valid JSON). TUYỆT ĐỐI KHÔNG thêm văn bản giải thích ngoài JSON.
2. CÁC TRƯỜNG TRONG JSON KHỚP 100% VỚI FLASHCARD UI:
   - `term` (Thuật ngữ): Từ/cụm từ tiếng Anh gốc (giữ nguyên không đổi).
   - `definition` (Định nghĩa): Định nghĩa tiếng Anh ngắn gọn, dễ hiểu kèm nghĩa tiếng Việt phải dựa theo note mà tôi cung câp trong ngoặc: `<Định nghĩa tiếng Anh súc tích>. (<Nghĩa tiếng Việt phải theo note cung cấp >)`.
   - `pronounce` (Phát âm): Phiên âm IPA chuẩn quốc tế.
   - `word_type` (Loại từ): Từ loại tiếng Anh (e.g. "verb phrase", "noun phrase", "phrasal verb", "phrase", "idiom",...).
   - `example` (Ví dụ): 1 câu ví dụ tiếng Anh tự nhiên, sinh động, chuẩn ngữ pháp, gắn với ngữ cảnh đời sống/học tập/công việc thực tế  , ko áp dúng quá nhiều từ vựng chuyên ngành , ví dụ đơn giản dễ  hiểu có liên quan đến thuật ngữ .
   - `synonyms` (Từ đồng nghĩa): Mảng các chuỗi (Array of strings) chứa 1-2 từ/cụm từ đồng nghĩa phổ biến BẰNG TIẾNG ANH (e.g. `["maintain health", "keep fit"]`). KHÔNG DÙNG TIẾNG VIỆT Ở ĐÂY.

VÍ DỤ MẪU JSON CHUẨN FLASHCARD:
{
  "title": "IELTS Vocabulary Flashcards",
  "words": [
    {
      "term": "staple food",
      "definition": "A food that makes up the main part of a person's regular diet (Lương thực chính, thực phẩm thiết yếu hàng ngày).",
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
---

be in shape : thể lực tốt (to be physically fit and healthy, often through regular exercise and proper nutrition)

ride : chuyến đi (a journey made on or in a vehicle, such as a bicycle, motorcycle, or car, often for leisure or transportation)

leisurely : nhàn nhã, thong thả (relaxed and unhurried, often associated with leisure activities or a calm lifestyle)

trail : đường mòn (a path or track, often in a natural setting, used for walking, hiking, or biking)

make lavish use of something : sử dụng nhiều / dồi dào cái gì đó (to use something generously, abundantly, or in large quantities)

sound fabulous : nghe tuyệt vời (to seem or appear extremely impressive, attractive, or enjoyable when described or heard)

vigilant : cảnh giác, cẩn thận (always alert and watchful, especially in order to detect or prevent danger or problems)

under threat : đang bị đe dọa (being in a situation where there is a risk of harm, danger, or negative consequences)

be of one mind : đồng lòng, nhất trí (to share the same opinion, belief, or perspective with others, often indicating agreement or unity in thought)

massacre : cuộc thảm sát (the deliberate and brutal killing of a large number of people, often in a violent or indiscriminate manner)

confront : đối mặt (to face or deal with a difficult situation, challenge, or person directly, often requiring courage or determination)

phenomenally : phi thường (to an extraordinary or exceptional degree, often used to describe remarkable abilities, achievements, or events)
