[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23574190&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** phamminhkhoi.05.09.12@gmail.com
**Name:** Phạm Minh Khôi

---

## Mo ta

Bài Lab này tập trung vào việc xây dựng một luồng dữ liệu tự động (ETL Pipeline) bao gồm các bước Extract, Validate, Transform và Load. Mục tiêu là làm sạch dữ liệu thô, loại bỏ các bản ghi lỗi (giá âm, rỗng) và chuẩn hóa dữ liệu trước khi nạp vào hệ thống. Đồng thời, bài Lab cũng thực hiện Stress Test để quan sát mức độ ảnh hưởng của dữ liệu rác (Garbage Data) so với dữ liệu sạch (Clean Data) đối với độ chính xác của AI Agent.

---

## Cach chay (How to Run)

### Prerequisites
Cài đặt các thư viện cần thiết trước khi chạy:
```bash
pip install pandas pytest