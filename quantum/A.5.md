# A.5 分離變數的藝術：球座標與氫原子

分離變數是求解偏微分方程的利器，特別是在球對稱問題中。以氫原子為例，這是將三維薛丁諤方程拆解為三個獨立方程的典型案例。

## 三維薛丁諤方程

氫原子的勢位為庫侖勢場：

$$V(r) = -\frac{e^2}{4\pi\varepsilon_0 r}$$

三維薛丁諤方程（含時）為：

$$i\hbar\,\frac{\partial\Psi}{\partial t} = -\frac{\hbar^2}{2m}\nabla^2\Psi + V(r)\Psi$$

我們尋找**定態解**，即波函數隨時間的相位因子分離：

$$\Psi(\mathbf{r},t) = \psi(\mathbf{r})\,e^{-iEt/\hbar}$$

代入後得到**定態薛丁諤方程**：

$$-\frac{\hbar^2}{2m}\nabla^2\psi + V(r)\psi = E\psi$$

## 引入球座標

為了利用勢場的球對稱性，我們引入**球座標** $(r,\theta,\phi)$ ：

- $r$ ：從原點到點的距離
- $\theta$ ：極角，從正 z 軸量度 $0 \to \pi$
- $\phi$ ：方位角，從 x 軸正方向量度 $0 \to 2\pi$

拉普拉斯算子在球座標下展開為：

$$\nabla^2 = \frac{1}{r^2}\frac{\partial}{\partial r}\!\left(r^2\frac{\partial}{\partial r}\right) + \frac{1}{r^2\sin\theta}\frac{\partial}{\partial\theta}\!\left(\sin\theta\frac{\partial}{\partial\theta}\right) + \frac{1}{r^2\sin^2\theta}\frac{\partial^2}{\partial\phi^2}$$

## 分離變數假設

我們假設解可以寫成**乘積形式**：

$$\psi(r,\theta,\phi) = R(r)\,\Theta(\theta)\,\Phi(\phi)$$

將其代入薛丁諤方程，兩邊除以 $\psi = R\Theta\Phi$ ，整理後項自然分為**三個獨立部分**：

1. **徑向方程**（只含 $r$ ）
2. **極向方程**（只含 $\theta$ ）
3. **方位向方程**（只含 $\phi$ ）

## (a) 方位向方程

只含 $\phi$ 的方程非常簡單，因為 $\phi$ 是週期變數（ $0 \to 2\pi$ ）：

$$\frac{\partial^2\Phi}{\partial\phi^2} + m^2\Phi = 0$$

其正規化解是**複指數**：

$$\Phi_m(\phi) = \frac{1}{\sqrt{2\pi}}e^{im\phi}, \quad m = 0, \pm1, \pm2, \dots$$

其中 $m$ 稱為**磁量子數**。週期性條件 $\Phi_m(\phi+2\pi) = \Phi_m(\phi)$ 強制 $m$ 必須是整數。

## (b) 極向方程

極向方程是**勒让德微分方程**：

$$\frac{1}{\sin\theta}\frac{\partial}{\partial\theta}\!\left(\sin\theta\,\frac{\partial\Theta}{\partial\theta}\right) + \left[l(l+1) - \frac{m^2}{\sin^2\theta}\right]\Theta = 0$$

其正規化解是**球諧函數** 的角部分：

$$\Theta_l^m(\theta) = N_{lm}\,P_l^m(\cos\theta)$$

其中 $P_l^m$ 是**相關勒让德多項式**， $l$ 稱為**角動量量子數**，取值 $l = 0, 1, 2, \dots, |m|$ 。

## (c) 徑向方程

徑向方程為：

$$-\frac{\hbar^2}{2m}\,\frac{1}{r^2}\frac{d}{dr}\!\left(r^2\frac{dR}{dr}\right) + \left(-\frac{e^2}{4\pi\varepsilon_0 r} + \frac{\hbar^2 l(l+1)}{2mr^2}\right)R = E R$$

引入無量綱變數 $\rho = \frac{2r}{n a_0}$ （見 A.6），方程變為：

$$\frac{d^2R}{d\rho^2} + \left(-\frac{1}{4} + \frac{1}{\rho} - \frac{l(l+1)}{\rho^2}\right)R = 0$$

這是柯西-楊勒方程，其解的行為決定了能階。

## 能階量子化

為了使波函數在 $r \to \infty$ 時趨於 0（束縛態），以及在 $r \to 0$ 時趨於 0（波函數必須歸零），我們得到能階條件：

$$E_n = -\frac{m e^4}{8\varepsilon_0^2 h^2 n^2} = -\frac{13.6\ \text{eV}}{n^2}$$

其中 $n$ 稱為**主量子數**，取值 $n = 1, 2, 3, \dots$ ，且 $n > l$ 。

## 本章小結

- 球座標 $(r,\theta,\phi)$ 利用球對稱性拆解薛丁諤方程
- 分離變數得到三個獨立方程：徑向、極向、方位向
- 角向解為球諧函數， $l$ （角動量量子數）與 $m$ （磁量子數）決定軌道形狀
- 能階 $E_n = -13.6/n^2$ eV 來自於徑向方程的歸一化條件
- 主量子數 $n$ 決定能階，角動量量子數 $l$ 決定軌道角 momentum

## 想一想

1. 為什麼週期性條件 $\Phi_m(\phi+2\pi) = \Phi_m(\phi)$ 強制 $m$ 必須是整數？
2. 徑向方程中 $\frac{\hbar^2 l(l+1)}{2mr^2}$ 這項稱為「離心項」，它的物理意義是什麼？
3. 主量子數 $n$ 與角動量量子數 $l$ 的關係 $n > l$ 為什麼必須存在？這與波函數的歸一化有何關係？