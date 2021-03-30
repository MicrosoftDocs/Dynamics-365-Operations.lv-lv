---
title: Grāmatoto nomas darījumu atsaukšana
description: Šajā tēmā skaidrots, kā atsaukt grāmatotos nomas darījumus. Jebkuru darījumu, kas tiek izveidots, izmantojot līdzekļu nomu, var atsaukt.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 22d8eee22221efaf5e7a715c8b95dff261bee62f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249729"
---
# <a name="reverse-posted-lease-transactions"></a><span data-ttu-id="1e9ca-104">Grāmatoto nomas darījumu atsaukšana</span><span class="sxs-lookup"><span data-stu-id="1e9ca-104">Reverse posted lease transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e9ca-105">Jebkuru darījumu, kas tiek izveidots, izmantojot līdzekļu nomu, var atsaukt.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-105">Any transaction that is created through Asset leasing can be reversed.</span></span> <span data-ttu-id="1e9ca-106">Darījumi, kas tiek atsaukti, izmantojot līdzekļu nomu, atjaunina jūsu nomas datus.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-106">Transactions that are reversed through Asset leasing update your lease data.</span></span> <span data-ttu-id="1e9ca-107">Tāpēc tās atjaunina arī nomas saistību un LLT uzskaites vērtības.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-107">Therefore, they also update the carrying values of the lease liability and right-of-use (ROU) asset.</span></span>

<span data-ttu-id="1e9ca-108">Lai izveidotu nomas atsaukšanas darījumu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-108">To create a reversing transaction for a lease, follow these steps.</span></span>

1. <span data-ttu-id="1e9ca-109">Lapā **Līdzekļu darījumi** vai **Saistību darījumi** atlasiet darījumu un pēc tam atlasiet **Atsaukt darījumu**.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-109">On either the **Asset transactions** page or the **Liability transactions** page, select the transaction, and then select **Reverse transaction**.</span></span>
2. <span data-ttu-id="1e9ca-110">Parādītajā dialoglodziņā varat labot datumu, kad tiks grāmatots atsaukšanas ieraksts.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-110">In the dialog box that appears, you can edit the date when the reversing entry will be posted.</span></span> <span data-ttu-id="1e9ca-111">Pēc noklusējuma lauks **Datums** ir iestatīts uz darījuma grāmatošanas datumu atlasītajam darījumam.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-111">By default, the **Date** field is set to the transaction posting date of the transaction that you selected.</span></span> <span data-ttu-id="1e9ca-112">Atsaukšanas ierakstu nevar grāmatot agrāk par atlasītā darījuma oriģinālo grāmatošanas datumu.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-112">The reversing entry can't be posted earlier than the original posting date of the selected transaction.</span></span>
3. <span data-ttu-id="1e9ca-113">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-113">Select **OK**.</span></span> <span data-ttu-id="1e9ca-114">Tiek grāmatots žurnāla ieraksts, kas atceļ atlasīto ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-114">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="1e9ca-115">Atcelšana tiek rādīta lapā **Līdzekļu darījumi** vai **Saistību darījumi**, un tiek atjaunināta pašreizējās bilances neto kopsumma, kas tiek rādīta lapā.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-115">The reversal is shown on the **Asset transactions** or **Liability transactions** page, and the net total of the current balance that is shown on the page is updated.</span></span>

<span data-ttu-id="1e9ca-116">Atlasot **Atsaukšanas izsekošana**, parādās dialoglodziņš, kas rāda gan sākotnējos darījumus, gan atsauktos darījumus kopā ar saistīto numuru, kas tiek saukts par *izsekošanas numuru*.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-116">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked number that is known as a *trace number*.</span></span> <span data-ttu-id="1e9ca-117">Lai atvieglotu atsaukšanas izpratni un uzlabotu redzamību, varat arī izsekot atsaukšanas, izmantojot nomas grafikus.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-117">To make the reversals easier to understand and to improve visibility, you can also track reversals by using the lease schedules.</span></span>

<span data-ttu-id="1e9ca-118">Lauks **Pēdējais žurnāla numurs** lapā **Grafiks** rāda darījumu žurnāla numurus.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-118">The **Latest journal number** field on the **Schedule** page shows the journal numbers of transactions.</span></span> <span data-ttu-id="1e9ca-119">Kad darbība ir atsaukta, šis lauks tiek atjaunināts ar atsaukšanas darījuma žurnāla numuru.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-119">When a transaction is reversed, this field is updated with the journal number of a reversing transaction.</span></span> <span data-ttu-id="1e9ca-120">Turklāt tiek atzīmēta izvēles rūtiņa **Atsaukts**, lai norādītu, ka darījums ir atsaukts, un ir atlasīts lauks **Grāmatots**.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-120">Additionally, the **Reversed** check box is selected to indicate that the transaction is reversed, and the **Posted** field is selected.</span></span>

