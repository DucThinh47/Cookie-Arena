# Web

## Content

- [HTTP Request Content-Length](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#http-request-content-length)
- [HTTP Request Transfer Encoding](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#http-request-transfer-encoding)
- [PHP Executor Playground](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#php-executor-playground)
- [Hello Twig](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#hello-twig)
- [NSLookup (Level 1)](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#nslookup-level-1)
- [NSLookup (Level 2)](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#nslookup-level-2)
- [NSLookup (Level 3)](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#nslookup-level-3)
- [Mass Assignment Profile](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#mass-assignment-profile)
- [Baby HTTP Method](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#baby-http-method)
- [What is your name?](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#what-is-your-name)
- [I Known Your IP](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#i-known-your-ip)
- [eViewer](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#eviewer)
- [Cookie Comic](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#cookie-comic)
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

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image19.png?raw=true)

**Flag: CHH{PHPFunct1Ons_986675c073d696bff00160b9e301232e}**

### Hello Twig

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image20.png?raw=true)

Start challenge:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image21.png?raw=true)

Xem source page:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image24.png?raw=true)

Đoạn mã được thử thách cung cấp:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image25.png?raw=true)

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

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image26.png?raw=true)

Thử dùng payload `{{['cat\x20/etc/passwd']|filter('system')}}`, thay thành `{{['cat\x20/flag.txt']|filter('system')}}`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image22.png?raw=true)

->Tìm được Flag.

Nộp flag:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image23.png?raw=true)

**Flag: CHH{SSTI_PHP_S1mpl3Twig_39e344b86ac999e092b87b3429386eed}**

### NSLookup (Level 1)

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image27.png?raw=true)

Truy cập website:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image28.png?raw=true)

Tôi thử nhập tên miền `google.com` và click `LOOKUP`, kết quả trả về là thông tin của tên miền:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image29.png?raw=true)

Dựa vào mô tả thử thách, liên quan đến lỗ hổng `Command Injection`, tôi đã thử nhập `google.com && id`, kết quả trả về cho thấy website có khả năng dính lỗ hổng `Command Injection`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image30.png?raw=true)

Tiếp theo tôi thử nhập `google.com && cat /flag.txt`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image31.png?raw=true)

**Flag: CHH{S1mpl3C0mmandInj3ct1on_3d8f1302ef289248496527315e5f6271}**
### NSLookup (Level 2)
![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image32.png?raw=true)

Truy cập website:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image33.png?raw=true)

Tôi thử nhập `google.com`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image34.png?raw=true)

Tiếp theo tôi thử nhập `google.com && id`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image35.png?raw=true)

Dựa vào phản hồi này, có vẻ ký tự `space` của tôi đã bị escape thành `\032` (giá trị ASCII cho ký tự `space`). Ý tưởng của tôi là sẽ bypass bộ lọc này bằng những cách nối lệnh khác. 

Sau khi thử một loạt payload, tôi đã tìm được payload `'; cat /flag.txt; #` - đây là cách đóng mở quote lại rồi chèn lệnh, như vậy payload cuối cùng sẽ là `google.com'; cat /flag.txt; #`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image36.png?raw=true)

### NSLookup (Level 3)

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image37.png?raw=true)

Truy cập website:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image38.png?raw=true)

Xem source code của trang web, tôi thấy rằng có một filter được áp dụng ở đây:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image39.png?raw=true)

Đây là filter được viết bằng JS, để tạm thời vô hiệu hóa filter này, tôi đã `Disable JS` trong dev tools:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image40.png?raw=true)

Sau khi thử một loạt các cách bypass bộ lọc câu lệnh của thử thách ,tôi đã tìm được payload sau: 

    google.com'; find / -type f 2>/dev/null | grep flag; #

Payload này sẽ giúp tôi dò file theo pattern được thử thách cung cấp `/flagXXXX.txt`. Kết quả trả về từ website:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image41.png?raw=true)

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image42.png?raw=true)

=> Tôi đã tìm được file chứa flag theo đúng định dạng: `/flagbsEQj.txt`. Để đọc nội dung file này, ý tưởng của tôi là mã hóa base64 nội dung file rồi decode lại:

    google.com'; base64 /flagbsEQj.txt; #

Kết quả là tôi đã tìm được nội dung flag được mã hóa base64:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image43.png?raw=true)

Decode nội dung này và tôi tìm được flag:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image44.png?raw=true)
### Mass Assignment Profile

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image45.png?raw=true)

