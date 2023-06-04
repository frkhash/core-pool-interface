---
title: FrkhashMiner
minVer: 1.12
releases: https://github.com/frkhash/frkhashminer/releases
---

```
#!/bin/bash

## This Miner is Opensource / Free | Dont ever trust closed source mining software. EVER!

#################################
## Begin of user-editable part ##
#################################

# Supported Pool
POOL=rebirth.expanse.tech:8008

# Address to send funds to. Change this address to yours!
WALLET=0xb97615a69fc6e15a1123480e9b49d312c41a3e6a

#################################
#  Cuda Example                 #
#################################

# ./frkminer/frkminer -U -P stratum://0xb97615a69fc6e15a1123480e9b49d312c41a3e6a.1@rebirth.expanse.tech:8008

#################################
#  CPU Example                  #
#################################

# ./frkminer/frkminer -C -P stratum://0xb97615a69fc6e15a1123480e9b49d312c41a3e6a.1@rebirth.expanse.tech:8008

#################################
##  End of user-editable part  ##
#################################

cd "$(dirname "$0")"

./frkminer/frkminer -U -P stratum://$WALLET.1@$POOL $@

```