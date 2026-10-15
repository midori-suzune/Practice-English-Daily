Tôi sẽ gửi LIST TỪ VỰNG IELTS. Hãy chuyển đổi danh sách này thành chuỗi JSON chuẩn hóa để import trực tiếp vào thẻ Flashcard theo đúng cấu trúc bên dưới.

QUY TẮC ĐỊNH DẠNG (BẮT BUỘC):
1. ĐẦU RA: Chỉ xuất ra DUY NHẤT 1 block JSON hợp lệ (Valid JSON). TUYỆT ĐỐI KHÔNG thêm văn bản giải thích ngoài JSON.
2. CẤU TRÚC JSON CỐ ĐỊNH (STRICT SCHEMA - CẤM TỰ Ý THÊM TRƯỜNG):
   - Cấp cao nhất (Root) CHỈ ĐƯỢC CHỨA ĐÚNG 2 KEY: `"title"` và `"words"`. TUYỆT ĐỐI KHÔNG thêm `"description"` hay bất kỳ trường nào khác.
   - Mỗi item trong `"words"` CHỈ ĐƯỢC CHỨA ĐÚNG 6 KEY sau:
     * `term`: Từ/cụm từ tiếng Anh gốc (giữ nguyên không đổi).
     * `definition`: Lấy định nghĩa tiếng Anh kèm nghĩa tiếng Việt theo đúng cấu trúc: `<Định nghĩa tiếng Anh>. (<Nghĩa tiếng Việt>)`. Bắt buộc có dấu chấm `.` kết thúc câu tiếng Anh trước khi mở ngoặc `(<Nghĩa tiếng Việt>)`.
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
ĐỊNH DẠNG ĐẦU VÀO:
term : định nghĩa tiếng Anh (nghĩa tiếng Việt)

convince somebody : to persuade or influence someone to believe or do something, often indicating a change in opinion or behavior (thuyết phục ai đó)

courtyard : an open area enclosed by the walls of a building or complex, often indicating a space for outdoor activities or gatherings (sân trong)

commoner : a person who is not of noble rank or status, often indicating an ordinary or average individual (dân thường)

enroll under the status of something : to register or join an institution, organization, or program with a specific designation or classification, often indicating a formal affiliation or membership (nhập học với tư cách là)

slowpoke : a person who is slow to act, respond, or understand, often indicating a lack of quickness or alertness (người chậm chạp)

commotion : a state of excitement, disturbance, or agitation, often indicating a situation of confusion or unrest (náo động, xôn xao)



