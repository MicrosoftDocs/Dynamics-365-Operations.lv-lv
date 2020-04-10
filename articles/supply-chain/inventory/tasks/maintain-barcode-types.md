---
title: Svītrkodu veidu uzturēšana
description: Šajā procedūrā parādīts, kā iestatīt jaunu svītrkoda definīciju, ko pēc tam var izmantot kā daļu no izdošanas saraksta pārskata.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7834745923bf5ec05018ff5829ddaa0b75df5db7
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145586"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="1c6f9-103">Svītrkodu veidu uzturēšana</span><span class="sxs-lookup"><span data-stu-id="1c6f9-103">Maintain barcode types</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c6f9-104">Šajā procedūrā parādīts, kā iestatīt jaunu svītrkoda definīciju, ko pēc tam var izmantot kā daļu no izdošanas saraksta pārskata.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="1c6f9-105">Šo procedūru var izmēģināt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="1c6f9-106">Ja izmantojat USMF varat izmantot piemēra vērtības, kas parādītas.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="1c6f9-107">Šos uzdevumus parasti veic noliktavas pārvaldnieks.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="1c6f9-108">Dodieties uz sadaļu Svītrkodi.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="1c6f9-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-109">Click New.</span></span>
3. <span data-ttu-id="1c6f9-110">Laukā Svītrkodu iestatījumi ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="1c6f9-111">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1c6f9-112">Atlasiet opciju laukā Svītrkoda tips.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="1c6f9-113">Ja izmantojat USMF, varat atlasīt "Kods 39".</span><span class="sxs-lookup"><span data-stu-id="1c6f9-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="1c6f9-114">Ievadiet skaitli laukā Lielums.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="1c6f9-115">Ievadiet skaitli laukā Maksimālais garums.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="1c6f9-116">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-116">Click Save.</span></span>
9. <span data-ttu-id="1c6f9-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-117">Close the page.</span></span>
10. <span data-ttu-id="1c6f9-118">Dodieties uz sadaļu Krājumu un noliktavas vadības parametri.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="1c6f9-119">Ievadiet vai atlasiet vērtību laukā Svītrkodu iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="1c6f9-120">Atlasiet svītrkoda iestatījumu, ko izveidojāt iepriekš, taču ņemiet vērā, ka svītrkoda formātam jāatbilst unikālā identifikatora formātam procesā izmantojamajam ieraksta tipam.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="1c6f9-121">Piemēram, izdošanas maršrutiem svītrkoda formātam ir jāatbilst izdošanas maršruta atsauces formātam, kas parasti ir numuru sērija.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="1c6f9-122">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-122">Click Save.</span></span>
13. <span data-ttu-id="1c6f9-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-123">Close the page.</span></span>

