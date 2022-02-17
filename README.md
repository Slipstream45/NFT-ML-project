## AnimeGogh NFT project
This is a project which attempt to introduce Machine Learning to the world of NFTs.
GA Neural Style Transfer will transfer anime immages into a unique ways which will then be deployed into the blockchain using the contract and other scripts!

Here is the idea implemented on a private wallet using the Ropsten test network:
![image](https://user-images.githubusercontent.com/55631460/154581254-cfeca499-b219-4be1-90ca-fa1f465bbca7.png)

## Parts of the Project

# 1.Contract creation and deploying the NFT contract
The first part is creating the solidity smart contract and writing subsequent test scripts and deploying the same into the Ropstein test network. The contract is using the openzeppelin ERC721 token standard. It uses the Counters.sol to keep track of the NFTs minted and sets the unique ID on the new NFT. The contract also sets up Access Control so only the owner of the NFT can mint the same. Then we have the function to actually mint the NFT. Ropstein faucets can be used to deploy the contract (since it requires some amount of gas). 

# 2. Deploy script and Hard-hat config
Ether.js is used in the Deploy script to interact with Ethereum. Hardhat config contains some important details

# 3. Creating and Training a Neural Style Transfer to generate unique Anime images
Steps are followed from https://www.tensorflow.org/tutorials/generative/style_transfer . Since I am no expert in this subject yet, I followed this tutorial and after adjusting some parameters in the model and adjusting epochs and batch sizes, the model generates a unique image. I used Nino's picture and a sample abstartct background for styling. It turned out to be pretty good. Seems like a water colour painting.
![image](https://user-images.githubusercontent.com/55631460/154582842-259f0e39-8f6b-435f-8c8f-21d773c6c2a1.png)

# 4. Uploading the media and metadata to Pinata
The metadata here desribes attribute properties of the media

# 5. mint.js
Mint.js simple does the tasks of putting everything together i.e it gets the ABI, contract address and setting up the transaction. Here I used alchemy-web3 for this app. THe metadata link should go at the end of the file to associate the media to the token

At the end of the day NFT is just a token like Dogecoin, and others on the network but with some different properties (ERC721). We associate media to it. 
We can extend this project in many ways. Find more efficient ways to generate unique artworks, can or cannot be anime likes, we can also deploy these on the main Ethereum Network and list our NFTs on OpenSeas.
This is just my attempt at bringing these two wonderful technologies togehter and finding out what wonders they can create!
