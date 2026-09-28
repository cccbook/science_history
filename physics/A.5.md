# A.5 分離變數的藝術：球座標與氫原子

## 分離變數法

分離變數法是求解偏微分方程（如薛丁格方程）的強大技術。當問題具有球對稱性時，我們將三維空間的座標 $(x, y, z)$ 變換為**球座標** $(r, \theta, \phi)$ ：

$$x = r\sin\theta\cos\phi, \quad y = r\sin\theta\sin\phi, \quad z = r\cos\theta$$

其中：
- $r$ ：從原點到點的距離（徑向座標）
- $\theta$ ：極角（從正z軸量度， $0 \leq \theta \leq \pi$ ）
- $\phi$ ：方位角（在xy-plane從正x軸量度， $0 \leq \phi < 2\pi$ ）

## 拉普拉斯算子在球座標中的形式

$$\nabla^2 = \frac{1}{r^2}\frac{\partial}{\partial r}\!\left(r^2\frac{\partial}{\partial r}\right) + \frac{1}{r^2\sin\theta}\frac{\partial}{\partial\theta}\!\left(\sin\theta\frac{\partial}{\partial\theta}\right) + \frac{1}{r^2\sin^2\theta}\frac{\partial^2}{\partial\phi^2}$$

## 氫原子的薛丁格方程

對於氫原子（一個電子繞過一個質質心的質子），薛丁格方程在球座標中化簡。利用**分離變數**思想，我們令：

$$\psi(r, \theta, \phi) = R(r) \Theta(\theta) \Phi(\phi)$$

將薛丁格方程 $-\frac{\hbar^2}{2m}\nabla^2\psi - \frac{e^2}{4\pi\varepsilon_0 r}\psi = E\psi$ 代入後，將 $r、\theta、\phi$ 的項分離，得到三個普通微分方程：

### 1. 徑向方程

$$\frac{d^2R}{dr^2} + \frac{2}{r}\frac{dR}{dr} + \left[\frac{2m}{\hbar^2}\!\left(E + \frac{e^2}{4\pi\varepsilon_0 r}\right) - \frac{l(l+1)}{r^2}\right]R = 0$$

### 2. 極角方程（拉盍方程）

$$\frac{1}{\sin\theta}\frac{d}{d\theta}\!\left(\sin\theta\frac{d\Theta}{d\theta}\right) + \left[l(l+1) - \frac{m^2}{\sin^2\theta}\right]\Theta = 0$$

### 3. 方位角方程

$$\frac{d^2\Phi}{d\phi^2} + m^2\Phi = 0 \quad \Rightarrow \quad \Phi(\phi) = \frac{1}{\sqrt{2\pi}}e^{im\phi}$$

其中 $m$ 為整數（ $m = 0, \pm1, \pm2, \dots$ ），對應角量子數。

## 解的形式

- **徑向函數**： $R_{nl}(r) \propto r^l e^{-r/na_0} L_{n-l-1}^{2l+1}\!\left(\frac{2r}{na_0}\right)$
  - $n$ ：主量子數 ( $n = 1, 2, 3, \dots$ )
  - $l$ ：角量子數 ( $l = 0, 1, \dots, n-1$ )
  - $a_0$ ：波耳半徑 ( $a_0 = \frac{4\pi\varepsilon_0\hbar^2}{me^2} \approx 5.29 \times 10^{-11}$ m)
  - $L$ ：拉格endre多項式

- **球諧函數**： $Y_l^m(\theta, \phi) = N_l^m P_l^m(\cos\theta) e^{im\phi}$
  - $P_l^m$ ：associated Legendre polynomials
  - $N_l^m$ ：正規化常數

## 氫原子能階

能量僅取決於主量子數 $n$ ：

$$E_n = -\frac{me^4}{8\varepsilon_0^2h^2}\frac{1}{n^2} = -\frac{13.6}{n^2}\text{ eV}$$

這解釋了氫光譜線的出現，以及為什麼電子躍遷時會釋放出特定波長的光子。

## 形狀與橢度

不同 $(l, m)$ 組合對應不同的軌道形狀：
- $l = 0$ (s軌道)：球對稱
- $l = 1$ (p軌道)： dumbbell 形狀， $m = -1, 0, 1$ 三個方向
- $l = 2$ (d軌道)：更複雜的雙曲面形狀， $m = -2, -1, 0, 1, 2$

## 應用實例

- **氫原子光譜**：萊曼、巴爾末、帕謝倫系列對應 $n$ 的躍遷
- **多電子原子**：哈特里-福克方法建立在氫原子解的基礎上
- **磁偶極矩**：電子自轉角動量與軌道角動量的量子態決定

## 練習問題

1. 推導：氫原子的能階公式 $E_n = -13.6/n^2$ eV。
2. 求出 $l = 1, m = 0$ 時的球諧函數 $Y_1^0(\theta, \phi)$ ，並說明其形狀。
3. 利用分離變數，解出氫原子的徑向方程，得到波爾半徑 $a_0$ 的物理意義。

---

*本節展示了如何利用對稱性與分離變數法，精確求解薛丁格方程，並獲得氫原子的能階、態與形狀。*