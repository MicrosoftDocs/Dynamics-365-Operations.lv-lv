---
title: Prece ir aizturēta šāda veida darījumiem
description: Pēc plānošanas pasūtījumu apstiprināšanas tiek saņemts kļūdas ziņojums, kurā norādīts, ka krājums ir aizturēts darījumiem.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301283"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="05787-103">Prece ir aizturēta šāda veida darījumiem</span><span class="sxs-lookup"><span data-stu-id="05787-103">Product is on hold for transactions</span></span>

<span data-ttu-id="05787-104">Kļūdas kods: SYS13295</span><span class="sxs-lookup"><span data-stu-id="05787-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="05787-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="05787-105">Symptoms</span></span>

<span data-ttu-id="05787-106">Pēc plānoto pasūtījumu apstiprināšanas saņemsit šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="05787-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="05787-107">Krājums %1 pašlaik ir aizturēts darbībām %2.</span><span class="sxs-lookup"><span data-stu-id="05787-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="05787-108">Iemesls</span><span class="sxs-lookup"><span data-stu-id="05787-108">Cause</span></span>

<span data-ttu-id="05787-109">Aprakstot bloķētos krājumus, sistēma lieto tādus savstarpēji aizvietojamus jēdzienus kā *bloķēti*, *apturēti* un *aizturēti*.</span><span class="sxs-lookup"><span data-stu-id="05787-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="05787-110">Šī kļūda nozīmē, ka noklusējuma pasūtījuma iestatījumos krājums ir iestatīts kā **Apturēts**.</span><span class="sxs-lookup"><span data-stu-id="05787-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="05787-111">Ja krājums tiek bloķēts un jūs pievienojat to pirkšanas pasūtījuma vai pārdošanas pasūtījuma rindai, saņemat brīdinājuma ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="05787-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="05787-112">Kad krājums ir bloķēts, inventāra transakcijas, kas saistītas ar pirkšanas pasūtījumu vai pārdošanas pasūtījumu līniju, nevar modificēt (piemēram, gramatojot pavadzīmi vai rēķinu).</span><span class="sxs-lookup"><span data-stu-id="05787-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="05787-113">Varat bloķēt iegādātu krājumu un vienlaicīgi pārdot šo krājumu.</span><span class="sxs-lookup"><span data-stu-id="05787-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="05787-114">Tādā gadījumā izvēles rūtiņa **Apturēts** tiek atlasīta pirkšanas pasūtījumā, bet krājums nav bloķēts krājumos vai pārdošanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="05787-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="05787-115">Tālāk ir norādīti daži nosacījumi, kuru dēļ krājuma kods var tikt bloķēts pārdošanai:</span><span class="sxs-lookup"><span data-stu-id="05787-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="05787-116">Krājums joprojām tiek izstrādāts vai ražots.</span><span class="sxs-lookup"><span data-stu-id="05787-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="05787-117">Tādēļ nevēlaties to pārdot vai rezervēt.</span><span class="sxs-lookup"><span data-stu-id="05787-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="05787-118">Jūs esat saņēmis daudzus bojātus krājumus, un defekti jāizlabo, pirms krājumu var pārdot.</span><span class="sxs-lookup"><span data-stu-id="05787-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="05787-119">Šāda veida gadījumos, jūs varat bloķēt šo krājumu līdz brīdim, kad problēma ir novērsta.</span><span class="sxs-lookup"><span data-stu-id="05787-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="05787-120">Ja krājums ir bloķēts un jūs izveidojat atgriešanas pasūtījuma rindu, jūs saņemat ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="05787-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="05787-121">Nevar bloķēt krājumu sēriju vai laidienu.</span><span class="sxs-lookup"><span data-stu-id="05787-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="05787-122">Ja krājuma daļas ir jābloķē, var bloķēt tās, pārvietojot krājumu vai bloķējot pilnu krājumu tam periodam.</span><span class="sxs-lookup"><span data-stu-id="05787-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="05787-123">Novēršana</span><span class="sxs-lookup"><span data-stu-id="05787-123">Resolution</span></span>

- <span data-ttu-id="05787-124">Atveriet lapu **Noklusējuma pasūtījuma iestatījumi** un noņemiet izvēles rūtiņas **Apturēts** atzīmi.</span><span class="sxs-lookup"><span data-stu-id="05787-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
