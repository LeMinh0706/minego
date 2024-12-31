---
title: "Toán tử trong javascript."
date: 2024-12-30
author: Lê Quang Minh
description: Cùng tìm hiểu về những khái niệm sơ bộ về toán tử (operator) trong javascript.
math: true
---

Toán tử là các ký hiệu đặc biệt hoặc từ khóa được sử dụng để thực hiện các thao tác trên các giá trị, biến hoặc biểu thức trong JavaScript.

JavaScript cung cấp một loạt các toán tử để xử lý dữ liệu và thực hiện các phép toán, từ toán học cơ bản đến logic phức tạp.

### 1. Phân loại Operators
1.1. Arithmetic Operators (Toán tử số học)

    const a = 10;
    const b = 3;

    console.log(a + b); // Cộng: 13
    console.log(a - b); // Trừ: 7
    console.log(a * b); // Nhân: 30
    console.log(a / b); // Chia: 3.333...
    console.log(a % b); // Chia lấy dư: 1
    console.log(a ** b); // Lũy thừa: 10^3 = 1000

1.2. Assignment Operators (Toán tử gán)

    let x = 5;

    x += 3; // Tương đương x = x + 3
    console.log(x); // 8

    x *= 2; // Tương đương x = x * 2
    console.log(x); // 16

    x %= 3; // Tương đương x = x % 3
    console.log(x); // 1

1.3. Comparison Operators (Toán tử so sánh)

    const a = 5;
    const b = "5";

    console.log(a == b);  // true 
    console.log(a === b); // false 
    console.log(a != b);  // false 
    console.log(a !== b); // true 

    console.log(a > 3);   // true
    console.log(a <= 5);  // true

1.4. Logical Operators (Toán tử logic)

    const x = true;
    const y = false;

    console.log(x && y); // AND: false
    console.log(x || y); // OR: true
    console.log(!x);     // NOT: false
