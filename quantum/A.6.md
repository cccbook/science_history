# A.6 特殊函數速查：Gamma、Zeta、球諧函數

特殊函數在量子力學中無處不在。從能階歸一化到軌道形狀，都離不開它們。

## Gamma 函數

**Gamma 函數** $\Gamma(z)$ 是階乘的廣義化，定義為：

$$\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt$$

性質：

- $\Gamma(n) = (n-1)!$，當 $n$ 為正整數
- $\Gamma(z+1) = z\Gamma(z)$，遞迴關係
- $\Gamma\!\left(\frac{1}{2}\right) = \sqrt{\pi}$

**在氫原子能階推導中**：
$$\int_0^\infty \frac{x^3}{e^x-1}dx = \Gamma(4)\,\zeta(4) = 3!\cdot\frac{\pi^4}{90} = \frac{\pi^4}{15}$$
這是求總輻射能量密度時的關鍵積分。

## Zeta 函數

**黎曼 Zeta 函數** $\zeta(s)$ 定義為：

$$\zeta(s) = \sum_{n=1}^\infty \frac{1}{n^s}, \quad \text{Re}(s) > 1$$

性質：

- $\zeta(2) = \frac{\pi^2}{6}$
- $\zeta(4) = \frac{\pi^4}{90}$
- 複平面上的解析延拓

**在傅立葉積分中**：
同上，$\int_0^\infty \frac{x^3}{e^x-1}dx = \Gamma(4)\zeta(4)$ 是連接階乘與 $\pi$ 的橋樑。

## 球諧函數

**球諧函數** $Y_l^m(\theta,\phi)$ 描述氫原子軌道的角分佈：

$$Y_l^m(\theta,\phi) = N_{lm}\, P_l^m(\cos\theta)\, e^{im\phi}$$

其中：
- $l = 0, 1, 2, \dots$ 是**角動量量子數**
- $m = -l, -l+1, \dots, l$ 是**磁量子數**
- $P_l^m$ 是**相關勒让德多項式**
- $N_{lm}$ 是**歸一化常數**：$N_{lm} = \sqrt{\frac{(2l+1)}{4\pi}\,\frac{(l-m)!}{(l+m)!}}$

### 軌道形狀一覽

- **s軌道** ($l=0$)：$Y_0^0 = \frac{1}{2}\sqrt{\frac{1}{\pi}}$，球對稱，無角節。
- **p軌道** ($l=1$)：$Y_1^{\pm1}, Y_1^0$，雙曲面形狀，沿坐標軸對稱。
- **d軌道** ($l=2$)：更複雜的四葉形狀或雙曲面組合。

## 本章小結

- Gamma 函數 $\Gamma(z)$ 將階乘推廣到複數，關鍵積分 $\int_0^\infty \frac{x^3}{e^x-1}dx = \Gamma(4)\zeta(4)$
- Zeta 函數 $\zeta(s)$ 系列值 $\zeta(2)=\pi^2/6, \zeta(4)=\pi^4/90$ 在傅立葉積分中頻繁出現
- 球諧函數 $Y_l^m(\theta,\phi)$ 決定氫原子軌道的角分佈，$l$ 與 $m$ 決定形狀與取向
- s、p、d、f 四種軌道的形狀由 $l$ 決定

## 想一想

1. Gamma 函數 $\Gamma(1/2) = \sqrt{\pi}$ 這個結果從何而來？它與高斯積分有何關係？
2. 球諧函數中的正規化常數 $N_{lm}$ 為什麼需要包含 $(l-m)!/(l+m)!$ 的比值？
3. 不同 $l$ 值對應的軌道（s、p、d、f），在化學週期表中分別對應哪些殼層？

---