# 逐張 Speaker Notes

> 對應 `defense.pdf` 主體 18 張 + 結語。每張包含「目的、講稿、提醒」。
> 講稿用中文＋英文技術名詞（適合在大陸中文答辯場合直接念）。
> 時間欄是建議分配，總計約 20 分鐘。**逐字背念效果差**，把每張的關鍵句記住、
> 其他用自己的話銜接即可。

---

## Slide 1 · 封面（0:00–0:30）

**目的**：開場立威。讓委員第一眼看清題目和你的所屬。

**講稿（30 秒）：**

> 各位老師早上 / 下午好。我是 [姓名]。今天向大家報告我的碩士學位論文，
> 題目是「任意阶多物理量普适不确定性关系及其应用」，英文題目
> "Universal Uncertainty Relations of Arbitrary Order and Multiple Observables
> with Applications"。導師是 [導師姓名] 教授。下面開始我的報告。

**提醒**：
- 站定、不要急著翻頁。
- 別念「謝謝大家給我這個機會」之類冗長客套，浪費時間。

---

## Slide 2 · Outline（0:30–1:00）

**目的**：給聽眾一張地圖。

**講稿（30 秒）：**

> 我的報告分為六個部分：背景與動機、母不等式的數學框架、任意階多物理量
> 普适不確定關係的主要結果、應用與例子，最後是總結與展望。

**提醒**：
- 不要逐條念六個小節。一句帶過即可。
- 心裡記住「**動機 → 框架 → 結果 → 應用 → 結論**」這條主線。

---

## Slide 3 · 變異數型 UR 回顧（1:00–2:30）

**目的**：建立共同語言，讓所有委員（不一定是量子光學或量子資訊背景）都能跟上。

**講稿（90 秒）：**

> 不確定關係是量子力學的核心結構之一。最為人熟知的版本是 1927 年 Heisenberg
> 給出、1929 年 Robertson 嚴格推廣、1930 年 Schrödinger 進一步加上協方差項
> 後得到的這個不等式（指公式）。它告訴我們：兩個不對易物理量的方差乘積，
> 由它們的對易子與反對易子的二次型給出下界。
>
> 這個結果有三個關鍵特徵。第一，它用**第二中心矩**——也就是方差——來度量
> 漲落。第二，它的證明只用到一條不等式，就是 Cauchy--Schwarz 不等式。
> 第三，它對 Gaussian / coherent / squeezed states 是緊的。
>
> 在過去近一個世紀，這個基本框架向三個方向被推廣：訊息熵方向（Hirschman、
> Maassen-Uffink、Berta 等）；可操作 / 誤差—擾動方向（Ozawa、Busch-Lahti-Werner）；
> majorization-based universal 方向（Friedland-Gheorghiu-Gour 等）。

**提醒**：
- 講「方差、Cauchy-Schwarz、Gaussian saturate」這三個關鍵詞時放慢、加重音。
- **不要展開**講三條已有的推廣路線——只是讓委員知道你掌握文獻就好。

---

## Slide 4 · 變異數的局限（2:30–4:00）

**目的**：點出問題。為什麼方差不夠？這張是動機的核心。

**講稿（90 秒）：**

> 然而，變異數型框架在以下三類情境下會丟失資訊。
>
> 第一，**非高斯態**。比如 Schrödinger cat state——右邊這張圖——它的 quadrature
> 分布是雙峰結構，但方差跟同樣大小的 coherent state 幾乎一樣。所以單看方差，
> 你看不到它的雙峰本質；要從 $\kappa_4$ 或更高階的中心矩才能看到。
>
> 第二，**開放系統與多體系統**。許多 noise 與 correlation 的非高斯特徵
> 都編碼在高階 cumulants $\kappa_3,\kappa_4$ 裡，這是方差完全捕捉不到的。
>
> 第三，**多物理量**。許多現代協議——量子計量、量子資訊、多參數估計——
> 涉及的不是一對 canonical pair，而是三個、四個、甚至 $n$ 個不對易的
> observables。
>
> 因此一個自然的問題是：能否寫出一個**任意矩階**、適用於**任意多個物理量**、
> 且在 $p=q=2$ 退化回 Robertson--Schrödinger 的**普适**不確定關係？
> 這正是本論文要回答的問題。

