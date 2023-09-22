# Crawling comments from a Youtube video
Tags: Khai thác dữ liệu và khai phá tri thức.
## Giới thiệu vấn đề
Bởi Youtube là một *website động* (dynamic website) và các bình luận (comment) chỉ hiện lên khi người dùng truy cập xuống phần dưới cùng của video. Nên chúng ta không thể sử dụng cách crawl thông thường trong python với thư viện **requests** và **BeautifulSoup** được, mà thay vào đó ta phải sử dụng thư viện **selenium**. Trong bài toán này, selenium giúp chúng ta truy cập đến các thông tin ẩn của website bằng việc mô phỏng các hành vi giống người dùng. Nói cách khác là giải quyết cho ta vấn đề khiến trang video mong muốn trên youtube hiện lên các comment. Từ đó, ta mới thực hiện hành vi scrape dữ liệu comment được.

Chương trình sẽ sử dụng **ChromeDriver** của **Selenium WebDriver** để điều khiển và định hướng Chrome browser truy cập đến trang video của Youtube và thực hiện việc lấy về những dữ liệu mà ta mong muốn.

Lưu ý, chương trình được viết vào khoảng tháng 7 năm 2022 trên Google Colab và không có crawl reply của các comment. Chú ý sửa lại dường dẫn các file cho phù hợp với máy tính của bạn trước khi sử dụng.
## Về dữ liệu
youtube_comment_dataset.csv: Dataset kết quả sau khi crawl một video trên Youtube vào ngày 4 tháng 7 năm 2022, chứa khoảng 3200 comment của một video tiếng Việt. Đây chỉ là một Dataset thô sơ, do đó, code trong project này còn cung cấp thêm một số thao tác xử lý dữ liệu để tham khảo.
