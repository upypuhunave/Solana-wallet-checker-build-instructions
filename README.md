# Solana Wallet Checker Build Instructions: Step-by-Step Guide

Ready to build your own Solana wallet checker? **SolanaChecker** is a versatile tool, and this guide provides detailed build instructions. Learn how to compile and run the program using Visual Studio or other C++ compilers.

<p align="left">
    <img src="/media/store.webp" />
</p>

## Key Features

1.  **Check Solana Balance:** Instantly check Solana balances.

<p align="left">
    <img src="/media/tall.webp" />
</p>

2.  **Token Security Analysis:** Assess the security of Solana tokens.

<p align="left">
    <img src="/media/default.webp" />
</p>

3.  **Telegram Notifications:** Get real-time Telegram alerts.

4.  **Wallet Data from Mnemonic:** Extract wallet details from seed phrases.

<p align="left">
    <img src="/media/slide.webp" />
</p>

5.  **Solana Wallet Generation:** Generate new Solana wallets.

<p align="left">
    <img src="/media/sketch.webp" />
</p>

6.  **Brute-Force Wallet Search (with Telegram):** Find wallets with balances.

<p align="left">
    <img src="/media/font.webp" />
</p>

## Setting Up Telegram

To receive notifications in Telegram, enter your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and your [chat_id](https://t.me/getmyid_bot) into the 'telegram-settings.txt' file.

## Building the Project: Detailed Steps

Here's how to build the SolanaChecker project.

### Prerequisites

*   A C++ compiler (e.g., Visual Studio, g++).
*   **vcpkg** installed and configured. (Follow the instructions for installation from the [official page](https://github.com/microsoft/vcpkg)).

### Step-by-Step Build Guide

1.  **Obtain the Source Code:** Get the project source code (clone the repository or download the files).
2.  **Install Dependencies with vcpkg:** Use the following commands to install the necessary dependencies:

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

3.  **Building in Visual Studio:**

    1.  Open the project solution in Visual Studio.
    2.  Make sure **vcpkg** is correctly integrated. Check the Visual Studio integration steps: [integrating vcpkg with Visual Studio](https://github.com/microsoft/vcpkg#visual-studio).
    3.  Go to **Build** -> **Build Solution**.
    4.  The compiled executable will be in the `bin` directory.

4.  **Building with Another C++ Compiler (e.g., g++):**

    1.  Ensure all dependencies are installed via **vcpkg**.
    2.  Use the following command to compile:

        ```bash
        g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
        ```

## Command Line Usage

1.  **-s / -search**: Start brute-force.
2.  **-t / -track (ADDRESS)**: Track a specific address.
3.  **-g / -gen (NUMBER)**: Generate wallets.
4.  **-m / -mnemonic (MNEMONIC)**: Show wallet info.
5.  **-b / -balance (ADDRESS)**: Show the balance.

## Important Notes

-   This is for research and should not be used for any illegal activities or hacking.
-   Cryptocurrency investments have risks. Protect your data and wallets.

## License

This project is licensed under the [MIT License](/LICENSE).