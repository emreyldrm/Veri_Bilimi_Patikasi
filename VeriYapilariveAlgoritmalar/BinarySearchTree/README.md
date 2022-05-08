# Proje 3

```[7, 5, 1, 8, 3, 6, 0, 9, 4, 2]``` dizisinin Binary-Search-Tree aşamalarını yazınız.

Örnek: root x'dir. root'un sağından y bulunur. Solunda z bulunur vb.

# Çözüm
```
・ Binary Search Tree ' de eleman eklemek için root' dan başlanır. 
・ Root ' dan küçük sayılar sol tarafa, büyük sayılar ise sağ
tarafına yazılırak bir ağaç(tree) yapısı oluşturulmuş olur.
```
> root = 7 'dir

```
5| 7'den küçük olduğu için 7'nin soluna yazılır.                                7
                                                                          5
```
```
1| 7'den ve 5'den küçük olduğu için 7 ve 5 'in soluna yazılır.                  7
                                                                          5
                                                                      1
```
```
8| 7'den büyük olduğu için 7'nin sağına yazılır.                                7
                                                                          5           8
                                                                      1
```
```
3| 7 ve 5' den küçük olduğu için soluna 1'den                                   7 
büyük olduğu için 1'in sağına yazılır.                                    5           8
                                                                      1
                                                                          3
```
```
6| 7'den küçük olduğu için soluna 5'den büyük                                   7
olduğu için 5'in sağına yazılır.                                          5           8
                                                                      1       6
                                                                          3
```
```
0| 7, 5 ve 1' den küçük olduğu için 1'in                                        7 
soluna yazılır.                                                           5           8
                                                                      1       6
                                                                  0       3
```
```
9| 7 ve 8' den büyük olduğu için 8'in                                           7 
sağına yazılır.                                                           5           8
                                                                      1       6           9
                                                                  0       3
```
```
4| 7 ve 5' den küçük olduğu için soluna                                         7
1 ve 3 den büyük olduğu için 3'ün sağına                                  5           8
yazılır.                                                              1       6           9
                                                                  0       3
                                                                              4
```
```
2| 7 ve 5' den küçük olduğu için soluna                                         7
1'den büyük olduğu için sağına 3 'den                                     5           8
küçük olduğu için 3' ün soluna yazılır.                               1       6           9
                                                                  0       3
                                                                      2       4
```
> 08.05.2022 [Patika.dev](https://www.patika.dev/tr)