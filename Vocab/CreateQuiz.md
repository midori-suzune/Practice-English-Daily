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

precast : đúc sẵn (to create or form something in advance, often indicating preparation or pre-fabrication for later use)

set on somewhere : đặt ở đâu đó (to place or position something in a specific location, often indicating intention or arrangement)

tile : gạch lát (a thin, flat piece of material used for covering floors, walls, or roofs, often indicating construction or decoration)

stoneware tile : gạch sứ, gạch gốm đá (a type of ceramic tile made from stoneware clay, often indicating durability and water resistance for flooring or wall applications)

paper-mill : nhà máy giấy (a facility where paper is produced from raw materials, often indicating industrial production or manufacturing)

exterior : ngoại thất (the outside part of a building, vehicle, or structure, often indicating design, appearance, or protection from the elements)

clad with : được bao phủ bằng, được ốp bằng (to cover or encase something with a layer of material, often indicating protection, insulation, or aesthetic enhancement)

quarry : khai thác đá (to extract stone, minerals, or other materials from a quarry, often indicating mining or construction activities)

performance venue : địa điểm biểu diễn (a location or facility where performances, events, or shows are held, often indicating entertainment or cultural activities)

grand setting : bối cảnh hoành tráng (an impressive or magnificent environment or backdrop, often indicating grandeur or splendor)

deliver : mang lại (to provide or present something, often indicating the act of giving or conveying a message, service, or product)

acoustics : chất lượng âm thanh, âm học (the properties or qualities of a room or building that determine how sound is transmitted in it)

forecourt : sân trước (an open area in front of a building or structure, often indicating a space for gathering, parking, or access)

ascend to : đi lên, leo lên (to move or climb upward, often indicating progression or elevation to a higher position or level)

re-engage : tái tham gia, tái hợp tác (to become involved or participate again in an activity, event, or process, often indicating renewed interest or commitment)

alteration : sự thay đổi, sự sửa đổi (the act or process of making changes or modifications, often indicating adjustment or transformation)

colonnade : hàng cột (a row of columns supporting a roof or structure, often indicating architectural design or classical style)

shade : che chắn, che bóng mát (to block or reduce light, often indicating protection from sunlight or creating a cooler environment)

patron : khách hàng quen (regular customer or supporter of a business, organization, or establishment, often indicating loyalty or frequent engagement)
