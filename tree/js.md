非線性結構
由一個或以上的 node 所組成。
存在一個特殊節點 root 。

### 合法樹
一棵合法樹，
node 可以相互連結，但不能形成無出口的迴圈。

### root
根 node。

#### degree
該 node 的分支(子樹)數目。

#### level
從 root 延伸的分支次數。

#### height
從 root 延伸的最遠 node，最高 level。

#### parent
上一 level 的 node。

#### child
下一 level 的 node。

#### ancestor & descendant
從 terminal node 往 root 推，所有 node。
從 root 往 terminal node 推，所有 node。

#### siblings
有相同 parent 的 node。

#### terminal nodes
又稱 leaf node。
樹的末端，
degree 為0的 node。

#### nonterminal nodes
有 degree 的 node。

#### generation
level 相同的 node。

#### forest
由 n 個互斥樹的集合(n >= 0)
移去 root 即為 forest。

---

一般樹在電腦記憶體中儲存方式為 linked list。

以 n-way 樹來說，
因為每一 node 的 degree 都不相同，所以表上取 n 為 最大固定長度。
假設有 m node，共用 n*m 欄位。

### 二元樹 knuth
最多只可以有 2 degree。(可以為空集合)


#### Fully binary tree
假設高度為 h ，ndoe = 2h次方 -1。
(每一 nonterminal node 有 2 degree)

#### Compelete binary tree
假設高度為 h ，node < 2h次方 -1。
(node 小於，但高度跟 fully 相同)

#### Skewed binary tree
完全沒有左節點或右節點。

#### strictly binary tree
每個 nonterminal node 均有 非空的 左右子樹。
