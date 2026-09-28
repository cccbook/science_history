# A.1 熱力學微積分速成：偏微分、全微分與馬克士威關係式

## 偏微分與全微分

在熱力學中，我們經常需要處理**狀態函數**（State Function），如內能 $U$ 、焓 $H$ 、熵 $S$ 與自由能 $G$ 。這些函數的變化取決於系統的初始與最終狀態，而非路徑。

### (a) 偏微分

當一個函數有多個變數時，我們稱 ** $\left(\frac{\partial z}{\partial x}\right)_y$ ** 為 $z$ 相對於 $x$ 的**偏微分**，意味著在 $y$ 保持不變的情況下， $z$ 隨 $x$ 變化的率。

舉例：對於函數 $f(x,y) = x^2y + y^3$ ，我們有：
$$\left(\frac{\partial f}{\partial x}\right)_y = 2xy, \quad \left(\frac{\partial f}{\partial y}\right)_x = x^2 + 3y^2$$

### (b) 全微分

如果 $z = f(x,y)$ 是一個可微函數，其**全微分**表示為：

$$dz = \left(\frac{\partial z}{\partial x}\right)_y dx + \left(\frac{\partial z}{\partial y}\right)_x dy$$

這表示 $z$ 的微小變化 $dz$ ，可以由 $x$ 與 $y$ 的微小變化 $dx, dy$ 共同決定。

### (c) 馬克士威關係式

在多變量函數中，混合偏微分的**相等性**給出了重要的物理關係。對於內能 $U(S,V)$ ，我們有：

$$dU = TdS - PdV$$

其中 $T = \left(\frac{\partial U}{\partial S}\right)_V$ 為溫度， $P = -\left(\frac{\partial U}{\partial V}\right)_S$ 為壓強。

對於這個全微分，馬克士威關係式為：

$$\left(\frac{\partial T}{\partial V}\right)_S = -\left(\frac{\partial P}{\partial S}\right)_V$$

這意味著：**在恆熵下，體積隨溫度變化的率，與在恆熵下，熵隨壓力變化的率（取負值）相等。**

### (d) 其他常見的馬克士威關係式

1. **焓 $H = U + PV$ **：
   $$\left(\frac{\partial T}{\partial P}\right)_H = \left(\frac{\partial V}{\partial S}\right)_P$$

2. **吉布斯自由能 $G = H - TS$ **：
   $$\left(\frac{\partial T}{\partial P}\right)_G = -\left(\frac{\partial V}{\partial S}\right)_T$$
   $$\left(\frac{\partial T}{\partial S}\right)_P = \left(\frac{\partial V}{\partial T}\right)_P$$

3. **亂度 $S$ **：
   $$\left(\frac{\partial T}{\partial V}\right)_S = -\left(\frac{\partial P}{\partial S}\right)_V$$

## 本章小結

- **偏微分**：在其他變量保持不變時，單一變量變化的率。
- **全微分**：多變量函數的總變化量，各分量貢獻之和。
- **馬克士威關係式**：源於混合偏微分的相等性，連接了不同熱力學變量間的互導數。
- **應用**：從內能、焓、吉布斯自由能出發，推導出溫度、壓力、體積、熵間的互動關係。

## 想一想

1. 如果我們從不同的能量函數（內能、焓、吉布斯自由能、亂度）出發，馬克士威關係式是否會有所不同？每一組關係式分別代表什麼物理意義？
2. 在實驗中，我們如何測量這些互導數？熱容測定、相變 calorimetry 是如何利用馬克士威關係式的？
3. 今天我們在熱力學軟體中，是否自動應用馬克士威關係式來轉換變量？這些軟體是如何處理多變量函數的？