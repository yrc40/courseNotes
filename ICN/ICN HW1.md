## P1
### Assumptions and Message Specification
1. ATM to Server

| Msg | Meaning |
|------|-----------|
| CARD insert (userId) | To let Server know a card is in ATM and it transmits user ID to server |
| ` <pwd>`  |  User enter password to server |
| BALANCE request | User request balance |
| `<amt>` | User enter amount to withdraw |
| DONE | User's operation done |

2. Server to ATM

| Msg | Meaning |
|-----|-----------|
| PWD request | Server ask user to enter password |
| OK | Last operation OK |
| ERROR | Laster operation ERROR |
| `<bal>` | Response to BALANCE request |
| DONE | Section done, display welcome screen |
### Operations
![[Pasted image 20231015211214.png]]

## P3
### a.
Circuit-switched network 會比較適合。題目提及此程式包含較長的 session 及穩定的頻寬，不屬 bursty data，這比較適合需要事先預定資源 `( end-end resources allocated)` 的 circuit-switched network，如此一來也比較不會造成資源的浪費。此外 call setup 的成本也可以攤銷在一整個很大的session。
### b.
因為每一個 link 都有足夠頻寬處理整個程式的傳輸速度，所以就算在最糟的情況，也就是整個程式同時對很多 link 傳輸資料時，也不會有 congestion 的問題，因此在容量遠大於傳輸頻寬的情況下沒有 congestion control 的需要。

## P9
### a.
$N=1Gbps/100kbps=10,000 \text{ users.}$
### b.
$f(p, M, N)=\sum_{n=N+1}^{M}(^M_n)p^n(1-p)^{M-n}$

## P18
### `tracert www.nycu.edu.tw`
* 2023/10/16 14 : 55
![[Pasted image 20231016145527.png]]
* 15 : 58
![[Pasted image 20231016155949.png]]
* 16:58
![[Pasted image 20231016171513.png]]
### a. 
### b.
### c.
### d. `tracert dictionary.cambridge.org`
* 2023/10/16 15 : 00
![[Pasted image 20231016150017.png]]
* 16 : 00
![[Pasted image 20231016160153.png]]
* 17 : 00
![[Pasted image 20231016171653.png]]

## P31
### a. 
Time to move the message from the source host to the first packet switch  =  $\frac{10^6}{5\times10^6}=0.2\text{ sec}$
Total time to move the message from source host to destination host = $0.2\times3=0.6 \text{ sec}$
### b.
Time to move the first packet from source host to the first switch = $\frac{10^4}{5\times10^6}=2\text{ ms}$
The time second packet is fully received at the first switch = $2\times2=4 \text{ ms}$
### c.
Time to move the file from source host to destination host when message segmentation is used = $6+(100-1)\times2=204\text{ ms}=0.204\text{ sec}$
Compare to result of part(a), using message segmentation cause slight delay (0.004 sec), which is significantly less.
### d.
