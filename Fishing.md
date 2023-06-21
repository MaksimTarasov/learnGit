# Как строить диаграммы? 
## Установка плагинов в Pycharm для работы с Mermaid
Если плагины не установленны, нужно нажать 
```mermaid
  graph LR;
      Ctrl+Alt+S-->Plugins-->Mermaid;
```
## Базовый блок
```
В тексте прописываем блок
    ```mermaid
        И в данном блоке описываем диаграмму
    ```
```
## Узлы
```
 Команды для создания узлов:
     flowchart TB
         node1[Node1]
         node2[/Node2/]
         node3[\Node3\]
         node4(Node4)
         node5((Node5))
         node6[/Node6\]
         node7[\Node7/]
         node8{Node8}
         node9{{Node9}}
         
    TB — «top to bottom», сверху вниз;
    TD — «top-down/ same as top to bottom», сверху вниз;
    BT — «bottom to top», снизу вверх;
    RL — «right to left», справа налево;
    LR — «left to right», слева направо.
```
```mermaid
    flowchart TB
     node1[Node1]
     node2[/Node2/]
     node3[\Node3\]
     node4(Node4)
     node5((Node5))
     node6[/Node6\]
     node7[\Node7/]
     node8{Node8}
     node9{{Node9}}
     
     
     
```

```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D;
```



