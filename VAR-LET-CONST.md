# 23-9-var-let-const

* VAR: 
    - Khai báo: 
        + Có thể khai báo lại.
            Ex:    
                var name = "Long";
                var name = "Son";

            console.log(name); => "Son"

        + Có thể khai báo biến mà không gán giá trị cho biến.
            Ex:
                var name;
                console.log(name); => undefined
    - Hoisting
        + Có hoisting.
            Ex: 
                console.log(name); => undefined
                var name = "Long" => cái name này sẽ được bê lên trên dòng console.log(name);
    - Scope:
        + Không có block scope 
            Ex: 
                if(true) {
                    var name = "Long"
                }
                
                console.log(name) => vẫn log ra "Long" bình thường

        + Chỉ có function scope(biến khai báo trong function scope chỉ tồn tại trong function scope)
            Ex: 
                function info() {
                    var name = "Long";
                }

                info();

                console.log(name); => báo lỗi

-------------------------------------------------------------------------------------------------------------------------------

* LET:
    - Khai báo:
        + Không thế khai báo lại.
            Ex:
                let name = "Long";
                let name = "Son";
            => báo lỗi

        + Không cho khai báo lại nhưng lại cho cập nhật giá trị của biến
            Ex:
                let name = "Long";
                name = "Son";
            => thế này thì ok con dê

        + Có thể khai báo biến mà không gán giá trị.
            Ex: 
                let name;
                console.log(name); => undefined

    - Hoisting: 
        + Thực chất là có hoisting nhưng let lại không có giá trị khởi tạo(còn var thì có giá trị khởi tạo là undefined) nên là dùng let trước khai báo sẽ báo lỗi "Reference Error".
            Ex:    
                console.log(name); => báo lỗi đỏ lòm
                let name = "Long"

    - Scope:
        + Có block scope, có cả function scope luôn.
            Ex: 
                if(true) {
                    let name = "Long";
                }

                console.log(name); => báo lỗi. (đối với function cũng tương tự).

        + trong vòng lặp for sẽ dùng let để khai báo biến
            Ex:
                for(let i = 0; i < 3; i++) {
                    console.log(i); => 0, 1, 2
                }

-------------------------------------------------------------------------------------------------------------------------------

* CONST:
    - Khai báo:
        + Nếu trường hợp kiểu của biến là kiểu primitive không thế khai báo lại cũng không thể cập nhật được luôn.
            (kiểu primitive gồm number, string, boolean, null, undefined)
            Ex:
                const name = "Long";
                const name = "Son";
                
                console.log(name) => báo lỗi

        + Còn nếu giá trị của biến mà ở dạng reference thì mặc dù không khai báo lại hoặc cập nhật được giá trị của biến cơ mà cập nhật thuộc tính của biến thì được.
            (kiểu reference gồm array, object, function)
            Ex: 
                const info = {
                    name: "Long",
                    address: "Ha Long"
                }

                info.name = "Son";
                console.log(info.name) => Son

        + Khi khai báo biến thì phải gán giá trị
            Ex: 
                const name; => báo lỗi ngay luôn

    - Hoisting:
        + Không có hoisting
            Ex: 
                console.log(name);
                const name = "Long"; => báo lỗi
    - Scope:
<<<<<<< HEAD
        + Có block scope(tương tự như let)

    ===> Chú ý: đối với vòng lặp for không được dùng const để khai báo vì const là duy nhất, là 1 hằng số, const không thay đổi
=======
        + Có block scope.


* VAR: 
    - Khai báo: 
        + Có thể khai báo lại.
        + Có thể khai báo biến mà không gán giá trị cho biến.
    - Hoisting
        + Có hoisting.
    - Scope:
        + Không có block scope 
        + Chỉ có function scope(biến khai báo trong function scope chỉ tồn tại trong function scope)

-------------------------------------------------------------------------------------------------------------------------------

* LET:
    - Khai báo:
        + Không thế khai báo lại.
        + Có thể khai báo biến mà không gán giá trị.
    - Hoisting: 
        + Không có hoisting.
    - Scope:
        + Có block scope.

-------------------------------------------------------------------------------------------------------------------------------

* CONST:
    - Khai báo:
        + Không thế khai báo lại.
        + Khi khai báo biến thì phải gán giá trị
    - Hoisting:
        + Không có hoisting
    - Scope:
        + Có block scope.

>>>>>>> 5a0f022572dde0382c995a128c60fcf460b39325