Truy cập trang web:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image46.png?raw=true)

Thử login vào tài khoản `alice`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image47.png?raw=true)

Tôi thử sửa Full Name thành `admin`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image48.png?raw=true)

Kiểm tra request này:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image49.png?raw=true)

Ý tưởng của tôi là thêm vào request body trường `role` với giá trị là `admin` và đã tìm được flag.

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image50.png?raw=true)
### Baby HTTP Method
![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image51.png?raw=true)

Truy cập website:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image52.png?raw=true)

Thử click `click me for the flag`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image53.png?raw=true)

Xem source code:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image54.png?raw=true)

Dựa vào mô tả thử thách, tôi cần tìm endpoint ẩn, sau đó gửi PUT request đến endpoint này. Nhìn qua source code, tôi để ý tới `<!-- /src -->`. Thử truy cập `/src`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image55.png?raw=true)

=> Đã tìm được endpoint ẩn, tiếp theo tôi gửi PUT request đến endpoint này và tìm được flag:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image56.png?raw=true)
### What is your name?
![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image57.png?raw=true)

Tôi đã kiểm tra source code nhưng không có gì. Khi kiểm tra response khi refresh lại trang, tôi đã nghĩ đến lỗ hổng `SSTI`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image58.png?raw=true)

Tiếp theo, khi nội dung trang web là `Hello. What is your name?`. Ý tưởng của tôi là tôi sẽ gửi một request đến `/?name={{7*7}}` để kiểm tra trang web có dính `SSTI` thật không:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image59.png?raw=true)

=> Như vậy đã xác định được trang web dính lỗ hổng `SSTI`. Tôi sẽ chèn payload `{{request.application.__globals__.__builtins__.__import__('os').popen('cat /flag.txt').read()}}`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image60.png?raw=true)
### I Known Your IP

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image61.png?raw=true)

Truy cập website:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image62.png?raw=true)

Đoạn code được thử thách cung cấp: 

from flask import Flask, request, render_template_string

    app = Flask(__name__)

    @app.route("/")
    def home():    
        try:
            client_ip = request.headers.getlist("X-Forwarded-For")[0].split(':')[0]
        except:
            client_ip = None
        if not client_ip:
            client_ip = request.remote_addr
        message = f"This page is being accessed from the remote address: {client_ip}"    
        return render_template_string(message)
        ## Fix Server Side Template Injection
        # message = "This page is being accessed from the remote address: {{client_ip}}"
        # return render_template_string(message, client_ip=client_ip)

    if __name__ == "__main__":
        app.run(debug=True, host='0.0.0.0', port=1337)

Phân tích đoạn code này, tôi thấy rằng đoạn code `Flask` này có một lỗ hổng `Server-Side Template Injection` (SSTI) khá rõ ràng:

    client_ip = request.headers.getlist("X-Forwarded-For")[0].split(':')[0]

Lấy IP của client từ header `X-Forwarded-For` (nếu có), nếu không thì dùng `request.remote_addr`.

    message = f"This page is being accessed from the remote address: {client_ip}"
    return render_template_string(message)

Biến `message` là một `f-string` chứa giá trị có thể do người dùng kiểm soát (client_ip từ header), sau đó `message` được truyền trực tiếp vào `render_template_string()`.

Vì `render_template_string()` sử dụng `Jinja2` (template engine mặc định của Flask), tôi có thể thử thêm header `X-Forwarded-For: {{7*7}}` vào request để kiểm tra:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image63.png?raw=true)

Tiếp theo tôi thay giá trị của `X-Forwarded-For` thành `{{ self.__init__.__globals__.__builtins__.__import__('os').popen('cat /flag.txt').read() }}` và tìm được flag:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image64.png?raw=true)
### eViewer

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image65.png?raw=true)

Truy cập trang web:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image66.png?raw=true)

Tôi thử nhập file name là `../../../flag.txt` và tìm được flag:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image67.png?raw=true)
### Cookie Comic

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image68.png?raw=true)

Truy cập trang web:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image69.png?raw=true)

Kiểm tra source code, tôi tìm được đường dẫn tới những bức ảnh được hiển thị trên trang web:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image70.png?raw=true)

Truy cập link này:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image71.png?raw=true)

Tôi đã thử thay đổi đường dẫn này thành:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image72.png?raw=true)

Sau khi Enter, 1 file `image.php` được tự động tải về và nội dung file chính là flag:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image73.png?raw=true)

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image74.png?raw=true)






















































