# Chapter 5：Trees（樹）
有階層關係的資料結構

本章要解決的核心問題是：
### 資料不只是排成一排，而是「有上下關係」。

---

## 5.1 Tree 基本概念（Terminology）

A tree is a hierarchical data structure consisting of nodes connected by edges.

### Tree 是一種「階層式」資料結構。
### 沒有 cycle（環），且有唯一的 root。

### 基本名詞
- Root（根）
- Parent（父節點）
- Child（子節點）
- Sibling（兄弟節點）
- Leaf（葉節點）
- Level / Depth（層數 / 深度）
- Height（高度）

---

## 5.2 Binary Tree（二元樹）

A binary tree is a tree in which each node has at most two children.

### 每個節點最多有兩個子節點（left / right）。

特性：
1. 左右子樹有順序  
2. 不一定是滿的  
3. 不一定是平衡的  

---

## 5.3 Tree Traversal（樹的走訪）

Traversal means visiting every node exactly once.

### Traversal 只是「拜訪節點的順序不同」。

### 三種基本走訪方式

#### Preorder（前序）
- Node → Left → Right  
- 常用於複製樹、表示結構

#### Inorder（中序）
- Left → Node → Right  
- **Binary Search Tree 的中序走訪會得到排序結果**

#### Postorder（後序）
- Left → Right → Node  
- 常用於刪除樹、計算運算式

---

## 5.4 Binary Search Tree（BST）

A binary search tree is a binary tree that satisfies:
- Left subtree < Node
- Right subtree > Node

### BST 是「有大小規則的二元樹」。

### BST 的特性
1. 左子樹所有值 < 節點值  
2. 右子樹所有值 > 節點值  
3. 中序走訪可得到排序結果  

### BST 的問題
- 插入順序不好，樹會嚴重傾斜

---

### Big-O（BST）

平均情況：
- 搜尋：O(log n)
- 插入：O(log n)
- 刪除：O(log n)

最壞情況：
- O(n)

---

## 5.5 Heap（堆積）

A heap is a complete binary tree that satisfies the heap property.

### Heap 是一種「受限制的 Binary Tree」。

---

### Heap 的兩個條件
1. Complete Binary Tree  
   - 由上到下、由左到右填滿  
2. Heap Property  
   - Max Heap：Parent ≥ Child  
   - Min Heap：Parent ≤ Child  

---

### 重要觀念
- Heap **不是排序結構**
- 只保證「根節點」是最大或最小

---

### Heap 的用途
- Priority Queue
- 排程（Scheduling）
- Top-K 問題

---

### Big-O（Heap）
- 插入：O(log n)
- 刪除最大 / 最小：O(log n)
- 取最大 / 最小：O(1)

---

## 5.6 Tree vs List 比較

| 項目 | Tree | Linked List |
|---|---|---|
| 結構 | 階層 | 線性 |
| 搜尋 | 快 | 慢 |
| 插入刪除 | 中等 | 快 |
| 記憶體 | 較多 | 較少 |

---

## Chapter 5 重點總結

- Tree 用「階層」換取「效率」
- Binary Tree：最多兩個子節點
- BST：有大小規則，但可能會歪
- Heap：只在乎最大 / 最小
- Tree 是 Heap、AVL、Red-Black Tree 的基礎

### Chapter 5 一句總結
> **Tree 是所有進階資料結構的地基。**
