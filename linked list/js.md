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