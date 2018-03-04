# Overview

https://ethereum.github.io/browser-solidity

* Prerequisites
Open VPN

* Development and Compile

![Browser-solidity](/picture/Browser-solidity.png)

![Browser-solidity](/picture/Detail.png)

![Browser-solidity](/picture/Detail1.png)

* Development 
```
  pragma solidity ^0.4.0;
    
    contract DemoTypes {
        function f(uint a) returns (uint b) 
        {
            uint result = a * 8;
            return result;
        }
    }
```
![Web IDE](/picture/Demo-Web-IDE.png)

```
WEB3DEPLOY
var demotypesContract = web3.eth.contract([{"constant":false,"inputs":[{"name":"a","type":"uint256"}],"name":"f","outputs":[{"name":"b","type":"uint256"}],"payable":false,"stateMutability":"nonpayable","type":"function"}]);
var demotypes = demotypesContract.new(
   {
     from: web3.eth.accounts[0], 
     data: '0x6060604052341561000f57600080fd5b60b68061001d6000396000f300606060405260043610603f576000357c0100000000000000000000000000000000000000000000000000000000900463ffffffff168063b3de648b146044575b600080fd5b3415604e57600080fd5b606260048080359060200190919050506078565b6040518082815260200191505060405180910390f35b600080600883029050809150509190505600a165627a7a72305820612a064a334601456b8667125a242e4edf7d215579c2eb1233255a6f411d58040029', 
     gas: '4700000'
   }, function (e, contract){
    console.log(e, contract);
    if (typeof contract.address !== 'undefined') {
         console.log('Contract mined! address: ' + contract.address + ' transactionHash: ' + contract.transactionHash);
    }
 })
```
![WEB3DEPLOY](/picture/WEB3DEPLOY.png)
