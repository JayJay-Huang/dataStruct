[參考資料](http://alrightchiu.github.io/SecondRound/linked-list-introjian-jie.html)

---

是一種線性表。
不會按順序儲存資料。
每一節點儲存下一節點指標(pointer)。

node: 節點。
data: 資料。
pointer: 節點指標。

---
# js

#### 
插入資料: O(1)
讀取資料: O(n)

### 建立
```
class linkedList{
    constructor(name, next = null){
        this.next = next; // pointer
        this.name = name;
    }
}

let link_0 = new linkedList('1號');
let link_1 = new linkedList('2號');
let link_2 = new linkedList('3號');

link_0.next = link_1;
link_1.next = link_2;
```
建立一個 class
將其建構子 預設 pointer = null;

### 存取元素
```
ptr = link_0; // 指定起點
while(ptr != null){
    console.log(ptr.name);
    ptr = ptr.next; // 指向下一元素
}
```
### 插入新節點
```
let link_3 = new linkedList('4號'); // 建立 node
link_3.next = link_0; // 指定 pointer
ptr = link_3; // head
```

---
C#

```
public class Node
{
    public Node next;
    public Node()
    {
        this.next = null;
    }
}
```
### 插入新節點
```
Node node1 = new Node();
Node node2 = new Node();
node1.da = 12; // 
node1.next = node2;
```
### 存取元素
```
WriteLine(node1.da);
node1 = node1.next; // 指向下一點
```

```
class Node<T>
{
    public Node<T> Next { get; set; }
    public Node<T> Previous { get; set; }
    public T Value { get; set; }

    public Node(T value)
    {
        Value = value;
    }
}
class LinkedList<T>
{
    public Node<T> First; // 首
    public Node<T> Last; // 尾
    public int Count;
    public void Add(T value)
    {
        Node<T> node = new Node<T>(value);
        if (Count == 0)
            First = node; // 將第一個 node 放置於 First
        else
        {
            Last.Next = node; // 當次的 node，放置於上次 node的next (此處 Last 還是先前 node)
            node.Prev = Last; // 前訪: 將先前node，放置於當次 node的 prev
        }
        Last = node; // 覆蓋先前資料 使 Last 成為當下 node
        ++Count; 
    }
}
```