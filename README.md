# THE CRYPTOCURRENCY PAY APP


![Unknown-2](https://user-images.githubusercontent.com/80144026/129491906-8c6dc3d8-085e-425e-9765-42bc323b414d.jpeg)



This is a payment application, which is integrated with the Ethereum blockchain network. It enables users to instantly pay/send cryptocurrency payments. I used the example of hiring a fintech professional for a contract job and paying the candidate with Ether. This application, once fine tuned,  would be great for people who send money internationally as remittance fees are very high, consumer to merchant transfers and peer to peer money transfers.



## DEMO IMAGES


### Send Transaction

<img width="1766" alt="Screen Shot 2021-08-25 at 2 49 31 PM" src="https://user-images.githubusercontent.com/80144026/130871670-be1af221-a4c4-41d8-a9ab-240351ad98ba.png">


### Transaction Complete

<img width="1701" alt="Screen Shot 2021-08-25 at 3 09 14 PM" src="https://user-images.githubusercontent.com/80144026/130871328-9c505c6b-5484-4cb5-8dce-1ebd9633ae57.png">

### Check Transaction on Kovan Etherscan

* Sender's Account

<img width="1303" alt="Screen Shot 2021-08-25 at 2 58 06 PM" src="https://user-images.githubusercontent.com/80144026/130871442-cff88f34-a0e8-4522-a18d-063a3c3f3aad.png">

* Transaction Details

<img width="1303" alt="Screen Shot 2021-08-25 at 2 58 20 PM" src="https://user-images.githubusercontent.com/80144026/130871452-3a959416-072b-41df-a71b-fede5402bf19.png">

* Receiver's Account 

<img width="1308" alt="Screen Shot 2021-08-25 at 2 58 36 PM" src="https://user-images.githubusercontent.com/80144026/130871458-19325537-3e50-473b-ab29-0b7164f7812c.png">





## How to Use

* In the terminal, navigate to the project folder and run the Streamlit application by using "streamlit run Fintech_Finder.py"
* On the resulting webpage, select a candidate that you would like to hire from the appropriate drop-down menu. Then, enter the number of hours that you would like to hire them for.
* Click the Send Transaction button to sign and send the transaction with your Ethereum account information. If the transaction is successfully
communicated to the Ethereum Kovan testnet, validated, and added to a block, a resulting transaction hash code will be written to the Streamlit application sidebar.
* Copy the customer’s (your) Ethereum address from the Streamlit application page, and navigate to [Kovan Etherscan](https://kovan.etherscan.io/).
* On the Kovan Etherscan page, click on the search bar and enter your ethereum address or the transaction Hash number associated with the transaction that paid the Fintech Finder candidate, click on the transaction details to verify payment success.



## Technologies

This project is written in Python within the Visual Code environment with the following packages:

* Streamlit
* Web 3
* Eth Tester
* mnemonic
* bip44
* Infura API https://infura.io


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

## Contributors:

[Van Maquilan](https://www.linkedin.com/in/van-miller-sarcov-maquilan-20b472202/)

## License
MIT
