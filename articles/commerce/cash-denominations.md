---
title: Pārdošanas punkta (POS) skaidras naudas denomināciju konfigurēšana
description: Skaidras naudas denomināciju banknotēm un monētām var definēt operāciju uzskaites daļā, ko izmanto kasieri, pārdevēji un vadītāji veikalā POS ietvaros.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a34ae8084c0ad55221f4ab93eb8c6481fa8c4771
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023253"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a><span data-ttu-id="788d8-103">Pārdošanas punkta (POS) skaidras naudas denomināciju konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="788d8-103">Configure cash denominations for the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="788d8-104">Skaidras naudas denomināciju banknotēm un monētām var definēt operāciju uzskaites daļā, ko izmanto kasieri, pārdevēji un vadītāji veikalā POS ietvaros.</span><span class="sxs-lookup"><span data-stu-id="788d8-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="788d8-105">Šādas denominācijas var izmantot kā palīdzību skaidras naudas skatīšanas procesā dienas beigu uzskaites darījumos vai ātram pārdošanas norēķinam.</span><span class="sxs-lookup"><span data-stu-id="788d8-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="788d8-106">Denomināciju definēšana</span><span class="sxs-lookup"><span data-stu-id="788d8-106">Define denominations</span></span>

<span data-ttu-id="788d8-107">Denominācijas tiek iestatītas katram veikalam lapā **Iestatīšana** \> **Skaidras naudas deklarēšana** no veikala rekvizīta.</span><span class="sxs-lookup"><span data-stu-id="788d8-107">The denominations are set up per store on the **Set up** \> **Cash declaration** option from the store property page.</span></span>

![Opcija Skaidras naudas deklarēšana](./media/image1-denomination.png)

<span data-ttu-id="788d8-109">Denominācijas definēšana</span><span class="sxs-lookup"><span data-stu-id="788d8-109">To define a denomination:</span></span>

1. <span data-ttu-id="788d8-110">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="788d8-110">Click **New**.</span></span>
1. <span data-ttu-id="788d8-111">Norādiet tipu (monēta vai banknote).</span><span class="sxs-lookup"><span data-stu-id="788d8-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="788d8-112">Norādiet summu (vērtība).</span><span class="sxs-lookup"><span data-stu-id="788d8-112">Specify the amount (value).</span></span>

![Lapa Skaidras naudas deklarācijas denominācijas](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="788d8-114">Funkcionalitātes profila konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="788d8-114">Configure the functionality profile</span></span>

<span data-ttu-id="788d8-115">Maksājot skaidrā naudā POS, lietotājs var izmantot banknotes denominācijas, lai ātri ievadītu klienta samaksāto summu.</span><span class="sxs-lookup"><span data-stu-id="788d8-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="788d8-116">Funkcionalitātes profilā varat konfigurēt divas opcijas denominācijas rādīšanai POS.</span><span class="sxs-lookup"><span data-stu-id="788d8-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

- <span data-ttu-id="788d8-117">**Lielāks vai vienāds ar summu apmaksai** — pēc noklusējuma POS parāda tikai tādu banknošu denominācijas, kas ir lielākas par summu apmaksai, un tas ļauj norēķināties ar vienu pieskārienu.</span><span class="sxs-lookup"><span data-stu-id="788d8-117">**Greater or equal to amount due** – By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="788d8-118">Piemēram, ja summa apmaksai ir 7,50 USD, POS tiek rādītas šādas denominācijas: 10 USD, 20 USD, 50 USD un 100 USD.</span><span class="sxs-lookup"><span data-stu-id="788d8-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="788d8-119">Pieskaroties kādai no šīm summām, automātiski tiek veikti norēķini par šo summu.</span><span class="sxs-lookup"><span data-stu-id="788d8-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="788d8-120">1 USD un 5 USD banknotes netiek rādītas, jo šīs summas ir mazākas par summu apmaksai.</span><span class="sxs-lookup"><span data-stu-id="788d8-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>
- <span data-ttu-id="788d8-121">**Visas denominācijas** — atlasiet šo opciju, lai POS vienmēr rādītu visas denominācijas neatkarīgi no summas apmaksai.</span><span class="sxs-lookup"><span data-stu-id="788d8-121">**All denominations** – Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="788d8-122">Tas nozīmē, ka lietotājs var izmantot banknošu kombinācijas, lai sasniegtu summu apmaksai.</span><span class="sxs-lookup"><span data-stu-id="788d8-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="788d8-123">Piemēram, ja summa apmaksai ir 25,00 USD, lietotājs var izvēlēties 20 USD un 5 USD banknotes apmaksas pabeigšanai.</span><span class="sxs-lookup"><span data-stu-id="788d8-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>
