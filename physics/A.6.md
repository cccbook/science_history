# A.6 特殊函數速查：Gamma、Zeta、球諧函數

## Gamma 函數

**Gamma 函數** 是階乘在實數與複數範圍的推廣，定義為：

$$\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt \quad (\Re(z) > 0)$$

### 性質

- **遞迴關係**：$\Gamma(z+1) = z\Gamma(z)$
- **階乘延伸**：$n! = \Gamma(n+1)$ （當 $n$ 為自然數）
- **反射公式**：$\Gamma(z)\Gamma(1-z) = \frac{\pi}{\sin(\pi z)}$
- ** Gauss 積分**：$\Gamma\!\left(\frac{1}{2}\right) = \sqrt{\pi}$

### 應用

- 概率分佈：Chi-square 分佈、Gamma 分佈
- 量子力學：氫原子徑向方程的解
- 數值分析：階乘的連續外推

---

## Zeta 函數

**黎曼 Zeta 函數** 定義為：

$$\zeta(s) = \sum_{n=1}^\infty \frac{1}{n^s} \quad (\Re(s) > 1)$$

### 關鍵值

- $\zeta(2) = \frac{\pi^2}{6}$ （巴塞爾問題）
- $\zeta(4) = \frac{\pi^4}{90}$
- $\zeta(-1) = -\frac{1}{12}$ （ Ramanujan 歸一化）
- $\zeta(0) = -\frac{1}{2}$

### 關鍵性質

- **邊界截距**：$\zeta(s)$ 在 $s=1$ 處有極點
- ** Funktionalgleichung（函數方程）**：

$$\zeta(s) = 2^s \pi^{s-1} \sin\!\left(\frac{\pi s}{2}\right) \Gamma(1-s) \zeta(1-s)$$

這條方程將正實部大於 1 的域與負實部連結起來，是數論與解析數論的核心。

### 應用

- 數論：質數分佈（質數計數函數 $\pi(x)$ 近似）
- 統計力學：玻斯-愛因斯坦統計、費米-狄拉克統計
- 量子場論：規範理論中的規範化技術

---

## 球諧函數

**球諧函數** $Y_l^m(\theta, \phi)$ 正規化的球面上對角狀本徵函數，滿足拉普拉斯算子的本徵值問題：

$$\nabla^2 Y_l^m = -\frac{l(l+1)}{r^2} Y_l^m$$

### 定義

$$Y_l^m(\theta, \phi) = (-1)^m \sqrt{\frac{2l+1}{4\pi} \frac{(l-m)!}{(l+m)!}} \; P_l^m(\cos\theta) \; e^{im\phi}$$

其中：
- $l = 0, 1, 2, \dots$：角量子數
- $m = -l, -l+1, \dots, l$：磁量子數
- $P_l^m$：associated Legendre 多項式
- $e^{im\phi}$：方位角部分

### 性質

- **正規化**：$\int_0^{2\pi}\int_0^\pi Y_l^{m*}(\theta,\phi) Y_{l'}^{m'}(\theta,\phi) \sin\theta\,d\theta\,d\phi = \delta_{ll'}\delta_{mm'}$
- **酉變換**：不同 $l, m$ 的球諧函數正交
- **旋轉態**：球諧函數在旋轉下變換遵循 Wigner D 矩陣

### 常見形式

- $l = 0, m = 0$: $Y_0^0 = \frac{1}{\sqrt{4\pi}}$ （常數，球對稱）
- $l = 1, m = 0$: $Y_1^0 = \sqrt{\frac{3}{4\pi}}\cos\theta$ （p軌道 z方向）
- $l = 1, m = \pm1$: $Y_1^{\pm1} = \mp\sqrt{\frac{3}{8\pi}}\sin\theta\,e^{\pm i\phi}$ （p軌道 xy方向）
- $l = 2, m = 0$: $Y_2^0 = \sqrt{\frac{5}{16\pi}}(3\cos^2\theta - 1)$ （d軌道 z方向）

### 應用

- 氫原子態：$\psi_{nlm}(r,\theta,\phi) = R_{nl}(r) Y_l^m(\theta,\phi)$
- 角 momentum 算符：$\hat{L}^2 Y_l^m = \hbar^2 l(l+1) Y_l^m$， $\hat{L}_z Y_l^m = \hbar m Y_l^m$
- 量子雲：電子雲的概率分佈視球諧函數的平方 $|\psi|^2$ 而定
- 光譜與繞射：球諧函數用於描述原子繞射、光譜線強度

### 練習問題

1. 證明：$\int_0^{2\pi}\int_0^\pi Y_l^{m*}(\theta,\phi) Y_{l'}^{m'}(\theta,\phi) \sin\theta\,d\theta\,d\phi = \delta_{ll'}\delta_{mm'}$。
2. 計算：$l=1, m=0$ 時的球諧函數 $Y_1^0$ 的方位角概率分佈 $P(\phi) = \int_0^\pi |Y_1^0|^2 \sin\theta\,d\theta$。
3. 利用關聯勒杰endre 多項式遞迴關係：$(l-m+1)P_l^{m-1} = \sqrt{(l+m)(l-m+1)} P_{l+1}^m - (2l+1)\cos\theta P_l^m$，驗證 $l=1$ 時的球諧函數正交性。

---

*本節提供了三種最常見的特殊函數速查，支撐量子力學、數論與應用物理中的計算需求。*