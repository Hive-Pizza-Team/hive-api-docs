      API Docs                       {"@context":"https://schema.org","@type":"WebSite","description":"Hive Developer Documentation.","headline":"titles.home","name":"Hive Developers","url":"https://developers.hive.io/"}

[![Hive Developers logo](/images/logotype_black.svg)](/)
========================================================

 

###### Introduction

*   [Intro to Hive](/#introduction-welcome)
*   [Web2 vs Web3](/#introduction-web3)
*   [Developer workflow](/#introduction-workflow)

###### Getting started

*   [Hive Nodes](/quickstart/#quickstart-hive-full-nodes)
*   [Hive Testnet](/quickstart/#quickstart-testnet)
*   [Accounts](/quickstart/#quickstart-accounts)
*   [Authentication](/quickstart/#quickstart-authentication)
*   [SDK Libraries](/quickstart/#quickstart-choose-library)
*   [Get and Set](/quickstart/#quickstart-fetch-broadcast)

###### JSON-RPC API

*   [Account By Key API](/apidefinitions/#apidefinitions-account-by-key-api)
*   [Account history API](/apidefinitions/#apidefinitions-account-history-api)
*   [Block API](/apidefinitions/#apidefinitions-block-api)
*   [Bridge](/apidefinitions/#apidefinitions-bridge)
*   [Condenser API](/apidefinitions/#apidefinitions-condenser-api)
*   [Database API](/apidefinitions/#apidefinitions-database-api)
*   [Debug Node API](/apidefinitions/#apidefinitions-debug-node-api)
*   [Follow API](/apidefinitions/#apidefinitions-follow-api)
*   [JSON RPC](/apidefinitions/#apidefinitions-jsonrpc)
*   [Market History API](/apidefinitions/#apidefinitions-market-history-api)
*   [Network Broadcast API](/apidefinitions/#apidefinitions-network-broadcast-api)
*   [RC API](/apidefinitions/#apidefinitions-rc-api)
*   [Reputation API](/apidefinitions/#apidefinitions-reputation-api)
*   [Rewards API](/apidefinitions/#apidefinitions-rewards-api)
*   [Tags API](/apidefinitions/#apidefinitions-tags-api)
*   [Transaction Status API](/apidefinitions/#apidefinitions-transaction-status-api)
*   [Wallet Bridge API](/apidefinitions/#apidefinitions-wallet-bridge-api)
*   [Witness API](/apidefinitions/#apidefinitions-witness-api)
*   [Broadcast OPS](/apidefinitions/#apidefinitions-broadcast-ops)
*   [Broadcast OPS Custom](/apidefinitions/#apidefinitions-broadcast-ops-customs)

###### Tutorials

*   [Recipes](/tutorials/#tutorials-recipes)
*   [Javascript](/tutorials/#tutorials-javascript)
*   [Python](/tutorials/#tutorials-python)
*   [PHP](/tutorials/#tutorials-php)
*   [Ruby](/tutorials/#tutorials-ruby)

###### Opportunities

*   [Hive Fund](/services/#services-dhf)
*   [Hive Hackathons](/services/#services-hackathon)
*   [Condenser](/services/#services-hive-blog)
*   [Vision](/services/#services-ecency-com)
*   [ImageHoster](/services/#services-imagehoster)
*   [VideoHoster](/services/#services-videohoster)

[

###### Node Setup

](/nodeop/)

###### Layer 2

*   [Hive Engine](/layer2/#layer2-engine)
*   [HoneyComb](/layer2/#layer2-honeycomb)
*   [VSC](/layer2/#layer2-vsc)

###### Resources

*   [Overview](/resources/#resources-overview)
*   [Whitepaper](/resources/#resources-whitepaper)
*   [Hivesigner](/resources/#resources-hivesigner)
*   [HiveKeychain](/resources/#resources-hive-keychain)
*   [HiveAuth](/resources/#resources-hiveauth)
*   [Jussi](/resources/#resources-jussi)
*   [Tools](/resources/#resources-tools)
*   [Dev support](/resources/#resources-developeradvocate)

###### Glossary

*   [Chain Basics](/glossary/#glossary-chain-basics)
*   [Governance](/glossary/#glossary-governance)
*   [Transactions](/glossary/#glossary-transactions)
*   [API](/glossary/#glossary-api)
*   [Market](/glossary/#glossary-market)

[![](/images/i18n/en.svg)]( /) [![](/images/i18n/es.svg)](/es/) [![](/images/i18n/hi.svg)](/hi/) [![](/images/i18n/de.svg)](/de/) [![](/images/i18n/fr.svg)](/fr/) [![](/images/i18n/ru.svg)](/ru/) [![](/images/i18n/zh.svg)](/zh/)

Hive Developer Portal
=====================

![](/images/honey-comb-92.png)

### Intro to Hive

**[Hive](https://hive.io)** is a decentralized blockchain with **fast** transaction speed (3s) without fees, **human readable account names**, **decentralized community fund** and **algorithmic stablecoin (HBD)** backed by HIVE.

Blockchain powered by Delegated Proof of Stakes (DPOS) consensus which perfectly balances **scaling**, **decentralization** and **speed**.

Hive blockchain pioneers innovations such as Resource Credits system, Human readable usernames, algorithmic stablecoin in blockchain space.

**Resource Credits** - system allows users to stake HIVE token and get allocated resources to perform basically free transactions on chain, without paying huge fees like other blockchains Bitcoin or Ethereum.

**Human readable usernames** - makes it easy to remember account names of businesses or people you interact with, making social and transactional interactions easy.

**Algorithmic stablecoin** - backed by HIVE token has been running almost a decade long without any issues, making it one of the very first algorithmic stable coins.

**Social networking** - initial and most successful applications built on Hive are decentralized, community owned social networking applications. Making it very first blockchain to truly empower free speech and decentralized information distribution network on web3.

**Decentralized Hive Fund** - community owned and controlled funds helping blockchain to allocate funds to many developers and teams across the world to build and innovate.

**Gaming, NFT, DEFI and more** - easy development and easy integration with above benefits giving developers/creators enough reason to build applications on Web3, that’s engaging and growing.

### Web2 vs Web3

Internet, we know of today mostly contain websites and services which is referred as Web2. Dominated by companies that provide services in exchange for your personal data. Blockchains such as Hive, powers websites and services that go into Web3 category, referring to decentralized apps which runs on the blockchain. These are apps that allow anyone to participate without monetising their personal data, true ownership.

Aspect

Web2

Web3

Data Ownership

Controlled by centralized entities

Decentralized, users own their data

Trust

Relies on trust in centralized entities

Trustless system through blockchain technology

Censorship

Vulnerable to censorship by centralized authorities

Resistant to censorship due to decentralization

Scalability

Limited scalability due to centralized infrastructure

Potential for greater scalability through decentralization

Transparency

Lack of transparency in data handling

Transparent, immutable record on the blockchain

Governance

Controlled by centralized entities

Community-driven governance through DAOs

Monetization

Centralized monetization models (e.g., advertising)

Decentralized monetization via tokens and smart contracts

Intermediaries

Relies heavily on intermediaries (e.g., social media platforms)

Removes intermediaries through decentralization

Innovation

Innovation driven by large tech companies

Innovation driven by decentralized protocols and communities

**Start developing and investing your time building products on Web3 to empower communities, now!**

### Developer workflow

This is high level representation of how websites or services talk with blockchain. It’s important to note that this is an oversimplification of the Hive network for the purposes of making it easier to understand learning.

![Hive devs workflow](/images/hive-dev-structure.png)

[Back to top](#)

document.getElementById("open-nav").addEventListener("click", function () { document.body.classList.toggle("nav-open"); }); // assets/js/post.js let codeBlocks = document.querySelectorAll('pre.highlight'); codeBlocks.forEach(function (codeBlock) { let copyButton = document.createElement('button'); copyButton.className = 'copy'; copyButton.type = 'button'; copyButton.ariaLabel = 'Copy code to clipboard'; copyButton.innerText = 'Copy'; codeBlock.append(copyButton); copyButton.addEventListener('click', function () { let code = codeBlock.querySelector('code').innerText.trim(); window.navigator.clipboard.writeText(code); copyButton.innerText = 'Copied'; let fourSeconds = 4000; setTimeout(function () { copyButton.innerText = 'Copy'; }, fourSeconds); }); });
