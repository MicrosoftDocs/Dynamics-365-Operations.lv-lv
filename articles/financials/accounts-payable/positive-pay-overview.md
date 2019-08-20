---
title: Pozitīvā maksājuma pārskats
description: Šajā rakstā ir sniegta informācija par pozitīvo maksājumu, kas tiek izmantots, lai izveidotu elektronisku čeku sarakstu, ko var iesniegt bankā.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2ba23cf5afe9f007f5e32a75e918595929ad79a1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834613"
---
# <a name="positive-pay-overview"></a><span data-ttu-id="a292d-103">Pozitīvā maksājuma pārskats</span><span class="sxs-lookup"><span data-stu-id="a292d-103">Positive pay overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a292d-104">Šajā rakstā ir sniegta informācija par pozitīvo maksājumu, kas tiek izmantots, lai izveidotu elektronisku čeku sarakstu, ko var iesniegt bankā.</span><span class="sxs-lookup"><span data-stu-id="a292d-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="a292d-105">Pozitīvais maksājums tiek izmantots, lai izveidotu elektronisku čeku sarakstu, ko var iesniegt bankā.</span><span class="sxs-lookup"><span data-stu-id="a292d-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="a292d-106">Pozitīvā maksājuma faili var bankām palīdzēt novērst krāpšanos ar čekiem.</span><span class="sxs-lookup"><span data-stu-id="a292d-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="a292d-107">Katru reizi, izdrukājot čekus, tiek iestatīts pozitīvais maksājums, lai izveidotu elektronisko čeku sarakstu.</span><span class="sxs-lookup"><span data-stu-id="a292d-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="a292d-108">Pēc tam, iesniedzot čeku bankā, tas tiek salīdzināts ar iepriekš iesniegto čeku sarakstu.</span><span class="sxs-lookup"><span data-stu-id="a292d-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="a292d-109">Ja čeks atbilst čekam sarakstā, banka to dzēš.</span><span class="sxs-lookup"><span data-stu-id="a292d-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="a292d-110">Ja čeks neatbilst čekam sarakstā, banka to aiztur uz pārskatīšanu.</span><span class="sxs-lookup"><span data-stu-id="a292d-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="a292d-111">Pozitīvo maksājumu sauc arī par SafePay.</span><span class="sxs-lookup"><span data-stu-id="a292d-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="a292d-112">Pozitīvo maksājumu faili var saturēt konfidenciālu informāciju par maksājumu saņēmējiem un čeku summām.</span><span class="sxs-lookup"><span data-stu-id="a292d-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="a292d-113">Šī iemesla dēļ nodrošiniet, lai no failu ģenerēšanas, līdz to saņemšanai bankā, tiek veikti atbilstoši drošības pasākumi.</span><span class="sxs-lookup"><span data-stu-id="a292d-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="a292d-114">Pozitīvā maksājuma faili tiek lejupielādēti saskaņā ar tīmekļa pārlūkprogrammas lejupielādes instrukcijām.</span><span class="sxs-lookup"><span data-stu-id="a292d-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="a292d-115">Pozitīvā maksājuma faili tiek izveidoti, izmantojot datu elementus.</span><span class="sxs-lookup"><span data-stu-id="a292d-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="a292d-116">Lai varētu izveidot pozitīvā maksājuma failu, vispirms ir jāiestata XML transformācijas formāti, kas pārveido datus bankai izmantojamā formātā.</span><span class="sxs-lookup"><span data-stu-id="a292d-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="a292d-117">Katram bankas kontam, kuram vēlaties ģenerēt pozitīvā maksājuma datus, jāpiešķir pozitīvā maksājuma formāts.</span><span class="sxs-lookup"><span data-stu-id="a292d-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="a292d-118">Kad maksājumi ir izveidoti, var izveidot pozitīvā maksājuma failu vienai juridiskajai personai un vienam bankas kontam.</span><span class="sxs-lookup"><span data-stu-id="a292d-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="a292d-119">Papildus var izveidot pozitīvo maksājumu failus vairākām juridiskajām personām un bankas kontiem vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="a292d-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="a292d-120">Kad čeki ir ievietoti sarakstā un pozitīvā maksājuma fails ir apmaksāts, banka jums nosūta apstiprinājuma numuru.</span><span class="sxs-lookup"><span data-stu-id="a292d-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="a292d-121">Pēc tam varat konfigurēt pozitīvā maksājuma failu programmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a292d-121">You can then confirm the positive pay file in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="a292d-122">Ja pozitīvā maksājuma fails ir jāmaina, to var atsaukt.</span><span class="sxs-lookup"><span data-stu-id="a292d-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="a292d-123">Pēc tam katra pozitīvā maksājuma failā tiek atiestatīts lauks, kas norāda, vai šis čeks ir iekļauts pozitīvā maksājuma failā.</span><span class="sxs-lookup"><span data-stu-id="a292d-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="a292d-124">Papildinformāciju skatiet tēmā [Pozitīvā maksājuma failu iestatīšana un ģenerēšana](set-up-generate-positive-pay-files.md).</span><span class="sxs-lookup"><span data-stu-id="a292d-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>



