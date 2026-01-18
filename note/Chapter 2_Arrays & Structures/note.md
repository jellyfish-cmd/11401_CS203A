# Chapter 2：Arrays & Structures
「資料放在記憶體裡的形式」

本章在回答一個最基本、也最重要的問題：
### 資料在電腦裡，到底是「怎麼放的」？

---

# 1. Array（陣列）

An array is a collection of elements of the same data type stored in contiguous memory locations.

### 陣列是一排「連續座位」的資料。
### 每個元素型別一樣、位置固定。

## 特點
- 記憶體 **連續**
- 可以用 index 直接存取
- 第 i 個元素 → O(1)

## 優點
- 存取速度快
- 結構簡單

## 缺點
- 大小固定（傳統陣列）
- 插入、刪除成本高（要搬資料）

## Big-O
- 存取：O(1)
- 搜尋：O(n)
- 插入 / 刪除：O(n)

### 一句話記法
> 「位置固定、拿很快，改很痛」

---

# 2. Structure（結構，struct）

A structure is a collection of variables of different data types grouped together.

### struct 是把「不同種類的資料」綁成一包。
### 像一張資料表的一列。

## 例子（概念）
```c
struct student {
    char name;
    int id;
    char grade;
};
