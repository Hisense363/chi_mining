# Chi Mining $CHI - SUI Network Mining Token

## Overview

Chi ($Chi) is an innovative hybrid project that combines the principles of Proof-of-Work (PoW) coins like Bitcoin with the viral nature of meme coins. It implements a PoW-based token mining system on the SUI network, incorporating a social element through referrals. The goal of this project is to get as many people as possible mining on their devices.

**TerraHash**
TerraHash is a custom Proof-of-Work Algorithm. It utilizes a modified version of the Equix algorithm, designed to be ASIC-resistant and CPU-friendly. The goal being allowing people with everyday devices to mine. We add a Blake2b step on top of Equix to allow for users to "choose their own difficulty" mining on a low powered devices? Choose an easier difficulty. Mining on a powerful rig? Choose a tougher difficulty. This ensures that no one is locked out of rewards.

**Periodic Mining Cycles**: Mining operations occur in defined cycles of 10 minutes with randomly generated seeds, preventing pre-computation attacks and maintaining a level playing field for all participants.

## Token Economics

### Dynamic Emission Rate

Chi implements an innovative, gradually decelerating emission schedule designed to incentivize early adoption while ensuring long-term sustainability.

**Initial Emission:**

- First 24 hours: 1,000,000 WIFI tokens

**Reduction Schedule:**
The emission rate undergoes a series of programmed reductions, following a pattern that balances initial abundance with increasing scarcity:

1. After 24 hours: Reduced to 880,000 tokens per day (88% of initial rate)
2. After 72 hours (Day 3): Further reduced to 774,400 tokens per day (88% of previous rate)
3. After 120 hours (Day 5): Adjusted to 681,472 tokens per day
4. After 192 hours (Day 8): Decreased to 599,695 tokens per day

This pattern continues, with each reduction occurring after a Fibonacci-sequence number of days (1, 2, 3, 5, 8, 13, 21, 34...) and reducing the daily emission to 88% of the previous rate.

**Long-term Trajectory:**
As the intervals between reductions grow exponentially, the emission rate stabilizes gradually. This creates a curve that rapidly decelerates in the early stages but smooths out over time, providing a balanced approach to token distribution.

**Key Features:**

1. Front-loaded Rewards: Higher initial emission rates incentivize early participation and network growth.
2. Progressive Scarcity: The diminishing emission rate may enhance token value over time.
3. Predictable Reductions: While dynamic, the reduction schedule follows a clear pattern, allowing for long-term planning.
4. Sustainable Distribution: The gradually decreasing emission rate helps ensure a prolonged and sustainable token distribution model.

### Referral System

Chi implements a dynamic referral reward system to incentivize network growth:

Miners must have a referrer. All miners are required to pay referral fees according to the following schedule:

- First 3 months (<12960 reward periods): 40% referral fee
- Months 4-6 (<25920 reward periods): 30% referral fee
- Months 7-12 (<51840 reward periods): 20% referral fee
- After 1 year (>51841 reward periods): 10% referral fee

Referral fees are a percentage of your mining rewards and the referral fees paid to you. Fees paid will travel up the tree at a decaying rate.

As an example. You are Alice. You refer Bob. Bob refers Carol. Carol mines 100 tokens. 40 go to Bob. Bob mines 100 tokens. 56 go to Alice. Carol retains 60 tokens. Bob retains 84 tokens, and Alice retains 93.6 tokens assuming they also have a 40% referral fee, or if they refer to the pitmaster, they would retain 78 tokens.

At the top of the tree is the pitmaster. This is not a miner, but rather the end of the referral tree. All miners that refer to the pitmaster must pay a 50% referral fee eternally. There is no fee reduction due to mining consistency, nor does mining consistency credit accumulate. This is to disincentivise referring to the burn account, while also ensuring that no one person sit's at the top collecting rewards.

### Claim Process

In order to reduce gas fees further, a treasury account will be used. This account mints all tokens. After each mining cycle the accounts ledger is updated to reflect rewards owed to miners. The rewards owed can then be claimed whenever the miner decides to collect.

## Goals

1. **Growth**: Incentives designed to get as many people as possible involved
2. **Decentralization**: Encourage a diverse and distributed network of miners.
3. **Efficiency**: While gas cost on SUI are already extraordinarily low, 10 minute reward windows will allow for longevity of mining with minimal startup cost.
4. **Predictability**: Maintain a consistent token emission rate to provide stability and transparency in the token economy.

## Technical Details

- **Language**: Implemented in Move, the smart contract language for the SUI blockchain.
- **Token Standard**: Follows SUI's native token standards for compatibility with wallets and exchanges.
- **Mining Cycles**: Each mining cycle lasts 10 minutes, with rewards distributed at the end of each cycle.
- **Reward Calculation**: Rewards are calculated based on the miner's proven computational effort during each cycle.
- **Supply Growth**: The total token supply increases according to the dynamic emission schedule, with no built-in cap, allowing for continuous mining opportunities.

## Smart Contract Structure

1. `mining_contract.move`: Main contract handling mining logic, reward distribution, and contract state management.
2. `pow.move`: Implements the proof-of-work algorithm and verification.
3. `token.move`: Defines the mineable token and its properties.

## Future Considerations

1. **Periodic Halving Events**: Potential introduction of temporary emission rate reductions to create scarcity and excitement.
2. **Staking Mechanism**: Possibility of allowing WIFI token staking for additional benefits.
3. **Governance Features**: Potential implementation of governance rights for token holders.
4. **Cross-chain Incentives**: Exploration of cross-chain rewards or interoperability features within the SUI ecosystem.

## Getting Started

(Include instructions for setting up the development environment, building the project, and running tests)

## Disclaimer

This project is for educational and experimental purposes. Please be aware of the risks associated with cryptocurrency mining and token systems. Participation in the Chi project is at your own risk.
