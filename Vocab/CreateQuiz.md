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
    }
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


just off + place : ngay gần đâu đó (located very close to a specific place or location, often indicating proximity or convenience)

It works out at + number : tổng cộng là (used to indicate the total amount or result of a calculation, often expressed in numerical terms)

get on : tiến triển , làm ăn (to progress or succeed in a particular activity or endeavor, often indicating positive development or achievement)

at + [time] + sharp : đúng ... giờ (at the exact or precise time, often indicating punctuality or timeliness)

sort something out : sắp xếp, giải quyết (to organize or resolve a situation or problem, often requiring effort or planning)

turn up : xuất hiện (to arrive or appear at a place or event, often unexpectedly or without prior notice)

overhead : mái che (a structure or covering that provides shelter or protection from above, often used in outdoor settings)

sandbag : bao cát (a bag filled with sand, often used for flood control, military fortifications, or construction purposes)

weigh something down : chèn/đè vật gì xuống cho nặng (to place a heavy object on something to keep it in place or prevent it from moving/blowing away)

socket : ổ cắm (a device or receptacle that allows electrical plugs to connect to a power source, often used for providing electricity to appliances or devices)

have a word with someone : nói chuyện riêng , nhắc nhở ai đó (to have a private conversation or discussion with someone, often to convey important information or advice)

email something : gửi cái gì qua email (to send a message or document electronically via email, often for communication or information sharing)

email someone something : gửi cái gì cho ai qua email (to send a message or document electronically to a specific person via email, often for communication or information sharing)

food hygiene : vệ sinh an toàn thực phẩm (the practice of maintaining cleanliness and safety in the handling, preparation, and storage of food to prevent contamination and ensure it is safe for consumption)

something sits with the council : cái gì thuộc về hội đồng (to be under the jurisdiction or responsibility of a local government council, often indicating administrative oversight or decision-making authority)

that side of it : phần việc đó (the aspect or part of a situation or issue, often indicating a specific perspective or responsibility)

take care of : lo liệu , xử lý (to manage or handle a task, responsibility, or situation, often indicating attention and diligence)

jar : lọ (a container, often made of glass or ceramic, used for storing food, liquids, or other substances, typically with a wide mouth and a lid)

send something over : gửi cái gì qua (to transmit or deliver something to another person or location, often indicating the act of sending an item or information)

go up : đăng lên (to post or upload content to a website or platform, often indicating the act of making information publicly accessible online)

insurance cover : mức , gói bảo hiểm (the extent or type of protection provided by an insurance policy, often indicating the scope of coverage for specific risks or events)
