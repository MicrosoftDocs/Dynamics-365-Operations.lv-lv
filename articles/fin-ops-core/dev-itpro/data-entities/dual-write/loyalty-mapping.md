---
title: Klientu lojalitātes programmas kartes un atlīdzības punkti
description: Šajā tēmā aprakstīta klientu lojalitātes programmu un atlīdzības karšu datu integrācija duālā ierakstā.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: d2c3845c1a7371d9e992495246e8dd0eb8631020
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747991"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="33190-103">Debitoru lojalitātes programmas kartes un atlīdzības punkti</span><span class="sxs-lookup"><span data-stu-id="33190-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="33190-104">Uzņēmumi klasificē klientus un sniedz sarežģītus pakalpojumus, pamatojoties uz klientu iepirkšanās un izdevumu modeļiem.</span><span class="sxs-lookup"><span data-stu-id="33190-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="33190-105">Piemēram, Dynamics 365 Commerce ir infrastruktūra un funkcijas, kas atvieglo un apstrādā klientu lojalitātes programmas kartes, atlīdzības punktus, lojalitātē balstītu cenu noteikšanu un atlīdzībā balstītu iepirkšanās pieredzi.</span><span class="sxs-lookup"><span data-stu-id="33190-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="33190-106">Kad dati par klientu lojalitātes programmas kartēm un atlīdzības punktiem pakalpojumā Commerce ir sinhronizēti ar Dataverse, klientu iesaistes programmas var šos datus izmantot.</span><span class="sxs-lookup"><span data-stu-id="33190-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="33190-107">Piemēram, Dynamics 365 Customer Service lietotāji var izmantot datus, lai nodrošinātu tos pašus sarežģītos pakalpojumus, izmantojot palīdzības dienestu.</span><span class="sxs-lookup"><span data-stu-id="33190-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="33190-108">Veidnes</span><span class="sxs-lookup"><span data-stu-id="33190-108">Templates</span></span>

| <span data-ttu-id="33190-109">Finance and Operations programmas</span><span class="sxs-lookup"><span data-stu-id="33190-109">Finance and Operations apps</span></span> | <span data-ttu-id="33190-110">Modeļa vadītas programmas programmā Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="33190-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="33190-111">apraksts</span><span class="sxs-lookup"><span data-stu-id="33190-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="33190-112">Lojalitātes programmas karte</span><span class="sxs-lookup"><span data-stu-id="33190-112">Loyalty card</span></span>                | <span data-ttu-id="33190-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="33190-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="33190-114">Šī veidne sinhronizē informāciju par klientu lojalitātes programmu kartēm.</span><span class="sxs-lookup"><span data-stu-id="33190-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="33190-115">Lojalitātes programmas atlīdzības punkti</span><span class="sxs-lookup"><span data-stu-id="33190-115">Loyalty reward points</span></span>       | <span data-ttu-id="33190-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="33190-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="33190-117">Šī veidne sinhronizē informāciju par klientu atlīdzības punktiem.</span><span class="sxs-lookup"><span data-stu-id="33190-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]