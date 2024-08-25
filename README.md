
# REKA:BIT -- Trung Tâm Hải Vinh

Phiên bản REKA:BIT này đã được Trung Tâm Hải Vinh chỉnh sửa để phù hợp với việc tích hợp nhiều hệ thống khác nhau. Đây là một công cụ hỗ trợ mạnh mẽ cho việc phát triển các dự án robot và STEM với micro:bit.

**REKA:BIT** hướng tới việc đơn giản hóa việc tạo ra các dự án robot và các ứng dụng khác với micro:bit. Với bộ điều khiển động cơ DC hai kênh tích hợp sẵn, điều khiển 4 servo và nguồn điện chuyên dụng, học sinh có thể bắt tay vào xây dựng các dự án với các chuyển động cơ học ngay lập tức. REKA:BIT còn đi kèm với 6 cổng Grove có đèn LED báo trạng thái trên tất cả các chân IO, giúp việc tích hợp thêm các cảm biến và module khác trở nên thuận tiện hơn. Sản phẩm này hoạt động tương thích với **micro:bit V1 & V2**.

Tên gọi '**REKA**' bắt nguồn từ từ 'reka bentuk' trong tiếng Mã Lai, có nghĩa là thiết kế.

![REKA:BIT](https://raw.githubusercontent.com/CytronTechnologies/pxt-rekabit/master/icon.png)

Dưới đây là cách bạn có thể thêm phần mở rộng REKA:BIT vào dự án MakeCode của mình.
![Thêm phần mở rộng](https://raw.githubusercontent.com/CytronTechnologies/pxt-rekabit/master/rekabit-adding-extension.gif)

## Động cơ DC

Chạy động cơ 1 tiến tới với tốc độ 50% khi nhấn nút A, dừng động cơ khi nhấn nút B.

```blocks
input.onButtonPressed(Button.A, function () {
    rekabit.runMotor(MotorChannel.M1, MotorDirection.Forward, 127)
})
input.onButtonPressed(Button.B, function () {
    rekabit.brakeMotor(MotorChannel.M1)
})
```

## Servo

- Nhấn nút A - Xoay Servo 1 đến góc 0 độ.
- Nhấn nút B - Xoay Servo 1 đến góc 180 độ.
- Nhấn đồng thời nút A+B - Vô hiệu hóa Servo 1, không có xung nào được gửi đến Servo 1 và có thể xoay Servo bằng tay.

```blocks
input.onButtonPressed(Button.A, function () {
    rekabit.setServoPosition(ServoChannel.S1, 0)
})
input.onButtonPressed(Button.B, function () {
    rekabit.setServoPosition(ServoChannel.S1, 180)
})
input.onButtonPressed(Button.AB, function () {
    rekabit.disableServo(ServoChannel.S1)
})
```

**REKA:BIT** cũng đi kèm với bốn nút kiểm tra nhanh động cơ DC. Bạn có thể nhấn các nút M1A, M1B, M2A hoặc M2B trên bo mạch để chạy động cơ DC mà không cần viết mã. Điều này rất tiện lợi cho việc kiểm tra kết nối và chức năng của động cơ DC.

## Giấy phép  
MIT

## Các mục tiêu hỗ trợ  
* cho PXT/microbit  

Bạn có thể mở trang này tại [https://cytrontechnologies.github.io/pxt-rekabit/](https://cytrontechnologies.github.io/pxt-rekabit/)
