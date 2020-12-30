---
title: Īstermiņa nomas saistību pārklasificēšana
description: Šajā tēmā skaidrots, kā izveidot mēneša žurnāla ierakstu, lai pārklasificētu nomas saistību daļu kā īstermiņa.
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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 46bcd396c93bc1d2944241165d438f8ccc013e20
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445783"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="ce18a-103">Īstermiņa nomas saistību pārklasificēšana</span><span class="sxs-lookup"><span data-stu-id="ce18a-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce18a-104">Šajā tēmā skaidrots, kā izveidot mēneša žurnāla ierakstu, lai pārklasificētu nomas saistību daļu kā īstermiņa.</span><span class="sxs-lookup"><span data-stu-id="ce18a-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="ce18a-105">Kad pakešuzdevuma procesā atlasītais grafiks ir **Īstermiņa nomas saistību pārklasificēšana**, tiek izveidots žurnāla ieraksts.</span><span class="sxs-lookup"><span data-stu-id="ce18a-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="ce18a-106">Šo ierakstu izmanto, lai grāmatotu nomas saistību pašreizējo daļu mēneša pēdējā dienā.</span><span class="sxs-lookup"><span data-stu-id="ce18a-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="ce18a-107">Tajā pašā laikā atgriešanas ieraksts tiek grāmatots no nākamā mēneša pirmās dienas.</span><span class="sxs-lookup"><span data-stu-id="ce18a-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="ce18a-108">Nomas saistību īstermiņa daļa tiek rādīta saistību amortizācijas grafikā.</span><span class="sxs-lookup"><span data-stu-id="ce18a-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="ce18a-109">Kad žurnāla ieraksts ir iegrāmatots, kļūst pieejama kolonna **Izveidots saistību pārkvalificēšanas žurnāls**, un žurnāla ID tiek norādīts arī grafikā.</span><span class="sxs-lookup"><span data-stu-id="ce18a-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="ce18a-110">Lai izveidotu un grāmatotu īstermiņa saistību pārklasificēšanas žurnāla ierakstu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="ce18a-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="ce18a-111">Doties uz **Līdzekļa noma \> Periodisks \> Žurnāla izveide partijā**.</span><span class="sxs-lookup"><span data-stu-id="ce18a-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="ce18a-112">Dialoglodziņa **Žurnāla izveide partijā** laukā **Atlasīt grafiku** atlasiet **Īstermiņa nomas saistību pārklasificēšana**.</span><span class="sxs-lookup"><span data-stu-id="ce18a-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="ce18a-113">Laukā **Nomas grupa** atlasiet nomas grupu.</span><span class="sxs-lookup"><span data-stu-id="ce18a-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="ce18a-114">Vai arī laukā **Grāmatas ID** atlasiet grāmatas ID.</span><span class="sxs-lookup"><span data-stu-id="ce18a-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="ce18a-115">Ieslēdziet parametru **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="ce18a-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="ce18a-116">Pretējā gadījumā, ja ieraksts ir jāizveido, bet nav jāgrāmato, atstājiet šo parametru izslēgtu.</span><span class="sxs-lookup"><span data-stu-id="ce18a-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="ce18a-117">Ieslēdziet parametru **Priekšskatīt pirms grāmatošanas**, lai skatītu ierakstu pirms tā grāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="ce18a-117">Turn on the **Preview before posting** parameter to view the entry before it's posted.</span></span>
6. <span data-ttu-id="ce18a-118">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ce18a-118">Select **OK**.</span></span>