**提醒**：
- 圖在右邊，講到第一點時要 **指圖**。
- 「Robertson--Schrödinger」字念清楚（不要省略 Schrödinger）。
- 結尾要把「普适」(universal) 三個字突出，這是你的 thesis statement。

---

## Slide 5 · 本文目標（4:00–5:00）

**目的**：把你具體要做的四件事羅列清楚。

**講稿（60 秒）：**

> 本論文的工作可以歸納為四點：
>
> 第一，從可積函數空間的 Hölder 不等式出發，透過量子—古典一致性要求，
> 把它 transfer 到算符泛函層面，得到一條 mother inequality。
>
> 第二，定義 $L^p$ 階的漲落度量 $\Delta_p(A) = \langle |A-\langle A\rangle|^p\rangle^{1/p}$，
> 用它取代標準差。
>
> 第三，從 mother inequality 推導出 $n=2,3,4,\dots$ 個 observable 任意階的
> universal UR，並給出偶 / 奇情形的封閉式。
>
> 第四，做了多個解析與數值算例：氫原子、谐振子、cat state、qubit、三比特 GHZ，
> 以及一個古典熱雙阱例子。

**提醒**：
- 四點對應接下來四個 section，這張是「報告骨架預告」。
- 不要展開細節，後面每張會講。

---

## Slide 6 · 從可積函數到算符（5:00–6:30）

**目的**：講清楚 functional 層面的起點。

**講稿（90 秒）：**

> 推導從可積函數空間的不等式開始。對於 $\mu$-可積函數 $f$、機率密度
> $\rho = \psi^\dagger \psi$，我們有左邊這條基本不等式：
> $|\int f\rho\,d\mu|^p \leq \int |f|^p \rho\,d\mu$，這對 $p\geq 1$ 成立。
>
> 在多變量情形，當指數滿足 $\sum_i 1/p_i = 1$ 時，Hölder 不等式給出
> 乘積積分的上界——下面這條公式。注意 Hölder 把多個 $L^p$ 範數的乘積
> 控制住乘積函數的 $L^1$ 範數。
>
> 把這套搬到量子算符上的關鍵是「量子—古典一致性」：把 $f$ 換成厄米算符
> $\hat f$，把機率密度 $\rho$ 視為密度算符對角元，要求標量函數情形下兩端
> 應當一致。這個替換的合法性來自於 self-adjoint operator 的 functional
> calculus——任意正幂次都可由譜分解定義。

**提醒**：
- 這張公式密、要講慢。
- 走到白板把 $1/r = \sum 1/p_i$ 寫一遍會更清楚。
- **不要**展開講一致性要求的所有技術細節，只說「functional calculus
  保證了合法性」即可——委員追問你再走 backup slide。

---

## Slide 7 · The Mother Inequality（6:30–8:00）

**目的**：寫出本論文的核心引理。後面所有結果都由此導出。

**講稿（90 秒）：**

> 這就是本論文的 **mother inequality**：對 $n$ 個厄米算符 $\hat f_1,\dots,\hat f_n$，
> 在歸一化態 $|\psi\rangle$ 下，當指數滿足 $\sum_i 1/p_i = 1/r$ 時，乘積算符
> 模的 $r$ 階期望，被各算符模 $p_i$ 階期望的乘積控制。
>
> 這條不等式有三個關鍵特性。
>
> 第一，**它在 $n=2,p_1=p_2=2$ 時就退化成 Cauchy--Schwarz**，因此所有變異數
> 型 UR 都是它的特例。
>
> 第二，**本論文後面所有的 UR 結果**——兩個觀測量、三個、四個、$n$ 個——
> 都是這條 mother inequality 在 $\hat f_i = \Delta\hat A_i$ 時的不同特化。
>
> 第三，求和條件 $\sum_i 1/p_i = 1/r$ 控制了**矩階如何在多個 observable
> 之間分配**——這個 degree of freedom 是變異數型 UR 沒有的。

