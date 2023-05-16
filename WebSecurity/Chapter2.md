---
date : 2023-02-23 9:46 Thu
alias : []
---
---

## 2/23
decimation加密法跟affine加密法的解密。


## 3/2
### PlayFair Key Matrix
先選擇好`key之後，將其先填入表格內`，後續的字母則依照順序排列。後再依照規則進行加解密。

>規則:
>取連續兩個明文
>1.若為對角      => 取另外兩個對角
>2.若為同一行  => 向右取兩密文
>3.若為同一列  => 向下取兩密文
>4.若相同         => 中間插入X(表示null later，為明文中不出現的字母)
>5.若明文為奇數，最後加入X

限制: key中不可有重複的字母
#### Security

## Polyalphabetic Cipher

###  <font color="orange">1. Vigenere Cipher</font>
#### Security
雖然因為key的關係，會使的明文會對應到不同的密文。可以藉此混淆字母頻率，但因為key是重複的關係，可以藉由觀察密文中重複的字母，來猜測key的長度，還是有被破解的可能。

### <font color="orange">2. Autokey Cipher</font>
在Vigenere Cipher上`加以改良`，原先是藉由同一個key一直循環，來對明文加密，Autokey則是以取一段明文做為下一
段明文的key進行加密。

#### Security
可以藉由`暴力法猜測key的長度`，再將明文分段後相同的位置做比較，以達到破解的效果。

### <font color="orange">3. Vernam Cipher</font>
藉由跟明文一樣長的key來做加密
#### Security

### <font color="orange">4. One-Time Pad</font>
為`Vernam Cipher的改良版`，每一次加密的key都不相同，因為key之間沒有關聯性，很難用字母頻率攻擊法破解。

#### Security
要每一次都產生不同的key會是加密法的問題之一。也有key distribution(*註1*)的問題。


## Transposition Cipher
### 1. Rail Fence Cipher
### 2. Row Transposition Ciphers


*註1 : 在加密時，因為是使用key下去進行加解密，所以加解密的雙方都需要知道key為和，而也就衍生出了要怎麼安全的傳遞key的問題，也就是所謂的key distribution*
