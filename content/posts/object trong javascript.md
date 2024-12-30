---
title: "Object trong javascript."
date: 2024-12-30
author: Lê Quang Minh
description: Cùng tìm hiểu về những khái niệm của Object.
math: true
---

Object là một trong những kiểu dữ liệu cơ bản và quan trọng nhất trong JavaScript. Nó cho phép bạn lưu trữ, quản lý và thao tác dữ liệu phức tạp dưới dạng các cặp key-value (khoá và giá trị). Hãy cùng tìm hiểu chi tiết về cách sử dụng Object trong JavaScript!

### 1. Khái niệm về Object

Trong JavaScript, Object là một tập hợp các cặp key-value.

- Key (khoá): Là một chuỗi (hoặc ký hiệu - symbol) đại diện cho tên thuộc tính.
- Value (giá trị): Có thể là bất kỳ kiểu dữ liệu nào, bao gồm cả hàm, các object khác, hoặc giá trị nguyên thuỷ.

        const person = {
            name: "Minh",
            age: 21,
            isStudent: false,
            greet: function() {
                console.log(`Hello, my name is ${this.name}!`);
            },
        };

        console.log(person.name); // "Minh"
        person.greet(); // "Hello, my name is Minh!"

### 2. Tạo Object
2.1. Tạo bằng cú pháp chữ (Object Literal)

Đây là cách phổ biến và đơn giản nhất để tạo một object.
    
    const car = {
        brand: "Toyota",
        model: "Vios",
        year: 2018,
    };

2.2. Tạo bằng từ khoá new Object()

Cách này ít được sử dụng nhưng vẫn hợp lệ.

    const car = new Object();
    car.brand = "Toyota";
    car.model = "Camry";
    car.year = 2022;

2.3. Tạo bằng hàm Constructor

Bạn có thể sử dụng hàm để tạo object.

    function Car(brand, model, year) {
        this.brand = brand;
        this.model = model;
        this.year = year;
    }

    const car1 = new Car("Toyota", "Vios", 2018);
    console.log(car1.brand); // "Toyota"

### 3. Truy cập thuộc tính trong Object
3.1. Sử dụng dấu chấm (.)

Dùng khi key là một tên hợp lệ của biến (không có khoảng trắng, ký tự đặc biệt).

    console.log(person.name); // "Minh"

3.2. Sử dụng dấu ngoặc vuông ([])

Dùng khi key là chuỗi hoặc chứa ký tự đặc biệt, hoặc khi truy cập bằng biến.

    console.log(person["age"]); // 21

    const key = "isStudent";
    console.log(person[key]); // true

### 4. Thêm, sửa, và xoá thuộc tính
4.1. Thêm thuộc tính

Chỉ cần gán giá trị cho một key mới.

    person.hair = "black";
    console.log(person.hair); // black

4.2. Sửa giá trị

Gán giá trị mới cho key hiện có.

    person.age = 22;
    console.log(person.age); // 22

4.3. Xoá thuộc tính

Sử dụng từ khoá delete.

    delete person.isStudent;
    console.log(person.isStudent); // undefined

### 5. Lặp qua các thuộc tính của Object
5.1. Sử dụng for...in

Duyệt qua tất cả các thuộc tính liệt kê được.

    for (let key in person) {
        console.log(`${key}: ${person[key]}`);
    }

5.2. Sử dụng Object.keys()

Trả về một mảng các key.

    Object.keys(person).forEach((key) => {
        console.log(`${key}: ${person[key]}`);
    });

5.3. Sử dụng Object.values()

Trả về một mảng các giá trị.

    console.log(Object.values(person)); // ["Minh", 22, undefined, ƒ]

5.4. Sử dụng Object.entries()

Trả về một mảng các cặp [key, value].

    Object.entries(person).forEach(([key, value]) => {
        console.log(`${key}: ${value}`);
    });

### 6. Tính kế thừa của Object
6.1. Kế thừa nguyên mẫu (Prototype)

Mỗi object trong JavaScript có một nguyên mẫu (prototype) mà nó kế thừa các thuộc tính và phương thức.

    const obj = {};
    console.log(obj.toString()); // "[object Object]"

6.2. Kế thừa bằng cách tạo Object

Sử dụng Object.create() để kế thừa.

    const parent = { greet: () => console.log("Hello!") };
    const child = Object.create(parent);
    child.name = "Child";
    child.greet(); // "Hello!"