## <a name="revoke-a-reversed-transaction"></a><span data-ttu-id="1e9ca-121">Anulētas darījuma atsaukšana</span><span class="sxs-lookup"><span data-stu-id="1e9ca-121">Revoke a reversed transaction</span></span>

<span data-ttu-id="1e9ca-122">Lai atsauktu anulētu darījumu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-122">To revoke a reversed transaction, follow these steps.</span></span>

1. <span data-ttu-id="1e9ca-123">Lapā **Grafiks** vai **Darījumi** atlasiet sākotnējo darījumu.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-123">On either the **Schedule** page or the **Transactions** page, select the original transaction.</span></span>
2. <span data-ttu-id="1e9ca-124">Izpildiet kādu no norādītajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-124">Follow one of these steps:</span></span>

    - <span data-ttu-id="1e9ca-125">Ja atlasījāt darījumu lapā **Grafiks**, sekojiet žurnāla izveides darbībām sadaļā [Ikmēneša žurnāla ierakstu izveide partijā](create-monthly-journals-batch.md).</span><span class="sxs-lookup"><span data-stu-id="1e9ca-125">If you selected the transaction on the **Schedule** page, follow the steps for creating a journal in [Create monthly journal entries in a batch](create-monthly-journals-batch.md).</span></span> <span data-ttu-id="1e9ca-126">Žurnāls ir manuāli jāgrāmato.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-126">You must manually post the journal.</span></span>
    - <span data-ttu-id="1e9ca-127">Ja atlasījāt darījumu lapā **Darījumi**, atlasiet **Atsaukt darījumu**.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-127">If you selected the transaction on the **Transactions** page, select **Reverse transaction**.</span></span> <span data-ttu-id="1e9ca-128">Tiek parādīts ziņojums, ka šī atsaukšana ir iepriekšējās anulēšanas atsaukšana, un jūs varat rediģēt grāmatošanas datumu šai atsaukšanai.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-128">You receive a message that states that this revocation is a revocation of an earlier reversal, and that you can edit the posting date for this revocation.</span></span> <span data-ttu-id="1e9ca-129">Tomēr vispārējās biznesa pārbaudes ietekmē datumus, kurus var ievadīt laukā **Datums**.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-129">However, general business validations affect the dates that can be entered in the **Date** field.</span></span> 

3. <span data-ttu-id="1e9ca-130">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-130">Select **OK**.</span></span> <span data-ttu-id="1e9ca-131">Tiek grāmatots žurnāla ieraksts, kas atceļ atlasīto ierakstu.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-131">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="1e9ca-132">Atsaukšana tiek rādīta lapā **Darījumi**, un neto kopējā pašreizējā bilance tiek atjaunota uz to, kas bija pirms pirmās atcelšanas.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-132">The reversal is shown on the **Transactions** page, and the net total current balance is restored to what it was before the first reversal.</span></span> <span data-ttu-id="1e9ca-133">Tāpēc ietekme, kas atsaukšanai ir uz bilancēm, tiek anulēta.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-133">Therefore, the impact that the reversal had on the balances is negated.</span></span>

<span data-ttu-id="1e9ca-134">Atlasot **Atsaukšanas izsekošana**, parādās dialoglodziņš, kas rāda gan sākotnējos darījumus, gan atsauktos darījumus kopā ar saistīto numuru.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-134">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked trace number.</span></span>

<span data-ttu-id="1e9ca-135">Varat arī izsekot atsaukšanu, izmantojot atbilstošo lapu **Grafiki**.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-135">You can also track revocations by using the appropriate **Schedules** page.</span></span> <span data-ttu-id="1e9ca-136">**Atgriešanas** lauks ir notīrīts, bet lauks **Žurnāls grāmatots** tiek atlasīts.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-136">The **Reverse** field is cleared, whereas the **Journal posted** field is selected.</span></span> <span data-ttu-id="1e9ca-137">Turklāt lauks **Pēdējais žurnāla numurs** tiek atjaunināts ar atsaukšanas darījuma žurnāla numuru un **Žurnāla numura** lauks tiek atjaunināts ar atgriešanas žurnāla numuru.</span><span class="sxs-lookup"><span data-stu-id="1e9ca-137">Additionally, the **Latest journal number** field is updated with the journal number of the revocation transaction, and the **Journal number** field is updated with the reversal journal number.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]