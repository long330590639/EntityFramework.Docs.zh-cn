---
title: 实体框架的 EF6 的案例研究
author: divega
ms.date: 2016-10-23
ms.prod: entity-framework
ms.author: divega
ms.manager: avickers
ms.technology: entity-framework-6
ms.topic: article
ms.assetid: cd5d3ae3-717d-4095-a2ef-0e8fd72b1a2f
caps.latest.revision: 3
ms.openlocfilehash: 27c911799f957dd81a1866a3fd49e7f6cfa0059b
ms.sourcegitcommit: 390f3a37bc55105ed7cc5b0e0925b7f9c9e80ba6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/09/2018
ms.locfileid: "39120488"
---
# <a name="microsoft-case-studies-for-entity-framework"></a><span data-ttu-id="af0bd-102">用于实体框架的 Microsoft 案例研究</span><span class="sxs-lookup"><span data-stu-id="af0bd-102">Microsoft Case Studies for Entity Framework</span></span>
<span data-ttu-id="af0bd-103">案例研究此页上突出显示采用了实体框架的几个实际生产项目。</span><span class="sxs-lookup"><span data-stu-id="af0bd-103">The case studies on this page highlight a few real-world production projects that have employed Entity Framework.</span></span>
> [!NOTE]
> <span data-ttu-id="af0bd-104">这些案例研究详细的版本不再可在 Microsoft 网站上。</span><span class="sxs-lookup"><span data-stu-id="af0bd-104">The detailed versions of these case studies are no longer available on the Microsoft website.</span></span> <span data-ttu-id="af0bd-105">因此已删除的链接。</span><span class="sxs-lookup"><span data-stu-id="af0bd-105">Therefore the links have been removed.</span></span>

## <a name="epicor"></a><span data-ttu-id="af0bd-106">Epicor</span><span class="sxs-lookup"><span data-stu-id="af0bd-106">Epicor</span></span>
<span data-ttu-id="af0bd-107">Epicor 是在超过 150 个国家/地区的公司开发企业资源规划 (ERP) 解决方案 （具有超过 400 个开发人员） 的大型全球软件公司。</span><span class="sxs-lookup"><span data-stu-id="af0bd-107">Epicor is a large global software company (with over 400 developers) that develops Enterprise Resource Planning (ERP) solutions for companies in more than 150 countries.</span></span>
<span data-ttu-id="af0bd-108">其旗舰产品 Epicor 9 为基础上面向服务的体系结构 (SOA) 使用.NET Framework。</span><span class="sxs-lookup"><span data-stu-id="af0bd-108">Their flagship product, Epicor 9, is based on a Service-Oriented Architecture (SOA) using the .NET Framework.</span></span>
<span data-ttu-id="af0bd-109">面对大量客户请求，以提供支持的语言集成查询 (LINQ)，并且还想要减少其后端 SQL 服务器上的负载时，团队决定升级到 Visual Studio 2010 和.NET Framework 4.0。</span><span class="sxs-lookup"><span data-stu-id="af0bd-109">Faced with numerous customer requests to provide support for Language Integrated Query (LINQ), and also wanting to reduce the load on their back-end SQL Servers, the team decided to upgrade to Visual Studio 2010 and the .NET Framework 4.0.</span></span>
<span data-ttu-id="af0bd-110">使用 Entity Framework 4.0，他们就能够实现这些目标，并还大大简化了开发和维护。</span><span class="sxs-lookup"><span data-stu-id="af0bd-110">Using the Entity Framework 4.0, they were able to achieve these goals and also greatly simplify development and maintenance.</span></span>
<span data-ttu-id="af0bd-111">具体而言，实体框架的丰富的 T4 支持将允许他们进行其生成代码的完全控制和自动生成性能保存功能，例如预编译的查询和缓存中。</span><span class="sxs-lookup"><span data-stu-id="af0bd-111">In particular, the Entity Framework’s rich T4 support allowed them to take full control of their generated code and automatically build in performance-saving features such as pre-compiled queries and caching.</span></span>

> <span data-ttu-id="af0bd-112">"最近与现有代码，某些性能测试，我们将展开，我们就能够减少 90%的请求 SQL Server。</span><span class="sxs-lookup"><span data-stu-id="af0bd-112">“We conducted some performance tests recently with existing code, and we were able to reduce the requests to SQL Server by 90 percent.</span></span>
<span data-ttu-id="af0bd-113">这是因为在 ADO.NET Entity Framework 4。"</span><span class="sxs-lookup"><span data-stu-id="af0bd-113">That is because of the ADO.NET Entity Framework 4.”</span></span> <span data-ttu-id="af0bd-114">– Erik johnson 的演示，副总裁产品研究</span><span class="sxs-lookup"><span data-stu-id="af0bd-114">– Erik Johnson, Vice President, Product Research</span></span>  

