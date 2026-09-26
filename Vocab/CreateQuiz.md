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

cement : xi măng (a grey powder that sets hard after being mixed with water, sand, and gravel, used in building)

concrete : bê tông (a hard building material made by mixing cement, sand, gravel, and water)

aggravate : làm trầm trọng thêm (to make a situation, problem, or feeling worse or more severe, often by adding to it or intensifying it)

scramble for something : cuộc tranh giành cái gì đó (a struggle or competition with others to obtain or achieve something, often in a hurried or chaotic manner)

underpin : củng cố, làm vững chắc (to support, strengthen, or justify something, often by providing evidence, reasoning, or additional information)

sheer : hoàn toàn, tuyệt đối (complete or absolute, often indicating a high degree or intensity of something)

in abundance : với số lượng lớn, dồi dào (existing or available in large quantities, often indicating plenty or excess)

thermal expansion : sự giãn nở nhiệt (the increase in size or volume of a material or substance due to an increase in temperature, often resulting in expansion or deformation)

straightforward : đơn giản, dễ hiểu (easy to understand or do, often indicating clarity or simplicity)

susceptible : dễ bị ảnh hưởng, dễ bị tác động (likely to be influenced, affected, or harmed by something, often indicating vulnerability or sensitivity)

adhesive : chất kết dính (a substance used to bond or stick materials together, often providing adhesion or cohesion)

crosswise : theo chiều ngang (in a direction or orientation that is perpendicular to the length or main axis of something, often indicating a horizontal arrangement)

vice-president : phó chủ tịch (a person who holds a position of authority or leadership in an organization, often serving as a deputy or second-in-command to the president or leader)

Finland : Phần Lan (a country in Northern Europe, known for its high quality of life, education system, and natural landscapes)

ash and slag : tro và xỉ (the solid residue left after the combustion of a material, often consisting of ash and other byproducts)

iron ore : quặng sắt (a naturally occurring mineral from which iron can be extracted, often used in the production of steel and other iron-based products)

byproduct : sản phẩm phụ (a secondary product or result that is produced in addition to the main product, often as a byproduct of a process or activity)

power plant : nhà máy điện (a facility that generates electricity, often using various energy sources such as fossil fuels, nuclear energy, or renewable resources)

content : hàm lượng (the amount or proportion of a substance or component present in a mixture, material, or product, often indicating its composition or concentration)

resistance : sự phản đối, sự kháng cự (the ability to withstand or oppose something, often indicating strength, durability, or opposition to change or influence)
