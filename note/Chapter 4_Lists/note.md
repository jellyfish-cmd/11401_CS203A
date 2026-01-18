# Chapter 4：Lists（連結串列）
「用指標把資料串起來」

本章的核心概念：
### 資料不一定要排排坐，只要「知道下一個是誰」。

---

# 1. Pointer（指標，為什麼危險）

A pointer is a variable that stores the memory address of another variable.

### 指標不是資料本身，
### 而是「資料住在哪裡」。

## 為什麼說指標危險？
- 指錯地方 → 改到不該改的記憶體
- 忘記初始化 → 野指標
- 忘記釋放 → 記憶體洩漏

### 但為什麼一定要用？
> **因為沒有指標，就沒有 Linked List。**

---

# 2. Singly Linked List（單向連結串列）

A singly linked list is a collection of nodes where each node contains data and a pointer to the next node.

### 每個節點只知道「下一個是誰」。

## 節點結構（概念）
```c
struct node {
    int data;
    struct node* next;
};
```

## 基本操作

### Traversal（走訪）

- 從 head 開始
- 一個一個往後走
- 直到 next == NULL

### Insertion（插入）

- 改指標，不搬資料
- 插入位置不同，步驟不同

### Deletion（刪除）

- 把「前一個」指到「下一個」
- 被刪的節點要 free

---

## Big-O

- 搜尋：O(n)
- 插入：O(1)（已知位置）
- 刪除：O(1)（已知位置）

### 一句話記法

> 「找人慢，牽手快」
# 3. Dynamically Allocated Storage（動態配置）

Dynamic memory allocation allows programs to request memory at runtime.

### Linked List 的節點通常是「動態產生」的。

## 常見函式

- malloc：要記憶體
- free：還記憶體

### 重要觀念

- malloc 後一定要 free
- 不然會造成 memory leak

---

# 4. Circular Linked List（環狀連結串列）

A circular linked list is a linked list where the last node points back to the first node.

### 最後一個，不指向 null，

### 而是指回 head。

## 結構示意

```
head → node → node

 ^               |
 
 └───────────────┘

```

## 特點

- 沒有真正的「結尾」
- 很適合循環操作

### 常見用途

- Round-robin 排程
- 重複輪詢的系統

---

# 5. Doubly Linked List（雙向連結串列）

A doubly linked list allows traversal in both directions.

### 每個節點知道：

- 下一個是誰
- 前一個是誰

## 節點結構（概念）

```c
structnode {
int data;
structnode*prev;
structnode*next;
};

```

## 優點

- 可以往前走
- 刪除某節點更方便

## 缺點

- 記憶體用更多
- 指標管理更複雜

---

# 6. Linked List vs Array
| 比較項目 | Array | Linked List |
| --- | --- | --- |
| 記憶體 | 連續 | 不連續 |
| 存取 | O(1) | O(n) |
| 插入刪除 | 慢 | 快 |
| 大小 | 固定 | 彈性 |

