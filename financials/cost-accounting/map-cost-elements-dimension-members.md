---
title: "Izmaksu elementu dimensiju elementus kartēt uz kopīgu dimensiju elementu kopu"
description: "Kartējot dažādu izmaksu elementa dimensiju dalībniekus vienotā izmaksu elementa dimensijas dalībnieku kopā, jūs sapludināt datus vispārējā formātā analīzes nolūkiem."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 9e13fc9fa7e51a1299ca8698f581de979b680a7b
ms.openlocfilehash: b15e251410937ff4f85ecdfaa55ca1a998d1d1ac
ms.contentlocale: lv-lv
ms.lasthandoff: 09/18/2017

---

# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="3886a-103">Izmaksu elementu dimensiju elementus kartēt uz kopīgu dimensiju elementu kopu</span><span class="sxs-lookup"><span data-stu-id="3886a-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3886a-104">Kartējot dažādu izmaksu elementa dimensiju dalībniekus vienotā izmaksu elementa dimensijas dalībnieku kopā, jūs sapludināt datus vispārējā formātā analīzes nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="3886a-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="3886a-105">Ja jūs esat globāla kompānija un atbilstat likumā noteiktajām grāmatvedības prasībām, jūs varat izmantot vairākus kontu plānus.</span><span class="sxs-lookup"><span data-stu-id="3886a-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="3886a-106">Importējot izmaksu elementa dimensijas dalībniekus no dažādiem kontu plāniem, jūs varat nonākt līdz kontu sajaukumam.</span><span class="sxs-lookup"><span data-stu-id="3886a-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="3886a-107">Tomēr šie konti varētu būt tāda paša rakstura, un jūs varētu vēlēties izanalizēt un sadalīt tiem izmaksas, izmantojot vienotu formātu.</span><span class="sxs-lookup"><span data-stu-id="3886a-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="3886a-108">Kartēt izmaksu elementa dimensijas dalībniekus vienotā formātā</span><span class="sxs-lookup"><span data-stu-id="3886a-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="3886a-109">Šajā piemērā ir parādīts, kā jūs kā izmaksu kontrolieris varat izveidot jaunu izmaksu elementa dimensiju Izmaksu uzskaitē, kas kartē izmaksu elementa dimensijas dalībniekus no ASV kontu plāna struktūras, un Francijas kontu plāna struktūras vienotā izmaksu elementa dimensijas dalībnieku izmaksu uzskaites kopā.</span><span class="sxs-lookup"><span data-stu-id="3886a-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="3886a-110">Jūs varat izmantot vienoto izmaksu elementa dimensijas dalībnieku kopu, lai analizētu izmaksu datus no divām juridiskām personām izmaksu uzskaites virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="3886a-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="3886a-111">Avots: ASV kontu plāns</span><span class="sxs-lookup"><span data-stu-id="3886a-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="3886a-112">Avots: Francijas kontu plāns</span><span class="sxs-lookup"><span data-stu-id="3886a-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="3886a-113">Jauna vienota izmaksu elementa dimensijas dalībnieku kopa</span><span class="sxs-lookup"><span data-stu-id="3886a-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3886a-114">Importēto izmaksu elementa dimensijas dalībnieki no ASV kontu plāna</span><span class="sxs-lookup"><span data-stu-id="3886a-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="3886a-115">Importēto izmaksu elementa dimensijas dalībnieki no Francijas kontu plāna</span><span class="sxs-lookup"><span data-stu-id="3886a-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="3886a-116">ASV un Francijas izmaksu elementa dimensijas dalībnieku kartēšana vienotā kopā</span><span class="sxs-lookup"><span data-stu-id="3886a-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="3886a-117">5001: Pārdošana</span><span class="sxs-lookup"><span data-stu-id="3886a-117">5001: Sales</span></span>                                                           | <span data-ttu-id="3886a-118">5001: Pārdošana un reklāma</span><span class="sxs-lookup"><span data-stu-id="3886a-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="3886a-119">5000: Pārdošana un reklāma</span><span class="sxs-lookup"><span data-stu-id="3886a-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="3886a-120">5030: Reklāma</span><span class="sxs-lookup"><span data-stu-id="3886a-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="3886a-121">6390: Krājumu pirkšana\*</span><span class="sxs-lookup"><span data-stu-id="3886a-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="3886a-122">7000: Tīrīšanas izdevumi</span><span class="sxs-lookup"><span data-stu-id="3886a-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="3886a-123">7001: Tīrīšanas izdevumi</span><span class="sxs-lookup"><span data-stu-id="3886a-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="3886a-124">7001: Komandējuma izdevumi</span><span class="sxs-lookup"><span data-stu-id="3886a-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="3886a-125">7001: Komandējuma izdevumi</span><span class="sxs-lookup"><span data-stu-id="3886a-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="3886a-126">\*Francijas izmaksu elementa dimensijas dalībnieks Krājumu pirkšana netiek kartēts.</span><span class="sxs-lookup"><span data-stu-id="3886a-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="3886a-127">Valūtas konvertācija</span><span class="sxs-lookup"><span data-stu-id="3886a-127">Currency conversion</span></span>
<span data-ttu-id="3886a-128">Dažādus kontu plānus, ko jūs izmantojat iespējams iestatīt izmantošanai dažādās valūtās.</span><span class="sxs-lookup"><span data-stu-id="3886a-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="3886a-129">Šajā gadījumā noteikti norādiet valūtas konvertāciju, lai izmaksu dati tiek apstrādāti, izmantojot pareizo valūtu, kā definēts izmaksu uzskaites virsgrāmatā, kur tiek izmantoti izmaksu elementa dimensijas dalībnieki.</span><span class="sxs-lookup"><span data-stu-id="3886a-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="3886a-130">Iepriekšējā piemērā, ja izmaksu uzskaites virsgrāmatā tiek izmantoti ASV dolāri (USD), nepieciešams izveidot valūtas konvertāciju no USD uz eiro (EUR), lai apstrādātu darījumus kartētajiem izmaksu elementa dimensijas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="3886a-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="3886a-131">Atjaunināt kartējumus jebkurā laikā</span><span class="sxs-lookup"><span data-stu-id="3886a-131">Update mappings at any time</span></span>
<span data-ttu-id="3886a-132">Jūs varat jebkurā laikā atjaunināt izmaksu elementa dimensijas definīcijas.</span><span class="sxs-lookup"><span data-stu-id="3886a-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="3886a-133">Tā kā kartējumiem nav stāšanās spēkā datuma, izmaiņas tiek pielietotas nākamajā reizē, kad apstrādājat izmaksu darbības vai izpildot izmaksu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="3886a-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>




