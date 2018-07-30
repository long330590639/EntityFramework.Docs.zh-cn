---
title: 使用断开连接的实体 - EF6
author: divega
ms.date: 2016-10-23
ms.prod: entity-framework
ms.author: divega
ms.manager: avickers
ms.technology: entity-framework-6
ms.topic: article
ms.assetid: 12138003-a373-4817-b1b7-724130202f5f
caps.latest.revision: 3
ms.openlocfilehash: 5419215a77b57ab3c92fb88a512510070ea23bd6
ms.sourcegitcommit: 45494121254ad4fdcec613d1dd22d850068d6f39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/08/2018
ms.locfileid: "37913437"
---
# <a name="working-with-disconnected-entities"></a><span data-ttu-id="f39fc-102">使用断开连接的实体</span><span class="sxs-lookup"><span data-stu-id="f39fc-102">Working with disconnected entities</span></span>
<span data-ttu-id="f39fc-103">在基于实体框架的应用程序中，上下文类负责检测应用于已跟踪实体的更改。</span><span class="sxs-lookup"><span data-stu-id="f39fc-103">In an Entity Framework-based application, a context class is responsible for detecting changes applied to tracked entities.</span></span> <span data-ttu-id="f39fc-104">调用 SaveChanges 方法会将上下文跟踪的更改保存到数据库。</span><span class="sxs-lookup"><span data-stu-id="f39fc-104">Calling the SaveChanges method persists the changes tracked by the context to the database.</span></span> <span data-ttu-id="f39fc-105">使用 n 层应用程序时，实体对象通常会在从上下文断开连接时发生变动，且必须决定如何跟踪更改并向上下文报告这些更改。</span><span class="sxs-lookup"><span data-stu-id="f39fc-105">When working with n-tier applications, entity objects are usually modified while disconnected from the context, and you must decide how to track changes and report those changes back to the context.</span></span> <span data-ttu-id="f39fc-106">本主题讨论使用实体框架和断开连接的实体时不同的可用选项。</span><span class="sxs-lookup"><span data-stu-id="f39fc-106">This topic discusses different options that are available when using Entity Framework with disconnected entities.</span></span>   

## <a name="web-service-frameworks"></a><span data-ttu-id="f39fc-107">Web 服务框架</span><span class="sxs-lookup"><span data-stu-id="f39fc-107">Web service frameworks</span></span>

