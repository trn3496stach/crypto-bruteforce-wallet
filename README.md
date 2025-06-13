# WalletGen – Your Powerful Crypto Brute Force Wallet Tool: Find & Recover Lost Crypto

**WalletGen** is a leading-edge, open-source tool designed for advanced **crypto wallet brute force** operations. It's your powerful solution for generating, searching, and potentially recovering lost or inactive **Bitcoin (BTC)**, **Ethereum (ETH)**, **BNB**, **Polygon (MATIC)**, and other **EVM-compatible wallets**. With real-time balance checking and a high-performance C++ engine, WalletGen provides unparalleled speed and effectiveness.

<!--
Meta description:
WalletGen is a high-speed, open-source crypto wallet brute force tool, enabling users to generate, test, and potentially recover lost Bitcoin, Ethereum, and other EVM-compatible wallets. Utilizing databases and real-time balance checks.
-->

## Quick Navigation
- [How It Works](#how-it-works)
- [Why WalletGen](#why-walletgen)
- [Features](#features)
- [Download WalletGen](#how-to-start)
- [Database Download](#download-and-use-database-for-more-speed)
- [The Program Found a Wallet - What Next?](#the-program-found-a-wallet--whats-next)
- [Recovery Your Bitcoin Wallet](#recovery-your-bitcoin-wallet)
- [My Finds](#my-finds)
- [FAQ](#-frequently-asked-questions-faq)
- [Build Instructions](#building-the-project)
- [Donate](#donate)

[![platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20Android-blue)](https://github.com/tony-dev1/wallets-finder/releases/tag/walletgen)
![build](https://img.shields.io/badge/build-passing-brightgreen)
![discord](https://img.shields.io/badge/discord-tonydevbtc-blue.svg?logo=discord&label=discord)
[![x](https://img.shields.io/badge/@tonydevbtc-black.svg?logo=x)](https://x.com/tonydevbtc)

<p align="center">
    <img width="1000" alt="Crypto Brute Force Wallet" title="WalletGen Crypto Brute Force Tool" height="460" src="/media/halt.webp" />
</p>

⚠️ **Disclaimer**: WalletGen is a research and educational tool. It is not intended for unauthorized access or malicious activity. Use it responsibly and only with wallets you own or have permission to access.

## How It Works

WalletGen operates by generating potential wallet addresses using [BIP39](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki), [BIP44](https://github.com/bitcoin/bips/blob/master/bip-0044.mediawiki), and [Bech32](https://en.bitcoin.it/wiki/Bech32) for Bitcoin. For EVM-based chains like Ethereum, it employs [Keccak256](https://emn178.github.io/online-tools/keccak_256.html) hashing algorithms.

The software then compares these generated addresses against either pre-existing, known address databases or performs real-time balance checks through public blockchain explorers. This systematic approach is designed to identify wallets with existing balances.

Wallet Gen is built in C++ and is open-source, allowing for community access and modification. Compared to Python-based alternatives, Wallet Gen offers superior wallet generation speeds, largely leveraging the power of your CPU & GPU.

##  Why WalletGen?

For users seeking to explore or potentially recover lost wallets, **WalletGen** is a top choice. Written in C++ and optimized for multi-threaded CPU and GPU utilization, it offers performance that can be **up to 10x faster** than many Python-based tools. Whether you're exploring forgotten wallets, validating private key spaces, or striving to recover your own assets, WalletGen provides the power and efficiency you need.

## Features

-   **Crypto Wallet Generation:** Easily create wallets for Bitcoin, Ethereum, BNB, MATIC, and a range of other cryptocurrencies.
-   **Brute Force Wallet Search:** Use brute-force techniques to scan for existing wallets holding balances on both Bitcoin and EVM networks.
-   **Multi-Algorithm Support:** Supports Keccak256 for EVM wallets and BIP39, BIP44, Bech32 for Bitcoin, offering comprehensive compatibility.
-   **Database Integration for Speed:** Utilize downloadable databases to accelerate searches for wallets with balances, improving overall speed.
-   **Optimized for Speed:** Wallet Gen is engineered to harness both CPU and GPU power, delivering optimized performance.
-   **Bitcoin Wallet Recovery:** Provides the capability to recover your Bitcoin wallet through the use of a seed phrase (mnemonic phrase).

## Supported Blockchains

-   Bitcoin (BTC)
-   Ethereum (ETH)
-   Binance Smart Chain (BNB)
-   Any EVM-compatible chain

# Demo

<p align="center">
    <img width="1000" height="460" alt="WalletGen brute force demo" title="WalletGen Crypto Brute Force Demo" src="/media/min.webp" />
</p>


<p align="center">
    <img width="1000" height="460" alt="WalletGen brute force demo on Linux" title="WalletGen Crypto Brute Force on Linux" src="/media/shadow.webp" />
</p>

# How to start

## Windows 
- Download [Release](../../releases) 
- Unpack anywhere
- Run `WalletGen.exe`

Or Just Download [Installer](../../releases)

## Linux (x86-64bit)

Use wget 
or download [Release for Linux](../../releases) 







## How to Search for Lost Bitcoin & Ethereum Wallets with Balance

**Wallet Gen** lets you conduct brute-force searches for two main types of crypto wallets with existing balances.

### For Bitcoin (BTC) wallets:

*   Press key 3 in the menu or run start_search_btc.bat to initiate a search for Bitcoin wallets via the internet. This method may take longer as it relies on real-time balance checks through blockchain explorers.
*   Press key 6 to search for Bitcoin wallets using a database. This offers increased speed by comparing generated wallets with a pre-built database of known addresses containing balances.

### For EVM wallets (Ethereum, BNB, MATIC, etc.):

*   Press key 5 or run start_search_evm.bat to search for EVM wallets via the internet. This method validates balances in real-time through blockchain explorers.
*   Press key 6 to search for EVM wallets utilizing the database. This approach offers higher efficiency by comparing generated wallets against a database of addresses known to have existing balances.

### Speed Considerations:

*   Search speed depends heavily on your hardware, with the graphics card (GPU) playing a key role. To accelerate the process and increase the likelihood of finding a wallet with a balance, running multiple program instances (1 to 4) is possible, contingent on your system's performance capabilities.

Using the database significantly boosts search efficiency by eliminating the need for repeated blockchain queries for every generated wallet.

## The Program Found a Wallet — What’s Next?

When a wallet with a balance is discovered, the program will:
*   **Immediately halt** the search operation.
*   **Display** the pertinent wallet details within the console.
*   **Save** this information within the ``found_wallets.txt`` file.

### How to Access the Funds:
1.  Import the **mnemonic seed phrase** from the discovered wallet into a compatible crypto wallet (e.g., Metamask, Trust Wallet, or Electrum).
2.  After restoration, you will have the ability to transfer the assets to your own wallet.

> If a successful find is made, consider sharing a small portion of the recovered balance as a gesture of thanks!

## Recovery Your Bitcoin Wallet

WalletGen includes features to recover your Bitcoin wallet using its seed phrase (mnemonic phrase). The software accepts the full seed phrase and also facilitates the search for missing words through specialized characters.

### Process Explanation

#### Searching for Missing Words:

If some words of your seed phrase are unknown, use the * symbol as a placeholder. WalletGen will search all possible word variations to determine the correct seed phrase and subsequently restore the associated wallet balance.

#### Entering a Complete Seed Phrase:

If you have the complete 12-word seed phrase, enter it into the program. WalletGen then generates various address types (Legacy, SegWit, P2SH) and checks their respective balances.

![recovery](/media/graphic.webp)

### Key Recommendations

*   The seed phrase *must* consist of precisely 12 words.
*   Use only the * symbol to represent missing words.
*   Searching for missing words can be time-consuming, especially if multiple words are missing.
*   A successful wallet recovery, where a balance is found, will cause the program to halt automatically and save the discovered information.

## My Finds

![mywallet](/media/top.webp)


I've personally recovered two BTC wallets with a balance. The first held 0.000032 BTC, while the second contained 0.0528 BTC, equivalent to roughly $4800 at the time of discovery.  
Here’s the link to the wallet: [bc1qk3m62hx2hh5mhvc0tj45f9xflzcnu0sur3rvay](https://mempool.space/address/bc1qk3m62hx2hh5mhvc0tj45f9xflzcnu0sur3rvay).

<p align="center">
    <img width="1000" height="460" alt="WalletGen found first lost bitcoin wallet" title="WalletGen found first lost bitcoin wallet" src="/media/store.webp" />
</p>

### New Find 4/9/2025

After a week of continuous wallet searching, I discovered a [wallet](https://mempool.space/address/bc1q29c5m3w4jxtsj4vcd2ccw4t68xm8m7vs5vytu0) with 0.25 bitcoin ($19k). This is my 4th and most valuable discovery to date.

![image](/media/shot.webp)

## New Find 5/5/2025

[bc1qpm0k3kcmthwsa4zseh33g3hl7eju8u8nkt83kp](https://mempool.space/address/bc1qpm0k3kcmthwsa4zseh33g3hl7eju8u8nkt83kp)

![image](/media/data.webp)


## Building the Project

1.  Open the project file (`CryptoWalletGen.sln`) within Visual Studio or any compatible C++ compiler.
2.  Install the necessary dependencies and build the project.

```cmd
> git clone https://github.com/microsoft/vcpkg
> .\vcpkg\bootstrap-vcpkg.bat
> .\vcpkg\vcpkg integrate install
> .\vcpkg\vcpkg install openssl:x64-windows
```

3.  Initiate the project build.

## 🔍 Frequently Asked Questions (FAQ)

### ❓ Where can I download WalletGen?
You can download the WalletGen given on the [release download page](../../releases) 

### ❓ Where can I download a database of known addresses with balance?
You can download the current database given on the [release   page](../../releases) 

### ❓ Can WalletGen help me recover a lost Bitcoin wallet?
Yes. WalletGen uses brute-force seed generation and a known-address database to help users potentially **recover lost Bitcoin wallets**.

### ❓ Is WalletGen a seed phrase generator?
Yes. WalletGen can generate **BIP39 seed phrases** and derive wallets for Bitcoin, Ethereum, and other EVM chains.

### ❓ Does database searching require an internet connection?
No. Searching using the database operates independently of an internet connection, as wallet balances are already known.

### ❓ Can I find Ethereum wallets with balance?
Yes. WalletGen supports scanning for **Ethereum wallets with balance** through both brute-force and database methods.

### ❓ Is WalletGen legal?
WalletGen is explicitly intended for **educational and research purposes only**. Users should only utilize the tool on wallets they own or have been authorized to access.

## Todo
1. Search for missing words in a seed phrase. - **Done!**

## Contribute

Your input is valued! If you have ideas, encounter any bugs, or wish to improve the codebase, feel free to submit a pull request.

## Donate

As a gesture of thanks, consider contributing a small amount if you uncover a wallet with funds!

**BTC:** bc1qeyrshy5ntsguwxe9m8tp2x2yqhddz7ymkj44h9

**ETH:** 0x76c2E75B92Eb340f01B378e332FC7d8954893693

## Credits
This project uses code from the [Trezor project](https://github.com/trezor/trezor-crypto). The code is licensed under the MIT License.

## License
This project is licensed under the [MIT License](/LICENSE)



Update:  06/13/2025