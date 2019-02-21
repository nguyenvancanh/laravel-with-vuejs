# Vì sao nên tích hợp VueJS vào Laravel project

Trong bài viết này, chúng ta sẽ đi tìm hiểu xem VueJs là gì, cách nó hoạt động bên trong 1 project Laravel, và vì sao chúng ta nên sử dụng VueJs vào trong project Laravel của mình.

Nếu bạn đã sử dụng Laravel với một số phiên bản gần nhất, bạn cũng đã nhận thấy rằng, VueJs đã được tích hợp sẵn vào trong project Laravel tương tự như bootstrap hay JQuery. Và trong document của Laravel, VueJs cũng được giới thiệu qua về cách sử dụng. Tại sao Laravel lại lựa chọn VueJs mà không phải là một framework nào khác? Chắc hẳn VueJs có những đặc điểm ưu việt và nổi trội hơn so với những framework khác.

## VueJS là gì?

- Vue là một framework để xây dựng lên giao diện người dùng, chỉ được sử dụng cho view layout của ứng dụng,vô cùng dễ dàng tích hợp cùng với các nền tảng khác nhau, phù hợp với việc thiết kế single app.

## VueJS hoạt động như thế nào?

- Vue sử dụng một DOM ảo để xử lý, căn bản là tạo ra một bản sao của DOM và lưu trữ nó. Khi có sự thay đổi của một phần DOM nào đó, Vuejs chỉ cập nhật duy nhất thành phần được thay đổi mà không cần tải lại cả DOM đó.

- VueJs lập tức tiếp nhận các events và thay đổi chúng ngay lập tức trên DOM

## Tại sao nên sử dụng Vue trong Laravel?

 Để trả lời câu hỏi này, tôi xin đưa ra một số luận điểm như sau:

- Mọi điều đều diễn ra trên front-end: Ngày nay, những trang web hay ứng dụng trên internet đều được xây dựng theo cách định hướng theo sự kiện. Chúng được xây dựng để đảm bảo người dùng có trải nghiệm liền mạch giống như họ đang xử dụng một dứng ụng đã được cài đặt sẵn trên máy tính của họ. Ngày nay, mọi việc đều được diễn ra trên front-end và người dùng không cần phải tải lại trang nữa.

- Reactive components tạo nên một ứng dụng hướng đối tượng tuyệt vời: Với Vue bạn có thể xây dựng được một ứng dụng toàn diện, là một ứng dụng hướng đối tượng vào mọi thao tác sẽ được thực hiện bên phía fontend. Nó cũng cung cấp các components có thể kết hợp được với nhau, giúp cho bạn dễ dàng sử dụng tùy theo ý muốn của bạn. Với việc kết hợp độc đáo với Laravel, bạn chỉ cần thực hiện một vài thao tác nhỏ với ứng dụng Laravel của mình và thực hiện thay đổi UI bằng cách chuyển tiếp giữa các component với nhau mà hoàn toàn không cần phải reload lại trang.

+ Việc thay đổi UI sẽ được diễn ra một cách liền mạch rên giao diện của bạn, điều này mang lại cho người dùng trải nghiệm tuyệt vời, ví dụ như khi bạn tạo một đoạn văn bản trên trang của bạn, cho phép người dùng chỉnh sửa, sau khi người dùng chỉnh sửa văn bản thì không cần phải tải lại trang nội dung vừa chỉnh sửa sẽ được cập nhật ngay trên web.

+ Về tốc độ và hiệu suất của Vue, ứng dụng của bạn chạy rất nhanh và mượt mà không chiếm quá nhiều tài nguyên máy tính của bạn.

- Tối ưu hóa các trang fontend phức tạp: Nếu bạn đang muốn tạo một ứng dụng web có các thành phần cần thay đổi thường xuyên và liên tục, thì chắc chắn bạn không có lựa chọn nào khác ngoài việc xây dựng một ứng dụng với fontend chạy hoàn toàn bằng Javascript

+ Thách thức với Javascript hoặc Jquery hoặc các thư viện Javascript khống có DOM ảo đó là bạn sẽ gặp phải vấn dề về tần suất cũng như hiệu suất khi số lượng thay đổi hay lượng dữ liệu trở lên quá lớn, các thay đổi trên DOM sẽ dần dần chậm lại, vấn đề này gây cho web của bạn độ delay nhất định. Với một người dùng ứng dụng, chắc chắn là họ sẽ không thể kiên nhẫn đợi web của bạn load quá lâu được.

+ Khi bạn làm ứng dụng của mình với các component của Vue, hệ thống sẽ biết chính xác được component nào cần thay đổi khi việc cập nhật dữ liệu xảy ra, điều này làm cho bản cập nhật cho DOM xử dụng tài nguyên tối thiểu, từ đó cải thiện hiệu quả của ứng dụng

+ Vue cũng tương thích với Flux, Redux và Vuex, rất phù hợp cho việc quản lý các luồng dữ liệu phức tạp

