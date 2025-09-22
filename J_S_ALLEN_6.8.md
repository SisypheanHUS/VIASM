**Tóm tắt: Các mô hình dịch bệnh SI, SIS, SIR và SIRS**

**Nguồn**: Trích từ tài liệu về mô hình hóa dịch bệnh trong Chương 6, Ứng dụng Sinh học của Phương trình Vi phân.

### **Tổng quan**:
Các mô hình dịch bệnh SI, SIS, SIR và SIRS được sử dụng để mô phỏng sự lây lan của các bệnh truyền nhiễm như sởi, quai bị, rubella, và thủy đậu. Dân số được phân loại theo trạng thái bệnh: **S** (dễ nhiễm), **I** (nhiễm bệnh), và **R** (hồi phục/miễn dịch). Các mô hình này sử dụng hệ phương trình vi phân thường (ODEs) để mô tả động lực lây truyền, với các tham số như tỷ lệ lây nhiễm (β), tỷ lệ hồi phục (γ), tỷ lệ mất miễn dịch (ν), và dân số tổng (N). Các mô hình giả định không có sinh/tử (b = 0) để tập trung vào động lực dịch bệnh.

### **Các mô hình chính**:

1. **Mô hình SI**:
   - **Cơ chế**: Không có hồi phục (S → I). Mọi người cuối cùng đều nhiễm bệnh.
   - **Phương trình**:
     ```
     dS/dt = -βSI/N
     dI/dt = βSI/N
     ```
     Với S + I = N (dân số không đổi).
   - **Kết quả**: Số ca nhiễm I(t) tăng theo mô hình logistic, tiến tới N (toàn bộ dân số nhiễm bệnh). Phù hợp với bệnh truyền nhiễm cao như cúm.
   - **Số tái sản xuất cơ bản (R₀)**: R₀ = β/γ. Không áp dụng trực tiếp do không có hồi phục.

2. **Mô hình SIS**:
   - **Cơ chế**: Có hồi phục nhưng không miễn dịch (S → I → S). Bệnh có thể trở thành dịch lưu hành (endemic).
   - **Phương trình**:
     ```
     dS/dt = -βSI/N + γI
     dI/dt = βSI/N - γI
     ```
     Với S + I = N.
   - **Kết quả**:
     - Nếu R₀ = β/γ > 1, bệnh lưu hành với I → (β - γ)N/β, S → γN/β.
     - Nếu R₀ ≤ 1, số ca nhiễm I → 0, dịch bệnh không tồn tại.
   - **Ứng dụng**: Bệnh lây qua đường tình dục như lậu, giang mai (hồi phục nhưng dễ nhiễm lại).
   - **Tỷ lệ lây nhiễm**: βSI/N (standard incidence) hoặc βSI (mass action). Khi N không đổi, hai cách này tương đồng.

3. **Mô hình SIR**:
   - **Cơ chế**: Có hồi phục và miễn dịch vĩnh viễn (S → I → R).
   - **Phương trình**:
     ```
     dS/dt = -βSI/N
     dI/dt = βSI/N - γI
     dR/dt = γI
     ```
     Với S + I + R = N.
   - **Kết quả**:
     - Nếu S(0) > γN/β, số ca nhiễm I(t) tăng đến đỉnh (dịch xảy ra) rồi giảm về 0.
     - Nếu S(0) ≤ γN/β, I(t) giảm về 0 (không có dịch).
     - S(∞) > 0 (luôn còn người không nhiễm), được xác định bởi phương trình ẩn.
   - **R₀ = β/γ**: Nếu R₀x > 1 (x = S(0)/N), dịch xảy ra; nếu không, dịch không lan.

4. **Mô hình SIRS**:
   - **Cơ chế**: Có hồi phục, miễn dịch tạm thời (S → I → R → S).
   - **Phương trình**:
     ```
     dS/dt = -βSI/N + νR
     dI/dt = βSI/N - γI
     dR/dt = γI - νR
     ```
     Với S + I + R = N.
   - **Kết quả**: Bệnh có thể trở thành lưu hành do mất miễn dịch (ν > 0). R₀ = β/γ xác định ngưỡng dịch lưu hành.

