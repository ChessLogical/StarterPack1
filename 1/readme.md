Sha-3-512 (rustc 1.78.0 (9b00956e5 2024-04-29)) 


![1](https://github.com/ChessLogical/StarterPack1/assets/169053333/837f4fcb-19d9-4418-a6de-82a515978a75)



The main.rs file uses the #![windows_subsystem = "windows"] attribute to ensure the application runs without a console window. Without it, the app would open 2 windows, the app 
one and the black console window. 



Prerequisites :
Rust toolchain (preferably the latest stable version). You can install Rust through rustup.
Cargo (comes with rustup installation).
Installation
Clone the repository or download the source code to your local machine.
Navigate to the directory containing the source code.
Build the application by running:

[[cargo build --release]]

The executable will be located in ./target/release/.
Running the Application
To run the application, navigate to the ./target/release/ directory and execute the sha3_hash_app file. This will open the GUI where you can interact with the application to generate SHA3-512 hashes.

How to Use
Input Text: Enter the text for which you want the SHA3-512 hash in the text input box at the top.
Generate Hash: Click the "Generate Hash" button to compute the hash of the input text. The hash will be displayed in the text box below.
Clear: To clear the current input and output, click the "Clear" button.
SHA3-512 Hash Algorithm
Overview
SHA3-512 is part of the Secure Hash Algorithm 3 (SHA-3) family, specified in the FIPS 202 standard by NIST. It produces a 512-bit (64 bytes) hash value. It is designed using the Keccak cryptographic primitive, which is based on a sponge construction.

Properties
Hash Length: 512 bits.
Collision Resistant: It is computationally infeasible to find two different inputs that produce the same hash.
Preimage Resistant: It is computationally infeasible to find any input that hashes to a given output.
Second Preimage Resistant: It is computationally infeasible to find any second input which has the same output as any specified input.
Number of Different Hash Outputs
SHA3-512 can theoretically produce 2^512 different hash outputs. This vast range makes it practically impossible for two different inputs to hash to the same output (collision resistance).

Input Size and Character Limits
Maximum Input Size: The underlying Keccak sponge construction of SHA3 can process input of any size. However, practical limits are set by system memory and processing power.
Character Encoding: The application accepts any UTF-8 encoded text as input. This includes ASCII as a subset. UTF-8 can encode any Unicode character, allowing for a wide range of input characters including emojis, symbols, and characters from various languages.
Security and Usage
SHA3-512 is suitable for various cryptographic applications where high security is required, such as digital signatures and message integrity checks. However, for password hashing or similar applications, purpose-built functions like Argon2, bcrypt, or PBKDF2 are recommended due to their resistance against brute force attacks.

Conclusion
This application provides a straightforward and efficient tool for generating SHA3-512 hashes, leveraging the robust security properties of the SHA3 algorithm to ensure reliable and secure hash values for any given input.
