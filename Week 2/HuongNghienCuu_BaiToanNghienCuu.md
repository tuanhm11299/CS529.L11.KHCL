# Chọn hướng nghiên cứu và bài toán nghiên cứu

## Hướng nghiên cứu
Computer Vision.

## Bài toán quan tâm

_Image Captioning là bài toán được kết hợp giữa Computer Vision và Natural Language Processing nhằm để máy tính có thể đưa ra câu chú thích cho ảnh. Đối với con người thì việc đó khá đơn giản, nhưng với máy tính thì lại là một vấn đề phức tạp. Theo nhóm thấy đa phần bài toán Image Captioning sẽ có cấu trúc là Encoder sẽ dùng mạng CNN để rút trích đặc trưng ảnh, sau đó Decoder sẽ lấy đặc trưng vừa rút trích đuợc để đưa ra chú thích cho bức ảnh thông qua mạng RNN. Với bài toán mà nhóm chọn thì phần Decoder sẽ được thay thế bằng mạng CNN để tạo sự mới mẻ cho bài toán Image Captioning. Ngoài ra mạng CNN thường được sử dụng trong lĩnh vực Computer Vision, vậy để xem mạng CNN có thể làm được gì trong lĩnh vực Natural Language Processing?_

**Tên bài báo:** CNN+CNN: Convolutional Decoders for Image Captioning.

**Tác giả:** Qingzhong Wang và Antoni B. Chan

**Link bài báo** https://arxiv.org/pdf/1805.09019.pdf

**Link Github** https://github.com/noctrog/cnn_image_captioning

**Thông tin tự tìm hiểu**
- **Input:** Ảnh
- **Output:** Đưa ra câu chú thích cho ảnh đầu vào
- Bài toán được chia thành từng module nhỏ với các chức năng riêng biệt bao gồm: vision module, language module, attention module, prediction module.
	* Vision module: sẽ rút trích đặc trưng ảnh huấn luyện thành những vector đặc trưng.
	* Language module: dùng mạng CNN để xử lý các câu chú thích tương ứng với ảnh thành vector.
	* Attention module: có nhiệm vụ kết hợp vector đặc trưng của Vision module và Language module để học được với mỗi đặc trưng trên ảnh sẽ tương ứng với từ nào trong ngôn ngữ tự nhiên.
	* Prediction module: đưa ra dự đoán chú thích cho ảnh.