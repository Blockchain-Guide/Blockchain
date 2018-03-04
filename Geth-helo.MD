# Overview
* Get accounts
```
> eth.accounts
["0xfae04344a4cb552e7ea2492c207b73cb03056950"]

> eth.getBalance("0xfae04344a4cb552e7ea2492c207b73cb03056950")
0

> acc0 = eth.accounts[0]
"0xfae04344a4cb552e7ea2492c207b73cb03056950"
> eth.getBalance(acc0)
0

```

* How to convert ether between two accounts
Earlier stated that each account's public key (address) is the core of all Ethereum account operations, but the address string is too long, we use acc0 / acc1 represent accounts [0] and [1], the other set to transfer 0.01 Ether
```

```
