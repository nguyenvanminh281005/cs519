<p align="center">
  <a href="https://www.uit.edu.vn/">
    <img src="https://www.uit.edu.vn/sites/vi/files/banner.png" alt="UIT Banner">
  </a>
</p>

<h1 align="center"><b>CS519.Q11.KHTN – Scientific Research Methodology</b></h1>

---

## 📌 Project Title (Vietnamese)

**XÂY DỰNG PHƯƠNG THỨC TÌM KIẾM MẠNG NƠ-RON ĐA KIẾN TRÚC TỰ ĐỘNG (NAS)
SỬ DỤNG ZERO-SHOT DỰA TRÊN KHÔNG GIAN TÌM KIẾM ĐA KIẾN TRÚC**

## 📌 Project Title (English)

**Zero-shot Neural Architecture Search in Hybrid Search Space**

---

## 👨‍🎓 Team Members

* [**Nguyễn Văn Minh**](https://www.facebook.com/nguyenvanminh281005) – 23520945
* [**Nguyễn Văn Hồng Thái**](https://www.facebook.com/hongthai1105z) – 23521418

---

## 🔗 Project Links

* **GitHub Repository**:
  👉 [CS519.Q11.KHTN – Scientific Research Methodology](https://github.com/nguyenvanminh281005/cs519)

* **YouTube Presentation Video**:
  👉 *(Updating)*
* **Slides**:
  👉 [Slide](https://github.com/nguyenvanminh281005/cs519/blob/main/Slides.pdf)
* **Proposal**:
  👉 [Proposal](https://github.com/nguyenvanminh281005/cs519/blob/main/Proposal.pdf)
* **Poster**:
  👉 [Poster](https://github.com/nguyenvanminh281005/cs519/blob/main/Poster.pdf)

---

## 🧠 Abstract

Thiết kế kiến trúc mạng nơ-ron hiệu quả đòi hỏi nhiều kinh nghiệm và chi phí tính toán lớn.
Các phương pháp Neural Architecture Search (NAS) truyền thống thường phải huấn luyện đầy đủ nhiều kiến trúc ứng viên, dẫn đến thời gian tìm kiếm kéo dài và tiêu tốn tài nguyên.

Trong đề tài này, chúng tôi tập trung xây dựng một **phương thức NAS sử dụng Zero-shot**, cho phép **ước lượng hiệu suất kiến trúc mà không cần huấn luyện**, dựa trên các chỉ số đánh giá thay thế (zero-shot proxies). Đặc biệt, phương pháp được mở rộng trên **không gian tìm kiếm đa kiến trúc (hybrid)**, kết hợp **CNN và Transformer**, nhằm tận dụng ưu điểm của cả hai trong các bài toán thị giác máy tính.

---

## 🎯 Research Objectives

### Mục tiêu tổng quát

Xây dựng một pipeline NAS hiệu quả, giảm chi phí tính toán và có khả năng áp dụng vào bài toán thực tế.

### Mục tiêu cụ thể

* Xây dựng **pipeline NAS zero-shot** dựa trên **BossNAS++** kết hợp **ElasticViT**
* Tối ưu hóa kiến trúc theo:

  * Độ sâu (depth)
  * Độ rộng (width)
  * Độ phân giải (resolution)
* Ứng dụng phương pháp vào **bài toán phân đoạn ảnh khối u (medical image segmentation)** nhằm:

  * Giảm độ phức tạp mô hình
  * Tăng độ chính xác
  * Định nghĩa một **không gian tìm kiếm hybrid thực sự**

---

## 🧪 Methodology

### 1️⃣ Tổng quan NAS và Hạn chế

Bài toán NAS được xác định qua ba thành phần chính:

* **Search Space**
* **Search Strategy**
* **Performance Estimation**

Các chiến lược tìm kiếm phổ biến:

* **Black-box Optimization** (RL, EA, Bayesian, MCTS): chính xác nhưng tốn thời gian
* **Gradient-based NAS** (DARTS, ENAS, OFA): nhanh nhưng thiếu ổn định

Hạn chế của Gradient-based NAS:

* *Rank Disorder*
* *Operation Bias*
* *Coupling giữa kiến trúc và trọng số*

---

### 2️⃣ Zero-shot NAS – BossNAS / BossNAS++

Để khắc phục các hạn chế trên, đề tài lựa chọn **Zero-shot NAS (BossNAS)** với các ưu điểm:

* Không cần supernet
* Không sử dụng mixture of operations
* Tốc độ nhanh, chi phí thấp
* Hoạt động tốt trên không gian đa kiến trúc

Phiên bản **BossNAS++** được sử dụng để cải thiện khả năng đánh giá kiến trúc **Transformer**.

---

### 3️⃣ Thử nghiệm và Tối ưu

* **Bài toán áp dụng**: Phân đoạn hình ảnh khối u (Segmentation)
* **Kiến trúc thay thế**: CNN + Transformer (ElasticViT)
* **Tối ưu đa mục tiêu (Pareto Optimization)** với:

  * Dice Loss
  * Transformer Loss
  * Complexity Loss
  * Entropy Loss

---

## 📊 Expected Outcomes

* Xây dựng thành công **pipeline NAS zero-shot hoàn chỉnh**
* Giảm độ phức tạp mô hình so với kiến trúc cố định
* Cải thiện độ chính xác (Dice score, segmentation quality)
* Chứng minh hiệu quả của NAS trên **không gian tìm kiếm hybrid**

---

## 📚 References

1. White, C. et al., *Neural Architecture Search: Insights from 1000 Papers*, arXiv, 2023
2. Yu, Z. et al., *HCT-Net: Hybrid CNN-Transformer NAS for Medical Image Segmentation*, 2023
3. Zoph, B., Le, Q.V., *Neural Architecture Search with Reinforcement Learning*, ICLR 2017
4. Liu, H. et al., *DARTS*, ICLR 2019
5. Real, E. et al., *Regularized Evolution for NAS*, ICML 2019

---

<p align="center">
  <i>CS519 – University of Information Technology (UIT)</i>
</p>
