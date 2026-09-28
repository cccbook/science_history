# A.3 希爾伯特空間：狄拉克的 bra-ket 語言

## bra-ket 記號

在量子力學中，狄拉克提出了一種極為優雅的數學表示法，稱為**bra-ket 記號**。這種記號將內積表示為：

$$\langle \phi | \psi \rangle$$

其中：
- $|\psi\rangle$ 稱為 **ket**（ket 向量），表示量子態
- $\langle \phi|$ 稱為 **bra**（bra 向量），表示共軛轉換後的態

## 希爾伯特空間的性質

**希爾伯特空間** 是一個完備的內積空間，滿足以下性質：

1. **線性性**：$\langle \alpha | (A|\beta\rangle) = (\langle \alpha|A)|\beta\rangle$
2. **共軛對稱性**：$\langle \phi | \psi \rangle = \overline{\langle \psi | \phi \rangle}$
3. **正定性**：$\langle \psi | \psi \rangle \geq 0$，且 $\langle \psi | \psi \rangle = 0$ 當且僅當 $|\psi\rangle = 0$

## 算符在希爾伯特空間中的表示

- **自伴算符**：$A = A^\dagger$，對應可觀測量
- **酉算符**：$U^\dagger U = UU^\dagger = I$，保持內積不變
- **本徵值問題**：$A|\psi\rangle = \lambda|\psi\rangle$

## 完備性與展開定理

任何量子態 $|\psi\rangle$ 都可以表示為本徵向的線性組合：

$$|\psi\rangle = \sum_i c_i |i\rangle \quad \text{或} \quad |\psi\rangle = \int c(\lambda)|\lambda\rangle d\lambda$$

其中 $\{|i\rangle\}$ 或 $|\lambda\rangle$ 形成希爾伯特空間的一個**正交基底**。

## 應用實例

在位置表現中：

$$\langle x|\psi\rangle = \psi(x)$$

這是波函數 $\psi(x)$ 的定義，展示了位置態 $|x\rangle$ 與態 $|\psi\rangle$ 之間的對應關係。

## 直和與正規化

- **直和**：$V = V_1 \oplus V_2$，表示兩個希爾伯特空間的直接直和
- **標準化**：$\langle \psi | \psi \rangle = 1$，確保概率總和為 1

## 練習問題

1. 給定 $| \psi \rangle = \begin{pmatrix} 1 \\ i \end{pmatrix}$，計算 $\langle \psi | \psi \rangle$ 並驗證其為 1（標準化）。
2. 若 $\langle \phi | \psi \rangle = 0$，證明 $|\phi\rangle$ 與 $|\psi\rangle$ 正交。
3. 簡化表達式：$\langle \phi | A | \psi \rangle$ 中的 $A$ 若為自伴算符，其實部為何？

---

*本節介紹了希爾伯特空間的數學基石，為理解量子力學的算符理準備必要工具。*