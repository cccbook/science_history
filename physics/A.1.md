# A.1 數學速查手冊

## 複數與波動

- **歐拉公式**：$e^{i\theta} = \cos\theta + i\sin\theta$
- **平面波**：$\psi(x,t) = A e^{i(kx - \omega t)}$
- **模方**：$|\psi|^2 = \psi^* \psi$

## 線性代數

- **本徵值問題**：$A\mathbf{v} = \lambda\mathbf{v}$
- **厄米矩陣**：$A = A^\dagger$
- **直和**：$V = V_1 \oplus V_2$

## 傅立葉分析

- **傅立葉級數**：$f(x) = \frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos\frac{n\pi x}{L} + b_n \sin\frac{n\pi x}{L})$
- **傅立葉變換**：$\hat{f}(k) = \int_{-\infty}^\infty f(x) e^{-2\pi i k x} dx$

## 分離變數

- **球座標**：$x = r\sin\theta\cos\phi$, $y = r\sin\theta\sin\phi$, $z = r\cos\theta$
- **拉普拉斯算子**：$\nabla^2 = \frac{1}{r^2}\frac{\partial}{\partial r}(r^2\frac{\partial}{\partial r}) + \frac{1}{r^2\sin\theta}\frac{\partial}{\partial\theta}(\sin\theta\frac{\partial}{\partial\theta}) + \frac{1}{r^2\sin^2\theta}\frac{\partial^2}{\partial\phi^2}$

## 特殊函數

- **Gamma 函數**：$\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt$
- **Zeta 函數**：$\zeta(s) = \sum_{n=1}^\infty \frac{1}{n^s}$
- **球諧函數**：$Y_{\ell}^m(\theta,\phi)$

---

*本手冊提供了本书中常用數學工具的速查索引，讀者可隨時翻閱。*