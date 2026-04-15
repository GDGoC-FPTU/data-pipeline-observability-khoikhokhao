# Experiment Report: Data Quality Impact on AI Agent

**Name:** Phạm Minh Khôi
**Date:** 15/04/2026

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Agent: Based on my data, the best choice is Laptop at $1200. | 10 | Phản hồi chính xác dựa trên tập dữ liệu đã được làm sạch và chuẩn hóa. |
| Garbage Data (`garbage_data.csv`) | Agent: Based on my data, the best choice is Nuclear Reactor at $999999. | 1 | Phản hồi sai lệch hoàn toàn do bị nhiễu bởi dữ liệu rác. |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Khi sử dụng bộ dữ liệu Garbage Data, AI Agent đã đưa ra câu trả lời sai lệch hoàn toàn vì logic cốt lõi của nó là tìm kiếm sản phẩm có giá cao nhất trong nhóm danh mục "electronics". Bộ dữ liệu rác chưa qua xử lý chứa một Outlier (dữ liệu ngoại lai) cực đoan là "Nuclear Reactor" với mức giá khổng lồ là 999999. Bên cạnh đó, dữ liệu rác còn chứa các vấn đề nghiêm trọng khác cản trở mô hình như Duplicate IDs (id trùng lặp gây nhiễu), Wrong types (sai kiểu dữ liệu ở trường giá), và Null values (thiếu hụt dữ liệu). Điều này minh chứng rằng nếu không có ETL Pipeline lọc dữ liệu ngay từ đầu, AI Agent sẽ hấp thụ và phản hồi dựa trên những thông tin độc hại, dẫn đến quyết định sai lầm.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** Đồng ý hoàn toàn. Một prompt dù có hoàn hảo đến đâu cũng không thể bù đắp cho một bộ dữ liệu đầu vào chứa đầy rác (Garbage in, Garbage out). Dữ liệu chất lượng cao là nền tảng cốt lõi để đảm bảo độ tin cậy và tính chính xác của bất kỳ AI Agent nào.