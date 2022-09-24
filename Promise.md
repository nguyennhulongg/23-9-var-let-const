* Promise: 
    - dùng để lập trình đồng bộ, phải chạy fn 1 để có data 1, dùng data 1 để query data 2

    1. là 1 đối tượng sẽ trả về 1 giá trị trong tương lai.
    2. giúp xử lý vấn đề bất đồng bộ hiệu quả hơn.
    3. sinh ra để giải quyết kết quả của 1 hành động cụ thể.
    4. giúp giải quyết vấn đề bất đồng bộ mà không rơi vào callback hell hoặc pyramid of doom
    5. có 3 trạng thái: 
                + Fulfilled: hành động xử lý xong và thành công.
                + Reject: hành động xử lý xong và thất bại.
                + Pending: hành động đang chờ xử lý hoặc bị từ chối,
    6. cú pháp tạo 1 promise: 
            var promise = new Promise(callback);

        Trong đó Callback là 1 function có 2 tham số truyền vào là: Resolve và Reject
            var promise = new Promise(function(resolve, reject){
        });

    - Promise all: tập hợp 1 mảng các promises và chỉ resolve khi tất cả các promises này hoàn thành.
    - Promise race: tập hợp 1 mảng các promises và resolve ngay khi một trong số những promise hoàn thành.    
