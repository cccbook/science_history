# A.2 線性代數速成

線性代數是量子力學的數學骨幹。從狄拉克的 bra-ket 記號到算子，全部建立在向量空間之上。

## 向量與空間

一個 **向量** $|\psi\rangle$ 可以看作是一個有方向和大小的數量。在量子力學中，我們關心的向量生活在 **希爾伯特空間** 中，這是一個有內積的完備向量空間。

### 基本向量

- **單位向量** $|0\rangle$ ：所有成分為 0 的向量。
- **本徵向量**：算子作用於向量不變方向的向量。若 $\hat A|\psi\rangle = \lambda|\psi\rangle$ ，則 $|\psi\rangle$ 是 $\hat A$ 的本徵向量， $\lambda$ 是對應的本徵值。

### 內積

兩個向量 $|\phi\rangle$ 與 $|\psi\rangle$ 的內積寫作 $\langle\phi|\psi\rangle$ 。它滿足以下性質：

1. **線性**： $\langle\phi|(|\psi_1\rangle + |\psi_2\rangle) = \langle\phi|\psi_1\rangle + \langle\phi|\psi_2\rangle$
2. **共軛對稱**： $\langle\phi|\psi\rangle = \langle\psi|\phi\rangle^*$
3. **定性**： $\langle\psi|\psi\rangle \geq 0$ ，且 $\langle\psi|\psi\rangle = 0$ 當且僅當 $|\psi\rangle = |0\rangle$

### 正交與歸一

- **正交**： $\langle\phi|\psi\rangle = 0$ 。
- **歸一**： $\langle\psi|\psi\rangle = 1$ 。

一組向量 $\{|e_i\rangle\}$ 如果滿足 $\langle e_i|e_j\rangle = \delta_{ij}$ （克羅內克 델塔），則稱為**正交歸一**的。

## 矩陣

矩陣是算子在特定基底下的表示。若 $\{|\phi_i\rangle\}$ 是一組基底，則算子 $\hat A$ 的矩陣元為：

$$A_{ij} = \langle\phi_i|\hat A|\phi_j\rangle$$

### 矩陣乘法

$(AB)_{ik} = \sum_j A_{ij}B_{jk}$ 。注意**非交換性**： $AB \neq BA$ 。這就是量子力學中算子非交換性的數學根源。

### 逆矩陣

若矩陣 $\hat A$ 可逆，則存在逆矩陣 $\hat A^{-1}$ ，滿足 $\hat A\hat A^{-1} = \hat A^{-1}\hat A = I$ 。

## 特殊矩陣

### 厄米矩陣

算子 $\hat A$ 為厄米矩陣，若 $\hat A^\dagger = \hat A$ 。厄米矩陣的本徵值是實數，這對可觀測量至關重要。位置算子 $\hat x$ 和動量算子 $\hat p$ 都是厄米的。

### unitary 矩陣

算子 $\hat U$ 為 unitary，若 $\hat U^\dagger\hat U = \hat U\hat U^\dagger = I$ 。unitary 變換保持內積不變，對應量子演化中的**守恆**（如薛丁諤方程的時間演化是 unitary 的）。

## 本章小結

- 向量 $|\psi\rangle$ 生活在希爾伯特空間中
- 內積 $\langle\phi|\psi\rangle$ 決定正交與歸一
- 矩陣表示算子，非交換性是量子力學的核心
- 厄米矩陣對應可觀測量， $|A|\lambda$ 實數
- unitary 變換保持量子態的歸一化

## 想一想

1. 為什麼可觀測量的算子必須是厄米的？其本徵值為何意義？
2. unitary 變換在量子演化中為什麼必須保持內積不變？
3. 什麼是耦合態？它如何從產生態演化而來？

---