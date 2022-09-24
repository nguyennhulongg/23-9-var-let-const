# es6

* New Features:
    - Default Parameters - dùng để khai báo các tham số mặc định 
        Example:    
            var link = function(height = 50, color = 'red', url = 'http://azat.co') {
                ...
            }

----------------------------------------------------------------------------------------------------------------------------------

    - Template Literals: dấu `${}`.
        Example: 
            var name = `Your name is ${first} ${last}.` 
            var url = `http://localhost:3000/api/messages/${id}`

----------------------------------------------------------------------------------------------------------------------------------

    - Multi-line String: string nhiều dòng ``.
        Example:
            var fourAgreements =`You have the right to be you.
                                You can only be you when you do your best.`

----------------------------------------------------------------------------------------------------------------------------------

    - Arrow Function - cách viết ngắn gọn hơn khi khai báo 1 function
        Thay vì viết: 
            function functionName() {
                ...
            }
        
        Thì viết: 
            const functionName = () => {

            }

        Nếu arrow function chỉ có 1 tham sô thì không cần dấu ngoặc tròn ()

----------------------------------------------------------------------------------------------------------------------------------

    - Destructuring Assignment.
        Ex: 
            const object = {
                name: "Long",
                address: "Ha Long",
                image: "image-link"
            }

        const { name, address, image } = object;
        const { name, ...rest } = object;

        console.log(name, address) ra "Long", "Ha Long" và "image-link"
        console.log(rest) ra "Ha Long" và "address-link" 

----------------------------------------------------------------------------------------------------------------------------------

    - Enhanced Object Literals: 
        - định nghĩa key và value ngắn gọn hơn
        - định nghĩa method cho object   
            Ex: 
                var name = "Long";
                var address = "Ha Long";

                var infor = {
                    name: name,
                    address: address,
                    getName: function() {
                        return name;
                    }
                };

            + ở ES6 bỏ chữ function cho method
            + Ở đây object infor có key và value trùng tên nhau(name trùng name, address trùng address) nên có thể viết luôn như này

                 var infor = {
                    name,
                    address ,
                    getName() {
                        return name;
                    },
                };
        - định nghĩa key cho object dưới dạng biến:
            Ex:
                var fieldName = "name";
                var fieldAddress = "address";

                var info = {
                    name: "Long"
                    address: "Ha Long"
                };

----------------------------------------------------------------------------------------------------------------------------------

    - Promises
        1. là 1 đối tượng sẽ trả về 1 giá trị trong tương lai.
        2. giúp xử lý vấn đề bất đồng bộ hiệu quả hơn.
        3. sinh ra để giải quyết kết quả của 1 hành động cụ thể.
        4. giúp giải quyết vấn đề Callback hell.
        4. có 3 trạng thái: 
                        + Fulfilled: hành động xử lý xong và thành công.
                        + Reject: hành động xử lý xong và thất bại.
                        + Pending: hành động đang chờ xử lý hoặc bị từ chối,
        5. cú pháp tạo 1 promise: 
                var promise = new Promise(callback);

            Trong đó Callback là 1 function có 2 tham số truyền vào là: Resolve và Reject
                var promise = new Promise(function(resolve, reject){
            });

----------------------------------------------------------------------------------------------------------------------------------

    - Block-Scoped Constructs Let and Const - Let cho phép chúng ta khai báo biến trong phạm vi các khối lệnh,
        các khối lệnh phạm vi bởi các cặp ngoặc nhọn {}.

----------------------------------------------------------------------------------------------------------------------------------

    - Classes.

----------------------------------------------------------------------------------------------------------------------------------

    - Modules: 
        + Ở 1 file tool.js export ra generateRandom và sum: 
            function generateRandom() {
                return Math.random();
            }

            function sum(a, b) {
                return a + b;
            }

            export { generateRandom, sum } 
        + ở 1 file js khác(App.js) có thể import module đã export ở trên.
            import { generateRandom, sum } from 'utility';

                console.log(generateRandom());
                console.log(sum(1, 2));
