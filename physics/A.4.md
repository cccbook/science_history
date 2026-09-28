# A.4 傅立葉分析：動量就是波數

## 傅立葉級數

對於週期函數 $f(x)$，週期為 $L$，其傅立葉級數展開為：

$$f(x) = \frac{a_0}{2} + \sum_{n=1}^\infty \left[ a_n \cos\left(\frac{n\pi x}{L}\right) + b_n \sin\left(\frac{n\pi x}{L}\right) \right]$$

其中系數為：

$$a_n = \frac{1}{L} \int_{-L}^{L} f(x) \cos\left(\frac{n\pi x}{L}\right) dx, \quad b_n = \frac{1}{L} \int_{-L}^{L} f(x) \sin\left(\frac{n\pi x}{L}\right) dx$$

## 傅立葉變換

對於非週期函數，我們使用傅立葉變換：

$$\hat{f}(k) = \int_{-\infty}^\infty f(x) e^{-2\pi i k x} dx$$

逆傅立葉變換：

$$f(x) = \int_{-\infty}^\infty \hat{f}(k) e^{2\pi i k x} dk$$

## 動量與波數的關係

在量子力學中，波函數 $\psi(x)$ 的傅立葉變換與動量空間波函數 $\phi(p)$ 有直接關係。根據狹義相對論與薛丁格方程，動量算符對應於空間導數：

$$\hat{p} = -i\hbar \frac{\partial}{\partial x}$$

因此，動量空間表示為：

$$\phi(p) = \frac{1}{\sqrt{2\pi\hbar}} \int_{-\infty}^\infty \psi(x) e^{-ipx/\hbar} dx$$

這顯示：**波數 $k$ 直接對應動量 $p = \hbar k$**。波數越大，動量越大。

## 不確定性原理的傅立葉證明

傅立葉變換證德國-海森堡不確定性原理 $\Delta x \Delta p \geq \hbar/2$ 的數學來源：一個函數與其傅立葉變換在「壓縮」與「展開」之間存在貿易關係。波函數越局域化（$\Delta x$ 小），其傅立葉變換就越分散（$\Delta p$ 大），反之亦然。

## 關鍵公式速查

| 概念 | 公式 |
|------|------|
| 傅立葉級數 | $f(x) = \frac{a_0}{2} + \sum_{n=1}^\infty [a_n \cos(k_n x) + b_n \sin(k_n x)]$ |
| 傅立葉變換 | $\hat{f}(k) = \int f(x) e^{-ikx} dx$ |
| 動量算符 | $\hat{p} = -i\hbar \frac{\partial}{\partial x}$ |
| 動量-波數關係 | $p = \hbar k$ |
| 不確定性原理 | $\Delta x \Delta p \geq \frac{\hbar}{2}$ |

## 練習問題

1. 求函數 $f(x) = x$（區間 $x \in [-\pi, \pi]$）的傅立葉級數展開。
2. 證明：波函數 $\psi(x) = A e^{-x^2/2\sigma^2}$ 的傅立葉變換仍為高斯函數，並求出其寬度變換關係。
3. 利用傅立葉變換，證明不確定性原理 $\Delta x \Delta p \geq \hbar/2$ 的數學本質。

---

*本節連接了波動力學與量子力學的核心橋梁，解釋了「動量即波數」的物理意義。*