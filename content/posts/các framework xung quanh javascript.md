---
title: "Các framework sử dụng Javascript."
date: 2024-12-30
author: Lê Quang Minh
description: Tìm hiểu về framework frontend, backend được xây dựng với ngôn ngữ javascript.
math: true
---

JavaScript là một trong những ngôn ngữ lập trình phổ biến nhất hiện nay, và nó có rất nhiều framework được thiết kế để hỗ trợ phát triển ứng dụng một cách nhanh chóng và hiệu quả. Dưới đây là các framework JavaScript nổi bật, được phân loại theo mục đích sử dụng:

### 1. Frontend Frameworks 
1.1. React

Đặc điểm:
- Được phát triển bởi Facebook.
- Hỗ trợ xây dựng giao diện người dùng thông qua các component.
- Sử dụng Virtual DOM để tăng hiệu suất.
Dùng cho: Xây dựng giao diện người dùng phức tạp.

        import React from 'react';

        function App() {
          return <h1>Hello, React!</h1>;
        }

        export default App;

1.2. Angular

Đặc điểm:
- Được phát triển bởi Google.
- Một framework toàn diện với cấu trúc mạnh mẽ.
- Hỗ trợ hai chiều dữ liệu (two-way data binding) và Dependency Injection.

Dùng cho: Ứng dụng web lớn với cấu trúc phức tạp.

        import { Component } from '@angular/core';

        @Component({
          selector: 'app-root',
          template: '<h1>Hello, Angular!</h1>',
        })
        export class AppComponent {}

1.3. Vue.js

Đặc điểm:

- Nhẹ, dễ học, linh hoạt.
- Tập trung vào giao diện người dùng.
- Hỗ trợ Single File Components (SFC) và reactive binding.

Dùng cho: Ứng dụng từ nhỏ đến vừa, hoặc tích hợp vào các dự án hiện có.

        import { createApp } from 'vue';

        const App = {
          template: '<h1>Hello, Vue!</h1>',
        };

        createApp(App).mount('#app');

### 2. Backend Frameworks (Phát triển phía server)

2.1. Node.js

Đặc điểm:

- Một runtime môi trường chứ không phải framework.
- Hỗ trợ xây dựng ứng dụng server nhanh và hiệu quả nhờ sử dụng event-driven.

Dùng cho: API backend, ứng dụng thời gian thực.

        const http = require('http');

        const server = http.createServer((req, res) => {
          res.writeHead(200, { 'Content-Type': 'text/plain' });
          res.end('Hello, Node.js!');
        });

        server.listen(3000);

2.2. Express.js

Đặc điểm:

- Framework nhẹ trên Node.js.
- Hỗ trợ middleware và xây dựng RESTful API dễ dàng.

Dùng cho: API backend hoặc ứng dụng web đơn giản.

        const express = require('express');
        const app = express();

        app.get('/', (req, res) => {
          res.send('Hello, Express!');
        });

        app.listen(3000, () => {
          console.log('Server running on port 3000');
        });


2.3. NestJS

Đặc điểm:

- Framework mạnh mẽ, dựa trên TypeScript.
- Hỗ trợ Dependency Injection và Module System.

Dùng cho: Ứng dụng server phức tạp, tổ chức theo module.

        import { Controller, Get } from '@nestjs/common';

        @Controller()
        export class AppController {
          @Get()
          getHello(): string {
            return 'Hello, NestJS!';
          }
        }

### 3. Full-Stack Frameworks

3.1. Next.js

Đặc điểm:

- Framework dựa trên React.
- Hỗ trợ Server-Side Rendering (SSR) và Static Site Generation (SSG).

Dùng cho: Ứng dụng web full-stack hoặc các dự án SEO.

        export default function Home() {
          return <h1>Hello, Next.js!</h1>;
        }
