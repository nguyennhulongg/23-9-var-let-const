# 23-9-bất-đồng-bộ

* Đồng bộ, bất đồng bộ:
    - Bất đồng bộ: khi A bắt đầu thực hiện, chương trình tiếp tục thực hiện B mà không đợi A kết thúc.
    - Đồng bộ: thực hiện các công việc 1 cách tuần tự, A thực hiện xong mới đến lượt B.

* CÓ 3 CÁCH XỬ LÝ BẤT ĐỒNG BỘ:
    - Callback: là 1 đoạn code được truyền vào như 1 tham số của 1 hàm.
        + Callback hell: quá nhiều callback được lồng vào nhau, nhìn khó đọc

    ------------------------------------------------------------------------------------------------

    - Promises: khi 1 promise được khởi tạo thì sẽ có 3 trạng thái:
        + Fulfilled: hành động xử lý xong và thành công.
        + Rejected: hành động xử lý xong và thất bại.
        + Pending: hành động đang chờ xử lý hoặc 1 từ chối

    ------------------------------------------------------------------------------------------------

    - Async/Await:
        + Function thường: từ khoá async đứng trước chữ function.
        + Arrow function: từ khoá async đứng trước tập tham số.
        + Return ra promise


