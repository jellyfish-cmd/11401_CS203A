# Chapter 7：Sorting（排序）
將資料依照規則重新排列

本章要解決的核心問題是：
### 如何把一堆「亂的資料」，有效率地排成「有序的資料」。

---

## 7.1 Sorting 的基本概念

Sorting 是指：
### 將資料依照某種順序（通常是遞增或遞減）重新排列。

### 為什麼排序很重要？
- 搜尋會變快
- 資料更好理解
- 許多演算法的前置步驟

---

## 7.2 Sorting 的分類方式

### 1. Internal Sorting
- 資料全部放在主記憶體中
- 本章重點

### 2. External Sorting
- 資料太大，需使用硬碟
- 不在本章重點範圍

---

## 7.3 Selection Sort（選擇排序）

Selection sort repeatedly selects the smallest element from the unsorted part.

### 概念
### 每一輪，從還沒排好的資料中，選出最小的，放到正確位置。

---

### 操作流程
1. 找最小值
2. 與目前位置交換
3. 縮小未排序範圍

---

### 特點
- 比較次數固定
- 實作簡單

---

### Big-O
- 最好：O(n²)
- 平均：O(n²)
- 最壞：O(n²)

---

## 7.4 Insertion Sort（插入排序）

Insertion sort builds the sorted list one element at a time.

### 概念
### 像整理撲克牌，一張一張插到對的位置。

---

### 操作流程
1. 假設左邊已排序
2. 取下一個元素
3. 插入正確位置

---

### 特點
- 資料接近有序時很快
- 適合小資料量

---

### Big-O
- 最好：O(n)
- 平均：O(n²)
- 最壞：O(n²)

---

## 7.5 Bubble Sort（氣泡排序）

Bubble sort repeatedly swaps adjacent elements if they are in the wrong order.

### 概念
### 大的數字會像氣泡一樣慢慢浮到後面。

---

### 特點
- 實作最簡單
- 效率最差之一

---

### Big-O
- 最好：O(n)（加上最佳化）
- 平均：O(n²)
- 最壞：O(n²)

---

## 7.6 Quick Sort（快速排序）

Quick sort uses divide-and-conquer strategy.

### 概念
### 選一個基準值（pivot），小的放左邊，大的放右邊。

---

### 特點
- 實務最常用
- 平均速度非常快

---

### Big-O
- 平均：O(n log n)
- 最壞：O(n²)
- 空間：O(log n)

---

## 7.7 Merge Sort（合併排序）

Merge sort divides the list into halves, sorts them, and merges them.

### 概念
### 一直對半切，排好再合起來。

---

### 特點
- 穩定排序
- 需要額外空間

---

### Big-O
- 最好：O(n log n)
- 平均：O(n log n)
- 最壞：O(n log n)
- 空間：O(n)

---

## 7.8 Heap Sort（堆積排序）

Heap sort uses a heap data structure to sort elements.

### 概念
### 利用 Heap，每次取最大或最小。

---

### 特點
- 不需要額外記憶體
- 一定是 O(n log n)

---

### Big-O
- 最好：O(n log n)
- 平均：O(n log n)
- 最壞：O(n log n)

---

## 7.9 Sorting 演算法比較（重點表）

| 排序法 | 平均時間 | 最壞時間 | 穩定性 |
|---|---|---|---|
| Selection | O(n²) | O(n²) | 無 |
| Insertion | O(n²) | O(n²) | 有 |
| Bubble | O(n²) | O(n²) | 有 |
| Quick | O(n log n) | O(n²) | 無 |
| Merge | O(n log n) | O(n log n) | 有 |
| Heap | O(n log n) | O(n log n) | 無 |

---

## Chapter 7 重點總結

- 排序是很多演算法的基礎
- 小資料 → Insertion
- 大資料（平均）→ Quick
- 要穩定 → Merge
- 要保證最壞情況 → Merge / Heap

### Chapter 7 一句總結
> **排序的選擇，決定效能的上限。**
