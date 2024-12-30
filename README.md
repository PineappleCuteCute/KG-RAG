<p align="center">
  <img src="https://github.com/BaranziniLab/KG_RAG/assets/42702311/0b2f5b42-761e-4d5b-8d6f-77c8b965f017" width="450">
</p>

## Mục lục

[KG-RAG là gì?](https://github.com/BaranziniLab/KG_RAG#what-is-kg-rag)  
[Ví dụ về ứng dụng KG-RAG](https://github.com/BaranziniLab/KG_RAG#example-use-case-of-kg-rag)  
 - [Dùng GPT mà không có KG-RAG](https://github.com/BaranziniLab/KG_RAG#without-kg-rag)  
 - [Dùng GPT với KG-RAG](https://github.com/BaranziniLab/KG_RAG#with-kg-rag)  
 - [Notebook minh họa](https://github.com/BaranziniLab/KG_RAG/blob/main/notebooks/kg_rag_based_gpt_prompts.ipynb)  

[Cách chạy KG-RAG](https://github.com/BaranziniLab/KG_RAG#how-to-run-kg-rag)  
 - [Bước 1: Clone kho lưu trữ](https://github.com/BaranziniLab/KG_RAG#step-1-clone-the-repo)  
 - [Bước 2: Tạo môi trường ảo](https://github.com/BaranziniLab/KG_RAG#step-2-create-a-virtual-environment)  
 - [Bước 3: Cài đặt các thư viện](https://github.com/BaranziniLab/KG_RAG#step-3-install-dependencies)  
 - [Bước 4: Cập nhật file config.yaml](https://github.com/BaranziniLab/KG_RAG#step-4-update-configyaml)  
 - [Bước 5: Chạy script thiết lập](https://github.com/BaranziniLab/KG_RAG#step-5-run-the-setup-script)  
 - [Bước 6: Chạy KG-RAG từ terminal](https://github.com/BaranziniLab/KG_RAG#step-6-run-kg-rag-from-your-terminal)  
    - [Sử dụng GPT](https://github.com/BaranziniLab/KG_RAG#using-gpt)  
    - [Sử dụng chế độ tương tác của GPT](https://github.com/BaranziniLab/KG_RAG/blob/main/README.md#using-gpt-interactive-mode)  
    - [Sử dụng Llama](https://github.com/BaranziniLab/KG_RAG#using-llama)  
    - [Sử dụng chế độ tương tác của Llama](https://github.com/BaranziniLab/KG_RAG/blob/main/README.md#using-llama-interactive-mode)  
 - [Tham số dòng lệnh](https://github.com/BaranziniLab/KG_RAG?tab=readme-ov-file#command-line-arguments-for-kg-rag)  

[BiomixQA: Dataset chuẩn](https://github.com/BaranziniLab/KG_RAG/tree/main?tab=readme-ov-file#biomixqa-benchmark-dataset)  

[Trích dẫn](https://github.com/BaranziniLab/KG_RAG/blob/main/README.md#citation)  

---

### KG-RAG là gì?

KG-RAG là viết tắt của "Knowledge Graph-based Retrieval Augmented Generation" (Truy xuất và Tạo dữ liệu tăng cường dựa trên Đồ thị Tri thức).

#### Bắt đầu bằng cách xem video giới thiệu KG-RAG:

<video src="https://github.com/BaranziniLab/KG_RAG/assets/42702311/86e5b8a3-eb58-4648-95a4-271e9c69b4ed" controls="controls" style="max-width: 730px;"></video>

KG-RAG là một khung công việc linh hoạt, kết hợp tri thức tường minh từ Đồ thị Tri thức (Knowledge Graph - KG) với tri thức ngầm từ Mô hình Ngôn ngữ Lớn (LLM). Chi tiết trong bài [arXiv](https://arxiv.org/abs/2311.17330).

Trong ứng dụng, chúng tôi sử dụng một KG y sinh đồ sộ mang tên [SPOKE](https://spoke.ucsf.edu/) để cung cấp ngữ cảnh y sinh. SPOKE bao gồm hơn 40 cơ sở dữ liệu y sinh từ nhiều lĩnh vực, tập trung vào các khái niệm như gen, protein, thuốc, bệnh và các mối quan hệ của chúng. SPOKE có hơn 27 triệu nút và 53 triệu cạnh [[Tham khảo](https://doi.org/10.1093/bioinformatics/btad080)].
