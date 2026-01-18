# Chapter 8：Hash Table（雜湊表）
用「計算」取代「搜尋」

本章要解決的核心問題是：
### 如何在大量資料中，用接近 O(1) 的時間找到目標。

---

## 8.1 Hash Table 基本概念

A hash table is a data structure that maps keys to values using a hash function.

### Hash Table 的核心思想是：
### key → hash function → index

---

### 為什麼 Hash Table 很快？
因為它不是「找」，而是：
> **算出位置，直接過去。**

---

## 8.2 Hash Function（雜湊函數）

A hash function maps a key to an integer index.

### 好的 hash function 應該：
1. 計算快  
2. 分布平均  
3. 減少碰撞（collision）  

---

### 常見 hash function 範例（概念）
- 除法法：h(k) = k mod m
- 字串加總法
- 多項式雜湊

---

## 8.3 Collision（碰撞）

Collision 發生在：
### 不同的 key，被算到同一個 index。

---

### 為什麼 collision 無法避免？
- index 數量有限
- key 數量可能非常多

---

## 8.4 Collision Resolution（碰撞處理）

### 1. Chaining（鏈結法）

- 每個 index 放一個 linked list
- 撞到就接在後面

#### 特點
- 實作簡單
- 記憶體較多

---

### 2. Open Addressing（開放定址）

- 撞到就找下一個空位
- 不用 linked list

#### 常見方式
- Linear Probing
- Quadratic Probing
- Double Hashing

---

## 8.5 Load Factor（負載因子）

Load Factor 定義為：
α = n / m

- n：資料數量
- m：table 大小

### 意義
- α 越大，collision 越多
- α 太大 → 效能下降

---

## 8.6 Rehashing（重新雜湊）

Rehashing 是：
### 當 table 太滿時，重新建立更大的 table。

流程：
1. 建立新 table
2. 對所有 key 重新 hash
3. 搬移資料

---

## 8.7 Hash Table 的 Big-O

### 平均情況（Average Case）
- 搜尋：O(1)
- 插入：O(1)
- 刪除：O(1)

---

### 最壞情況（Worst Case）
- O(n)（所有 key 都撞在一起）

---

## 8.8 Hash Table vs Tree

| 比較項目 | Hash Table | Tree |
|---|---|---|
| 搜尋 | O(1)（平均） | O(log n) |
| 資料有序 | ❌ | ✅ |
| 範圍查詢 | ❌ | ✅ |
| 實作複雜度 | 中 | 高 |

---

## 8.9 Hash Table 的應用

- Dictionary / Map
- Set
- Symbol Table
- Cache
- Database Index（部分）

---

## Chapter 8 重點總結

- Hash Table 用「計算」換取「速度」
- Collision 無法避免，但可以管理
- 平均情況下效能極佳
- 不適合需要排序或範圍查詢的場景

### Chapter 8 一句總結
> **Hash Table 是追求快速查詢的資料結構。**
