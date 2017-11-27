---
title: "Pārdošanas tendenču un modeļu analīze"
description: "Programmatūrā Microsoft Dynamics 365 for Retail varat reāllaikā pētīt pārdošanas tendences un modeļus."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b2a23b6013fd9096457647142a40a6710da6ca88
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="analyze-sales-trends-and-patterns"></a><span data-ttu-id="96d91-103">Analizēt pārdošanas tendences un modeļus</span><span class="sxs-lookup"><span data-stu-id="96d91-103">Analyze sales trends and patterns</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="96d91-104">Programmatūrā Microsoft Dynamics 365 for Retail varat reāllaikā pētīt pārdošanas tendences un modeļus.</span><span class="sxs-lookup"><span data-stu-id="96d91-104">You can study sales trends and patterns in real time in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="96d91-105">Programmatūrā Dynamics 365 for Retail lietotāji var reāllaikā pētīt pārdošanas tendences un modeļus dažādos organizācijas hierarhijas līmeņos vairāku gadu periodā, lietojot standarta pārskatu **Kanāla pārdošanas pārskats pa gadiem**.</span><span class="sxs-lookup"><span data-stu-id="96d91-105">As part of Dynamics 365 for Retail, users can study sales trends and patterns in real time across different levels of the organization hierarchy over a period of years by using the out-of-box **Channel sales by year** report.</span></span> <span data-ttu-id="96d91-106">Šo pārskatu var atvērt no šādām vietām:</span><span class="sxs-lookup"><span data-stu-id="96d91-106">You can open this report from any of the following locations:</span></span>

-   <span data-ttu-id="96d91-107">Darbvieta **Mazumtirdzniecības veikala pārvaldība** &gt; **Mazumtirdzniecība** &gt; **Kanāli** &gt; **Mazumtirdzniecības veikala pārvaldība** &gt; **Pārskati** &gt; **Kanāla pārdošanas pārskats pa gadiem**</span><span class="sxs-lookup"><span data-stu-id="96d91-107">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
-   <span data-ttu-id="96d91-108">Darbvieta **Mazumtirdzniecības veikala finanses** &gt; **Mazumtirdzniecība** &gt; **Kanāli** &gt; **Mazumtirdzniecības veikala finanses** &gt; **Pārskati** &gt; **Kanāla pārdošanas pārskats pa gadiem**</span><span class="sxs-lookup"><span data-stu-id="96d91-108">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by year report**</span></span>
-   <span data-ttu-id="96d91-109">Sadaļa **Pieprasījumi un pārskati** &gt; **Mazumtirdzniecība** &gt; **Pieprasījumi un pārskati** &gt; **Pārdošanas pārskati** &gt; **Kanāla pārdošanas pārskats pa gadiem**</span><span class="sxs-lookup"><span data-stu-id="96d91-109">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by year report**</span></span>

<span data-ttu-id="96d91-110">Lietotāji arī var izpētīt pārdošanas tendences un modeļus pa stundām dažādos organizācijas hierarhijas līmeņos atlasītajā periodā, lietojot standarta pārskatu **Kanāla pārdošanas pārskats pa stundām**.</span><span class="sxs-lookup"><span data-stu-id="96d91-110">Users can also study sales trends and patterns by hour across different levels of the organization hierarchy over a selected period by using the out-of-box **Channel sales by hour** report.</span></span> <span data-ttu-id="96d91-111">Šo pārskatu var atvērt no šādām vietām:</span><span class="sxs-lookup"><span data-stu-id="96d91-111">You can open this report from any of the following locations:</span></span>

-   <span data-ttu-id="96d91-112">Darbvieta **Mazumtirdzniecības veikala pārvaldība** &gt; **Mazumtirdzniecība** &gt; **Kanāli** &gt; **Mazumtirdzniecības veikala pārvaldība** &gt; **Pārskati** &gt; **Kanāla pārdošanas pārskats pa stundām**</span><span class="sxs-lookup"><span data-stu-id="96d91-112">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
-   <span data-ttu-id="96d91-113">Darbvieta **Mazumtirdzniecības veikala finanses** &gt; **Mazumtirdzniecība** &gt; **Kanāli** &gt; **Mazumtirdzniecības veikala finanses** &gt; **Pārskati** &gt; **Kanāla pārdošanas pārskats pa stundām**</span><span class="sxs-lookup"><span data-stu-id="96d91-113">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel sales by hour report**</span></span>
-   <span data-ttu-id="96d91-114">Sadaļa **Pieprasījumi un pārskati** &gt; **Mazumtirdzniecība** &gt; **Pieprasījumi un pārskati** &gt; **Pārdošanas pārskati** &gt; **Kanāla pārdošanas pārskats pa stundām**</span><span class="sxs-lookup"><span data-stu-id="96d91-114">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel sales by hour report**</span></span>



