## Phần 1

**1.**
- something you know: thứ mình biết, như mật khẩu, pin.
- something you have: thứ mình có, như điện thoại, app authenticator, sim.
- something you are: thứ là của mình, như vân tay, khuôn mặt.

khi bật 2fa thì mật khẩu là yếu tố know, mã otp là yếu tố have (vì mã sinh ra từ điện thoại mình đang cầm).

**2.** lúc cài, server và app cùng giữ một khóa bí mật (shared secret) qua mã qr. mã otp được tính từ khóa bí mật này và thời gian hiện tại, cứ 30 giây đổi một mã 6 số. điện thoại có đồng hồ riêng nên tự tính được mà không cần mạng, server cũng tính ra cùng mã để so sánh. vì vậy bật chế độ máy bay vẫn ra mã đúng.

## Phần 2

**3.**

| tiêu chí | sms otp | totp authenticator |
|---|---|---|
| chống sim swapping và nghe lén ss7 | kém, dễ bị chiếm số | rất tốt, khóa bí mật nằm trong điện thoại |
| offline, ra nước ngoài | cần sóng, mất sóng thì không nhận mã | chạy offline, kể cả trên máy bay |
| tiện dụng, chi phí | quen thuộc nhưng tốn phí gửi sms | miễn phí, mở app là có mã |
| khi mất điện thoại | làm lại sim là có mã nhưng dễ bị trộm sim | cần backup codes hoặc cloud sync mã hóa |

**4.** nên chọn giải pháp 2, totp authenticator. vì kỹ sư hay đi công tác nước ngoài và bay nên sms dễ không nhận được mã, còn totp dùng offline. tài khoản chứa mã nguồn và doanh thu lớn nên cần chống sim swapping, mà sms thì kém phần này. totp lại miễn phí.

## Phần 3

**5.** backup codes dùng để vào lại tài khoản khi mất điện thoại hoặc không dùng được app authenticator. mỗi mã dùng được 1 lần.

2 chỗ lưu an toàn:
- in ra giấy cất trong két sắt hoặc tủ khóa.
- lưu trong két mật khẩu bitwarden đã mã hóa.

sai lầm cần tránh: chụp màn hình để trong điện thoại hoặc gửi qua zalo, email, vì máy bị hack hay mất là lộ luôn mã.