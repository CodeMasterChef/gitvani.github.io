Hai model này đều dựa vào khoảng cách để tính.

# K-Nearest Classifier:

![image](https://user-images.githubusercontent.com/10974517/64253435-81deca00-cf47-11e9-9243-64361eb52fa9.png)

![image](https://user-images.githubusercontent.com/10974517/64253696-04678980-cf48-11e9-89fb-d459f10be7d6.png)

Mình mặc định rằng những cái gần nào thì có cùng tính chất. K chọn là giá trị lẻ để tránh trường hợp  1 nửa chẳn, 1 nửa lẻ.

![image](https://user-images.githubusercontent.com/10974517/64253974-9e2f3680-cf48-11e9-91b1-0083681f59af.png)

# SVM Classifier:

Mục tiêu của SVM là tìm mặt phẳng chia dữ liệu làm 2 phần:

![image](https://user-images.githubusercontent.com/10974517/64254488-b9e70c80-cf49-11e9-87fe-1e8c3b95ab84.png)

Việc chọn mặt phẳng là rất quan trọng, SVM đưa ra thuộc tính Margin. SVM tối ưu chọn margin lớn nhất:
![image](https://user-images.githubusercontent.com/10974517/64254931-91134700-cf4a-11e9-9991-fd6c1bbd952c.png)

SVM không trả về xác xuất như các model khác, nó chỉ về class. SVM sử dụng support vector để tìm:
![image](https://user-images.githubusercontent.com/10974517/64255064-d8013c80-cf4a-11e9-9f67-12d8b39b15df.png)

Trong thực tế, ta có thể không vẽ được đường thẳng nào do vùng biên không được chứa điểm nào. Do đó, ta có thêm hệ thống soften để chấp nhận một số điểm lọt vào vùng biên:
![image](https://user-images.githubusercontent.com/10974517/64255267-362e1f80-cf4b-11e9-84a5-d58c78f1c838.png)

SVM có thể áp dụng biến đổi chiều để chia cắt dễ hơn:
![image](https://user-images.githubusercontent.com/10974517/64255445-945b0280-cf4b-11e9-84ed-0acdfd8c7689.png)

Khi nào dùng linear SVM, khi nào dùng thêm dimession? Đều này phụ thuộc vào số lượng data, số lượng feature. Khi mình có nhiều feature thì nên dùng linear:
![image](https://user-images.githubusercontent.com/10974517/64255660-04698880-cf4c-11e9-9df2-f54daafcd202.png)

# References:

https://data-flair.training/blogs/svm-kernel-functions/#targetText=SVM%20Kernel%20Functions,functions%20can%20be%20different%20types
