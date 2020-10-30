# -FIT_CDIO_CV_APPS_Lab01-_1612154
Các thư viện sử dụng: numpy, pandas, matplotlib, Scikit-learn, keras

Cài đặt Anaconda và instal các thư viện cần thiết như keras, numpy, pandas, matplotlib, Scikit-learn
Cài đặt CUDA và các Tool kit phù hợp với Tensorflow 2 theo như hướng dẫn ở: https://www.tensorflow.org/install/gpu
Data: FashionMNIST

1. Thử xây dựng 3 fully connected layer để giải quyết bài toán phân loại. Tuy số lượng điểm được phân loại đúng trong toàn bộ số điểm 'accuracy' đạt từ 86% ~ 89& nhưng cách này không phải tối ưu cho dữ liệu ảnh vì dữ liệu ảnh hai chiều ban đầu đã được dàn phẳng ra thành dữ liệu một chiều, làm mất đi nhiều thông tin.

2. Vì mô hình ở cách 1 bị Overfitting, nên phải tìm cách để tránh Overfitting, Dropout là một trong những kỹ thuật có khả năng đó.

3. Sử dụng các convolution layer dùng để lấy feature từ image và lấy feature nổi bật giúp giảm parameter khi training.

4. Sau đó sử dụng 2 fully connected layer với mức dropout = 50%

5. Train model bằng kỹ thuật k-fold, chia tập train thành k tập nhỉ, mỗi model của tập thứ k được xây dựng trên k-1 tập còn lại. Chọn k = 10.

6. Mô hình xây dựng bởi mạng CNN trên vẫn chưa phải là tối ưu nhất do vẫn chưa giải quyết được việc mất mát dữ liệu bởi hàm flatten().
