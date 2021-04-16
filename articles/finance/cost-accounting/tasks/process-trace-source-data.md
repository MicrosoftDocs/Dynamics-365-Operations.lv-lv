---
title: Avota datu apstrāde un izsekošana
description: Visu datu apstrādi nodrošina darbi.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34612469f763cf1b30be46ff088605ae22883022
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841001"
---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="b40bf-103">Avota datu apstrāde un izsekošana</span><span class="sxs-lookup"><span data-stu-id="b40bf-103">Process and trace source data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b40bf-104">Visu datu apstrādi nodrošina darbi.</span><span class="sxs-lookup"><span data-stu-id="b40bf-104">All data processing is run by jobs.</span></span> <span data-ttu-id="b40bf-105">Katra darba un datu nodrošinātāja dokumentam tiek izveidots žurnāls par to, ka process tika palaists un ka ieraksti pašreizējā darbā tika apstrādāti.</span><span class="sxs-lookup"><span data-stu-id="b40bf-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="b40bf-106">Izmantojiet šo procedūru, lai iestatītu datu avotu un pēc tam izsekotu noteikta izmaksu ieraksta izcelsmi.</span><span class="sxs-lookup"><span data-stu-id="b40bf-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="b40bf-107">Šajā ierakstā tiek izmantots USP2 demonstrācijas datu uzņēmums USP2.</span><span class="sxs-lookup"><span data-stu-id="b40bf-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="b40bf-108">Pirms varat pabeigt šo uzdevumu, atskaņojiet šādus uzdevuma ceļvežus: "Izmaksu uzskaites virsgrāmatas izveide", "Izmaksu vadības ierīču definēšana" un "Izmaksu uzskaites virsgrāmatas datu avota pārvaldība".</span><span class="sxs-lookup"><span data-stu-id="b40bf-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="b40bf-109">Dodieties uz Izmaksu uzskaite > Virsgrāmatas iestatīšana > Izmaksu uzskaites virsgrāmatas.</span><span class="sxs-lookup"><span data-stu-id="b40bf-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="b40bf-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b40bf-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b40bf-111">Atlasiet iepriekš izveidoto izmaksu uzskaites virsgrāmatu.</span><span class="sxs-lookup"><span data-stu-id="b40bf-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="b40bf-112">Noklikšķiniet uz Faktiskās versijas.</span><span class="sxs-lookup"><span data-stu-id="b40bf-112">Click Actual versions.</span></span>
4. <span data-ttu-id="b40bf-113">Darbības rūtī noklikšķiniet uz Avota datu apstrāde.</span><span class="sxs-lookup"><span data-stu-id="b40bf-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="b40bf-114">Noklikšķiniet uz Virsgrāmatas ierakstu pārsūtīšanas žurnāli.</span><span class="sxs-lookup"><span data-stu-id="b40bf-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="b40bf-115">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b40bf-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="b40bf-116">Noklikšķiniet uz Žurnāla ieraksti.</span><span class="sxs-lookup"><span data-stu-id="b40bf-116">Click Journal entries.</span></span>
8. <span data-ttu-id="b40bf-117">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="b40bf-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b40bf-118">Noklikšķiniet uz Izmaksu ieraksti.</span><span class="sxs-lookup"><span data-stu-id="b40bf-118">Click Cost entries.</span></span>
10. <span data-ttu-id="b40bf-119">Noklikšķiniet uz Avota ieraksts.</span><span class="sxs-lookup"><span data-stu-id="b40bf-119">Click Source entry.</span></span>
11. <span data-ttu-id="b40bf-120">Darbības rūtī noklikšķiniet uz Avota datu apstrāde.</span><span class="sxs-lookup"><span data-stu-id="b40bf-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="b40bf-121">Noklikšķiniet uz Virsgrāmata.</span><span class="sxs-lookup"><span data-stu-id="b40bf-121">Click General ledger.</span></span>
13. <span data-ttu-id="b40bf-122">Laukā Finanšu kalendāra periods ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="b40bf-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="b40bf-123">Šim piemēram atlasiet 2017. finanšu gads, 9. periods.</span><span class="sxs-lookup"><span data-stu-id="b40bf-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="b40bf-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="b40bf-124">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]