# Blockchain & RSA Cryptography Simulator

A Python-based educational project demonstrating blockchain technology and RSA encryption with interactive GUI interfaces.

## 📋 Overview

This project consists of two main components:

1. **Blockchain Simulator** - A functional blockchain implementation with digital signatures and transaction verification
2. **RSA Encryption Tool** - An interactive demonstration of RSA public-key cryptography

## 🎯 Features

### Blockchain Simulator
- **Genesis Block Creation** - Initialize the blockchain with a genesis block
- **Digital Signatures** - RSA-based signing and verification for blocks and transactions
- **Multi-Node Support** - Simulate multiple authority nodes with their own key pairs
- **Transaction Management** - Create, sign, and verify transactions between users
- **Block Mining** - Authority nodes can mine blocks containing pending transactions
- **Chain Validation** - Verify the integrity of the entire blockchain
- **Tamper Detection** - Demonstrates how blockchain detects unauthorized modifications
- **GUI Interface** - User-friendly Tkinter interface for all operations

### RSA Encryption Tool
- **Key Generation** - Automatically generate RSA public/private key pairs
- **Message Encryption** - Encrypt messages using public keys
- **Message Decryption** - Decrypt messages using private keys
- **Custom Keys** - Option to input custom public keys for encryption
- **Dual Interface** - Sender and Receiver panels to simulate communication
- **Visual Feedback** - Real-time display of encrypted and decrypted messages

## 🚀 Getting Started

### Prerequisites

```bash
# Python 3.x
# Required libraries:
pip install pycryptodome
```

### Running the Applications

**Blockchain Simulator:**
```bash
python blockchain_gui.py
```

**RSA Encryption Tool:**
```bash
python GUI.py
```

## 🔧 How It Works

### Blockchain

The blockchain implementation uses:

1. **RSA Key Pairs** - Each node has a public/private key pair for signing
2. **SHA-256 Hashing** - Blocks are hashed to create immutable links
3. **Digital Signatures** - Transactions and blocks are signed using PKCS1_v1_5
4. **Chain Validation** - Each block references the previous block's hash

**Block Structure:**
- Index
- Creator's public key
- Previous block hash
- Timestamp
- Transaction data
- Digital signature

**Transaction Structure:**
- Sender address (public key)
- Recipient address
- Amount
- Timestamp
- Digital signature

### RSA Encryption

The RSA implementation includes:

1. **Prime Generation** - Generates large prime numbers (p, q)
2. **Key Calculation** - Computes n (p × q) and φ(n)
3. **Public Key** - (e, n) where e is coprime to φ(n)
4. **Private Key** - (d, n) where (e × d) mod φ(n) = 1
5. **Encryption** - message^e mod n
6. **Decryption** - ciphertext^d mod n

## 💡 Usage Examples

### Blockchain Operations

1. **Create Genesis Block** - Start a new blockchain
2. **Select a Node** - Choose which node to operate as
3. **Create Transaction** - Send units between addresses
4. **Verify Transaction** - Check transaction validity
5. **Mine Block** - Package pending transactions into a block
6. **Verify Blockchain** - Ensure chain integrity

### RSA Encryption Flow

1. **Generate Key Pair** - Create public/private keys for both sender and receiver
2. **Sender Side:**
   - Enter a message
   - Encrypt using recipient's public key
   - Send encrypted message
3. **Receiver Side:**
   - Receive encrypted message
   - Decrypt using private key
   - View original message

