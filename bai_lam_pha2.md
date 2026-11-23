# BÀI LÀM PHA 2 (ĐỀ LUYỆN TẬP CHỦ ĐỀ TÀI CHÍNH CÁ NHÂN)

- **Họ tên:** nguyễn công vinh
- **Lớp:** cntt3 
- **Link repository Pha2:**https://github.com/vinhduy200608-wq/HN-KS26-CNTT1_PromptAI_H03_Pha1.git
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đăng ký hội thảo ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": "DT",
    "ngay_su_kien": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "hang_ve": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "CB",
    "ngay_su_kien": "2027-01-10",
    "nguoi_lon": 3,
    "tre_em": 0,
    "hang_ve": "thuong",
    "ghi_chu": "Có một người dùng xe lăn cần lối đi riêng"
  },
  {
    "ma_goi": "VIP",
    "ngay_su_kien": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "hang_ve": "vip",
    "ghi_chu": "có một anh mắt kém cần ngồi bàn đầu gần màn hình chiếu"
  }
]
```

**Link trò chuyện:** https://share.gemini.google/u5q1MhlKca1O

## 4.3. Báo giá vé hội thảo bằng Chain-of-Thought

**KET QUA AI**

```text
**Bước 1: Tiền người lớn**
Khách hàng chọn gói DT (Gói Đầu Tư) có đơn giá 1.500.000 đồng/người lớn. Nhóm có 4 người lớn:

$$4 \times 1.500.000 = 6.000.000\text{ đồng}$$

**Bước 2: Tiền trẻ em**
Nhóm có 3 trẻ em gồm:

* 2 trẻ em (8 tuổi và 11 tuổi) thuộc độ tuổi từ 6 đến 12 tuổi, tính 50% giá người lớn: $1.500.000 \times 50\% = 750.000\text{ đồng/trẻ}$.
* 1 bé 4 tuổi thuộc độ tuổi dưới 6 tuổi nên được miễn phí (0 đồng).
Tổng tiền vé trẻ em là:

$$(2 \times 750.000) + (1 \times 0) = 1.500.000\text{ đồng}$$

**Bước 3: Tiền vé (Tổng tiền vé người lớn và trẻ em)**

$$6.000.000 + 1.500.000 = 7.500.000\text{ đồng}$$

**Bước 4: Giảm giá nhóm**
Theo quy tắc, nhóm có từ 4 người lớn trở lên được giảm 10% trên tiền vé (tiền người lớn + tiền trẻ em). Nhóm khách hàng có đủ 4 người lớn nên thỏa mãn điều kiện giảm giá:

* Số tiền được giảm: $7.500.000 \times 10\% = 750.000\text{ đồng}$
* Tiền vé sau giảm: $7.500.000 - 750.000 = 6.750.000\text{ đồng}$

**Bước 5: Phụ thu sổ tay**
Đơn giá bộ sổ tay lập kế hoạch tài chính cá nhân là 200.000 đồng/bộ và không áp dụng giảm giá. Nhóm đặt mua 2 bộ:

$$2 \times 200.000 = 400.000\text{ đồng}$$

**Bước 6: Tổng tiền cuối cùng**

$$\text{Tổng tiền} = \text{Tiền vé sau giảm} + \text{Phụ thu} = 6.750.000 + 400.000 = 7.150.000\text{ đồng}$$

[RESULT: 7.150.000 đồng]
```

**Link trò chuyện:** https://share.gemini.google/6fXugLZI5gWs

### b) Kiểm tra kết quả AI

ai làm ra kết quả đúng 

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_khu_vuc",
  "so_khach": 2,
  "so_hiep_bi_anh_huong": 2,
  "tom_tat": "Khách mua gói DT bị xếp ngồi ghế phụ thiếu bàn viết và ổ cắm trong 2 phiên học đầu."
}
```

