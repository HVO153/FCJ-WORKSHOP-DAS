---
title: "Chạy và kết quả"
date: "2025-08-05"
weight: 5
chapter: false
pre: " <b> 5.</b> "
---

{{% notice info %}}
Đây là phần chạy project và xem các kết quả đạt được.Trong đây bao gồm các kết quả về việc ngăn xóa, chỉnh sửa của Object Lock; hay việc tự chuyển đổi lớp lưu trữ và hết hạn phiên bản đối tượng thông qua Lifecycle Policies.
{{% /notice %}}


- Bạn cần chạy lệnh `npm install` và `npm run build` sau đó `npm run dev` cho mỗi service khi mới tải về.
![conseque](images/5.Consequence/001-runproject.png)
![conseque](images/5.Consequence/002-runproject.png)
![conseque](images/5.Consequence/003-runproject.png)

- Bạn tạo một bài viết mới, dữ liệu của bài viết sẽ được chuyển về bucket S3.Sau đó, bạn vào bucket kiểm tra đã thành công hay chưa.
![conseque](images/5.Consequence/004-runproject.png)
![conseque](images/5.Consequence/005-runproject.png)
![conseque](images/5.Consequence/006-runproject.png)

- Bạn hãy thử xóa file dữ liệu trong bucket và xem kết quả có giống bên dưới không.
![conseque](images/5.Consequence/007-deletefile.png)
- Bạn xóa file dữ liệu nhưng nó chưa thực sự mất, hãy bật **show version** để xem, khi đó file chỉ đánh dấu phiên bản xóa và thực chất nó vẫn nằm đó.Nếu bản cố gắng xóa file gốc sẽ bị thông báo **Failed to delete objects**.Điều này chứng minh cho bạn thấy Object Lock mà ta thiết lập đã hoạt động tốt.
![conseque](images/5.Consequence/008-deletefile.png)
![conseque](images/5.Consequence/009-deletefile.png)
- Hãy chờ hết hạn thời gian mà ta đã thiết lập Object Lock và thử xóa lại.
![conseque](images/5.Consequence/010-deletefile.png)
![conseque](images/5.Consequence/011-deletefile.png)
![conseque](images/5.Consequence/012-deletefile.png)
- Sau khi xóa thành công, bạn thử bật lại **show version** lúc này file đã được xóa đi sạch sẽ.
![conseque](images/5.Consequence/013-deletefile.png)


- Khi hết thời gian Object Lock vào ngày 6/8/2025 lúc 22:39:15, file đủ điều kiện chuyển sang Glacier Flexible Retrieval theo lifecycle rule. Tuy nhiên, đến khoảng 21:50 ngày 7/8 tầm khoảng 22 ~ 23 giờ sau, quá trình chuyển đổi mới thực sự diễn ra.
- Nguyên nhân vì AWS S3 không thực hiện lifecycle transition ngay lập tức, mà xử lý theo lịch quét nội bộ, không có thời gian cụ thể.
![conseque](images/5.Consequence/014-glacier.png)
{{% notice note %}}
Do đó, trong mọi tình huống, người dùng cần lưu ý rằng: việc chuyển đổi trạng thái lưu trữ có thể xảy ra trễ so với thời điểm dự kiến, dù lifecycle rule đã được cấu hình đúng
{{% /notice %}}
{{% notice warning %}}
Chú ý: File dữ liệu lưu trữ trong bucket bắt buộc lớn hơn 218KB, nếu điều kiện này không thỏa quy trình chuyển đổi lớp lưu trữ sẽ không thể diễn ra.Bạn cần tính toán sao cho khi tạo bài viết có dung lượng lưu trữ trên 218KB.
{{% /notice %}}
![conseque](images/5.Consequence/016-restore.png)
- Sau khi đối tượng đã chuyển đổi qua lớp lưu trữ **Glacier Flexible Retrieval**, ta thực hiện **restore** để có thể tải và kiểm tra lại file đảm bảo tính toàn vẹn dữ liệu không bị thay đổi.
![conseque](images/5.Consequence/017-restore.png)
![conseque](images/5.Consequence/018-restore.png)
![conseque](images/5.Consequence/019-restore.png)
- Sau khi restore thành công, bạn có thể xem bằng cách click **Open** hoặc tải về bằng cách click **Download**.
- Hãy kiểm tra thời gian hết hạn phiên bản và quay lại sau đó để xác nhận điều này có diễn ra hay không.
![conseque](images/5.Consequence/020-expiration.png)
![conseque](images/5.Consequence/021-expiration.png)
![conseque](images/5.Consequence/022-expiration.png)
 - Dấu hiệu cho thấy nó đã hoạt động tốt, bạn khi vô bucket **blog-micro-data-archive** sẽ không thấy bất kì folder hay file nào, và bạn chỉ có thể thấy khi bật **show version**.



