---
title: Laika logi
description: Laika logus varat izmantot, lai optimizētu pakalpojuma pasūtījumu rindu plānošanas.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63a166806c2c8ac84cc1d71d6ec84fcb28033feb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206523"
---
# <a name="time-windows"></a><span data-ttu-id="1ebd5-103">Laika logi</span><span class="sxs-lookup"><span data-stu-id="1ebd5-103">Time windows</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ebd5-104">Laika logus varat izmantot, lai optimizētu pakalpojuma pasūtījumu rindu plānošanas.</span><span class="sxs-lookup"><span data-stu-id="1ebd5-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="1ebd5-105">Sistēmu var iestatīt tā, lai tajā automātiski tiktu izveidoti pakalpojumu pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="1ebd5-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="1ebd5-106">Pamatojoties uz laika loga norādītajiem kritērijiem, vēlamo skaitu pakalpojumu pasūtījumu rindu varat savienot ar vēlamo skaitu pakalpojumu pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="1ebd5-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="1ebd5-107">Laika logi nosaka, cik tālu pakalpojuma pasūtījuma rinda var pārvietoties no sava aprēķinātā datuma.</span><span class="sxs-lookup"><span data-stu-id="1ebd5-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="1ebd5-108">Aprēķinātais datums ir datums, kurā tika planota pakalpojuma pasūtījuma rindas parādīšanās.</span><span class="sxs-lookup"><span data-stu-id="1ebd5-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="1ebd5-109">Šis datums ir atkarīgs no tā intervāla iestatījuma un pakalpojuma perioda, ko definējāt lapā **Pakalpojumu pasūtījumu izveide**.</span><span class="sxs-lookup"><span data-stu-id="1ebd5-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="1ebd5-110">Jūs definējat laika logu, izmantojot vērtības šajā tabulā:</span><span class="sxs-lookup"><span data-stu-id="1ebd5-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="1ebd5-111">Metode</span><span class="sxs-lookup"><span data-stu-id="1ebd5-111">Method</span></span> | <span data-ttu-id="1ebd5-112">apraksts</span><span class="sxs-lookup"><span data-stu-id="1ebd5-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ebd5-113">Nedēļa</span><span class="sxs-lookup"><span data-stu-id="1ebd5-113">Week</span></span>   | <span data-ttu-id="1ebd5-114">Datums, kad pakalpojuma pasūtījuma rindu var pārvietot uz jebkuru pieejamo dienu sākotnējā aprēķinātā datuma nedēļā.</span><span class="sxs-lookup"><span data-stu-id="1ebd5-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="1ebd5-115">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="1ebd5-115">Month</span></span>  | <span data-ttu-id="1ebd5-116">Datums, kad pakalpojuma pasūtījuma rindu var pārvietot uz jebkuru pieejamo dienu sākotnējā aprēķinātā datuma mēnesī.</span><span class="sxs-lookup"><span data-stu-id="1ebd5-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="1ebd5-117">Piemēram, pakalpojuma pasūtījuma rindas aprēķinātais datums ir 2017. gada 15. februāris.</span><span class="sxs-lookup"><span data-stu-id="1ebd5-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="1ebd5-118">Pakalpojuma pasūtījuma rindu var ieplānot jebkurā nedēļas dienā no 2017. gada 1. februāra līdz 28. februārim.</span><span class="sxs-lookup"><span data-stu-id="1ebd5-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="1ebd5-119">Manuāli</span><span class="sxs-lookup"><span data-stu-id="1ebd5-119">Manual</span></span> | <span data-ttu-id="1ebd5-120">Jūs nosakāt maksimālo dienu skaitu pirms vai pēc sākotnējā aprēķinātā datuma, uz kuru var pārvietot pakalpojuma pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="1ebd5-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="1ebd5-121">Ja pakalpojumu līguma rindai nenorādāt laika logu, tad pakalpojuma pasūtījuma rinda, kas ir atvasināta no pakalpojumu līguma, ir jāizpilda tieši tajā datumā, kurā tā tika sākotnēji ieplānota.</span><span class="sxs-lookup"><span data-stu-id="1ebd5-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ebd5-122">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="1ebd5-122">Related topics</span></span>

[<span data-ttu-id="1ebd5-123">Laika loga izveide</span><span class="sxs-lookup"><span data-stu-id="1ebd5-123">Create time windows</span></span>](create-time-windows.md)

