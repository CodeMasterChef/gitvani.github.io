Cài đặt OpenCV cho Jupyter Notebook cần cài đặt từ gói [opencv của conda-forge](https://anaconda.org/conda-forge/opencv) với label là broken:

```
conda install -c conda-forge/label/broken opencv
```

Sở dĩ phải dùng label là `broken` vì chúng ta cần cài đặt phiên bản nhỏ hơn 3.4 để dùng phương thức xfeatures2d:

```
sift = cv2.xfeatures2d.SIFT_create()

```
Ở phiên bản 4.1 trở đi thì xfeatures2d không còn hỗ trợ.

Ngoài ra, chúng ta phải start Jupyter Notebook bằng lệnh sau, tuyệt đối không dùng phần mềm Anaconda để start Jupyter Notebook vì phiên bản sẽ dùng openCV 4.1:

```
jupyter notebook
```

Kiểm tra lại phiên bản cuả OpenCV bằng cách gõ lệnh sau trong trình soạn thảo của Jupyter Notebook:

```
import cv2
cv2.__version__

```
