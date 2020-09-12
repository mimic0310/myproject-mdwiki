# Dowload Page


## Euclid Lemma

> ***Lemma1: d可整除a,且d可整除b  <==> d可整除(a-b), 且d可整除b   (假設a大於b)***

proof:
==>
另a = dp, b = dq, (p,q為整數)
則(a-b) = d(p-q) (p-q亦為整數) 因此(a-b)可被d整除

<==
另 a-b = dp, b = dq  (p,q為整數)
則 a = b + dp = dq + dp = d(q+p)   (q+p亦為整數)   因此a可被d整除


> ***Lemma2: d可整除a,且d可整除b  <==> d可整除(a%b), 且d可整除b   (假設a大於b)***
proof:

令 a = k*b + r      (這邊的r就等價於 a%b)

    (=>)
    已知 
        a=dp  (式1)
        b=dq  (式2)    
    移項得 r = a-k*b
    帶入(式1)(式2)得 r = dp -kdq = d(p-kq)
    已知p,k,q皆為整數, 因此r 必可被d整除, 因此d為r之因數 
    因此d為 b,r之公因數

    (<=)
    已知
        r = dp  (式1)
        b = dq  (式2)
    帶入可知 a = kdq + dp = d(kq+p), 因此d為a之因數


>證明GCD(a,b) = GCD(b,a%b) 
(todo)



是一種有效率的算法, 目的是求兩個整數的最大公因數, 核心的概念來自Euclid Lemma

給任兩數, 不斷的將大數減去小數的結果取代大數, 最後其中一個數會是0
例如 
Iteration_1: (a,b) = (50,15)
Iteration_2: (a,b) = (50-15,15) = (35,15)
Iteration_3: (a,b) = (35-15,15) = (20,15)
Iteration_4: (a,b) = (20-15,15) = (5,15)
Iteration_5: (a,b) = (5,15-5) = (5,10)
Iteration_6: (a,b) = (5,10-5) = (5,5)
Iteration_7: (a,b) = (5,5-5) = (5,0)
