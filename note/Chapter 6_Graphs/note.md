# Chapter 6：Graphs（圖）
描述「點與關係」的資料結構

本章要解決的核心問題是：
### 當資料之間的關係不再是「線性」或「階層」，而是「彼此相連」。

---

## 6.1 Graph 基本概念（Basic Definitions）

A graph consists of a set of vertices and a set of edges.

### Graph 是由：
- Vertex（頂點、點）
- Edge（邊、連線）

所組成的資料結構。

---

### 基本名詞
- Vertex (V)：節點
- Edge (E)：邊
- Adjacent：兩個點之間有邊
- Degree：一個點連出去的邊數
- Path：從一個點走到另一個點的路徑
- Cycle：走一圈又回到原點

---

## 6.2 Graph 的種類

### 1. Undirected Graph（無向圖）
- 邊沒有方向
- 例如：朋友關係

### 2. Directed Graph（有向圖）
- 邊有方向
- 例如：網頁連結、交通單行道

---

### 3. Weighted Graph（加權圖）
- 邊上有權重（距離、成本、時間）

### 4. Unweighted Graph（無權重圖）
- 邊只代表「有沒有連」

---

## 6.3 Graph 的表示法（Representation）

### 1. Adjacency Matrix（鄰接矩陣）

- 使用二維陣列表示
- matrix[i][j] = 1 表示 i 與 j 相連

#### 特點
- 存取快
- 空間需求大（O(V²)）

---

### 2. Adjacency List（鄰接串列）

- 每個 Vertex 有一個 list
- 記錄它連到哪些點

#### 特點
- 空間省
- 適合稀疏圖

---

### 比較

| 表示法 | 空間 | 查詢邊 |
|---|---|---|
| Adjacency Matrix | O(V²) | O(1) |
| Adjacency List | O(V+E) | O(degree) |

---

## 6.4 Graph Traversal（圖的走訪）

Traversal 是指：
### 讓每個頂點「至少被拜訪一次」。

---

### 6.4.1 Depth First Search（DFS）

DFS 是：
### 一條路走到黑，再回頭。

#### 特點
- 使用 Stack（或遞迴）
- 適合找路徑、檢查 cycle

---

### DFS 的概念流程
1. 拜訪目前節點
2. 走向尚未拜訪的鄰居
3. 走到底後回溯

---

### 6.4.2 Breadth First Search（BFS）

BFS 是：
### 一層一層向外擴散。

#### 特點
- 使用 Queue
- 適合找最短路徑（無權重）

---

### BFS 的概念流程
1. 將起點放入 queue
2. 拿出一個點
3. 將尚未拜訪的鄰居加入 queue

---

## 6.5 DFS vs BFS（一定要會比）

| 比較項目 | DFS | BFS |
|---|---|---|
| 使用結構 | Stack | Queue |
| 搜尋方式 | 深度優先 | 廣度優先 |
| 最短路徑 | 否 | 是（無權重） |

---

## 6.6 Graph 的應用

- 地圖與導航系統
- 社交網路
- 網頁連結分析
- 排程與依賴關係

---

## 6.7 Big-O（Graph Traversal）

以鄰接串列表示時：

- DFS：O(V + E)
- BFS：O(V + E)

### 意義
> 每個點與每條邊，最多只會被走一次。

---

## Chapter 6 重點總結

- Graph 用來表示「關係」
- Vertex 是點，Edge 是連線
- 常見表示法：Matrix、List
- DFS 用 Stack，BFS 用 Queue
- BFS 可用於無權重最短路徑

### Chapter 6 一句總結
> **Graph 是描述世界關係的資料結構。**
