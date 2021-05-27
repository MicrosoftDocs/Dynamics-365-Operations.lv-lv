---
title: Finanšu dimensiju kopas
description: Šajā tēmā aprakstītas finanšu dimensiju kopas un sniegti daži padomi to lietošanas optimizēšanai.
author: yukonpeegs
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ba11be028ebeea140df93e2a07dbb463402e3ef0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021832"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="fe143-103">Finanšu dimensiju kopas</span><span class="sxs-lookup"><span data-stu-id="fe143-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe143-104">Šajā tēmā aprakstītas finanšu dimensiju kopas un sniegti daži padomi to lietošanas optimizēšanai.</span><span class="sxs-lookup"><span data-stu-id="fe143-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="fe143-105">Dimensiju kopa ir sakārtots finanšu dimensiju saraksts, ko var izmantot, lai apkopotu Virsgrāmatas datus lietotāja definētā veidā.</span><span class="sxs-lookup"><span data-stu-id="fe143-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="fe143-106">Dimensiju kopu primārā izmantošana ir definēt apgrozījuma bilanci.</span><span class="sxs-lookup"><span data-stu-id="fe143-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="fe143-107">Vienīgā standarta dimensiju kopa ir dimensiju kopa, kas ietver tikai galveno kontu.</span><span class="sxs-lookup"><span data-stu-id="fe143-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="fe143-108">Lapa **Finanšu dimensiju kopas** tiek izmantota finanšu dimensiju kopu izveidošanai un pārvaldīšanai.</span><span class="sxs-lookup"><span data-stu-id="fe143-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="fe143-109">Dimensiju kopas bilances</span><span class="sxs-lookup"><span data-stu-id="fe143-109">Dimension set balances</span></span>

<span data-ttu-id="fe143-110">Dimensiju kopai var būt bilances, kas pamatotas uz tās finanšu dimensijām.</span><span class="sxs-lookup"><span data-stu-id="fe143-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="fe143-111">Bilances pastāv Virsgrāmatā, un tās ir balstītas uz dimensiju kopas definīciju.</span><span class="sxs-lookup"><span data-stu-id="fe143-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="fe143-112">Bilances tiek apkopotas no Virsgrāmatas datiem, lai palīdzētu uzlabot veiktspēju to izgūšanas laikā (piemēram, kad tiek ģenerēta apgrozījuma bilance).</span><span class="sxs-lookup"><span data-stu-id="fe143-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="fe143-113">Izveidot bilances</span><span class="sxs-lookup"><span data-stu-id="fe143-113">Create balances</span></span>

<span data-ttu-id="fe143-114">Izmantojiet pogu **Izveidot bilances**, lai inicializētu bilances dimensiju kopai, kurai pašlaik nav bilances.</span><span class="sxs-lookup"><span data-stu-id="fe143-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="fe143-115">Ieteicams ierobežot to dimensiju kopu skaitu, kurām ir bilances, jo bilances atjauninājumi ietekmē visas Virsgrāmatas grāmatošanas darbības.</span><span class="sxs-lookup"><span data-stu-id="fe143-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="fe143-116">Atjaunināt bilances</span><span class="sxs-lookup"><span data-stu-id="fe143-116">Update balances</span></span>

<span data-ttu-id="fe143-117">Izmantojiet pogu **Atjaunināt bilances**, lai bilancēs iekļautu pēdējo Virsgrāmatas grāmatošanas aktivitāti.</span><span class="sxs-lookup"><span data-stu-id="fe143-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="fe143-118">Bilances atjauninājumi ir vieglas darbības.</span><span class="sxs-lookup"><span data-stu-id="fe143-118">Balance updates are light operations.</span></span> <span data-ttu-id="fe143-119">Tām ir jāapstrādā tikai Virsgrāmatas grāmatošanas aktivitāte, kas ir notikusi kopš pēdējās atjaunināšanas.</span><span class="sxs-lookup"><span data-stu-id="fe143-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="fe143-120">Rādot apgrozījuma bilanci, tiek veikta atjaunināšana, lai pārliecinātos, vai parādītās bilances ir aktuālas.</span><span class="sxs-lookup"><span data-stu-id="fe143-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="fe143-121">Apsveriet iespēju izmantot periodisku pakešuzdevumu, lai jūsu visbiežāk izmantoto dimensiju kopu atjauninājumi būtu ātri.</span><span class="sxs-lookup"><span data-stu-id="fe143-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="fe143-122">Šādā veidā jūs palīdzat samazināt laiku, kas apgrozījuma bilances lietotājiem ir jāgaida.</span><span class="sxs-lookup"><span data-stu-id="fe143-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="fe143-123">Atjaunot bilances</span><span class="sxs-lookup"><span data-stu-id="fe143-123">Rebuild balances</span></span>

<span data-ttu-id="fe143-124">Izmantojiet pogu **Atjaunot bilances**, lai no jauna izveidotu bilances.</span><span class="sxs-lookup"><span data-stu-id="fe143-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="fe143-125">Šādā veidā jūs palīdzat nodrošināt, lai tie atbilstu Virsgrāmatas datiem.</span><span class="sxs-lookup"><span data-stu-id="fe143-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="fe143-126">Bilanču atjaunošanai ir vajadzīga liela pārstrāde, un parasti tā nav obligāta.</span><span class="sxs-lookup"><span data-stu-id="fe143-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="fe143-127">Ja ir scenārijs, kas regulāri pieprasa bilanču atjaunošanu, ieteicams sazināties ar klientu atbalsta dienestu.</span><span class="sxs-lookup"><span data-stu-id="fe143-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="fe143-128">Klientu atbalsts var palīdzēt noteikt, kāpēc bilances neatbilst Virsgrāmatas datiem.</span><span class="sxs-lookup"><span data-stu-id="fe143-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="fe143-129">Notīrīt bilances</span><span class="sxs-lookup"><span data-stu-id="fe143-129">Clear balances</span></span>

<span data-ttu-id="fe143-130">Izmantojiet pogu **Dzēst bilances**, lai noņemtu bilances un apturētu turpmākus atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="fe143-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="fe143-131">Dimensiju kopa vairs neietekmēs Virsgrāmatas grāmatošanas aktivitātes.</span><span class="sxs-lookup"><span data-stu-id="fe143-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="fe143-132">Papildinformāciju skatiet tēmā [Finanšu dimensijas](financial-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="fe143-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
