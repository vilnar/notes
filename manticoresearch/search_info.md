## Інвертований індекс (повнотекстовий)

```
id  | name
1   | fastest apple iphone ios
2   | fastest apple ipad
3   | fastest android phone from samsung
```

```
слово: [айді документів]
fastest: [1,2,3]
apple: [1,2]
ios: [1]
ipad: [2]
android: [3]
phone: [3]
from: [3]
samsung: [3]
```

Щоб врахувати порядок слів, потрібна ще позиція слова
```
слово: [[айді документу,позиція]]
fastest: [[1,0],[2,0],[3,0]]
apple: [[1,1],[2,1]]
ios: [[1,3]]
ipad: [[2,2]]
android: [[3,1]]
phone: [[3,2]]
from: [[3,3]]
samsung: [[3,4]]
```



Оптимізація MapReduce
```
====== -> Map() -> k1,v1
============ -> Map() -> k1,v2
========= -> Map() -> k2,v1
======= -> Map() -> k1,v3

# сортування і групування
k1, [v1,v2,v3]
k2, [v1]

# Shuffle
Reduce(k1, [v1,v2,v3]) -> [v,v,v]
Reduce(k2, [v1]) -> [v,v,v]
```
