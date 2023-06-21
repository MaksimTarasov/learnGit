# Как строить диаграммы?  Шпаргалка
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
     click A "http:\\ya.ru"
     
     
     
```
## Стрелки между узлами
```
  Команды для создания стрелок:  
    flowchart TB
        node1[А] --> node2[/B/]
        C --- D
        node3[\c/] -.-> node4[/f\]
        node5[\c/] ==> node5[/f\]
        node6((c)) --o node7[/f\]
        node7((c)) --o node6[/f\]
        K --x L
        K --> K
```
```mermaid
    flowchart TB
        node1[А] --> node2[/B/]
        C --- D
        node3[\c/] -.-> node4[/f\]
        node5[\c/] ==connect==> node5[/f\]
        node6((c)) --o node7[/f\]
        node7((c)) --o|WTF|node6[/f\]
        K --x L
        K --> K
```
## Подграфы
Используются для визуального объединения.
```

```
```mermaid
    flowchart TB
        subgraph Zone1
            A1 --> A2
            end
        subgraph Zone2
            A3 --> A2
            end
                
        
```


## Примеры
### Ремонт интернета)))
```mermaid
   flowchart TB
      A[Нет интернета]--> B{Интернет оплачен?}
      A[Нет интернета]--> С{Работает ли роутер?}
      B{Интернет оплачен?}  --да--> Call[Позвонить в службу] --> D3[Проверить интернет]  
      B{Интернет оплачен?} --Нет--> D2[Оплатить интернет] -->D3[Проверить интернет] 
      D3[Проверить интернет] --Нет интернета--> A[Нет интернета]  
      D3[Проверить интернет] --Есть интернет--> End1((Конец))
      
```


```mermaid
sequenceDiagram
    participant Рыболов
    participant Водоем - кормовая точка
    participant Рыба
    %%Рыболов->>Водоем: Кидает кормушку с кормом
    loop Стартовый закорм 10 мин
        Рыболов->>Водоем - кормовая точка: Заброс кормушки с кормом
    end
    loop Основной процесс рыбалки
        Рыболов->>Водоем - кормовая точка: Заброс кормушки с кормом и с наживкой
        Водоем - кормовая точка-->>Рыба:Кормовой сигнал идет к рыбе.
        activate Рыба
        Note left of Рыба: Движется к кормовой точке!
        Рыба -->>+Водоем - кормовая точка: Ест корм!
        Note left of Рыба: Находит наживку!
        Рыба -->> Рыболов: Сигнализация поклевки
        activate  Рыболов
        Рыболов ->> Рыба: Подсечка, вываживание рыбы
        deactivate Рыба
        deactivate Рыболов
    end
```

Полезная ссылки , где еще больше кайфов, от доброго человека.
https://habr.com/ru/articles/652867/
https://mermaid.js.org/syntax/sequenceDiagram.html


