# Chapter 3：Stacks & Queues
「有規則的線性資料結構」

本章重點：
### 資料「從哪裡進、從哪裡出」。

---

# 1. Stack（堆疊，後進先出）

A stack is a linear data structure that follows the Last In First Out (LIFO) principle.

### Stack 是「後進先出」。
### 最後放進去的，最先拿出來。

---

## 結構
push ↑
[ ]
[ ]
[ ] ← pop
- 只能從「同一端」進出
- 不允許從中間拿資料

---

## 基本操作
- push：放資料進去
- pop：拿最上面的資料
- peek / top：偷看最上面（不拿）

---

## 常見用途
- 函式呼叫（Call Stack）
- 遞迴
- 括號配對檢查
- 中序 / 後序運算式計算
- DFS（Depth First Search）

---

## 為什麼要 Stack？
### 因為很多事情「一定要先處理最後發生的事」

---

## Big-O
- push：O(1)
- pop：O(1)
- peek：O(1)

---

### 一句話記法
> 「最後來的，最先走」

---

# 2. Queue（佇列，先進先出）

A queue is a linear data structure that follows the First In First Out (FIFO) principle.

### Queue 是「先進先出」。
### 像排隊買東西。

---

## 結構
enqueue → [ A | B | C ] → dequeue
- 一端進（rear）
- 一端出（front）

---

## 基本操作
- enqueue：資料進隊
- dequeue：資料出隊
- front：看最前面的是誰

---

## 常見用途
- 工作排程（Scheduling）
- 等待資源
- Buffer
- BFS（Breadth First Search）

---

## 為什麼要 Queue？
### 因為「公平、照順序」

---

## Big-O
- enqueue：O(1)
- dequeue：O(1)
- front：O(1)

---

### 一句話記法
> 「誰先來，誰先走」

---

# Stack vs Queue（一定要分清楚）

| 比較項目 | Stack | Queue |
|---|---|---|
| 規則 | 後進先出 | 先進先出 |
| 進出口 | 同一端 | 不同端 |
| 常搭配 | DFS、遞迴 | BFS、排程 |

---

# Chapter 3 總結（考前速讀）

### Stack
- 管「順序的反轉」
- 管「回到上一個狀態」

### Queue
- 管「公平順序」
- 管「一個一個處理」

### Chapter 3 一句總結
> **Stack 管「最後的事」，Queue 管「先來的事」。**
