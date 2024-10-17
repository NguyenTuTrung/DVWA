# CRSF (Cross-Site Request Forgery)

**Mức độ: Thấp.**

![alt text](image.png)

Đây là màn hình đầu tiên của ứng dụng. Ta sẽ thay đổi từ 'password' thành '10122003'
-> Sau khi thay đổi thành thông sẽ hiện thị thông báo "Password Changed" -> CSRF mục tiêu là sẽ lừa người dùng bấm vào 1 đường linh lạ hoặc 1 email độc,... 

Ta sẽ tạo ra 1 file csrf_attck.html để thực hiện việc trên:
```HTML
<a href="http://localhost/DVWA/vulnerabilities/csrf/?password_new=password&password_conf=password&Change=Change#">
    <img src="http://localhost/DVWA/vulnerabilities/csrf/image.jpg" alt="Click Here">
</a>
```

Trang Web đó sẽ hiển thị như sau:

![alt text](image-1.png)

Ban đầu mật khẩu sẽ là 10122003 cho tài khoảng admin

![alt text](image-2.png)

Sau khi bấm vô linh mà ta tạo ra thì password sẽ tự động bị đổi thành password

![alt text](image-3.png)
-> Mật khẩu cũ người dùng đổi đã bị sai

![alt text](image-4.png)

**Mức độ: Trung bình.**