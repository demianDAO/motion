# motion


### ICP概念


非交互式去中心密钥生成协议（NI-DKG）是一个全新的、非交互式的密钥重分享协议。每个旧的签名者只需要向新的签名者广播一条信息即可。为了确保安全地完成这项工作，协议利用了许多高级密码学原语，包括具有前向保密性的加密和非交互式零知识证明。在一个子网的整个生命周期中，子网具备唯一的公钥用于验证与签名，而互联网计算机上的其他各子网与节点不必跟踪其不断变化的公钥。


当涉及到区块链初创企业时，硅谷所习惯与喜欢的陈旧叙事被完全推翻。上次活动与TechCrunch 合作，介绍了创业者该如何在没有技术垄断破平台的情况下，建立大规模的商业。听取了 Fleek、Capsule、Tacen 和 Distrikt 的创始人，以及 Polychain Capital合伙人的发言，他们讲述了建立的开放互联网上的初创企业，在投融资、产品创意、招聘、筹资和退出等方面的情况。


网络神经系统（NNS）是一个控制互联网计算机网络的开放式算法治理系统。它最引人注目的几项创新在于，它能够升级节点机器使用的协议和软件，将新的节点与机器纳入网络，并创建新的子网（也就是区块链分片）以增加网络容量。最重要的是，NNS 的工作方式是接受提案，并根据数以千计的「神经元」持有者的投票活动，决定采用或拒绝这些提案。


ETH是一台强制同步、共享状态的状态更新机器，而DFINITY是一台排序消息的消息处理机器，DFINITY可以实现异步运行，DFINITY的软件容器（即智能合约的升级）可以看作一个单独的个体，因为不强制共享共享状态，容器中也可以设置“隐私”与“公开”部分，容器仅通过内部的确定性计算与外部的消息通信来运行，而DFINITY的共识对消息顺序进行排序。


神经元的投票权，以及他们能获取的投票奖励，与放入神经元的 ICP 数量、溶解延迟的长度，以及神经元存在的年龄成正比。其中值得特别关注的是，溶解延迟就类似于一个倒计时，当倒计时结束时，质押在神经元中的 ICP 才能解锁。溶解延迟的时间可以由创建者自由设置，最长为 8 年。一旦神经元创建完成，那么质押的 ICP 就相当于被锁定，只有等到溶解延迟达到设定的时间，才能够释放。为了鼓励更多神经元选择设置更长的溶解延迟周期，该时间设置的越长，相应的获得治理奖励的权重也会越高。

### icp nft


https://github.com/dfinance-tech/ic-nft


https://forum.dfinity.org/t/non-fungible-token-nft-standard-community-consideration/6157

https://forum.dfinity.org/t/thoughts-on-the-token-standard/4694/83


https://github.com/Deland-Labs/dfinity-fungible-token-standard

https://medium.com/dab-ooo/dab-an-open-internet-service-for-internet-computer-data-registries-starting-with-the-nft-list-11a361f2196c

https://docs.dab.ooo

### Candid

Candid is an Interface Description Language (IDL). Its primary purpose is to describe the public interface of a canister that runs on the Internet Computer.


### ICP开发经验

所有的异步调用都要在最外层，不能链式await，尽量一个await解决问题。

通过了解代码的开发人员将发现：
* 		具有JavaScript前端和Motoko后端的全栈Web dapp；
* 		Motoko的高级功能，例如Motoko软件包管理器容器；
* 		API中的许多系统功能，例如时间和授权；
* 		与Internet身份服务集成；
* 		端到端测试和持续集成的最佳实践。

### Icp 应用设想


如果没个罐都需要消耗cycles 但是如何均衡cycles当成一种更适合的资源消耗，或许有一个更大的市场，比如现在的snowflake

用索引的形式搞定最低的存储和资源使用最大化分配，在icp上做一个超级大的SaaS服务，


16年的snowflake论文，the snowflake elastic data warehouse


计算和存储分离，集群扩容，重新分配计算资源，弹性扩容没个应用canid（程序罐），Rust重写

如何使用：每个用户或项目方可以写好代码 然后直接托管在snowflake上，实行资源共享和最低化成本跑应用，而项目方只需要按需付费icp即可，并且实行严格的ddos防御和锁资源服务

datacloud ，自由数据交易的marketplace，数据商店？


snowflake的招股书中文版


或者是做了一个区块链版的pingcap？


目前已经存在测产品：GRT、cere

观点和见解

1. Snowflake就相当于一个统一的数据整理和储存层：不管你的底层是本地服务器，还是几个云服务商，Snowflake都在这些基础设施的上一层提供了一个统一的存储管理功能，也给数据的使用者提供一个统一的交互界面。


2. 三大主流云计算服务商也都提供数据仓库服务。比如，亚马逊有 Redshift，谷歌有 BigQuery，微软有 Azure SQL Data Warehouse。但 Snowflake 的其中一个优势就在于它同时支持 AWS、Azure 和 Google Cloud Platform，无论客户用的是哪一家的服务，都能接入 Snowflake，不必担心被「强买强卖」——比如你想用 Redshift 就只能同时用亚马逊的 AWS。这样，企业就能根据自己的预算和需求，设计出更低成本的购买方案。

3. 这里我们不难看出，Snowflake 充当的是一个转销商（reseller）的角色，也因此成了「云中立」的平台。更重要的，Snowflake 这种无缝连接多个云的能力，解决了行业中棘手的数据孤岛和数据管理问题，客户可以自由地整合及问询数据。
4. snowflake的大亮点就是弹性数据仓库，所谓的存储与计算力分离，与传统的数据仓库公司相比，他们是按照算力来算价钱的，由于大部分时候都不需要运算，所以价格上会更加吸引用户。再加上与三家云服务供应商的整合做得好，所以基本可以采用ELT传输，即不需要太多的数据工程师来挖掘和整理原始数据。


术语：ndr（net dollar revenue），收入留存率
