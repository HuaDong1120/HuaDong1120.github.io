---
title: C++著名库Boost.asio
date: 2023-08-20 18:22:07
tags: Asio
categories: C++
keywords: "C++"
cover: https://hdblog-image.oss-cn-nanjing.aliyuncs.com/image/asio.png
---
```c++
#include<Windows.h>
//函数原型
HANDLE  CreateRemoteThread(
    Handle hProcess,                        
    LPSECURITY_ATTRIBUTES lpThreadAttributes,
    SIZE_T dwStackSize,
    LPTHREAD_START_ROUTINE lpStartAddress,
    LPVOID lpParameter,
    DWORD dwCreationFlags,
    LPDWORD lpThreadId);
//参数解释
//1,hProcess  -- 目标进程的进程句柄，一般通过获取进程id来获取，HANDLE hProc = OpenProcess(PROCESS_ALL_ACCESS, 1, pid);pid为进程id
//2,lpThreadAttributes   -- 线程安全描述符，一般为NULL
//3,dwStackSize   --- 新的线程栈大小，0表示使用默认大小
//4,lpStartAddress   --- 新线程的入口函数，需要是可执行代码地址，这个一般用来加载注入的代码，ex:(LPTHREAD_START_ROUTINE)loadLibraryA
//5,lpParameter   --- 传给新线程的参数
//6,dwCreationFlags  --- 新线程创建标志，一般为0
//7,lpThreadId   ---  接收新线程的ID地址
//return HANDLE --- 返回值,如果成功返回新线程的句柄，失败返回NULL.
```