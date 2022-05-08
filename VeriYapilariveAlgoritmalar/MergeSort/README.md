# Proje 2

```[16,21,11,8,12,22]``` -> Merge Sort

1. Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.

2. Big-O gösterimini yazınız.

# Çözüm

1. Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.
```
                                [16,21,11,8,12,22]
Level 0                
                        [16,21,11]                [8,12,22]
Level 1
                    [16,21]        [11]        [8,12]        [22]
Level 2
                [16]    [21]    [11]       [8]    [12]    [22]
Merge(Level 2)
                    [16,21]   [11]             [8,12]   [22]
Merge(Level 1)
                        [11,16,21]                [8,12,22] 
Merge(Level 0)
                                [8,11,12,16,21,22]
```

2. Big-O gösterimini yazınız.
```
    n    tane sayıda      2^0 (n-1) tane karşılaştırma oluyor.
n/2  n/2 tane sayıda      2^1 (n/2-1) tane karşılaştırma oluyor.
      .                                 .
      .                                 .
      .                                 .
      .                                 .
Bunu formül haline getirirsek:    ∑ 2^i [(n/2^i)-1] haline geliyor.
```
```
log(n)-1
    ∑ (2^i [(n/2^i)-1])  | i=0 dan |log(n)-1'e kadar.
   i=0
```
> Peki bu log(n)-1 nereden çıktı.
```
    Yukarıdaki örneğe bakıldığında Level 0, Level 1, Level 2 olarak 3 tane katmanımız bulunuyor. Biz de formül hesaplarken kolaylık olması için i=0 dan başlattık. 
    Yukarıdaki örneğe göre log(n)-1'i doğrulayalım:
     log(8)-1 = 3 - 1 = 2 |Yani i=0 dan başladığında |0,1,2| tane olmak üzere 3 tane katman olmuş oluyor.| Doğru! 
```
```
log(n)-1
    ∑ (2^i [(n/2^i)-1])  
   i=0

  =>(2^i ler sadeleşir.) 

                    log(n)-1            log(n)-1       log(n)-1
                        ∑ (n)-2^i]) =>     ∑ (n)    +     ∑ (2^i)
                       i=0                i=0            i=0
```
> Formülümüz 2 kısıma ayrıldı.
```
log(n)-1
    ∑ (n) =>  n * [(log(n)-1) - (0) + 1] => (nlog(n))
 i=0
```
```
log(n)-1
    ∑ (2^i) => (1 + 2 + 4 + .... + 2^(log(n)-1))  => (Bu sayılar için bir toplama formülü bulunuyor sonuç ise şöyle) [(2^log(n)-1+1) - 1] / (2-1)
 i=0

 Buradan ilerlersek => 2^log(n) - 1  => Sonucumuz (n-1) oluyor. 
```

> Sonuç:       nlog(n) - (n-1) 

> Ve burada dominant faktör nlog(n) olduğu için   

```
Big-O notation = O(nlog(n)) olmuş oluyor.
```