<span data-ttu-id="f39fc-108">Web 服务技术通常支持可用于在各个断开连接的对象上保存更改的模式。</span><span class="sxs-lookup"><span data-stu-id="f39fc-108">Web services technologies typically support patterns that can be used to persist changes on individual disconnected objects.</span></span> <span data-ttu-id="f39fc-109">例如，通过 ASP.NET Web API 可编写控制器操作，这些操作可以包括对 EF 的调用，以保存对数据库上的对象所做的更改。</span><span class="sxs-lookup"><span data-stu-id="f39fc-109">For example, ASP.NET Web API allows you to code controller actions that can include calls to EF to persist changes made to an object on a database.</span></span> <span data-ttu-id="f39fc-110">实际上，Visual Studio 中的 Web API 工具可以轻松地从实体框架 6 模型构建 Web API 控制器。</span><span class="sxs-lookup"><span data-stu-id="f39fc-110">In fact, the Web API tooling in Visual Studio makes it easy to scaffold a Web API controller from your Entity Framework 6 model.</span></span> <span data-ttu-id="f39fc-111">有关详细信息，请参阅[一起使用 Web API 和实体框架 6](https://docs.microsoft.com/en-us/aspnet/web-api/overview/data/using-web-api-with-entity-framework/)。</span><span class="sxs-lookup"><span data-stu-id="f39fc-111">For more information, see [using Web API with Entity Framework 6](https://docs.microsoft.com/en-us/aspnet/web-api/overview/data/using-web-api-with-entity-framework/).</span></span>   

<span data-ttu-id="f39fc-112">以前，还有其他一些 Web 服务技术提供与实体框架的集成，例如 [WCF 数据服务](https://docs.microsoft.com/dotnet/framework/data/wcf/create-a-data-service-using-an-adonet-ef-data-wcf)和 [RIA 服务](https://docs.microsoft.com/en-us/previous-versions/dotnet/wcf-ria/ee707344(v=vs.91))。</span><span class="sxs-lookup"><span data-stu-id="f39fc-112">Historically, there have been several other Web services technologies that offered integration with Entity Framework, like [WCF Data Services](https://docs.microsoft.com/dotnet/framework/data/wcf/create-a-data-service-using-an-adonet-ef-data-wcf) and [RIA Services](https://docs.microsoft.com/en-us/previous-versions/dotnet/wcf-ria/ee707344(v=vs.91)).</span></span>

## <a name="low-level-ef-apis"></a><span data-ttu-id="f39fc-113">低级别 EF API</span><span class="sxs-lookup"><span data-stu-id="f39fc-113">Low-level EF APIs</span></span>

<span data-ttu-id="f39fc-114">如果不想使用现有的 n 层解决方案，或者想要自定义 Web API 服务中控制器操作内发生的内容，则可通过实体框架提供的 API 应用在断开连接的层上所做的更改。</span><span class="sxs-lookup"><span data-stu-id="f39fc-114">If you don't want to use an existing n-tier solution, or if you want to customize what happens inside a controller action in a Web API services, Entity Framework provides APIs that allow you to apply changes made on a disconnected tier.</span></span> <span data-ttu-id="f39fc-115">有关详细信息，请参阅[添加、附加和实体状态](~/ef6/saving/change-tracking/entity-state.md)。</span><span class="sxs-lookup"><span data-stu-id="f39fc-115">For more information, see [Add, Attach, and entity state](~/ef6/saving/change-tracking/entity-state.md).</span></span>  

## <a name="self-tracking-entities"></a><span data-ttu-id="f39fc-116">自跟踪实体</span><span class="sxs-lookup"><span data-stu-id="f39fc-116">Self-Tracking Entities</span></span>  

<span data-ttu-id="f39fc-117">在从 EF 上下文断开连接时，跟踪实体的任意图上的更改是一个难题。</span><span class="sxs-lookup"><span data-stu-id="f39fc-117">Tracking changes on arbitrary graphs of entities while disconnected from the EF context is a hard problem.</span></span> <span data-ttu-id="f39fc-118">可采用自跟踪实体代码生成模板来尝试解决。</span><span class="sxs-lookup"><span data-stu-id="f39fc-118">One of the attempts to solve it was the Self-Tracking Entities code generation template.</span></span> <span data-ttu-id="f39fc-119">此模板生成实体类作为实体本身的状态，该类包含可跟踪断开连接的层上所做更改的逻辑。</span><span class="sxs-lookup"><span data-stu-id="f39fc-119">This template generates entity classes that contain logic to track changes made on a disconnected tier as state in the entities themselves.</span></span> <span data-ttu-id="f39fc-120">还会生成一组扩展方法，将这些更改应用于上下文。</span><span class="sxs-lookup"><span data-stu-id="f39fc-120">A set of extension methods is also generated to apply those changes to a context.</span></span>

<span data-ttu-id="f39fc-121">此模板可与使用 EF 设计器创建的模型一起使用，但不能与 Code First 模型一起使用。</span><span class="sxs-lookup"><span data-stu-id="f39fc-121">This template can be used with models created using the EF Designer, but can not be used with Code First models.</span></span> <span data-ttu-id="f39fc-122">有关详细信息，请参阅[自跟踪实体](self-tracking-entities/index.md)。</span><span class="sxs-lookup"><span data-stu-id="f39fc-122">For more information, see [Self-Tracking Entities](self-tracking-entities/index.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="f39fc-123">我们不再建议使用自跟踪实体模板。</span><span class="sxs-lookup"><span data-stu-id="f39fc-123">We no longer recommend using the self-tracking-entities template.</span></span> <span data-ttu-id="f39fc-124">它将仅继续用于支持现有应用程序。</span><span class="sxs-lookup"><span data-stu-id="f39fc-124">It will only continue to be available to support existing applications.</span></span> <span data-ttu-id="f39fc-125">如果应用程序需要使用断开连接的实体图，请考虑其他替代方案，例如[可跟踪实体](http://trackableentities.github.io/)，它与自跟踪实体类似，社区在更积极地开发这种技术，或使用低级别更改跟踪 API 编写自定义代码。</span><span class="sxs-lookup"><span data-stu-id="f39fc-125">If your application requires working with disconnected graphs of entities, consider other alternatives such as [Trackable Entities](http://trackableentities.github.io/), which is a technology similar to Self-Tracking-Entities that is more actively developed by the community, or writing custom code using the low-level change tracking APIs.</span></span>