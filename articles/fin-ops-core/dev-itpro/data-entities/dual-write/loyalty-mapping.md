---
title: Klientu lojalitātes programmas kartes un atlīdzības punkti
description: Šajā tēmā aprakstīta klientu lojalitātes programmu un atlīdzības karšu datu integrācija starp Finance and Operations programmām un Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e7e67946930404ab7ba0c7fccf468722f723d675
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172973"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="201c7-103">Klientu lojalitātes programmas kartes un atlīdzības punkti</span><span class="sxs-lookup"><span data-stu-id="201c7-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="201c7-104">Uzņēmumi klasificē klientus un sniedz sarežģītus pakalpojumus, pamatojoties uz klientu iepirkšanās un izdevumu modeļiem.</span><span class="sxs-lookup"><span data-stu-id="201c7-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="201c7-105">Programmas Microsoft Dynamics 365 programmu klāstā ir Dynamics 365 Commerce, kurai ir infrastruktūra un funkcijas, kas atvieglo un apstrādā klientu lojalitātes programmas kartes, atlīdzības punktus, lojalitātē balstītu cenu noteikšanu un atlīdzībā balstītu iepirkšanās pieredzi.</span><span class="sxs-lookup"><span data-stu-id="201c7-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="201c7-106">Kad dati par klientu lojalitātes programmas kartēm un atlīdzības punktiem pakalpojumā Commerce ir sinhronizēti ar Common Data Service, Dynamics 365 modeļa vadītā programmas var šos datus izmantot.</span><span class="sxs-lookup"><span data-stu-id="201c7-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="201c7-107">Piemēram, Dynamics 365 Customer Service lietotāji var izmantot datus, lai nodrošinātu tos pašus sarežģītos pakalpojumus, izmantojot palīdzības dienestu.</span><span class="sxs-lookup"><span data-stu-id="201c7-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="201c7-108">Veidnes</span><span class="sxs-lookup"><span data-stu-id="201c7-108">Templates</span></span>

| <span data-ttu-id="201c7-109">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="201c7-109">Finance and Operations apps</span></span> | <span data-ttu-id="201c7-110">Modeļa vadītas programmas programmā Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="201c7-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="201c7-111">apraksts</span><span class="sxs-lookup"><span data-stu-id="201c7-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="201c7-112">Lojalitātes programmas karte</span><span class="sxs-lookup"><span data-stu-id="201c7-112">Loyalty card</span></span>                | <span data-ttu-id="201c7-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="201c7-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="201c7-114">Šī veidne sinhronizē informāciju par klientu lojalitātes programmu kartēm.</span><span class="sxs-lookup"><span data-stu-id="201c7-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="201c7-115">Lojalitātes programmas atlīdzības punkti</span><span class="sxs-lookup"><span data-stu-id="201c7-115">Loyalty reward points</span></span>       | <span data-ttu-id="201c7-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="201c7-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="201c7-117">Šī veidne sinhronizē informāciju par klientu atlīdzības punktiem.</span><span class="sxs-lookup"><span data-stu-id="201c7-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
