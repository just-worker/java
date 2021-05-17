# 同步和异步

| attr | description                      | example                  |
| ---- | -------------------------------- | ------------------------ |
| 同步 | 动作发起，等待结果返回后继续处理 | 上菜，等人吃完，收碗刷碗 |
| 异步 | 动作发起，结果不必自身处理       | 吃完，走人               |

# 阻塞和非阻塞

| attr   | description    | example                            |
| ------ | -------------- | ---------------------------------- |
| 阻塞   | 强制等待结果   | 点餐，死等厨房门口，不能做其他事情 |
| 非阻塞 | 不强制等待结果 | 点餐，等待叫号，安排随意           |

# IO

| io      | 同步      | 阻塞      | 说明                                                         |
| ------- | --------- | --------- | ------------------------------------------------------------ |
| ``BIO`` | ``true``  | ``true``  | 阻塞：``IO``读写不能做其他的<br />同步：读写完毕继续做后续收尾 |
| ``NIO`` | ``true``  | ``false`` | 同步：后续事件继续完成<br />非阻塞：``IO``无需等待，中途做其他事情，多路复用监听``IO``状态 |
| ``AIO`` | ``false`` | ``false`` | 非阻塞：``IO``无需等待<br />异步：状态无需监听，状态达到自动触发回调，收尾不在发起线程 |
