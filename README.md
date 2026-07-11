# NFT Marketplace

## Overview
This project is a full-stack decentralized application (dApp) designed for creating, listing, and trading Non-Fungible Tokens (NFTs) on a blockchain. It showcases expertise in smart contract development and integration with contemporary web technologies.

## Features
- **NFT Creation**: Users can mint new NFTs.
- **NFT Listing**: Functionality to list NFTs for sale on the marketplace.
- **NFT Trading**: Enables users to buy and sell NFTs.
- **Creator Dashboard**: A dedicated dashboard for creators to manage their minted and listed NFTs.
- **Asset Management**: Users can view and manage their owned NFT assets.

## Tech Stack

![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Hardhat](https://img.shields.io/badge/Hardhat-24272B?style=for-the-badge&logo=hardhat&logoColor=white)
![Solidity](https://img.shields.io/badge/Solidity-363636?style=for-the-badge&logo=solidity&logoColor=white)
![Ethers.js](https://img.shields.io/badge/Ethers.js-24272B?style=for-the-badge&logo=Ethers.js&logoColor=white)
![IPFS](https://img.shields.io/badge/IPFS-65C1FF?style=for-the-badge&logo=ipfs&logoColor=white)


## Setup
1.  **Clone the repository**:
    ```bash
    git clone [repository-url]
    cd nft-market
    ```
2.  **Install dependencies**:
    ```bash
    npm install
    # or yarn install
    ```
3.  **Configure Hardhat**: Ensure `hardhat.config.js` is set up correctly for your desired network.
4.  **Compile Smart Contracts**:
    ```bash
    npx hardhat compile
    ```
5.  **Deploy Smart Contracts**: Deploy `NFT.sol` and `NFTMarket.sol` to your blockchain network using Hardhat. Update `config.js` with the deployed contract addresses.
    ```bash
    npx hardhat run scripts/deploy.js --network [your-network]
    ```
6.  **Run the Next.js application**:
    ```bash
    npm run dev
    # or yarn dev
    ```
    The application will be accessible at `http://localhost:3000`.

## Usage
1.  **Connect Wallet**: On the dApp interface, connect your Web3 wallet (e.g., MetaMask) via Web3Modal.
2.  **Create NFT**: Navigate to the 'Create Item' section to mint a new NFT, providing details such as name, description, and an image (uploaded to IPFS).
3.  **List NFT**: After creation, you can list your NFT for sale on the marketplace by specifying a price.
4.  **Browse and Buy**: Explore listed NFTs on the main page (`index.js`) and purchase them directly from other users.
5.  **Manage Assets**: View your owned NFTs in 'My Assets' and track your created NFTs and sales in the 'Creator Dashboard'.

## Project Structure
.|
├── components/                  # Reusable UI components
│   ├── ...
├── contracts/                   # Solidity smart contracts
│   ├── NFT.sol
│   ├── NFTMarket.sol
├── pages/                       # Next.js pages/routes
│   ├── _app.js                  # Custom App component
│   ├── create-item.js           # NFT creation page
│   ├── creator-dashboard.js     # Creator's dashboard
│   ├── index.js                 # Main marketplace page
│   ├── my-assets.js             # User's owned assets page
│   ├── api/                     # API routes (if any)
├── public/                      # Static assets
│   ├── manifest.json
│   ├── robots.txt
├── scripts/                     # Hardhat deployment scripts
│   ├── deploy.js
├── styles/                      # Tailwind CSS and global styles
│   ├── main.css
├── test/                        # Smart contract tests
│   ├── ...
├── hardhat.config.js            # Hardhat configuration
├── next.config.js               # Next.js configuration
├── package.json                 # Project dependencies and scripts
├── postcss.config.js            # PostCSS configuration
├── tailwind.config.js           # Tailwind CSS configuration
└── config.js                    # Frontend configuration (contract addresses, etc.)

## Interview Questions
1.  Explain the interaction flow between the `NFTMarket.sol` and `NFT.sol` smart contracts during the lifecycle of an NFT, from creation to sale. How do they work together to ensure ownership and transfer?
2.  This project utilizes IPFS for storing NFT metadata and images. Discuss the advantages of using IPFS over centralized storage solutions for a dApp like an NFT marketplace, and outline any potential challenges or considerations.
3.  Describe how `Ethers.js` and `Web3Modal` are integrated into the Next.js frontend to enable wallet connection and smart contract interactions. What are the key functionalities each library provides in this context?
