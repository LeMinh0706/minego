---
title: "Multithread trong java."
date: 2024-12-30
author: Lê Quang Minh
description: Tìm hiểu về đa luồng trong java.
math: true
---

Multithreading trong Java là một kỹ thuật lập trình cho phép thực hiện đồng thời nhiều luồng (thread) trong một ứng dụng. Đây là một phần quan trọng trong lập trình song song để tận dụng tài nguyên CPU tốt hơn và cải thiện hiệu năng.

### 1. Tổng quan về Thread trong Java

Thread: Là đơn vị thực thi nhỏ nhất trong một chương trình.

Multithreading: Là việc thực hiện đồng thời nhiều thread trong một ứng dụng.

JVM quản lý các thread, cung cấp khả năng tạo và quản lý chúng dễ dàng thông qua các API Java.

### 2. Tạo thread trong Java

Multithreading trong Java là một kỹ thuật lập trình cho phép thực hiện đồng thời nhiều luồng (thread) trong một ứng dụng. Đây là một phần quan trọng trong lập trình song song để tận dụng tài nguyên CPU tốt hơn và cải thiện hiệu năng.
1. Tổng quan về Thread trong Java

    Thread: Là đơn vị thực thi nhỏ nhất trong một chương trình.
    Multithreading: Là việc thực hiện đồng thời nhiều thread trong một ứng dụng.
    JVM quản lý các thread, cung cấp khả năng tạo và quản lý chúng dễ dàng thông qua các API Java.

2. Tạo Thread trong Java

Có hai cách chính để tạo thread trong Java:

    // Cách 1
    class MyThread extends Thread {
        @Override
        public void run() {
            System.out.println("Thread đang chạy: " + Thread.currentThread().getName());
        }
    }

    public class Main {
        public static void main(String[] args) {
            MyThread thread1 = new MyThread();
            MyThread thread2 = new MyThread();

            thread1.start(); // Bắt đầu thread
            thread2.start();
        }
    }


    // Cách 2
    class MyRunnable implements Runnable {
        @Override
        public void run() {
            System.out.println("Thread đang chạy: " + Thread.currentThread().getName());
        }
    }

    public class Main {
        public static void main(String[] args) {
            Thread thread1 = new Thread(new MyRunnable());
            Thread thread2 = new Thread(new MyRunnable());

            thread1.start();
            thread2.start();
        }
    }