**提醒**：
- 這是 **anchor slide**——被追問時走回這張。
- 講「本論文後面所有的 UR 結果都是它的特例」這句要 **強調**。
- 不要解釋 $\sum 1/p_i = 1/r$ 怎麼來的，留給 backup。

---

## Slide 8 · 兩個觀測量任意階（8:00–10:00）

**目的**：第一個主要結果。**這張可能花最久時間，包括白板演算 RS recovery**。

**講稿（120 秒）：**

> 把 $\hat f = \Delta \hat A$、$\hat g = \Delta \hat B$ 代入 mother inequality，
> 得到兩個觀測量任意階的 universal UR：$\Delta_p(A) \Delta_q(B)$ 大於等於
> 對易子加反對易子的 $\frac{pq}{p+q}$ 階期望開根號——就是這個 boxed 公式。
>
> 這個結果的關鍵特性是：**在 $p=q=2$ 時退化回 Robertson--Schrödinger**。
> 我簡單演算一下。當 $p=q=2$ 時，$pq/(p+q) = 1$，右邊就變成
> $\frac{1}{2}\langle |[\Delta\hat A,\Delta\hat B] + \{\Delta\hat A,\Delta\hat B\}|\rangle$
> 的某種模。利用 $|x+iy|^2 = x^2 + y^2$（因為交換子是 anti-Hermitian、
> 反交換子是 Hermitian），把它平方就得到
> $\frac{1}{4}|\langle[A,B]\rangle|^2 + \mathrm{Cov}(A,B)^2$，
> 這正是 Schrödinger 1930 年的結果。
>
> 在 $p\neq q$ 或 $p\neq 2$ 的情形下，這是一個全新的 bound，特別敏感於
> 兩個觀測量的尾部漲落以及它們之間的不對稱性。

**提醒**：
- **如果時間允許**，走到白板把 $p=q=2$ 演算寫一遍——這是答辯加分項。
- **如果沒空**，至少**指公式逐項對應**：「這項退化成方差積、這項退化成 RS 右側」。
- 委員最常問的問題就是 Q7（怎麼退回 RS），準備好。

---

## Slide 9 · 三、四個觀測量（10:00–11:00）

**目的**：把推廣的趨勢展示出來。

**講稿（60 秒）：**

> 同樣的 mother inequality 在 $n=3$ 時給出三個觀測量的 universal UR——
> 上面這條公式，其中 $F_3$ 是三個 $\Delta\hat A_i$ 的對稱化乘積。
>
> 在 $n=4$ 時，因為偶數個算符的乘積結構更乾淨，可以直接寫成乘積形式——
> 下面這條。
>
> 這兩個結果都比任何兩兩 pairwise UR 的組合**嚴格更強**——只要這幾個
> observable 之間有真正的多體相關性（multipartite correlations）。
> 這一點在後面的 GHZ 例子裡會看得最清楚。

**提醒**：
- 此張節奏可以稍快。
- 「strictly stronger than pairwise」這句講重，預告 GHZ 那張要說的話。

---

## Slide 10 · $n$ 個觀測量的偶 / 奇通式（11:00–12:00）

**目的**：把 universal 結果寫成一個式子。

**講稿（60 秒）：**