**Link trò chuyện:** https://share.gemini.google/reon8V9ajzZC

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **1. Tính chính xác về thông tin & chính sách** (Trọng số: 40% / 4.0 điểm) | 0.0/4.0 | **Lỗi 1:** Câu bị lỗi: *"Vé gói Đầu Tư bên em giá chỉ 1.200.000đ/người thôi"* – Lý do sai: Giá vé gói DT (Gói Đầu Tư) theo thông tin chuẩn là 1.500.000 đồng/người lớn, báo sai thành 1.200.000đ/người. **Lỗi 2:** Câu bị lỗi: *"đi học về đầu tư chứng khoán lời khủng luôn ạ."* – Lý do sai: Cam kết/khẳng định "lời khủng" về đầu tư là không có căn cứ trong thông tin chuẩn và mang tính phóng đại rủi ro tài chính. **Lỗi 3:** Câu bị lỗi: *"Anh/chị báo huỷ trước 4 ngày thì bên em hoàn lại đủ 100% tiền vé nha"* – Lý do sai: Theo chính sách huỷ vé chuẩn, huỷ trước từ 3 đến 6 ngày chỉ được hoàn 50% tiền vé (hoàn 100% áp dụng khi huỷ trước từ 7 ngày trở lên). | **Lỗi 1:** *"Vé gói Đầu Tư (Gói DT) của chương trình có giá 1.500.000 đồng/người lớn ạ."* **Lỗi 2:** *"Hội thảo cung cấp kiến thức và góc nhìn giúp anh/chị chủ động hơn trong quá trình tìm hiểu đầu tư."* **Lỗi 3:** *"Nếu anh/chị huỷ vé trước ngày hội thảo từ 3 đến 6 ngày, Ban tổ chức sẽ hoàn lại 50% giá trị vé ạ."* |
| **2. Tính đầy đủ & đáp ứng đúng câu hỏi/nhu cầu khách hàng** (Trọng số: 30% / 3.0 điểm) | 1.0/3.0 | **Lỗi 1:** Câu bị lỗi: *"Vé gói Đầu Tư bên em giá chỉ 1.200.000đ/người thôi, đi học về đầu tư chứng khoán lời khủng luôn ạ. Anh/chị báo huỷ trước 4 ngày thì bên em hoàn lại đủ 100% tiền vé nha, cứ yên tâm chốt đơn đi ạ!"* – Lý do sai: Trả lời thiếu đầy đủ và sai lệch các quy định hoàn huỷ (không nêu rõ các mốc 7 ngày trở lên hoàn 100%, 3–6 ngày hoàn 50%, dưới 3 ngày không hoàn tiền), đồng thời không làm rõ đối tượng áp dụng giá vé là "người lớn" theo thông tin chuẩn. | *"Gói Đầu Tư (gói DT) có mức giá 1.500.000 đồng/người lớn. Về chính sách huỷ vé, Ban tổ chức hoàn 100% nếu huỷ trước ngày hội thảo từ 7 ngày trở lên, hoàn 50% nếu huỷ trước từ 3 đến 6 ngày, và không hoàn tiền nếu huỷ dưới 3 ngày ạ."* |
| **3. Thái độ, văn phong & cách trình bày chuyên nghiệp** (Trọng số: 30% / 3.0 điểm) | 1.5/3.0 | **Lỗi 1:** Câu bị lỗi: *"Dạ chào anh/chị nha! ... bên em hoàn lại đủ 100% tiền vé nha, cứ yên tâm chốt đơn đi ạ!"* – Lý do sai: Văn phong quá suồng sã, dùng từ cảm thán/khẩu ngữ kém trang trọng ("nha", "lời khủng", "chốt đơn đi ạ") trong ngữ cảnh tư vấn hội thảo tài chính chuyên nghiệp. | *"Dạ em chào anh/chị ạ! Em xin gửi anh/chị thông tin chi tiết về gói Đầu Tư và chính sách huỷ vé của hội thảo để anh/chị cân nhắc ạ."* |
| **Tổng điểm** | **2.5/10** | Có 3 lỗi thông tin/chính sách ở Tiêu chí 1, thiếu đầy đủ quy định chính sách ở Tiêu chí 2, và văn phong chưa đủ chuyên nghiệp ở Tiêu chí 3. | Chuẩn hoá lại toàn bộ số liệu giá vé, điều kiện hoàn tiền theo từng mốc ngày và sử dụng văn phong tư vấn lịch sự, rõ ràng. |
```

**Link trò chuyện:** https://share.gemini.google/C1vYlA4v1Bry
