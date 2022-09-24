# For in, For of

- cả for in và for of đều lặp lại trên danh sách các phần tử.
     + nhưng for in sẽ trả về danh sách index của đối tượng đang được lặp.
     + còn for of sẽ trả về values của đối tượng đang được lặp

    => Ex:
        let colors = ['red', 'green', 'blue'];

        for (let i in colors) {
            console.log(i); // "0", "1", "2"
        }

        for (let i of colors) {
            console.log(i); // "red", "green", "blue"
        }

    + For in có thể lặp qua array lẫn object.
    + còn For of chỉ có thể lặp qua array, map, set.

    => Ex: 
        const object = {
            name: "Long",
            address: "Ha Long"
        }

        for (let i in object) {
            console.log(i); // "1", "2"
            console.log(object[i]); // "Long", "Ha Long"
        }