### **Các tham số chính**:
- **β**: Số tiếp xúc đủ để lây nhiễm trung bình của một người nhiễm bệnh mỗi đơn vị thời gian.
- **γ**: Tỷ lệ hồi phục (1/γ: thời gian nhiễm trung bình).
- **ν**: Tỷ lệ mất miễn dịch (1/ν: thời gian miễn dịch trung bình).
- **R₀ = β/γ**: Số tái sản xuất cơ bản, quyết định dịch có lan rộng (R₀ > 1) hay không (R₀ ≤ 1).

### **Mở rộng mô hình**:
- **SEIR**: Thêm trạng thái tiếp xúc (E) – giai đoạn ủ bệnh trước khi trở thành nhiễm bệnh (I).
- **MSEIR**: Thêm trạng thái miễn dịch thụ động ở trẻ sơ sinh (M) do kháng thể từ mẹ.
- **Tiêm chủng**:
  - Giảm S(0) xuống (1-p)N, với p là tỷ lệ tiêm chủng.
  - Ngưỡng ngăn dịch: R₀(1-p) < 1 → p > 1 - 1/R₀.
  - Ví dụ: Sởi (R₀ ≈ 13) cần tiêm chủng ≥ 92% để ngăn dịch.
  - Hiệu ứng miễn dịch cộng đồng (herd immunity): Giảm lây nhiễm gián tiếp.
- **Hệ quả tiêm chủng**: Tăng tuổi trung bình nhiễm bệnh, có thể gây biến chứng nghiêm trọng (ví dụ: rubella ở phụ nữ mang thai).

### **Ứng dụng thực tế**:
- **SI**: Phù hợp với bệnh lây nhiễm cao, không hồi phục (như cúm giai đoạn đầu).
- **SIS**: Áp dụng cho bệnh tái nhiễm (như bệnh lây qua đường tình dục).
- **SIR/SIRS**: Mô phỏng bệnh có miễn dịch (sởi, thủy đậu) hoặc miễn dịch tạm thời.
- **Cách ly/kiểm soát**: Áp dụng trong dịch SARS (2003) khi không có vắc-xin hoặc điều trị.

### **Mô hình HIV trong tế bào**:
- **Khác biệt**: Không mô phỏng toàn dân số mà tập trung vào động lực tế bào trong một cá nhân (tế bào T CD4+, tế bào nhiễm, và virus tự do).
- **Phương trình**:
  ```
  dx/dt = λ - d₁x - βxv
  dy/dt = βxv - d₂y
  dv/dt = ky - d₃v - βxv
  ```
  Với x (tế bào T khỏe), y (tế bào nhiễm), v (virus tự do), λ (tỷ lệ sản xuất tế bào T), d₁, d₂, d₃ (tỷ lệ chết), β (tỷ lệ lây nhiễm), k = Nd₂ (sản xuất virus).
- **R₀ = Nβλ/(d₁d₃)**: Nếu R₀ > 1, virus HIV lan rộng; nếu R₀ < 1, virus không thiết lập.
- **Động lực**: Virus tăng nhanh ban đầu, sau đó giảm 2-3 bậc trong vài tuần. Mô hình chỉ mô phỏng giai đoạn đầu, không đến AIDS (nhiều năm sau).

### **Kết luận**:
- Các mô hình SI, SIS, SIR, SIRS cung cấp nền tảng để hiểu và dự đoán động lực dịch bệnh, với R₀ là chỉ số quan trọng.
- Mở rộng như SEIR, MSEIR, hoặc mô hình HIV cải tiến tăng tính thực tế, hỗ trợ tiêm chủng và kiểm soát dịch.
- Tiêm chủng và cách ly là chiến lược quan trọng, nhưng cần cân nhắc hệ quả như tăng tuổi nhiễm bệnh.
