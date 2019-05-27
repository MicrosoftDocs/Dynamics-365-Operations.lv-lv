---
title: Uzskaites avota pārlūks
description: Šajā rakstā ir sniegta informācija par uzskaites avota pārlūku, kuru var izmantot detalizētai virsgrāmatas uzskaites ierakstu avota informācijas analīzei.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de5de039c0e3332943bae4846768fc628810906e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559378"
---
# <a name="accounting-source-explorer"></a><span data-ttu-id="a4a99-103">Uzskaites avota pārlūks</span><span class="sxs-lookup"><span data-stu-id="a4a99-103">Accounting source explorer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4a99-104">Šajā rakstā ir sniegta informācija par uzskaites avota pārlūku, kuru var izmantot detalizētai virsgrāmatas uzskaites ierakstu avota informācijas analīzei.</span><span class="sxs-lookup"><span data-stu-id="a4a99-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="a4a99-105">Uzskaites avota pārlūks ir jauna lapa, kas parāda avota informāciju.</span><span class="sxs-lookup"><span data-stu-id="a4a99-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="a4a99-106">Uzskaites avota pārlūku varat izmantot vai nu kā savrupu rīku, vai arī, lai analizētu virsgrāmatas uzskaites ierakstu detalizētos datus.</span><span class="sxs-lookup"><span data-stu-id="a4a99-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="a4a99-107">Uzskaites avota pārlūku varat izmantot, piemēram, lai iegūt visdetalizētāko apgrozījuma bilances vai dokumenta transakcijas avota informāciju.</span><span class="sxs-lookup"><span data-stu-id="a4a99-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="a4a99-108">Pēc tam varat izmantot līdzekli Eksportēt uz programmu MS EXcel, lai veiktu informācijas papildu apstrādi programmā Microsoft Excel (piemēram, tabulā PivotTable vai PivotTable atskaitē).</span><span class="sxs-lookup"><span data-stu-id="a4a99-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="a4a99-109">Uzskaites avota pārlūkā vienas un tās pašas kopsummas katram virsgrāmatas kontam vienmēr tiek rādītas kā Vispārīgas virsgrāmatas (piemēram, Apgrozījuma bilance).</span><span class="sxs-lookup"><span data-stu-id="a4a99-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="a4a99-110">Apgrozījuma bilancē segmentus var parādīt atsevišķās kolonnās.</span><span class="sxs-lookup"><span data-stu-id="a4a99-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="a4a99-111">Vienkārši izvēlieties atbilstošu finanšu dimensiju kopu.</span><span class="sxs-lookup"><span data-stu-id="a4a99-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="a4a99-112">Parametrus var izmantot, lai definētu datumu intervālu analīzei.</span><span class="sxs-lookup"><span data-stu-id="a4a99-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="a4a99-113">Šī funkcionalitāte ir līdzīga apgrozījuma bilances funkcionalitātei.</span><span class="sxs-lookup"><span data-stu-id="a4a99-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="a4a99-114">Visiem dokumentiem, kas izmanto pirmdokumenta struktūru, uzskaites avotu pārlūkā tiek rādīta papildinformācija, pamatojoties uz uzskaites sadalēm un, ja piemērojams, projekta uzskaites sadalēm.</span><span class="sxs-lookup"><span data-stu-id="a4a99-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="a4a99-115">Šī informācija ietver naudas summas tipu, projektu, aktivitāti, kategoriju un rindas rekvizītu.</span><span class="sxs-lookup"><span data-stu-id="a4a99-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="a4a99-116">Tālāk ir sniegti daži iespējamās analīzes piemēri.</span><span class="sxs-lookup"><span data-stu-id="a4a99-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="a4a99-117">Novirzes starp pirkšanas pasūtījumiem un kreditora rēķiniem, jo katras novirzes ir sniegtas, izmantojot naudas summas veidu, piemēram, maksas novirze.</span><span class="sxs-lookup"><span data-stu-id="a4a99-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="a4a99-118">Apmaksājamās un neapmaksājamās stundas un izdevumi projektam, biznesa vienībai un galvenajam kontam.</span><span class="sxs-lookup"><span data-stu-id="a4a99-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="a4a99-119">Avota dokumentiem, kas izmanto pirmdokumenta atsauces identitātes koncepciju, uzskaites avota pārlūks rāda vēl sīkāku informāciju, piemēram, debitoru, kreditoru, darbinieku, preces, daudzumu, vienību tekstu un aprakstus.</span><span class="sxs-lookup"><span data-stu-id="a4a99-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="a4a99-120">Tālāk ir sniegti daži iespējamās analīzes piemēri.</span><span class="sxs-lookup"><span data-stu-id="a4a99-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="a4a99-121">Viesnīcas izdevumi katrai biznesa vienībai un viesnīcas zīmols finanšu periodā, pamatojoties uz izdevumu pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="a4a99-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="a4a99-122">Atlaides kreditoriem, precēm, nodaļām</span><span class="sxs-lookup"><span data-stu-id="a4a99-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="a4a99-123">Šiem dokumentiem no uzskaites avota pārlūka var pārvietoties uz faktisko pirmdokumentu.</span><span class="sxs-lookup"><span data-stu-id="a4a99-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>



