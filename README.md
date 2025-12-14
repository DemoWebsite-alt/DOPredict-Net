🧬 DO-Predict Net
Decision Oncology Prediction Network
DO-Predict Net là hệ thống hỗ trợ ra quyết định điều trị ung thư dựa trên đột biến gen – thông tin lâm sàng – loại ung thư – giai đoạn bệnh, được thiết kế để mô phỏng một mạng tri thức ung thư (oncology decision network) phục vụ nghiên cứu, thử nghiệm mô hình AI và xây dựng hệ thống hỗ trợ lâm sàng.

🎯 Mục tiêu hệ thống
Chuẩn hóa dữ liệu ung thư theo hướng gen – đột biến – bối cảnh lâm sàng
Hỗ trợ dự đoán/đề xuất thuốc và phác đồ điều trị
Làm tập dữ liệu nền cho:
Hệ thống hỏi đáp y sinh (Biomedical QA)
Demo hệ thống hỗ trợ quyết định điều trị ung thư

🧠 Phạm vi dữ liệu
Hệ thống hiện bao gồm:
Thành phần	              Số lượng
🧬 Gene	                  321 mã gene
🧪 Loại đột biến	        313 loại đột biến
🎗️ Loại ung thư	          153 loại ung thư
📊 Giai đoạn ung thư	    17 giai đoạn
📁 Ca bệnh mẫu	          500 trường hợp ung thư

🗂️ Cấu trúc dữ liệu
Mỗi ca bệnh được lưu dưới dạng JSON, mô tả đầy đủ yếu tố sinh học phân tử và lâm sàng.
📄 Ví dụ một mẫu dữ liệu
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

🧩 Ý nghĩa các trường dữ liệu
Trường	                  Mô tả
id	                      Mã định danh ca bệnh
gene	                    Gene đích có liên quan
mutation	                Đột biến cụ thể (chuẩn y sinh)
clinical_info	            Thông tin lâm sàng tóm tắt (tuổi, giới, thể trạng, điều trị trước đó…)
cancer_type	              Loại ung thư (tiếng Việt)
stage	                    Giai đoạn bệnh
recommended_drug	        Thuốc điều trị chính được đề xuất
recommended_combination	  Phác đồ hoặc phối hợp điều trị
drug_effectiveness_info  	Cơ sở sinh học – lâm sàng của quyết định điều trị

🧪 Nguyên tắc xây dựng dữ liệu
Dựa trên y văn ung thư học hiện đại (NCCN, ESMO, FDA approvals)
Gắn kết đột biến → cơ chế sinh học → đáp ứng thuốc
Không chứa thông tin bệnh nhân thật
Phục vụ nghiên cứu – mô phỏng – giáo dục

🚀 Ứng dụng tiềm năng
🔍 Hệ thống hỏi đáp y sinh (Biomedical QA)
🧠 AI hỗ trợ quyết định điều trị
📊 Huấn luyện mô hình GraphRAG / Retrieval-Augmented Generation
🧪 Demo web y sinh (DOPredict-Net UI)
🎓 Đào tạo sinh viên CNTT – y sinh – khoa học dữ liệu

⚠️ Lưu ý

DO-Predict Net không thay thế quyết định lâm sàng.
Mọi thông tin chỉ phục vụ mục đích nghiên cứu, học tập và thử nghiệm mô hình AI.
