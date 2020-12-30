---
title: Žurnālā grāmatoto ierakstu reģistrēšana žurnālā
description: Šajā procedūrā parādīts, kā reģistrēt žurnālā iegrāmatotos žurnāla ierakstus.
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f50ee568df492bcd811d2fefb1784bb55b50384b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445519"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="0d6a8-103">Žurnālā grāmatoto ierakstu reģistrēšana žurnālā</span><span class="sxs-lookup"><span data-stu-id="0d6a8-103">Journalize posted journal entries</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d6a8-104">Šajā procedūrā parādīts, kā reģistrēt žurnālā iegrāmatotos žurnāla ierakstus.</span><span class="sxs-lookup"><span data-stu-id="0d6a8-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="0d6a8-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="0d6a8-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="0d6a8-106">Sadaļā **Navigācijas rūts** dodieties uz **Moduļi > Virsgrāmata > Virsgrāmatas uzstādījumi > Virsgrāmatas parametri**.</span><span class="sxs-lookup"><span data-stu-id="0d6a8-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="0d6a8-107">Lauku **Paplašinātā virsgrāmata** var iestatīt uz Jā vai Nē.</span><span class="sxs-lookup"><span data-stu-id="0d6a8-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="0d6a8-108">Ja jā, pārskatu izvades var atšķirties.</span><span class="sxs-lookup"><span data-stu-id="0d6a8-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="0d6a8-109">Atlasiet vai periods var būt slēgts, ja reģistrācijas žurnāla process nav izpildīts.</span><span class="sxs-lookup"><span data-stu-id="0d6a8-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="0d6a8-110">Ja šī opcija ir iestatīta uz Jā, periodu nevar slēgt, kamēr attiecīgajam periodam netiek izpildīts reģistrācijas žurnāla process.</span><span class="sxs-lookup"><span data-stu-id="0d6a8-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="0d6a8-111">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0d6a8-111">Close the page.</span></span>
5. <span data-ttu-id="0d6a8-112">Sadaļā **Navigācijas rūts** dodieties uz **Moduļi > Virsgrāmata > Periodiski uzdevumi > Reģistrācija žurnālā**.</span><span class="sxs-lookup"><span data-stu-id="0d6a8-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="0d6a8-113">Noklikšķiniet uz **Filtrēt**.</span><span class="sxs-lookup"><span data-stu-id="0d6a8-113">Click **Filter**.</span></span>
7. <span data-ttu-id="0d6a8-114">Iezīmējiet rindu ar filtra kritēriju, kuru vēlaties definēt.</span><span class="sxs-lookup"><span data-stu-id="0d6a8-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="0d6a8-115">Laukā **Kritēriji** ievadiet vai atlasiet filtra kritērijus.</span><span class="sxs-lookup"><span data-stu-id="0d6a8-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="0d6a8-116">Noklikšķiniet uz **Labi**, lai aizvērtu filtra lapu.</span><span class="sxs-lookup"><span data-stu-id="0d6a8-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="0d6a8-117">Noklikšķiniet uz **Labi**, lai uzsāktu reģistrāciju žurnālā.</span><span class="sxs-lookup"><span data-stu-id="0d6a8-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="0d6a8-118">Kad process ir pabeigts, tiek ģenerēts pārskats.</span><span class="sxs-lookup"><span data-stu-id="0d6a8-118">A report will be generated after the process is complete.</span></span>  

