---
title: "Hàm trong javascript."
date: 2024-12-30
author: Lê Quang Minh
description: Cùng tìm hiểu về những khái niệm sơ bộ về hàm.
math: true
---

Hàm (Function) là một khối mã được định nghĩa để thực hiện một nhiệm vụ cụ thể. Nó cho phép bạn tổ chức và tái sử dụng mã trong chương trình một cách hiệu quả. Trong JavaScript, hàm có nhiều loại và có thể được sử dụng linh hoạt. Hãy cùng tìm hiểu chi tiết!

### 1. Định nghĩa hàm

Hàm được định nghĩa bằng từ khóa function, theo sau là tên hàm, danh sách tham số (nếu có), và thân hàm được đặt trong cặp ngoặc {}.

    function functionName(parameters) {
        // Thân hàm
        return value; // Giá trị trả về (tùy chọn)
    }

Hàm trong JavaScript

Hàm (Function) là một khối mã được định nghĩa để thực hiện một nhiệm vụ cụ thể. Nó cho phép bạn tổ chức và tái sử dụng mã trong chương trình một cách hiệu quả. Trong JavaScript, hàm có nhiều loại và có thể được sử dụng linh hoạt. Hãy cùng tìm hiểu chi tiết!
1. Định nghĩa hàm

Hàm được định nghĩa bằng từ khóa function, theo sau là tên hàm, danh sách tham số (nếu có), và thân hàm được đặt trong cặp ngoặc {}.
Cú pháp cơ bản:

function functionName(parameters) {
    // Thân hàm
    return value; // Giá trị trả về (tùy chọn)
}

Ví dụ:

function greet(name) {
    return `Hello, ${name}!`;
}
console.log(greet("Alice")); // "Hello, Alice!"

### 2. Một số loại hàm trong JavaScript
2.1. Hàm khai báo (Function Declaration)

Được định nghĩa bằng từ khóa function.
Có thể được gọi trước khi khai báo nhờ hoisting.

    sayHello();

    function sayHello() {
        console.log("Hello!");
    }

2.2. Hàm biểu thức (Function Expression)

Hàm được gán vào một biến hoặc hằng số.
Không được hoisting.

    const greet = function(name) {
        return `Hi, ${name}!`;
    };
    console.log(greet("Bob"));

2.3. Arrow Function

Cú pháp ngắn gọn hơn.
Không có từ khóa this, arguments, super, hoặc khả năng được hoisting.

    // const functionName = (parameters) => expression;

    const add = (a, b) => a + b;
    console.log(add(5, 3)); // 8

Với thân hàm phức tạp, dùng {}:

    const greet = (name) => {
        console.log("Hello");
        return `Hello, ${name}!`;
    };
    console.log(greet("Alice"));