## <a name="veracity-solutions"></a><span data-ttu-id="af0bd-115">真实性解决方案</span><span class="sxs-lookup"><span data-stu-id="af0bd-115">Veracity Solutions</span></span>
<span data-ttu-id="af0bd-116">具有获得会难以维护和扩展通过长期的事件规划软件系统，真实性解决方案用于 Visual Studio 2010 重新编写它，如在 Silverlight 4 上构建一个功能强大且易于使用丰富 Internet 应用程序。</span><span class="sxs-lookup"><span data-stu-id="af0bd-116">Having acquired an event-planning software system that was going to be difficult to maintain and extend over the long-term, Veracity Solutions used Visual Studio 2010 to re-write it as a powerful and easy-to-use Rich Internet Application built on Silverlight 4.</span></span>
<span data-ttu-id="af0bd-117">使用.NET RIA 服务，他们就能够快速构建实体框架，避免代码重复和常规的验证和身份验证逻辑允许跨层之上的一个服务层。</span><span class="sxs-lookup"><span data-stu-id="af0bd-117">Using .NET RIA Services, they were able to quickly build a service layer on top of the Entity Framework that avoided code duplication and allowed for common validation and authentication logic across tiers.</span></span>  

> <span data-ttu-id="af0bd-118">"我们售出了实体框架时首次引入和 Entity Framework 4 已被证明是更好。</span><span class="sxs-lookup"><span data-stu-id="af0bd-118">“We were sold on the Entity Framework when it was first introduced, and the Entity Framework 4 has proven to be even better.</span></span>
<span data-ttu-id="af0bd-119">改进的工具，并很方便地操纵定义概念模型、 存储模型和这些模型之间的映射的.edmx 文件...使用实体框架中，我可以获得一天中使用该数据访问层，并生成它出我继续操作的过程。</span><span class="sxs-lookup"><span data-stu-id="af0bd-119">Tooling is improved, and it’s easier to manipulate the .edmx files that define the conceptual model, storage model, and mapping between those models... With the Entity Framework, I can get that data access layer working in a day—and build it out as I go along.</span></span>
<span data-ttu-id="af0bd-120">实体框架是我们的事实数据访问层;我不知道为什么任何人都不会使用它。"</span><span class="sxs-lookup"><span data-stu-id="af0bd-120">The Entity Framework is our de facto data access layer; I don’t know why anyone wouldn’t use it.”</span></span> <span data-ttu-id="af0bd-121">– Joe McBride 高级开发人员</span><span class="sxs-lookup"><span data-stu-id="af0bd-121">– Joe McBride, Senior Developer</span></span>

## <a name="nec-display-solutions-of-america"></a><span data-ttu-id="af0bd-122">NEC 显示解决方案的 America</span><span class="sxs-lookup"><span data-stu-id="af0bd-122">NEC Display Solutions of America</span></span>
<span data-ttu-id="af0bd-123">NEC 想要输入的解决方案获益广告商和网络所有者并提高其自己的收入数字基于位置的广告的市场。</span><span class="sxs-lookup"><span data-stu-id="af0bd-123">NEC wanted to enter the market for digital place-based advertising with a solution to benefit advertisers and network owners and increase its own revenues.</span></span>
<span data-ttu-id="af0bd-124">为了做到这一点，它启动对传统的广告活动中所需的手动过程自动化的 web 应用程序。</span><span class="sxs-lookup"><span data-stu-id="af0bd-124">In order to do that, it launched a pair of web applications that automate the manual processes required in a traditional ad campaign.</span></span>
<span data-ttu-id="af0bd-125">使用 ASP.NET、 Silverlight 3、 AJAX 和 WCF，数据访问层中的实体框架，与 SQL Server 2008 以及生成站点。</span><span class="sxs-lookup"><span data-stu-id="af0bd-125">The sites were built using ASP.NET, Silverlight 3, AJAX and WCF, along with the Entity Framework in the data access layer to talk to SQL Server 2008.</span></span>

> <span data-ttu-id="af0bd-126">"借助 SQL Server，我们认为我们无法获取我们需要使用实时和可靠性，以帮助确保始终将提供我们的任务关键型应用程序中的信息中的信息提供广告商和网络吞吐量"-Mike Corcoran主管 IT</span><span class="sxs-lookup"><span data-stu-id="af0bd-126">“With SQL Server, we felt we could get the throughput we needed to serve advertisers and networks with information in real time and the reliability to help ensure that the information in our mission-critical applications would always be available”- Mike Corcoran, Director of IT</span></span>

