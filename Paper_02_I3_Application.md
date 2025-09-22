**Tóm tắt bài báo: Mô hình hóa dịch bệnh và ứng dụng bảo hiểm trong đại dịch: Nghiên cứu điển hình tại Victoria, Australia**

**Tác giả**: Chang Zhai, Ping Chen, Zhuo Jin, Tak Kuen Siu  
**Nguồn**: Annals of Actuarial Science (2024), 18, pp. 242–269  
**DOI**: 10.1017/S1748499523000246  

**Tóm tắt**:  
Bài báo nghiên cứu mô hình hóa dịch bệnh và ứng dụng trong bảo hiểm đại dịch, tập trung vào trường hợp COVID-19 tại Victoria, Australia. Các tác giả giới thiệu mô hình ngăn (compartment model) SVEI3RD (Susceptible-Vaccinated-Exposed-Infected-Containing-3-Substates-Recovered-Dead) cải tiến từ mô hình SVEIRD, nhằm mô tả động lực lây truyền dịch bệnh và định giá bảo hiểm. Dữ liệu thực tế được sử dụng để hiệu chỉnh mô hình, từ đó phân tích hiệu quả tiêm chủng và đề xuất hai sản phẩm bảo hiểm: bảo hiểm y tế và bảo hiểm du lịch.

### **Điểm chính**:

1. **Mô hình hóa dịch bệnh**:
   - **Mô hình SIR cơ bản**: Dân số được chia thành ba nhóm: dễ nhiễm (S), nhiễm bệnh (I), và hồi phục (R). Hệ phương trình vi phân (ODEs) mô tả tỷ lệ chuyển đổi giữa các nhóm.
   - **Mô hình SVEIRD**: Mở rộng SIR với các trạng thái tiêm chủng (V), tiếp xúc (E), và tử vong (D). Thêm các tham số như tỷ lệ tiêm chủng (α), hiệu quả tiêm chủng (σ), tỷ lệ ủ bệnh (γ), tỷ lệ hồi phục (δ), và tỷ lệ tử vong (μ).
   - **Mô hình SVEI3RD**: Cải tiến SVEIRD bằng cách chia trạng thái nhiễm bệnh (I) thành ba nhóm phụ (I1: triệu chứng nhẹ, I2: nhập viện, I3: ICU) để phản ánh mức độ nghiêm trọng của bệnh. Các tham số bổ sung (β1, β2, β3, p1, p2, δ1, δ2, δ3) mô tả tỷ lệ lây nhiễm và chuyển đổi giữa các trạng thái.

2. **Hiệu chỉnh dữ liệu**:
   - Sử dụng bộ dữ liệu COVID-19 từ Victoria (tính đến tháng 3/2022), bao gồm số ca nhiễm, tử vong, hồi phục, nhập viện, ICU, và tiêm chủng.
   - Hai giai đoạn được phân tích: liều vắc-xin thứ nhất (29/08/2021–04/10/2021) và liều thứ hai (11/10/2021–01/11/2021), khi tỷ lệ tiêm chủng đạt từ 50% đến 80%.
   - Mô hình SVEI3RD cho kết quả hiệu chỉnh tốt hơn SVEIRD, với sai số chuẩn nhỏ hơn và các tham số thực tế hơn (ví dụ, hiệu quả vắc-xin 95% ở liều thứ hai, phù hợp với báo cáo ngành).

3. **Ứng dụng bảo hiểm**:
   - **Bảo hiểm y tế**:
     - Thu phí bảo hiểm liên tục từ nhóm dễ nhiễm (S) và đã tiêm vắc-xin (V).
     - Chi trả lợi ích theo mức độ triệu chứng: $50 (I1), $200 (I2), $1,000 (I3), và $100,000 (tử vong).
     - Phí bảo hiểm công bằng (zero-profit) được tính bằng Nguyên lý Tương đương: kỳ vọng phí thu bằng kỳ vọng lợi ích chi trả.
     - Phân tích dự trữ tài chính (reserve) cho thấy mức phí cao hơn (10% hoặc 20% loading) giúp tăng dự trữ, nhưng dự trữ thực tế thường cao hơn dự đoán do hiệu quả vắc-xin tăng.
   - **Bảo hiểm du lịch**:
     - Thu phí một lần vào đầu hợp đồng, chi trả lợi ích tương tự y tế nhưng bổ sung $20 cho nhóm tiếp xúc (E) phải cách ly.
     - Phí bảo hiểm công bằng cao hơn khi kỳ hạn hợp đồng dài hơn (30 ngày: $28.60–$9.88; 60 ngày: $32.89–$10.34).
     - Dự trữ giảm dần do chi trả lợi ích tăng, đặc biệt trong kỳ hạn 60 ngày, có nguy cơ âm nếu phí không đủ cao.

4. **Kết quả mô phỏng**:
   - Mô hình SVEI3RD dự đoán tốt hơn SVEIRD về động lực dân số và hiệu quả vắc-xin, đặc biệt ở liều thứ hai.
   - Tỷ lệ tử vong (μ) tăng nhẹ ở liều thứ hai do giảm số ca nặng (I3), nhưng nguy cơ tử vong vẫn cao ở người có sức khỏe yếu.
   - Dự trữ thực tế cao hơn dự đoán, đặc biệt ở liều thứ nhất, do tỷ lệ lây nhiễm giảm nhờ vắc-xin.

5. **Thảo luận thực tiễn**:
   - **Bảo hiểm y tế**: Cần chi trả lợi ích theo mức độ triệu chứng để tránh bất lợi cho khách hàng khỏe mạnh và giảm rủi ro chọn lọc ngược (adverse selection). Ở các nước phát triển như Australia, chính phủ chi trả phần lớn chi phí điều trị, giảm áp lực cho bảo hiểm tư nhân.
   - **Bảo hiểm du lịch**: Phải định giá phí bảo hiểm cẩn trọng để đảm bảo đủ dự trữ, đặc biệt khi tỷ lệ lây nhiễm tăng nhanh. Các yếu tố như điểm đến, độ tuổi, và chính sách miễn trừ ảnh hưởng đến định giá.
   - Dữ liệu công khai từ chính phủ và WHO hỗ trợ hiệu chỉnh mô hình, tăng độ tin cậy và khả năng áp dụng thực tế.

6. **Kết luận**:
   - Mô hình SVEI3RD cải tiến cung cấp cách tiếp cận chi tiết hơn để mô hình hóa dịch bệnh và định giá bảo hiểm, phù hợp với thực tế hơn SVEIRD.
   - Tiêm chủng (đặc biệt liều thứ hai) giảm tỷ lệ lây nhiễm và nhu cầu y tế, ảnh hưởng đến phí bảo hiểm và dự trữ.
   - Các sản phẩm bảo hiểm y tế và du lịch cần cân nhắc yếu tố triệu chứng và điều kiện y tế địa phương để đảm bảo tính cạnh tranh và khả năng thanh toán.
   - Hướng nghiên cứu tương lai: tích hợp mô hình dịch bệnh với quản lý rủi ro động, xem xét các yếu tố như biến thể virus mới hoặc chiến dịch tiêm chủng mở rộng.

**Từ khóa**: COVID-19, mô hình dịch tễ học, bảo hiểm đại dịch, SVEI3RD, Victoria, Australia.
