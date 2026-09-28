# A.3 希爾伯特空間：狄拉克的 bra-ket 記號

希爾伯特空間是量子力學的數學家園。而**狄拉克的 bra-ket 記號**則是其中最直觀、最強大的工具。

## ket 記號 $| \psi \rangle$

**ket**（寫作 $|\psi\rangle$ ）表示一個希爾伯特空間中的向量。它可以是任意態，例如：

- 基態 $|0\rangle, |1\rangle$
- 波函數 $|\psi(x)\rangle$
- 自旋態 $|\uparrow\rangle, |\downarrow\rangle$

**讀作**：「ket psi」或「psi 向量」。

## bra 記號 $\langle \phi |$

**bra**（寫作 $\langle\phi|$ ）是 ket 的**共軛轉置**。讀作：「bra phi」或「phi 縮釋」。

若 $|\psi\rangle = \begin{pmatrix} a \\ b \end{pmatrix}$ ，則 $\langle\psi| = \begin{pmatrix} a^* & b^* \end{pmatrix}$ 。

## 内積

bra-ket 組合即為**內積**：

$$\langle\phi|\psi\rangle$$

這是一個標量，表示 $|\psi\rangle$ 在 $|\phi\rangle$ 方向上的投影長度（乘以模）。

### 性質

1. **線性**： $\langle\phi|(|\psi_1\rangle + |\psi_2\rangle) = \langle\phi|\psi_1\rangle + \langle\phi|\psi_2\rangle$
2. **共軛對稱**： $\langle\phi|\psi\rangle = \langle\psi|\phi\rangle^*$
3. **定性**： $\langle\psi|\psi\rangle \geq 0$ ，且 $\langle\psi|\psi\rangle = 1$ 當 $|\psi\rangle$ 歸一化時

## 外積

**外積** $|\psi\rangle\langle\phi|$ 產生一個算子。對任意態 $|\chi\rangle$ 作用：

$$(|\psi\rangle\langle\phi|)|\chi\rangle = |\psi\rangle(\langle\phi|\chi\rangle)$$

這是一個將 $|\chi\rangle$ 投影到 $|\phi\rangle$ 方向上，然後再乘以 $|\psi\rangle$ 的運算。

### 例子：投影算子

投影算子 $P = |\psi\rangle\langle\psi|$ 具有以下性質：

- $P^2 = P$ （投射性）
- $P^\dagger = P$ （厄米性）
- 若 $|\psi\rangle$ 歸一化，則對於任意態 $|\phi\rangle$ ， $P|\phi\rangle$ 就是 $|\psi\rangle$ 在 $|\phi\rangle$ 方向上的投影。

## 算子的表示

任何算子 $\hat A$ 都可以表示為本徵值與本徵向量的和：

$$\hat A = \sum_i \lambda_i |\lambda_i\rangle\langle\lambda_i|$$

其中 $\lambda_i$ 是本徵值， $|\lambda_i\rangle$ 是對應的本徵向量。這是**薛丁格展開**，類似於福里葉級數。

## 本章小結

- ket $|\psi\rangle$ 表示態，bra $\langle\phi|$ 表示其共軛轉置
- 內積 $\langle\phi|\psi\rangle$ 給出投影與機率幅
- 外積 $|\psi\rangle\langle\phi|$ 產生投影算子
- 薛丁格展開將算子表示為本徵值與本徵向量的和

## 想一想

1. 為什麼說 bra-ket 記號同時同時兼顧了向量與共軛的功能？它在數學上為什麼這麼有效？
2. 外積 $|\psi\rangle\langle\phi|$ 為什麼會產生一個投影算子？這在量子測量中有何應用？
3. 薛丁格展開在實際問題（如氫原子）中如何應用？它如何幫助我們求解薛丁諤方程？

---