> 把所有情形合在一起，本論文得到任意 $n$ 個觀測量任意階的 universal UR：
> 偶數 $n$ 直接寫成乘積形式，奇數 $n$ 用 fully symmetrized product
> $\mathcal S$。
>
> 這個結果三個特性。第一，**單一條不等式包含一整族 UR**：兩個參數家族——
> $(p_1,\dots,p_n)$ 掃描矩階、$n$ 掃描觀測量數。
> 第二，它**包含了**Robertson、Schrödinger 以及若干已知的多 observable bounds
> 作為特例。
> 第三，它對 multi-parameter quantum estimation 提供一個直接的高階類比。

**提醒**：
- 「一條公式包含一族 UR」這句話委員會記住，是你 elevator pitch 的一部分。
- 不要展開「multi-parameter estimation」，後面講 outlook 再提。

---

## Slide 11 · 中心力場應用（12:00–13:00）

**目的**：把抽象結果落到一個具體物理問題上。

**講稿（60 秒）：**

> 第一個應用是中心力場系統。對於勢能 $V = -\beta/r^\alpha$，virial 定理給出
> 動能與位能期望的關係：$\langle T\rangle = -\frac{\alpha}{2}\langle V\rangle$。
>
> 把 mother inequality 應用到 $\hat r$、$1/\hat r$ 或 $\hat r$、$\hat p$，
> 我們得到約束**任意正階** $\langle r^k\rangle$、$\langle r^{-k}\rangle$、
> $\langle p^k\rangle$ 之間關係的不等式。
>
> 對氫原子基態，所有 $\langle r^k\rangle$ 都是 Gamma 函數積分，可以解析計算。
> 結果顯示：對於非高斯徑向密度，pairwise 的 $\Delta_p(r)\Delta_q(p)$
> 嚴格高於變異數型下界——這是 $L^p$ 階層在原子物理中的具體可測量信號。

**提醒**：
- 別把 virial 演算展開——一句話帶過即可。
- 「Gamma 函數積分」這樣講過去，委員不會追問細節。

---

## Slide 12 · 氫原子（13:00–14:30）

**目的**：第一個量化例子，建立可信度。

**講稿（90 秒）：**

> 氫原子基態提供了最乾淨的非高斯解析例子。
>
> 第一，所有 $\langle r^k\rangle$（$k > -3$）都有閉合形式：
> $\langle r^k\rangle = \frac{4}{a_0^3}(2/a_0)^{-(k+3)}\Gamma(k+3)$。
>
> 第二，$\Delta_p(r)$ 在 $p=4$ 起就明顯偏離 Gaussian profile——也就是說，
> 即使在這麼簡單的系統，**變異數已經不夠用**。
>
> 第三，從 $p$ 隨變化的曲線可以看出基態 $\psi_{100}$ 的徑向 tail 結構：
> 高 $p$ 探測尾部、低 $p$ 探測整體擴散。右邊這張圖就是不同 $(p,q)$ 下
> $\Delta_p(r)\Delta_q(p)$ 的曲線，可以看到它形成一個 non-trivial 階層。
>
> 解析端與 RS bound 的數值比較我們也都做了，論文 Chapter 4 詳細給出。

**提醒**：
- **指圖**：「右邊這張圖」要實際指一下。
- 「non-trivial」這個英文詞在中文場合直接念可以，但發音放慢。

---

## Slide 13 · 諧振子（14:30–15:30）

**目的**：用 Gaussian 標桿建立比較參照。

**講稿（60 秒）：**

> 谐振子是 universal Gaussian reference。Coherent / squeezed states 在 $p=q=2$
> 下飽和 Robertson；高階比值 $R_{p,q} = \Delta_p(x)\Delta_q(\hat p) /
> \text{LHS-bound}$ 在 Gaussian family 上取**普适的 $(p,q)$-依賴值**。
>
> 這意味著：任何在現實系統中觀測到的 $R_{p,q}$ 偏離 Gaussian 標準值，
> 就是該系統「非高斯」的定量訊號。這提供了一個直接可實驗檢測的基準。

