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
    flowchart TB
     node1[Node]
     node2[/Node/]
     node3[\Node\]
     node4[Node]
```
```mermaid
    flowchart TB
     node1[Node]
     node2[/Node/]
     node3[\Node\]
     node4[Node]
     
```

```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D;
```



