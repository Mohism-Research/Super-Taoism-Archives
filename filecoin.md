FIL Economics
The future of data storage
Filecoin (FIL) serves as the native asset to the Filecoin blockchain and powers the data storage and data retrieval markets, which form the core of the Filecoin project. Economic incentives and disincentives are baked into the blockchain to produce the optimal number of storage and retrieval miners providing honest service to clients. The FIL supply is capped at 2 billion and will be released through block rewards over the subsequent decades.

Token allocation
70%
to Filecoin Miners
Mining block reward
For providing data storage service, maintaining the blockchain, distributing data, running contracts, and more.  
15%
to Protocol Labs
Genesis allocation, 6-year linear vesting
For research, engineering, deployment, business development, marketing, distribution, and more.  
10%
to Investors
Genesis allocation, 6 month to 3 year linear vesting
For funding network development, business development, partnerships, support, and more.  
5%
to Filecoin Foundation
Genesis allocation, 6-year linear vesting
For long-term network governance, partner support, academic grants, public works, community building, etc


December 10, 2020

## Understanding Filecoin Circulating Supply

![Understanding Filecoin Circulating Supply](https://filecoin.io/vintage/images/blog/filecoin-circulating-supply-header.jpg)



This blog post aims to unpack how Filecoin tokens enter circulating supply, provide more insights on how various stakeholders take part in its economy, and shed light on how one should approach and think about Filecoin token economics. This post should be paired by reading the paper on [Filecoin’s Economy](https://filecoin.io/2020-engineering-filecoins-economy-en.pdf) and the detailed mechanisms outlined in the [Filecoin Spec](https://spec.filecoin.io/#).

### The Filecoin Ecosystem

The growing momentum in the Filecoin ecosystem is a primary driver of use cases, tooling, and infrastructure for all Filecoin stakeholders. Since the [release of Filecoin’s mainnet](https://filecoin.io/blog/journey-to-liftoff/) on October 15th, 2020, the network has now surpassed a number of important milestones:

- The network exceeding 1EiB of storage capacity from 700+ miners
- An ecosystem of 90+ projects building applications, developer tooling and infrastructure on the network
- 200+ new projects entering the ecosystem through [Hackathons and Accelerators](https://ignite.fil.events/)
- Over 5400 developers contributing to the project’s GitHub repos
- Development of a number of use cases, including [Consumer Storage Apps](https://slate.host/), [Archival Storage](https://store.filecoin-discover.com/), [DeFi](https://codefi.consensys.net/blog/consensys-codefi-to-launch-a-filecoin-defi-bridge-and-storage-market), [Decentralized Video](https://file.video/), and many others

For more, here’s a deep dive on the state of the [Filecoin Ecosystem](https://www.youtube.com/watch?v=FHqtIX4FPP4) from Liftoff Week or a recent [recap of the network](https://filecoin.io/blog/journey-to-liftoff/) from October 2020.

### Filecoin as a Utility Token

Filecoin is a utility token that is meant to be used, giving token holders a right to use the network. One can think of Filecoin as an [Island Economy](https://filecoin.io/2020-engineering-filecoins-economy-en.pdf) where participants come together to produce valuable storage goods and services and export them to the world. On the network, one should expect to see storage providers with their own unique characteristics, smart contracts systems, lending services, a diverse set of use cases and many more. Each of these could become their own unique business. The utility of the network is reflected in the attractiveness of those goods and services that participants produce in the network.

The overarching goal for the whole economy, across miners, developers, researchers, clients, and token holders is to efficiently produce attractive storage-related goods and services that can be exported to the outside world. An economy producing more valuable goods more efficiently will lead to more demand for the goods and more demand for the networkʼs token. An increase in the purchasing power of the participants within the economy will allow them to expand and improve their operations to provide an even better, cheaper service to the world.

![Filecoin Participants](https://filecoin.io/vintage/images/blog/filecoin-circulating-supply-participants.png)

### Token Minting: Aligning the Miner Minting Curve with Network Utility

As a utility token that aligns participants’ incentives with the long-term goal and vision of the network, Filecoin minting is aligned with the overall provable utility of the network. This means that the majority of Filecoin supply would only be minted if the network achieved some ambitious growth and utility targets.

Unlike most other blockchain networks, Filecoin has innovatively adopted a [dual minting model](https://spec.filecoin.io/#section-systems.filecoin_token.minting_model): Simple and Baseline:

- **Baseline Minting**: Upto 770M FIL tokens, the majority of the Storage Mining Allocation, is minted based on the performance of the network. This creates a strong incentive for the network to collaborate to reach storage capacity targets that would ultimately store a large share of humanity’s most important information. The full release of these tokens would only occur if the Filecoin network reached a Yottabyte of storage capacity in under 20 years. According to some analysts, there is less than a Zettabyte of data stored in data centers today (although growing rapidly), so this goal is 1000x larger than today’s cloud storage estimates.
- **Simple Minting**: 330M FIL tokens are released on a 6 year half-life based on time. A 6 year half life means that 97% of these tokens will be released in approximately 30 years time. This small but meaningful amount is minted independent of agent actions to provide counter pressure to shocks.
- **Mining Reserve**: 300M FIL tokens is held back in reserve to incentivize future types of mining. It will be up to the community to decide how these tokens would be released and which sets of stakeholders should be incentivized, but for now this portion of total supply is held back in reserve.

As such, effective token minting from mining is in the hands of the community and falls anywhere between the two lines in Figure 1. Figure 2 provides a sense of how much the network needs to grow to hit maximum minting. While the community may come together to update the baseline of the network, hitting the baseline requires competitive collaboration among all stakeholders, researchers, miners, developers, token holders, ecosystem partners, and storage clients.

![img](https://filecoin.io/vintage/images/blog/filecoin-circulating-supply-minting.png)Figure 1: Maximum and Minimum Minting from Storage Mining.

![img](https://filecoin.io/vintage/images/blog/filecoin-circulating-supply-baseline.png)Figure 2: Network Storage Baseline for Max Baseline Minting on Log Scale.

More information can be found in the Filecoin spec.

### Token Vesting: Aligning Stakeholders with Long-Term Behavior

Another core principle and mechanism that incentivizes long-term alignment, steers participants away from short-term speculation, and encourages all stakeholders to work together to make the Filecoin network more useful in the long-term includes stakeholder vesting.

This applies to each of Filecoin’s core stakeholders, including:

1. **Mining Rewards**. All mining rewards undergo [some form of vesting](https://spec.filecoin.io/#section-systems.filecoin_mining.miner_collaterals.block-reward-collateral) to encourage long term network alignment. For example, 75% of block rewards earned by miners vest linearly over 180 days while 25% are made immediately available to improve miner cash flow and profitability. Of course, all earned rewards are subject to slashing throughout the lifetime of a sector as described below. Unreliable storage reduces the utility of the network and hence block rewards earned by these sectors will be slashed and burned.

2. SAFT Investors

   . All SAFT holders received their FIL subject to 6 month, 1 year, 2 year, and 3 year linear vesting terms beginning at network launch. The majority of SAFT tokens purchased are vesting linearly over 3 years:

   - 58% of SAFT tokens vest linearly over 3 Years
   - 5% of SAFTs tokens vest linearly over 2 Years
   - 15% of SAFTs tokens vest linearly over 1 Years
   - 22% of SAFTs tokens vest linearly over 6 Months

3. **Filecoin Foundation**. The Filecoin Foundation’s 100M FIL vest linearly over 6 years, beginning at network launch.

4. **Protocol Labs**. Protocol Labs’s 300M FIL vest linearly over 6 years, beginning at network launch. When Protocol Labs encourages ecosystem development through grants with important collaborators, those also typically vest over 6 years

These long-term vesting schedules for token holders help ensure that participants have skin-in-the-game, and take long-term views with respect to their actions on the network.

### Collateral and Slashing: Aligning Participants with Reliable Storage

Blockchain networks like Filecoin incentivize good behavior with rewards and penalize bad behavior with penalties. The penalties – called **slashing** – come from collaterals participants must post, or potential rewards participants might have earned. Filecoin has many such mechanisms in order to incentivize high quality, reliable, long-term storage.

From providing storage capacity to the network to meeting storage demand of clients, miners must lock Filecoin tokens for consensus security, storage reliability, and contract guarantees. Filecoin tokens are locked as [pledge collateral](https://spec.filecoin.io/#section-systems.filecoin_mining.miner_collaterals.initial-pledge-collateral) to bring storage supply to the network and required as [deal collateral and payment](https://spec.filecoin.io/#section-systems.filecoin_mining.miner_collaterals.storage-deal-collateral) to meet storage demand.

Naturally, the amount of Filecoin tokens that are locked in collateral and slashed for misbehavior is in the hands of the community:

- On a network level, the amount of pledge collateral locked depends on the amount of storage capacity committed onto the network and the network’s circulating supply at the time of commitment. On an individual level, pledge collateral is determined by projected block rewards that a miner will earn to ensure that pledge collateral is not too prohibitive. There will always be Filecoin tokens locked at any point in time as long as there is storage on Filecoin.
- The amount of tokens locked for deal collateral and payment is the result of a collective effort by all participants in making storage goods and services on Filecoin more attractive.
- Collateral and all earned rewards by miners are subject to slashing throughout the lifetime of a sector. Unreliable storage reduces the utility of the network and hence block rewards earned by these sectors will be [slashed and burned](https://spec.filecoin.io/#section-systems.filecoin_mining.sector.sector-faults).

### Filecoin Plus: Aligning Participants with Useful Storage

Filecoin is a global marketplace enabled by blockchain technologies. Without a reliable way to algorithmically distinguish real useful data from generated randomness, the Filecoin Network innovatively and pragmatically introduced a layer of social trust on top of the technical layer, [Filecoin Plus](https://github.com/filecoin-project/FIPs/blob/master/FIPS/fip-0003.md). Filecoin Plus puts power in the hands of the storage clients as miners storing deals from these clients, who are notarized by a network of notaries, gain a 10x advantage in storage power and hence 10x their share of the network’s block reward.

This mechanism incentivizes all participants to invest in business development, recruit useful data and use cases, and make Filecoin more useful. When a miner earns 10x the share of the block reward, they are also required to put up 10x the collateral with 10x the penalty to ensure that the incentives are aligned. This is also a big step forward in community governance and decentralized cryptoeconomics as operations and processes are being shaped by the community in [public](https://github.com/filecoin-project/notary-governance).

### Network Transaction Fee: Aligning Token Supply with Network Usage

As long as there is any action or utility on the network, Filecoin tokens will be [consumed](https://filecoin.io/blog/filecoin-features-gas-fees/) to compensate for the computation and storage resources on-chain messages consume. Similar to the rate of token minting for miners, the rate of token consumption is also in the hands of the community, as participants compete for on-chain resources.

As of today, Filecoin daily token consumption has climbed as high as 180k FIL per day, which is a sign of a thriving economy.

### Conclusion

The economic mechanisms embedded in the Filecoin protocol ensure that network activities and stakeholders are fully aligned with the long-term health of the network. Mechanisms such as variable minting based on network growth, vesting structures, token consumption, collateral requirements and more align participant incentives and motivations with the long-term success of the network.

Making Web3 mainstream requires the efforts of all ecosystem participants. The incentives of the Filecoin protocol have to balance the interests of all stakeholders, storage clients, miners, developers, token holders, and ecosystem partners. A thriving economy benefits everyone in the network and aligns the long-term incentives of all participants. And most importantly, the future of Filecoin lies in the hands of all its community.



------



### *Addendum: Mechanical Definitions of Circulating Supply*

The blog post above details some of the mechanisms to model circulating supply. This addendum outlines two different mechanical calculations of circulating supply used in PL’s APIs.

#### API #1: Filecoin Protocol Definition

The reference implementation of the Filecoin protocol ([Lotus](http://github.com/filecoin-project/lotus)) exposes an API call for the current network circulating supply: [StateCirculatingSupply](https://github.com/filecoin-project/lotus/blob/2d3b61675b93b977b299eae29945599c26f38cd2/api/api_full.go#L411). This API call returns the circulating supply as a result of subtracting total token outflows from total token inflows. Total token inflows include mining rewards, vested SAFT tokens, disbursed Mining Reserve, and vested tokens originally owned by the Filecoin Foundation and Protocol Labs. Total token outflows include tokens programmatically locked on chain or programmatically burned that are not transferable at the time of invocation. For example, collateral, locked block rewards, not-yet-vested tokens, etc are not included in this calculation. This API is used by a variety of community members, including various Filecoin block explorers.

#### API #2: Used by Cryptocurrency Price and Market Capitalization Websites

Many cryptocurrency price and market capitalization tracking websites use their own specific definitions for circulating supply to keep comparisons across projects as standardized as possible. This sometimes diverges from the circulating supply definition used by a particular network. For example, websites like [CoinMarketCap](https://support.coinmarketcap.com/hc/en-us/articles/360043396252-Supply-Circulating-Total-Max-) and [CoinGecko](https://www.coingecko.com/en/glossary/circulating-supply) consider vested tokens by the project teams (e.g. Filecoin Foundation, Protocol Labs, and project team members) to be part of the circulating supply only when those tokens have moved from their original wallets.

While Filecoin had implemented only API #1 at launch, the network is implementing a second API (“API #2”) to accommodate the definition used by these cryptocurrency price and market capitalization tracking websites. To reiterate the difference, API #1 *includes* all vested tokens from the Filecoin Foundation, Protocol Labs, and project team members in circulating supply and API #2 *excludes* those tokens until they leave their original wallets at which point they become part of the circulating supply. As such, the Filecoin circulating supply as defined by cryptocurrency price and market capitalization websites may sometimes be lower than what the native Filecoin Protocol API returns.

As of December 14, 2020, API #1 yields a circulating supply of 54M FIL while API #2 would yield 31M FIL. Certain cryptocurrency price and market capitalization tracking websites had previously used Filecoin’s API #1 formula, and will in the future switch to using API #2 with a different formula. In order to ensure a smooth transition as those websites switch from the first formula to the second formula, we have paused the circulating supply figure on the API that those particular websites are using (at around 44 million FIL) until the number calculated for API #2 reaches that number, at which point those websites will use the API #2 formula going forward.

Members of the community may use each of the different APIs / formulas for calculating circulating supply for particular purposes. For example, Lotus will use API #1 in order to execute various protocol level calculations. Other cryptoasset tracking websites will use API #2 in order to ensure comparability against the calculations used to calculate circulating supply for other crypto networks. Both options will be freely available for the community to leverage and use.