**提醒**：
- 念「Gaussian reference」時可以說「高斯參考」。
- 不要展開計算，這是 backup 內容。

---

## Slide 14 · 貓態（15:30–17:00）

**目的**：本論文最戲劇性的例子——「方差幾乎一樣，高階矩天差地別」。

**講稿（90 秒）：**

> 接下來是 Schrödinger cat states $|\mathrm{cat}_\pm\rangle \propto |\alpha\rangle
> \pm |-\alpha\rangle$。
>
> 它的關鍵特性是：**方差幾乎不變**——cat state 與相同 amplitude 的 coherent
> state 在 $\Delta_2$ 上幾乎沒有差別——但 $\kappa_4$ 與 $\Delta_p(x)$（$p\geq 4$）
> **大幅變化**。換句話說，cat state 的雙峰結構**完全藏在高階矩裡**，方差看不見。
>
> 因此 cat state 是本論文最直接的反駁證據：證明高階 UR **不是**變異數型 UR
> 的重新表述，而是承載著實質性的新訊息。
>
> 右圖是不同 $\alpha$ 下的高階 moment indicators，可以看到 cat 與 coherent
> 在 $\Delta_2$ 上幾乎重合，但在 $\Delta_4$、$\Delta_6$ 上明顯分離。

**提醒**：
- 這張要**站起來、聲音稍微提高**——是論文的核心 demonstration。
- 「方差看不見」這句話可以重複一次。

---

## Slide 15 · 量子比特與 GHZ（17:00–18:30）

**目的**：證明多 observable 部分是真的有用，不是擺設。

**講稿（90 秒）：**

> Qubit 與 GHZ 是有限維情形，所有量都可以解析計算。
>
> 對於單比特三個 Pauli observable，本論文的多 observable bound 在
> Bloch vector 各向異性的混合態上**嚴格緊於** Robertson 不等式——
> 右圖比較了三-observable bound 與 Robertson 在 Bloch ball 上的差距。
>
> 對於三比特 GHZ 態，事情變得更有意思。從 quantum information geometry 角度看：
> GHZ 的所有兩比特約化態都是極大混合的，所以 pairwise UR 對 GHZ
> **完全沒有訊息**。但 $\langle X_1 X_2 X_3 \rangle = 1$，三-observable bound
> 直接捕捉到這個三體相關性——這正是真正的 multipartite correlation
> 必須由多 observable UR 表達的明證。

**提醒**：
- GHZ 的「兩體無訊息、三體有訊息」這句是亮點，講清楚。
- 委員可能追問 quantum Fisher information 與 Heisenberg scaling，
  你說「outlook 中還會展開」即可。

---

## Slide 16 · 古典雙阱（18:30–19:30）

**目的**：說明框架不只是量子的，還適用古典統計分布。

**講稿（60 秒）：**

> 最後一個例子是古典熱雙阱：平衡密度 $\rho \propto e^{-\beta V}$，$V(x)$ 是
> 雙阱勢能。
>
> 三個觀察。第一，$\Delta_2(x)$ 對勢壘高度幾乎不敏感。第二，加入更高的偶矩
> $\langle x^4\rangle$、$\langle x^6\rangle$ 等等，逐步收緊對平衡分布的
> max-entropy reconstruction，最終收斂到真實雙峰形狀。
>
> 因此這是同一套高階矩 hierarchy 在**純古典統計**下的展示——本論文的 framework
> 不是量子特有的，它對任何由矩描述的分布都適用。這也是與 cat state 例子在
> 邏輯上對稱的補充。

**提醒**：
- 講完這張可以**短暫停頓 2 秒**，做為例子部分結束的訊號，再進總結。

---

## Slide 17 · Summary（19:30–20:30）

**目的**：簡短、扎實。重述五項貢獻。

**講稿（60 秒）：**

