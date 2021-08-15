# THE CRYPTOCURRENCY PAY APP


![Unknown-2](https://user-images.githubusercontent.com/80144026/129491906-8c6dc3d8-085e-425e-9765-42bc323b414d.jpeg)



This is a payment application, which is integrated with the Ethereum blockchain network. It enables users to instantly pay/send cryptocurrency payments. I used the example of hiring a fintech professional for a contract job and paying the candidate with Ether. This application, once fine tuned,  would be great for people who send money internationally as remittance fees are very high, consumer to merchant transfers and peer to peer money transfers.



## Technologies

This project is written in Python within the Visual Code environment with the following packages:

* Streamlit
* Web 3
* Eth Tester
* mnemonic
* bip44


## Installation Guide
Before running the application first install and verify the following dependencies:
 
* Steamlit from PyPI
 ```python
 pip install streamlit
 ```
* Web 3 from PyPI
 ```python
 pip install web3==5.17
 ```
 * Eth Tester from PyPI
 ```python
 pip install eth-tester==0.5.0b3
 ```
 * Mnemonic from PyPI
 ```python
 pip install mnemonic
 ```
 * Bip 44 from PyPI
 ```python
 pip install bip44
 ```
 
Next, Import the Modules


Crypto_wallet.py:

 ```python
import os
import requests
from dotenv import load_dotenv
load_dotenv()
from bip44 import Wallet
from web3 import Account
from web3.auto.infura.kovan import w3
from web3 import middleware
from web3.gas_strategies.time_based import medium_gas_price_strategy
```

Fintech_Finder.py
 ```python
 import streamlit as st
from dataclasses import dataclass
from typing import Any, List
```
 
Clone to your local repo and open in VS Code


## How to Use

* In the terminal, navigate to the project folder and run the Streamlit application by using "streamlit run instantpayapp.py"
* On the resulting webpage, select a candidate that you would like to hire from the appropriate drop-down menu. Then, enter the number of hours that youwould like to hire them for.
* Click the Send Transaction button to sign and send the transaction with your Ethereum account information. If the transaction is successfully
communicated to the Ethereum Kovan testnet, validated, and added to a block, a resulting transaction hash code will be written to the Streamlit application sidebar.
* Copy the customer’s (your) Ethereum address from the Streamlit application page, and navigate to [Kovan Etherscan](https://kovan.etherscan.io/).
* On the Kovan Etherscan page, click on the Txn Hash number associated with the transaction that paid the Fintech Finder candidate.
* Return to the original transaction, and click the transaction’s to address.

## License
MIT
