# Proje 1

```[22,27,16,2,18,6]``` -> Insertion Sort
1.  Yukarıda verilen dizinin Insertion Sort türüne göre aşamalarını yazınız.
2. Big-O gösterimini yazınız.
3. Time Complexity
    *  Average case: Aradığımız sayının ortada olması

    * Worst case: Aradığımız sayının sonda olması

    * Best case: Aradığımız sayının dizinin en başında olması.

4. Dizi sıralandıktan sonra 18 sayısı hangi case kapsamına girer? Yazınız.

5. ```[7,3,5,8,2,9,4,15,6]``` dizisinin Insertion Sort'a göre ilk 4 adımını yazınız.
# Çözüm

1. Yukarıda verilen dizinin Insertion Sort türüne göre aşamalarını yazınız.
```
    [22,27,16,2,18,6] (n)       |      1'den n'e kadar olan
    [2|27,16,22,18,6] (n-1)     |       sayıların toplamı
    [2,6|16,22,18,27] (n-2)     |    [n.(n-1)]/2 = [n^2-n]/2
    [2,6,16|22,18,27] (n-3)     |        Big-O => O(n^2) 
    [2,6,16,18,22,27] (1)       |
```
2. Big-O gösterimini yazınız.
```
    Big-O => O(n^2) |  => O(6^2) = O(36)
```
3.  Time Complexity
    *  Average case: Aradığımız sayının ortada olması

    * Worst case: Aradığımız sayının sonda olması

    * Best case: Aradığımız sayının dizinin en başında olması.
4. Dizi sıralandıktan sonra 18 sayısı hangi case kapsamına girer? Yazınız.
```
    18 sayısı dizinin ortasında olduğu için 'Average Case'  
    kapsamına girer.
```
5. ```[7,3,5,8,2,9,4,15,6]``` dizisinin Insertion Sort'a göre ilk 4 adımını yazınız.
```
    [7,3,5,8,2,9,4,15,6]
 1. [2|3,5,8,7,9,4,15,6]
 2. [2,3|4,8,7,9,5,15,6]
 3. [2,3,4|5,7,9,8,15,6]
 4. [2,3,4,5|6,9,8,15,7] 
```