---
title: "Biến, kiểu dữ liệu, ép kiểu và ghi chú trong Javascript."
date: 2024-12-30
author: Lê Quang Minh
description: Tìm hiểu về cách đặt tên biến, các kiểu dữ liệu, cách ép hiểu và ghi chú trong javascript.
math: true
---

### 1. Biến (Variables)

Biến là các thành phần dùng để lưu trữ dữ liệu hoặc giá trị trong chương trình. Trong JavaScript, bạn có thể khai báo biến bằng các từ khóa: var, let, hoặc const.

let:

Có phạm vi khối (block scope) - nghĩa là chỉ tồn tại trong {}.
Có thể thay đổi giá trị sau khi khai báo

    let age = 25;
    age = 30;

const:

Có phạm vi khối giống let.
Giá trị không thể thay đổi sau khi gán (dùng cho hằng số).

    const pi = 3.14;
    // pi = 3.15; // Lỗi

var:

Phạm vi toàn cục hoặc phạm vi hàm (không phải khối).
Có thể ghi đè giá trị, nhưng dễ gây lỗi nếu không cẩn thận. Vì vậy, nên tránh sử dụng var trong các dự án hiện đại.

    var name = "Minh";

Hoisting:
Với var, khai báo biến sẽ được "đưa lên đầu" phạm vi nhưng không gán giá trị.
Với let và const, biến chỉ tồn tại trong phạm vi khối và không được "hoisted".

### 2. Kiểu dữ liệu (Data Types)

JavaScript hỗ trợ nhiều kiểu dữ liệu khác nhau. Các kiểu dữ liệu này được chia làm hai nhóm chính:

2.1. Kiểu dữ liệu nguyên thủy (Primitive Types):

1. String: Chuỗi ký tự.
    
        let greeting = "Hello, World!";

2. Number: Số nguyên và số thực.    

        let score = 99.5;

3. Boolean: Giá trị logic true hoặc false.

        let isActive = true;

4. Null: Biểu thị một giá trị "trống".

        let emptyValue = null;

5. Undefined: Biến chưa được gán giá trị.

        let notAssigned;

2.2. Kiểu dữ liệu phức tạp (Complex Types)

1. Object: Tập hợp các cặp key-value.

        let person = { name: "Minh", age: 21 };

2. Array: Mảng các giá trị.

        let car = ["Toyota", "Mercedes", "Nissan"];

3. Function: Hàm cũng được coi là một kiểu dữ liệu.

        function greet() {
            return "Hello!";
        }

### 3. Ép kiểu (Type Casting)

JavaScript là một ngôn ngữ kiểu động (dynamically typed), nghĩa là kiểu dữ liệu của biến có thể thay đổi trong quá trình thực thi. Do đó, ép kiểu là một phần quan trọng để kiểm soát dữ liệu.

3.1. Ép kiểu ngầm định (Implicit Type Casting):

JavaScript tự động chuyển đổi kiểu khi thực hiện các phép toán hoặc so sánh.

    console.log('5' + 5); // "55" (chuỗi)
    console.log('5' - 2); // 3 (số)
    console.log(true + 1); // 2 (số)

3.2. Ép kiểu tường minh (Explicit Type Casting):

Lập trình viên có thể chủ động chuyển đổi kiểu bằng cách sử dụng các phương thức như Number(), String(), hoặc Boolean().

    let str = "123";
    let num = Number(str); // Ép kiểu sang số
    console.log(num); // 123
    
    let bool = Boolean(0); // Ép kiểu sang boolean
    console.log(bool); // false

### 4. Ghi chú (Comment)
Ghi chú giúp mã nguồn dễ đọc hơn, đồng thời hỗ trợ trong quá trình bảo trì và debug.

4.1. Comment một dòng

Sử dụng // để thêm ghi chú ngắn gọn.

    let x = 10; // Đây là biến

4.2. Comment nhiều dòng

Sử dụng /* ... */ để ghi chú dài hơn.

    /* Đây là comment thứ nhất
    Còn đây là dòng thứ hai */
    let x = 10; // Đây là biến