## <a name="darwin-dimensions"></a><span data-ttu-id="af0bd-127">达尔文维度</span><span class="sxs-lookup"><span data-stu-id="af0bd-127">Darwin Dimensions</span></span>
<span data-ttu-id="af0bd-128">使用各种各样的 Microsoft 技术，Darwin 的团队着手创建 Evolver-使用者可以使用来创建令人惊叹、 逼真的头像，用于在游戏、 动画和社交网络页的联机头像门户。</span><span class="sxs-lookup"><span data-stu-id="af0bd-128">Using a wide range of Microsoft technologies, the team at Darwin set out to create Evolver - an online avatar portal that consumers could use to create stunning, lifelike avatars for use in games, animations, and social networking pages.</span></span>
<span data-ttu-id="af0bd-129">使用实体框架和组件，如 Windows Workflow Foundation (WF) 和 Windows Server AppFabric （高度可缩放内存中应用程序缓存） 中拉取的高效率优点，团队就能够在 35%中提供令人惊叹的产品开发时间。</span><span class="sxs-lookup"><span data-stu-id="af0bd-129">With the productivity benefits of the Entity Framework, and pulling in components like Windows Workflow Foundation (WF) and Windows Server AppFabric (a highly-scalable in-memory application cache), the team was able to deliver an amazing product in 35% less development time.</span></span>
<span data-ttu-id="af0bd-130">尽管团队成员拆分跨多个国家/地区，团队遵循敏捷开发流程，并且每周发布。</span><span class="sxs-lookup"><span data-stu-id="af0bd-130">Despite having team members split across multiple countries, the team following an agile development process with weekly releases.</span></span>

 > <span data-ttu-id="af0bd-131">"我们尝试不想创建起见技术的技术。</span><span class="sxs-lookup"><span data-stu-id="af0bd-131">“We try not to create technology for technology’s sake.</span></span> <span data-ttu-id="af0bd-132">为启动时，这一点至关重要，我们利用技术节省时间和资金。</span><span class="sxs-lookup"><span data-stu-id="af0bd-132">As a startup, it is crucial that we leverage technology that saves time and money.</span></span>
 <span data-ttu-id="af0bd-133">.NET 是快速、 经济高效的开发的选择。"</span><span class="sxs-lookup"><span data-stu-id="af0bd-133">.NET was the choice for fast, cost-effective development.”</span></span> <span data-ttu-id="af0bd-134">– Zachary Olsen，架构师</span><span class="sxs-lookup"><span data-stu-id="af0bd-134">– Zachary Olsen, Architect</span></span>  

## <a name="silverware"></a><span data-ttu-id="af0bd-135">Silverware</span><span class="sxs-lookup"><span data-stu-id="af0bd-135">Silverware</span></span>
<span data-ttu-id="af0bd-136">使用超过 15 年的经验开发对于小型和中型餐馆组销售点 (POS) 解决方案，Silverware 的开发团队着手增强其产品与更多的企业级功能，为了吸引更大连锁餐馆。</span><span class="sxs-lookup"><span data-stu-id="af0bd-136">With more than 15 years of experience in developing point-of-sale (POS) solutions for small and midsize restaurant groups, the development team at Silverware set out to enhance their product with more enterprise-level features in order to attract larger restaurant chains.</span></span>
<span data-ttu-id="af0bd-137">使用 Microsoft 的开发工具的最新版本，他们就能够生成新的解决方案四次超乎以往的速度。</span><span class="sxs-lookup"><span data-stu-id="af0bd-137">Using the latest version of Microsoft’s development tools, they were able to build the new solution four times faster than before.</span></span>
<span data-ttu-id="af0bd-138">密钥的新功能，如 LINQ 和实体框架进行简化了从 Crystal Reports 迁移到 SQL Server 2008 和 SQL Server Reporting Services (SSRS) 用于其数据存储和报告需求。</span><span class="sxs-lookup"><span data-stu-id="af0bd-138">Key new features like LINQ and the Entity Framework made it easier to move from Crystal Reports to SQL Server 2008 and SQL Server Reporting Services (SSRS) for their data storage and reporting needs.</span></span>

> <span data-ttu-id="af0bd-139">"有效的数据管理是 SilverWare – 取得成功至关重要，这是为什么我们决定使用 SQL Reporting"。</span><span class="sxs-lookup"><span data-stu-id="af0bd-139">“Effective data management is key to the success of SilverWare – and this is why we decided to adopt SQL Reporting.”</span></span> <span data-ttu-id="af0bd-140">-Nicholas Romanidis，主管 IT / 软件工程</span><span class="sxs-lookup"><span data-stu-id="af0bd-140">- Nicholas Romanidis, Director of IT/Software Engineering</span></span>