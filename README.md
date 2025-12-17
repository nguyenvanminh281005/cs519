<p align="center">
  <a href="https://www.uit.edu.vn/">
    <img src="https://www.uit.edu.vn/sites/vi/files/banner.png" alt="UIT Banner">
  </a>
</p>

<h1 align="center"><b>CS519.Q11.KHTN – Scientific Research Methodology</b></h1>

## 👨‍🏫 Instructor

* [**Lê Đình Duy**](https://www.facebook.com/inhduyle.507900) – [ldduy@uit.edu.vn](mailto:ldduy@uit.edu.vn)


---

## 📌 Project Title (Vietnamese)

**XÂY DỰNG PHƯƠNG THỨC TÌM KIẾM MẠNG NƠ-RON TỰ ĐỘNG (NAS) SỬ DỤNG ZERO-SHOT TRÊN KHÔNG GIAN TÌM KIẾM ĐA KIẾN TRÚC**

## 📌 Project Title (English)

**ZERO-SHOT NEURAL ARCHITECTURE SEARCH (NAS) METHOD BASED ON A MULTI-ARCHITECTURE SEARCH SPACE**

---

## 👨‍🎓 Team Members

* [**Nguyễn Văn Minh**](https://www.facebook.com/nguyenvanminh281005) – [23520945](mailto:23520945@gm.uit.edu.vn)
* [**Nguyễn Văn Hồng Thái**](https://www.facebook.com/hongthai1105z) – [23521418](mailto:2351418@gm.uit.edu.vn)

---

## 🔗 Project Links

* **GitHub Repository**:
  👉 [CS519.Q11.KHTN – Scientific Research Methodology](https://github.com/nguyenvanminh281005/cs519)

* **YouTube Presentation Video**:
  👉 [Youtube](https://www.youtube.com/watch?v=wGjmmFUMoXM)
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
## 📚 References

1. White, C. et al., "Neural Architecture Search: Insights from 1000 Papers", arXiv preprint arXiv:2301.08727, 2023.
2. Yu, Z. et al., "HCT-Net: Hybrid CNN-Transformer Model Based on a Neural Architecture Search Network for Medical Image Segmentation", Tên Tạp chí/Hội nghị, 2023.
3. Zoph, B., Le, Q.V., "Neural Architecture Search with Reinforcement Learning", ICLR, 2017.
4. Liu, H. et al., "DARTS: Differentiable Architecture Search", ICLR, 2019.
5. Li, C. et al., "BossNAS: Exploring Hybrid CNN-Transformers with Block-Wisely Self-Supervised Neural Architecture Search", Proceedings of the IEEE/CVF International Conference on Computer Vision, 2021.
6. Gu, W. et al., "MS-NAS: Multi-Scale Neural Architecture Search for Medical Image Segmentation", MICCAI, 2020.
7. Chen, Y. et al., "DPE-NAS: Differential Progressive Evolution for Neural Architecture Search in Medical Image Segmentation", IEEE JBHI, 2022.
8. Kim, S. et al., "Scalable Neural Architecture Search for 3D Medical Image Segmentation", MICCAI, 2019.
9. Jiang, Y. et al., "H-NAS: Hybrid Neural Architecture Search for 3D Medical Image Segmentation", MICCAI, 2020.
10. Tian, Z. et al., "DeeperLab: Single-Shot Segmentation with Combined Semantic and Instance Predictions", CoRR abs/1902.05093, 2019.
11. Zhang, Y. et al., "Customizable Architecture Search for Semantic Segmentation", CVPR, 2019.
12. Liu, C. et al., "Auto-DeepLab: Hierarchical Neural Architecture Search for Semantic Image Segmentation", CVPR, 2019.
13. Hill, P. et al., "NAS-U-Net: Neural Architecture Search for Medical Image Segmentation", IEEE Access, 2019.
14. Xie, Y. et al., "NAS-Shape: Neural Architecture Search for Shape-aware Medical Image Segmentation", MICCAI, 2021.
15. Chen, H. et al., "V-NAS: Neural Architecture Search for Volumetric Medical Image Segmentation", 3DV, 2019.
16. Gong, X. et al., "Auto-GAN: Neural Architecture Search for Generative Adversarial Networks", ICCV, 2019.
17. Zuo, C. et al., "C2FNAS: Coarse-to-Fine Neural Architecture Search for 3D Medical Image Segmentation", CVPR, 2020.
18. Yang, D. et al., "Searching Learning Strategy with Reinforcement Learning for 3D Medical Image Segmentation", MICCAI, 2019.
19. Kuang, Z. et al., "Fashion-Cut: Interactive Segmentation for Fashion Images", ACM MM, 2018.
20. Chen, X. et al., "Progressive Differentiable Architecture Search: Bridging the Depth Gap between Search and Evaluation", ICCV, 2019.
21. Xie, Y. et al., "CoTr: Efficiently Bridging CNN and Transformer for 3D Medical Image Segmentation", MICCAI, 2021.

---

<p align="center">
  <i>University of Information Technology (UIT)</i>
</p>
