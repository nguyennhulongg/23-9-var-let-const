* Promise: 
    + ra mắt ở ES6, dùng để tránh callback hell,
    + dùng để lập trình đồng bộ, phải chạy fn 1 để có data 1, dùng data 1 để query data 2

    + cú pháp:
        const promise = new Promise(resolve, reject => {
            
        })

    - Promise all: tập hợp 1 mảng các promises và chỉ resolve khi tất cả các promises này hoàn thành.
    - Promise race: tập hợp 1 mảng các promises và resolve ngay khi một trong số những promise hoàn thành.    
