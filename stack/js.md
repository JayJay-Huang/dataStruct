#### 用 function 建立
```
const max = 3; // 定義最大容量
let stack = []; // stack 本身
let top = -1; // 頂端

// 確認空值
function isEmpty(){
    if(top == -1) return true;
    else return false;
}

// 放入
function push(data){
    if(top < max -1){
        top++;
        stack[top] = data;
        console.log('push:',stack[top]);
    } else {
        console.log('已滿');
    }
}

// 拿出
function pop(){
    if(!isEmpty()){
        console.log('pop:',stack[top]);
        top--;
    } else {
        console.log('已空');
    }
}
```
#### 用 class 建立
```
class stack {
    constructor(){
        this.top = -1;
        this.buff = [];
    }
    // 放入
    push(data){
        this.top++;
        this.buff[this.top] = data;
        console.log('push:', this.buff[this.top])
    }
    // 拿出
    pop(){
        if(this.top > -1){
            let pop = this.buff[this.top];
            this.top--;
            return pop;
        } else {
            return null
        }
    }
}
```

#### 使用 js array
```
let stack = [];

stack.push('A')
stack.push('B')
stack.push('C')
stack.pop()
stack.pop()
stack.pop()
```
當無值時，pop() 會回傳 undefined


#### 使用 linked list 實作 stack
```
class node{
    constructor(){
        this.data = 0;
        this.next = null;
    }
}

let top = null;

// 判斷空值
function isEnmpty(){
    if(top == null){
        return true;
    } else {
        return false;
    }
}

// 存入
function push(data){
    new_node = new node();
    new_node.data = data;
    new_node.next = top;
    top = new_node;
}

// 取出
function pop(){
    if(isEnmpty()){
        return -1;
    } else {
        ptr = top;
        top = top.next;
        return ptr.data;
    }
}
```

