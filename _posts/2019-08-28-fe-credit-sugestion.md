Check template:
- Loại bỏ để lấy lại template
- Yêu cầu: đủ 18 tuổi hay không, quê quán đúng chuẩn VN không.
Bài toán FE chia làm 3 hướng:
- Face dectection, so sánh với ảnh sefile: Face-recognition.
- OCR: detect thông tin trên CMND: trên 18 và correct City: Firebase có MK Kit để detech chữ.
- document template check:  remove các thông tin cá nhân đi, bôi đen để lấy template. Similarity: cho ra độ tương quan một tiêu chuẩn nào đó.

2 ảnh khác nhau nhau không: dựa vào 2 ma trận 3 chiều của 2 hai. Dựa theo công thức pytago  (x1-x2)^ 2 + (y1-y2)^2. 

Khoảng cách cho phép?

standard dimation: chia tất cả điểm ảnh cho 255 hoặc X = X - Xmean.

OpenCV.

30 x 30 

deep learning: tự động extract features.

Chuẩn hóa độ sáng: X - Xmean
