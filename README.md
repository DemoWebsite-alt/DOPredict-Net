# 🧬 DO-Predict Net  
**Decision Oncology Prediction Network**

DO-Predict Net là hệ thống hỗ trợ ra quyết định điều trị ung thư dựa trên **đột biến gen – thông tin lâm sàng – loại ung thư – giai đoạn bệnh**.  
Hệ thống được thiết kế nhằm mô phỏng một **mạng tri thức ung thư (oncology decision network)**, phục vụ nghiên cứu, thử nghiệm mô hình AI và xây dựng hệ thống hỗ trợ lâm sàng.

---

## 🎯 Mục tiêu hệ thống
- Chuẩn hóa dữ liệu ung thư theo hướng **gene – đột biến – bối cảnh lâm sàng**
- Hỗ trợ **dự đoán / đề xuất thuốc và phác đồ điều trị**
- Làm tập dữ liệu nền cho:
  - Hệ thống hỏi đáp y sinh (Biomedical QA)
  - Mô hình AI hỗ trợ quyết định điều trị ung thư
  - Demo hệ thống lâm sàng (DOPredict-Net UI)

---

## 🧠 Phạm vi dữ liệu
Hệ thống hiện bao gồm:

- 🧬 **321 mã gene**
- 🧪 **313 loại đột biến**
- 🎗️ **153 loại ung thư**
- 📊 **17 giai đoạn ung thư**
- 📁 **500 ca bệnh mẫu**

---

## 🗂️ Cấu trúc dữ liệu
Mỗi ca bệnh được lưu dưới dạng **JSON**, mô tả đầy đủ yếu tố sinh học phân tử và lâm sàng.

### 📄 Ví dụ một mẫu dữ liệu
```json
{
  "id": 1,
  "gene": "BRCA1",
  "mutation": "BRCA1 c.5266dupC",
  "clinical_info": "Nữ, 58 tuổi; Karnofsky 80%; đã phẫu thuật cắt tử cung - buồng trứng tối ưu (residual ≤1 cm); hoàn thành 6 chu kỳ platinum-taxane; platinum-sensitive.",
  "cancer_type": "Ung thư buồng trứng biểu mô",
  "stage": "Giai đoạn III",
  "recommended_drug": "Olaparib (Lynparza) — liệu pháp bảo trì",
  "recommended_combination": [
    "Olaparib duy trì",
    "Bevacizumab duy trì (nếu không chống chỉ định)"
  ],
  "drug_effectiveness_info": "Đột biến BRCA1 làm suy giảm HRR, tăng nhạy với PARP inhibitor. Kéo dài PFS rõ rệt trong SOLO1. Cần theo dõi thiếu máu, giảm BC, chức năng thận."
}
```

---

## 🧪 Nguyên tắc xây dựng dữ liệu
- Dựa trên y văn ung thư học hiện đại (NCCN, ESMO, FDA approvals)
- Liên kết đột biến → cơ chế sinh học → đáp ứng thuốc
- Không chứa dữ liệu bệnh nhân thật
- Phục vụ nghiên cứu – học tập – thử nghiệm AI
