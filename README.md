# Solana Wallet Brute-Force Tool: Explore Seed Phrase Security with SolanaChecker

**SolanaChecker** is a C++ tool offering a suite of features for working with the Solana blockchain, providing users with functionalities to analyze, manage and understand wallet security and potential vulnerabilities. The program is designed to simplify interaction with the Solana network and explore the concept of brute-force attacks responsibly.

<p align="left">
    <img src="/img/output.webp" />
</p>

## Program Features Relevant to Brute-Force Exploration

1.  **Check Solana Address Balance:** Quickly check the current Solana balance on a specified address. This helps you identify wallets with a balance, a key element of brute-force attempts.

<p align="left">
    <img src="/img/sidebar.webp" />
</p>

2.  **Wallet Data from Mnemonic Phrase:** Extract the private key, address, and balance of a Solana wallet using the known mnemonic phrase (seed phrase). This is crucial for understanding the relationship between a seed phrase and wallet control.

<p align="left">
    <img src="/img/line.webp" />
</p>

3.  **Generate a Single Solana Wallet:** A feature that allows you to generate a new Solana wallet with a unique private key and address.

<p align="left">
    <img src="/img/copy.webp" />
</p>

4.  **Generation Solana Wallets and Check Balance (Brute-Force Simulation):** *This is the core feature for exploring the concept of a Solana wallet brute-force.* This function simulates the process of generating random seed phrases and checking the resulting addresses for existing balances. *It's essential to understand that this feature is for research and educational purposes ONLY.* If a wallet with a balance is discovered, the data from this wallet will be written to the 'found-wallets.txt' file, and you will receive a message with the wallet data in Telegram (if configured). *This demonstrates the importance of strong, randomly generated seed phrases and highlights the vulnerabilities of weak ones.*

<p align="left">
    <img src="/img/activity.webp" />
</p>

## Setting up Telegram Notifications (for Simulated Brute-Force Results)

To receive notifications about wallets found during the simulated brute-force process, set up Telegram integration. Enter your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and your [chat_id](https://t.me/getmyid_bot) in the 'telegram-settings.txt' file.

## Getting Started: Download or Build

Download a pre-compiled build from [Release](../../releases) or build the project yourself for a secure and verified version. *Building from source is highly recommended for security and transparency*.

## Building the Project for Security and Trust

Building the project from the source code is highly recommended. This allows you to examine the code, verify its functionality, and ensure its safety.

### Installing Dependencies Using vcpkg:

1.  Install **vcpkg** if you do not have it already.
2.  Add vcpkg to your system PATH.
3.  Install the following dependencies:

    -   Install **OpenSSL**:
        ```bash
        vcpkg install openssl
        ```

    -   Install **nlohmann-json**:
        ```bash
        vcpkg install nlohmann-json
        ```

    -   Install **Crypto++**:
        ```bash
        vcpkg install cryptopp
        ```

    -   Install **libsodium**:
        ```bash
        vcpkg install libsodium
        ```

4.  Build the project using Visual Studio, or another C++ compiler.

### Building via Visual Studio:

1.  Open the project solution in Visual Studio.
2.  Make sure **vcpkg** is correctly integrated with your environment.
3.  Click **Build** -> **Build Solution**.
4.  The executable will be in the `bin` directory.

### Building with Another C++ Compiler:

1.  Ensure all dependencies are installed and available to your compiler.
2.  Compile the project using a command similar to this (adapt as necessary):

    ```bash
    g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
    ```

## Command Line: Using the Brute-Force Feature and Other Functions

Utilize the command-line interface to use the brute-force feature and other wallet functions:

1.  **-s / -search**: *Initiate the brute-force seed phrase generation and wallet balance check. USE ONLY for educational purposes or with explicit permission.*
2.  **-t / -track (ADDRESS)**: Track a specific address (monitor transactions).
3.  **-g / -gen (NUMBER)**: Generate a specified number of Solana wallets.
4.  **-m / -mnemonic (MNEMONIC)**: Display wallet information using a seed phrase.
5.  **-b / -balance (ADDRESS)**: Check the Solana balance of a given address.

## Notes

*   **Use this tool responsibly and ethically.** The brute-force feature is for research and educational purposes only.
*   Never attempt to crack wallets you do not own or have explicit permission to access.
*   All cryptocurrency operations carry inherent risks. Protect your wallets and data.
*   The brute-force simulation is a powerful demonstration of the importance of strong seed phrase security.

## License

This project is licensed under the [MIT License](/LICENSE).

Update: url is back online and functioning