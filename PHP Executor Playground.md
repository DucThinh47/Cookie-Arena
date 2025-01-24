# PHP Executor Playground
![img](https://imgur.com/kRvaaOA.png)

![img](https://imgur.com/ehuDIni.png)

### Web page: 
![img](https://imgur.com/EKh9852.png)

Thử string là *admin* và function là *strlen*:

![img](https://imgur.com/FH8Jhbg.png)

Thử string là *admin* và function là *strtoupper*:

![img](https://imgur.com/QgYlpqU.png)

Thử string là *ADMIN* và function là *strtolower*:

![img](https://imgur.com/QphCNcf.png)

Thử string là *admin* và function là *addslashes*:

![img](https://imgur.com/1KIBhpt.png)

Thử string là *admin* và function là *print_r*:

![img](https://imgur.com/qVx1jF3.png)

Thử string là *admin* và function là *exec*:

![img](https://imgur.com/EPAkBZW.png)

Thử string là *admin* và function là *passthru*:

![img](https://imgur.com/3n7o5ol.png)

Thử string là *admin* và function là *shell_exec*:

![img](https://imgur.com/QDve4ps.png)

Thử string là *admin* và function là *escapeshellarg*:

![img](https://imgur.com/qvhCYQ5.png)

Thử string là *admin* và function là *escapeshellcmd*:

![img](https://imgur.com/Usm3JXN.png)

Trong PHP, hàm *shell_exec* sẽ thực hiện 1 lệnh từ shell và trả về toàn bộ kết quả dưới dạng chuỗi. Hàm *exec* cũng thực hiện 1 lệnh từ shell nhưng chỉ trả về dòng cuối cùng của kết quả dưới dạng chuỗi. Hàm *passthru* thực hiện 1 lệnh từ shell và xuất trực tiếp kết quả đến browser (hoặc thiết bị đầu ra khác). 

Thử nhập chuỗi *find / -name *.txt* và dùng hàm *shell_exec*:

![img](https://imgur.com/T6zlegl.png)

Click Execute và có đầu ra như sau: 

![img](https://imgur.com/5ljSHIf.png)

--> Tìm được file */flag.txt*.

Thử nhập chuỗi *cat /flag.txt* và dùng hàm *passthru*:

![img](https://imgur.com/Y5PUBlk.png)

### Flag: CHH{PHPFunct1Ons_986675c073d696bff00160b9e301232e}