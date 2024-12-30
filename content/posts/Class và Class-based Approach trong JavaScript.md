---
title: "Class và Class-based Approach trong JavaScript."
date: 2024-12-30
author: Kris Nóva
description: Tìm hiểu về cách đặt tên biến, các kiểu dữ liệu, cách ép hiểu và ghi chú trong javascript.
math: true
---

Trong JavaScript, class là một cách tổ chức và sử dụng code để tạo các đối tượng theo hướng lập trình hướng đối tượng (OOP). Nó được giới thiệu từ ECMAScript 2015 (ES6) và cung cấp cú pháp rõ ràng, dễ đọc hơn so với việc sử dụng các hàm khởi tạo (constructor function) truyền thống.

### 1. Class là gì?

Class trong JavaScript là một "khuôn mẫu" (blueprint) để tạo các đối tượng có thuộc tính (property) và phương thức (method). Class cung cấp cú pháp đơn giản hơn để làm việc với lập trình hướng đối tượng.

    class Person {
        constructor(name, age) {
            this.name = name; // Thuộc tính
            this.age = age;
        }

        greet() { // Phương thức
            console.log(`Hi, I'm ${this.name}, and I'm ${this.age} years old.`);
        }
    }

    const person1 = new Person("Minh", 22);
    person1.greet(); // "Hi, I'm Minh, and I'm 22 years old."


### 2. Cấu trúc của một Class

2.1. Constructor

Phương thức đặc biệt được gọi khi một đối tượng mới được tạo từ class.
Sử dụng để khởi tạo giá trị thuộc tính.

    class Car {
        constructor(brand, model) {
            this.brand = brand;
            this.model = model;
        }
    }

2.2. Thuộc tính

Được định nghĩa trong constructor hoặc trực tiếp trong class (từ ES2022 hỗ trợ).

    class Car {
        brand = "Toyota"; // Thuộc tính trực tiếp
        constructor(model) {
            this.model = model; // Thuộc tính qua constructor
        }
    }

2.3. Phương thức

Được định nghĩa trực tiếp trong class, dùng để thêm hành vi cho các đối tượng.

    class Car {
        start() {
            console.log("Car is starting...");
        }
    }

2.4. Getter và Setter

Getter để lấy giá trị thuộc tính.
Setter để gán giá trị thuộc tính.

    class Person {
        constructor(name) {
            this._name = name; 
        }

        get name() {
            return this._name.toUpperCase();
        }

        set name(newName) {
            this._name = newName;
        }
    }

    const person = new Person("Alice");
    console.log(person.name); // "ALICE"
    person.name = "Bob";
    console.log(person.name); // "BOB"

2.5. Static Method

Là phương thức thuộc về class, không thuộc về đối tượng cụ thể.
Được gọi bằng class thay vì đối tượng.

    class MathUtils {
        static add(a, b) {
            return a + b;
        }
    }

    console.log(MathUtils.add(2, 3)); // 5

### 3. Tính kế thừa (Inheritance)

JavaScript cho phép một class kế thừa từ class khác bằng từ khoá extends. Class con có thể sử dụng và mở rộng thuộc tính, phương thức của class cha.

    class Animal {
        constructor(name) {
            this.name = name;
        }

        speak() {
            console.log(`${this.name} makes a sound.`);
        }
    }

    class Dog extends Animal {
        speak() {
            console.log(`${this.name} barks.`);
        }
    }

    const dog = new Dog("Buddy");
    dog.speak(); // "Buddy barks."

### 4. Class-based Approach

Cách tiếp cận dựa trên class (class-based approach) là một phong cách lập trình trong đó bạn sử dụng class để xây dựng ứng dụng. Điều này thường được sử dụng trong các ứng dụng lớn cần tổ chức rõ ràng.
Ưu điểm:

Tái sử dụng code: Class cho phép bạn sử dụng lại các thuộc tính và phương thức thông qua kế thừa.
Tổ chức tốt hơn: Mã nguồn dễ đọc và quản lý hơn với các khối rõ ràng.
Hỗ trợ tốt cho OOP: Các khái niệm như kế thừa, đóng gói (encapsulation), và đa hình (polymorphism) được hỗ trợ tự nhiên.

    class User {
        constructor(username, email) {
            this.username = username;
            this.email = email;
        }
    
        login() {
            console.log(`${this.username} logged in.`);
        }
    
        logout() {
            console.log(`${this.username} logged out.`);
        }
    }
    
    class Admin extends User {
        deleteUser(user) {
            console.log(`Admin deleted user: ${user.username}`);
        }
    }
    
    const user1 = new User("johnDoe", "john@example.com");
    user1.login(); // "johnDoe logged in."
    
    const admin = new Admin("adminUser", "admin@example.com");
    admin.deleteUser(user1); // "Admin deleted user: johnDoe"