- Ứng dụng một trang: Theo quản điểm cá nhân tôi, single Page application là điều tuyệt vời nhất,toàn bộ data cho ứng dụng của bạn được tải duy nhất 1 lần, và được lưu trong bộ nhớ cache

- Dễ dàng học và xử dụng: VueJs rất dễ dàng để học, nó cung cấp rất ít các tùy chọn cho bạn như là một nhà phát triển, các khái niệm của Vue cũng không có gì là truừ tượng khó hiểu, khi lập trình với Vue, tương tự như việc bạn đang viết javascript thuần vậy. Một điều tuyệt vời khác của Vue là mẫu HTML bình thường bạn viết cũng được chấp nhận trong Vue. Bạn có thể thêm css hay xử lý bằng JS, tùy thuộc vào nhu cầu xử dụng của cá nhân mỗi người

## Xử dụng Vue với Laravel cơ bản

Vue tích hợp độc đáo với Laravel, bạn có thể tạo các Vue Components và xử dụng chúng tương tự như HTML tag bên trong file blade của mình. Từ file blade để truyền dữ liệu vào component của mình, bạn có thể thao tác qua props. 

Trước tiên, hãy tạo một project laravel mới:

```
laravel new vueapp 
```
Nếu Laravel của bạn chưa được cài đặt thì hãy cài đặt nó bằng lệnh sau:

```
composer global require "laravel/installer"
```
Sau khi tạo được một project mới xong, hãy chuyển tới thư mục làm việc bằng lệnh sau:

```
cd vueapp
```

Cài đặt Vue và các thư viện Javascript liên quan bằng lệnh

```
npm install
```
Để ứng dụng của bạn được cập nhật khi có thay đổi trong code, chạy lệnh

```
 $ npm run watch
```

Chạy 

```
$ php artisan serve
```
và truy cập vào ứng dụng của bạn.

## Tạo mới Vue Component

Tạo mới 1 component vô cùng đơn giản, nếu bạn mở file _resources/assets/js/app.js_, bạn có thể thấy Vue đã được import sẵn cho bạn trong đó. Bạn có thể tạo mới Vue component bằng nhiều cách khác nhau, trong bài viết này, tôi sẽ tạo mới mỗi components riêng biệt trong file _resources/assets/js/components_ để mọi thứ gọn gàng hơn. Tất cả các Vue templte đều được kết thúc bằng .vue. Tên bạn có thể đặt tùy ý theo ý thích, miễn sao khi bạn đọc tên một component lên bạn có thể hiểu ngay được ý nghĩa component đó của bạn đang muốn làm gì. Bây giờ hãy tạo một file Welcome.vue với nội dung sau:

```
<template>
        <div class="flex-center position-ref full-height">
            <div class="content">
                <div class="title m-b-md">
                    Welcome to Vue.js on Laravel
                </div>
                <div class="links">
                    <a href="https://laravel.com/docs">View Laravel Docs</a>
                    <a href="https://vuejs.org/v2/guide/">View Vue Docs</a>
                    <a href="https://laracasts.com">Watch Videos</a>
                </div>
            </div>
        </div>
    </template>
    <script>
        export default {}
    </script>
    <style scoped>
        html, body {
            background-color: #fff;
            color: #636b6f;
            font-family: 'Raleway', sans-serif;
            font-weight: 100;
            height: 100vh;
            margin: 0;
        }

        .full-height {
            height: 100vh;
        }

        .flex-center {
            align-items: center;
            display: flex;
            justify-content: center;
        }

        .position-ref {
            position: relative;
        }

        .top-right {
            position: absolute;
            right: 10px;
            top: 18px;
        }

        .content {
            text-align: center;
        }

        .title {
            font-size: 84px;
        }

        .links > a {
            color: #636b6f;
            padding: 0 25px;
            font-size: 12px;
            font-weight: 600;
            letter-spacing: .1rem;
            text-decoration: none;
            text-transform: uppercase;
        }

        .m-b-md {
            margin-bottom: 30px;
        }
    </style>
```

- <template> chứa các tag HTMl cho trang chúng ta đang thực hiện, nếu bạn không đưa HTMl vào thẻ template bạn sẽ phải chỉ định template là gì

- Thẻ <script> là nơi chúng ta xác định toàn bộ logic trên trang
  
## Sử dụng component trong file blade

Để sử dụng được component, trước tiên chúng ta cần khai báo compoent đó. Mở file _resources/assets/js/app.js_ và thêm đoạn code

```
require('./bootstrap');

    window.Vue = require('vue');

    Vue.component('welcome', require('./components/Welcome.vue'));

    const app = new Vue({
        el: '#app'
    });
```

Tiếp theo trong file _resources/views/welcome.blade.php_

```
[...]
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <meta name="csrf-token" content="{{ csrf_token() }}">

            <title>Laravel</title>

    [...]
        <body>
            <div id="app">
                <welcome></welcome>
            </div>
            <script type="text/javascript" src="js/app.js"></script>
        </body>
    [...]
```

Hãy thử reload lại trang web của bạn. Nội dung trong component sẽ được hiển thị

## Truyền data vào trong component

