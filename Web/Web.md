# Web

## Content

- [HTTP Request Content-Length]()
- [HTTP Request Transfer Encoding]()
- [PHP Executor Playground]()

### HTTP Request Content-Length

Challenge:

![img](0)

Xem source page:

![img](1)

**Flag: CHH{HTTPContentLength_eb4e5beb118f2242c00d142ede3bb218}**

### HTTP Request Transfer Encoding

Challenge:

![img](2)

Xem source page:

![img](3)

**Flag: CHH{HTTPTransferEncoding_d11e934c7546bacaa97b2c826878d80b}**

### PHP Executor Playground

Challenge:

![img](4)

![img](5)

Xem website:

![img](6)

Thử string là `admin` và function là `strlen`:

![img](7)

Thử string là `admin` và function là `strtoupper`:

![img](8)

Thử string là `ADMIN` và function là `strtolower`:

![img](9)

Thử string là `admin` và function là `addslashes`:

![img](10)

Thử string là `admin` và function là `print_r`:

![img](11)

Thử string là `admin` và function là `exec`:

![img](12)

Thử string là `admin` và function là `passthru`:

![img](13)

Thử string là `admin` và function là `shell_exec`:

![img](14)

Thử string là `admin` và function là `escapeshellarg`:

![img](15) 

Thử string là `admin` và function là `escapeshellcmd`:

![img](16)

Trong PHP, hàm `shell_exec` sẽ thực hiện 1 lệnh từ shell và trả về toàn bộ kết quả dưới dạng chuỗi. Hàm `exec` cũng thực hiện 1 lệnh từ shell nhưng chỉ trả về dòng cuối cùng của kết quả dưới dạng chuỗi. Hàm `passthru` thực hiện 1 lệnh từ shell và xuất trực tiếp kết quả đến browser (hoặc thiết bị đầu ra khác).

Thử nhập chuỗi `find / -name *.txt` và dùng hàm `shell_exec`:

![img](17)

Click `Execute` và có đầu ra như sau:

![img](18)

->Tìm được file `/flag.txt`.

Thử nhập chuỗi `cat /flag.txt` và dùng hàm `passthru`:

![img](19)

**Flag: CHH{PHPFunct1Ons_986675c073d696bff00160b9e301232e}**















