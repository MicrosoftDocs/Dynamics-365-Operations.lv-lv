--- 
title: "Svītrkodu veidu uzturēšana"
description: "Šajā procedūrā parādīts, kā iestatīt jaunu svītrkoda definīciju, ko pēc tam var izmantot kā daļu no izdošanas saraksta pārskata."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a0d7092228f078f528ec1cb9ac56d7034c44bccf
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="maintain-barcode-types"></a><span data-ttu-id="d24ad-103">Svītrkodu veidu uzturēšana</span><span class="sxs-lookup"><span data-stu-id="d24ad-103">Maintain barcode types</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d24ad-104">Šajā procedūrā parādīts, kā iestatīt jaunu svītrkoda definīciju, ko pēc tam var izmantot kā daļu no izdošanas saraksta pārskata.</span><span class="sxs-lookup"><span data-stu-id="d24ad-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="d24ad-105">Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="d24ad-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="d24ad-106">Ja izmantojat USMF varat izmantot piemēra vērtības, kas parādītas.</span><span class="sxs-lookup"><span data-stu-id="d24ad-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="d24ad-107">Šos uzdevumus parasti veic noliktavas pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="d24ad-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="d24ad-108">Dodieties uz sadaļu Svītrkodi.</span><span class="sxs-lookup"><span data-stu-id="d24ad-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="d24ad-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d24ad-109">Click New.</span></span>
3. <span data-ttu-id="d24ad-110">Laukā Svītrkodu iestatījumi ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="d24ad-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="d24ad-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="d24ad-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d24ad-112">Atlasiet opciju laukā Svītrkoda tips.</span><span class="sxs-lookup"><span data-stu-id="d24ad-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="d24ad-113">Ja izmantojat USMF, varat atlasīt "Kods 39".</span><span class="sxs-lookup"><span data-stu-id="d24ad-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="d24ad-114">Ievadiet skaitli laukā Lielums.</span><span class="sxs-lookup"><span data-stu-id="d24ad-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="d24ad-115">Ievadiet skaitli laukā Maksimālais garums.</span><span class="sxs-lookup"><span data-stu-id="d24ad-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="d24ad-116">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d24ad-116">Click Save.</span></span>
9. <span data-ttu-id="d24ad-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d24ad-117">Close the page.</span></span>
10. <span data-ttu-id="d24ad-118">Dodieties uz sadaļu Krājumu un noliktavas vadības parametri.</span><span class="sxs-lookup"><span data-stu-id="d24ad-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="d24ad-119">Ievadiet vai atlasiet vērtību laukā Svītrkodu iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="d24ad-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="d24ad-120">Atlasiet svītrkoda iestatījumu, ko izveidojāt iepriekš, taču ņemiet vērā, ka svītrkoda formātam jāatbilst unikālā identifikatora formātam procesā izmantojamajam ieraksta tipam.</span><span class="sxs-lookup"><span data-stu-id="d24ad-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="d24ad-121">Piemēram, izdošanas maršrutiem svītrkoda formātam ir jāatbilst izdošanas maršruta atsauces formātam, kas parasti ir numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="d24ad-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="d24ad-122">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d24ad-122">Click Save.</span></span>
13. <span data-ttu-id="d24ad-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d24ad-123">Close the page.</span></span>


