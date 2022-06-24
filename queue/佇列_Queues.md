# Queue 佇列
一有資料進入add(enqueue)，同時有資料出去delete(dequeue)。

## rear 後端
資料進入。
## front 前端
資料出去。

# FIFO (first in first out)
stack完全依照LIFO，
但queue則不一定都依照FIFO，有一些queue(ex: priority queue)任何元素位置都可以出列。


# 使用時機
需要排隊的行程。
如多工系統中，共用CPU資源，必須用queue做「排程」(scheduling)。