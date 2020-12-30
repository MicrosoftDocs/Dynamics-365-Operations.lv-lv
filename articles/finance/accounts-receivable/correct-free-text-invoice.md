---
title: Brīva teksta rēķina labošana
description: Šajā rakstā ir paskaidrots, kā labot brīva teksta rēķinu, kas jau ir iegrāmatots, un kā to vēlreiz izsniegt kā labotu rēķinu.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf6e7a070d7c151c6ff5d868f4f916359b82683
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445458"
---
# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="65d6f-103">Brīva teksta rēķina labošana</span><span class="sxs-lookup"><span data-stu-id="65d6f-103">Correct a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65d6f-104">Šajā rakstā ir paskaidrots, kā labot brīva teksta rēķinu, kas jau ir iegrāmatots, un kā to vēlreiz izsniegt kā labotu rēķinu.</span><span class="sxs-lookup"><span data-stu-id="65d6f-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="65d6f-105">Lai labotu brīva teksta rēķinu, kas jau ir grāmatots, atveriet iegrāmatoto brīva teksta rēķinu.</span><span class="sxs-lookup"><span data-stu-id="65d6f-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="65d6f-106">Lapā **Rēķins** atlasiet vienumu **Atcelt** un pēc tam — **Labot rēķinu**.</span><span class="sxs-lookup"><span data-stu-id="65d6f-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="65d6f-107">Atlasiet iemesla kodu, pievienojiet komentārus un atlasiet datumu jaunajam labotajam rēķinam.</span><span class="sxs-lookup"><span data-stu-id="65d6f-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="65d6f-108">Varat modificēt laboto rēķinu un to grāmatot.</span><span class="sxs-lookup"><span data-stu-id="65d6f-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="65d6f-109">Kad grāmatojat laboto rēķinu, tiek izveidots atcelšanas rēķins par kredīta summu, kas ir vienāda ar sākotnējā rēķina summu.</span><span class="sxs-lookup"><span data-stu-id="65d6f-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="65d6f-110">Līdz ar to sākotnējā rēķina un atcelšanas rēķina apvienotā bilance ir 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="65d6f-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="65d6f-111">Atcelšanas rēķins tiek segts pret sākotnējo rēķinu.</span><span class="sxs-lookup"><span data-stu-id="65d6f-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="65d6f-112">Pēc labotā rēķina grāmatošanas jums ir trīs rēķini:</span><span class="sxs-lookup"><span data-stu-id="65d6f-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="65d6f-113">**Sākotnējais rēķins** — rēķins, kas ietver informāciju, kuru jūs labojat.</span><span class="sxs-lookup"><span data-stu-id="65d6f-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="65d6f-114">**Atcelšanas rēķins** — sistēmas ģenerēts kredītrēķins, kas tika izveidots, lai atceltu pēdējo laboto rēķinu.</span><span class="sxs-lookup"><span data-stu-id="65d6f-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="65d6f-115">**Labotais rēķins** — rēķins, kas ietver labotā rēķina informāciju.</span><span class="sxs-lookup"><span data-stu-id="65d6f-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="65d6f-116">Atcelšanas un labošanas rēķinus varat identificēti divējādi:</span><span class="sxs-lookup"><span data-stu-id="65d6f-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="65d6f-117">Lapā **Visi brīva teksta rēķini** ietver kolonnu **Labojums**, kur varat redzēt, kuri rēķini ir atcelšanas rēķini un labotie rēķini.</span><span class="sxs-lookup"><span data-stu-id="65d6f-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="65d6f-118">Brīva teksta rēķina virsrakstā ir redzams statuss **Atcelšanas rēķins '\[rēķina numurs\]'** vai **Labotais rēķins '\[rēķina numurs\]'**.</span><span class="sxs-lookup"><span data-stu-id="65d6f-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="65d6f-119">Šis līdzeklis ir pieejams tikai tad, ja ir atlasīta konfigurācijas atslēga **Brīva teksta rēķina labojums**.</span><span class="sxs-lookup"><span data-stu-id="65d6f-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span> <span data-ttu-id="65d6f-120">Papildinformācijai par to, kā iespējot konfigurācijas atslēgas, skatiet tēmu Iespējot (vai atspējot) konfigurācijas atslēgas [Uzturēšanas režīms](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="65d6f-120">For more information on how to enable Configuration keys refer to the Enable (or disable) configuration keys section in the [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) topic.</span></span> 



