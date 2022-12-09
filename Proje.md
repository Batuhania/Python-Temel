## 1- Flatten function
 Bir listeyi düzleştiren (flatten) fonksiyon yazın. Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak:

input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

output: [1,'a','cat',2,3,'dog',4,5]


```{python}
l = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]
nl = []
def flatten(n):
    for i in n :
        if isinstance(i,list):
            flatten(i)
        else:
            nl.append(i)

flatten(l)
print(nl)
```


## 2- Reverse
Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. Örnek olarak:

input: [[1, 2], [3, 4], [5, 6, 7]]

output: [[[7, 6, 5], [4, 3], [2, 1]]


```{python}
input = [[1, 2], [3, 4], [5, 6, 7]]
input.reverse()
for i in range(len(input)):
    (input[i])=(input[i])[::-1]

print(input)
```