> 簡單總結本論文的工作。
>
> 第一，提出一條 operator-functional Hölder 「mother inequality」，作為任意階
> UR 的數學源頭。
> 第二，建立 $n=2,3,4,\dots$ 個 observable、任意正矩階的 universal UR，
> 並給出偶 / 奇情形的封閉通式。
> 第三，在 $p=q=2$ 退化回 Robertson--Schrödinger，與經典結果一致。
> 第四，做了氫原子、谐振子、cat state、qubit、GHZ、古典雙阱六個解析或數值
> 例子。
> 第五，這些例子共同證明：**高階矩承載的訊息不能被簡單歸結為方差的重新表述**。

**提醒**：
- 五點，每點一句，**節奏要快但清楚**。
- 第五點的結論是論文的 take-home message，要**講重**。

---

## Slide 18 · Outlook + Thank you（20:30–21:00）

**目的**：留白給 Q&A，並體面地結束。

**講稿（30 秒）：**

> 後續可探索的方向有四條：UR 的 saturation states 完整刻畫、$L^p$ 階層
> 與 quantum metrology 的精確橋接、實驗端對高階矩的可靠估計
> （cumulant / max-entropy reconstruction），以及在開放系統 noise diagnostics
> 中的應用。
>
> 報告到此，謝謝各位老師，請各位老師批評指正。

**提醒**：
- 鞠躬 / 點頭，**不要說「我講完了」**。
- 站定不要立刻坐下，等委員開始提問。
- **準備好 backup slides**，預期會被問到 Q7（RS recovery）、Q15（GHZ 為什麼必須多體）、
  Q17（實驗如何測高階矩）這幾題——分別對應 backup 第 2、3、6 張。

---

## Backup 區（不一定講）

Backup slides 不需要逐張稿，但你心裡要清楚每張**對應哪個常見問題**，
這樣被問到時可以說「這個我有準備一張 backup，請看」並翻過去。

| Backup # | 對應問題 |
|---------|---------|
| Hölder 細節 | Q4「為什麼選 Hölder」 |
| 兩體 RS 演算 | Q7「怎麼退回 RS」 |
| GHZ correlator | Q15「GHZ 為什麼要多體 UR」 |
| Qubit noise | Q19「對 NISQ 噪聲有用嗎」 |
| GHZ hierarchy convergence | 「高階收斂到什麼？」 |
| 數值管線 | Q17「實驗如何測高階矩」 |
| UR family 對照表 | Q10、Q11、Q12 |
| Cat cumulant 診斷 | Q14「為何選 cat 為非高斯例子」 |

---

## 整體節奏控制

- **總時間 21 分鐘**（保留 1 分鐘緩衝給委員打斷 / 翻頁慢）。
- 20 分鐘節奏節點：講到 slide 14（cat state）時應該已經 17 分鐘。如果落後
  超過 3 分鐘，**從這裡開始切戲**：把 Slide 13（諧振子）一句帶過、
  Slide 16（古典雙阱）一句帶過。
- 不要在 Slide 6, 7（mother inequality）拖太久，這兩張容易超時。
- **被打斷時的處理**：先回答完問題再繼續，**不要一邊翻頁一邊回答**——
  顯得手忙腳亂。

---

## 實戰小提醒

- **指卡（presenter notes）**：把每張 slide 的「第一句話」寫在小卡片上，
  比看 PPT notes 更可靠（特別是緊張時）。
- **不要看委員手裡的論文**——他們在低頭讀的時候你以為他不在聽，其實在看
  你具體寫了什麼。**繼續正常講就好**。
- **如果某張 slide 公式記不住**，**先轉動作**：往白板走、邊走邊說
  「我簡單推一下這裡的關鍵步驟」——買你 5 秒回想時間。
- **節拍器**：如果你 22 分鐘以上，會被委員打斷；如果你 16 分鐘以下，
  會被問「你準備好了嗎」。**目標是 19–21 分鐘**這個區間。

祝順利！
