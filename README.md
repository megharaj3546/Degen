# GameSubscription Smart Contract 

## Overview

The GameSubscription smart contract is an Ethereum-based ERC-20 token that facilitates a game subscription system. Users can acquire different subscription levels (BASIC, PREMIUM, VIP) by redeeming tokens, and they are rewarded with additional tokens for each subscription redeemed. The smart contract also allows users to claim their earned rewards and transfer subscription tokens to other users.

## Features

1. *Subscription Levels:* Three subscription levels are available: BASIC, PREMIUM, and VIP.

2. *Token Minting and Burning:* The contract owner can mint new tokens and destroy existing ones.

3. *Redeem Subscriptions:* Users can redeem subscriptions by burning an amount of tokens corresponding to the desired subscription level.

4. *Reward System:* Users receive rewards for each subscription redeemed. Rewards can be claimed and transferred to the user's balance.

5. *Transfer Subscription Tokens:* The contract owner can transfer subscription tokens to other users.

## Contract Structure

- *ERC-20 Token:* The contract inherits from the OpenZeppelin ERC-20 implementation, providing standard token functionalities.

- *Ownable:* The contract is owned, and certain functions can only be executed by the owner.

- *Subscription Levels:* Enumerated type SubscriptionLevel defines the three subscription levels.

- *Events:*
  - SubscriptionRedeemed: Triggered when a user redeems a subscription.
  - RewardClaimed: Triggered when a user claims their rewards.

- *Mappings:*
  - userSubscriptions: Maps user addresses to their subscription levels.
  - userRewards: Maps user addresses to their accumulated rewards.

- *Constants:*
  - Basic_level, Premium_level, VIP_level: Cost of each subscription level.
  - Reward_Per_Subscription: Reward given for each subscription redeemed.

## Functions

1. **mintTokens(address to, uint256 total)**
   - Only owner can mint new tokens.
   - Mints a specified amount of tokens and assigns them to the specified address.

2. **destroyTokens(uint256 total)**
   - Burns a specified amount of tokens. Can only be called by the token owner.

3. **redeemSubscription(uint8 subscriptionNumber)**
   - Users can redeem a subscription by burning an amount of tokens corresponding to the chosen subscription level.
   - Rewards the user with additional tokens.

4. **claimRewards()**
   - Users can claim their accumulated rewards.

5. **transferSubscriptionTokens(address user, uint256 total)**
   - Only the owner can transfer subscription tokens to another user.

6. **getSubscriptionCost(uint8 subscriptionNumber) -> uint256**
   - Returns the cost of a subscription based on the provided subscription number.

## Usage

1. *Deploy Contract:*
   - Deploy the smart contract to the Ethereum blockchain.

2. *Mint Tokens:*
   - The owner can mint tokens using the mintTokens function.

3. *Redeem Subscriptions:*
   - Users can redeem subscriptions using the redeemSubscription function.

4. *Claim Rewards:*
   - Users can claim their rewards using the claimRewards function.

5. *Transfer Subscription Tokens:*
   - The owner can transfer subscription tokens to other users using the transferSubscriptionTokens function.
## Author

Megharj TS

megharaj25317@gmail.com
