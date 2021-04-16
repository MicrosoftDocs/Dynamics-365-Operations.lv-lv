---
title: Mērvienības pārvaldība
description: Šajā procedūrā parādīts, kā definēt mērvienību, nodrošināt mērvienības tulkojumus un aprakstu, un definēt pārveidošanas noteikumus saistītām mērvienībām.
author: sorenva
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 966e189e7395bec15d2c62735c6df3df2ab34b8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817969"
---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="54c91-103">Mērvienības pārvaldība</span><span class="sxs-lookup"><span data-stu-id="54c91-103">Manage unit of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="54c91-104">Šajā procedūrā parādīts, kā definēt mērvienību, nodrošināt mērvienības tulkojumus un aprakstu, un definēt pārveidošanas noteikumus saistītām mērvienībām.</span><span class="sxs-lookup"><span data-stu-id="54c91-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="54c91-105">Šo procedūru var izmēģināt, izmantojot demonstrācijas datus vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="54c91-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="54c91-106">Dodieties uz **Navigācijas rūts > Moduļi > Preču informācijas pārvaldība > Izlaisto preču uzturēšana**.</span><span class="sxs-lookup"><span data-stu-id="54c91-106">Go to **Navigation pane > Modules > Product information management > Released product maintenance**.</span></span>
2. <span data-ttu-id="54c91-107">Noklikšķiniet uz **Mērvienības**.</span><span class="sxs-lookup"><span data-stu-id="54c91-107">Click **Units**.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="54c91-108">Mērvienības izveide</span><span class="sxs-lookup"><span data-stu-id="54c91-108">Create a unit of measure</span></span>
1. <span data-ttu-id="54c91-109">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="54c91-109">Click **New**.</span></span>
2. <span data-ttu-id="54c91-110">Laukā **Vienība** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="54c91-110">In the **Unit** field, type a value.</span></span> <span data-ttu-id="54c91-111">Ievadiet ID vai simbolu, kas jāizmanto, atsaucoties uz mērvienību.</span><span class="sxs-lookup"><span data-stu-id="54c91-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="54c91-112">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="54c91-112">In the **Description** field, type a value.</span></span> <span data-ttu-id="54c91-113">Ievadiet mērvienības aprakstošo nosaukumu sistēmas valodā.</span><span class="sxs-lookup"><span data-stu-id="54c91-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="54c91-114">Laukā **Mērvienību kategorija** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="54c91-114">In the **Unit class** field, select an option.</span></span> <span data-ttu-id="54c91-115">Mērvienību kategorija nosaka, kādam loģiskam grupējumam pieder mērvienība, piemēram, platībai, masai vai daudzumam.</span><span class="sxs-lookup"><span data-stu-id="54c91-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="54c91-116">Laukā **Decimālā precizitāte** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="54c91-116">In the **Decimal precision** field, enter a number.</span></span> <span data-ttu-id="54c91-117">Norādiet decimāldaļu skaitu, līdz kuram jānoapaļo konvertētā mērvienība, kad mērvienības aprēķins ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="54c91-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="54c91-118">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="54c91-118">Click **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="54c91-119">Vienību tulkojumu definēšana</span><span class="sxs-lookup"><span data-stu-id="54c91-119">Define unit translations</span></span>
1. <span data-ttu-id="54c91-120">**Darbību rūtī** noklikšķiniet uz **Vienību teksti**.</span><span class="sxs-lookup"><span data-stu-id="54c91-120">On the **Action Pane**, click **Unit texts**.</span></span>
2. <span data-ttu-id="54c91-121">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="54c91-121">Click **New**.</span></span> <span data-ttu-id="54c91-122">Izmantojiet vienības tekstu, lai izveidotu ID vai simbola, kas apzīmē mērvienību, tulkojumu izmantošanai ārējos dokumentos debitoram vai kreditoram specifiskā valodā.</span><span class="sxs-lookup"><span data-stu-id="54c91-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="54c91-123">Laukā **Valoda** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="54c91-123">In the **Language** field, enter or select a value.</span></span>
4. <span data-ttu-id="54c91-124">Laukā **Teksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="54c91-124">In the **Text** field, type a value.</span></span>
5. <span data-ttu-id="54c91-125">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="54c91-125">Click **Save**.</span></span>
6. <span data-ttu-id="54c91-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="54c91-126">Close the page.</span></span>
7. <span data-ttu-id="54c91-127">**Darbību rūtī** noklikšķiniet uz **Tulkotie vienību apraksti**.</span><span class="sxs-lookup"><span data-stu-id="54c91-127">On the **Action Pane**, click **Translated unit descriptions**.</span></span>
8. <span data-ttu-id="54c91-128">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="54c91-128">Click **New**.</span></span> <span data-ttu-id="54c91-129">Definējiet valodai raksturīgus mērvienības aprakstus.</span><span class="sxs-lookup"><span data-stu-id="54c91-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="54c91-130">Laukā **Valoda** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="54c91-130">In the **Language** field, enter or select a value.</span></span>
10. <span data-ttu-id="54c91-131">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="54c91-131">In the **Description** field, type a value.</span></span>
11. <span data-ttu-id="54c91-132">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="54c91-132">Click **Save**.</span></span>
12. <span data-ttu-id="54c91-133">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="54c91-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="54c91-134">Vienību pārveidošanas noteikumu definēšana</span><span class="sxs-lookup"><span data-stu-id="54c91-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="54c91-135">**Darbību rūtī** noklikšķiniet uz **Vienību pārveidošana**.</span><span class="sxs-lookup"><span data-stu-id="54c91-135">On the **Action Pane**, click **Unit conversions**.</span></span> <span data-ttu-id="54c91-136">Definējiet noteikumus mērvienības pārveidošanai uz citām mērvienībām un no citām mērvienībām atlasītajā mērvienību kategorijā.</span><span class="sxs-lookup"><span data-stu-id="54c91-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="54c91-137">Noklikšķiniet uz **Jauns**, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="54c91-137">Click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="54c91-138">Laukā **Koeficients** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="54c91-138">In the **Factor** field, enter a number.</span></span> <span data-ttu-id="54c91-139">Pārveidošanas koeficients no No vienības uz Uz vienību.</span><span class="sxs-lookup"><span data-stu-id="54c91-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="54c91-140">Piemēram, pārveidošanas koeficients no centimetriem uz metriem ir 100, jo viena metrā ir 100 centimetru.</span><span class="sxs-lookup"><span data-stu-id="54c91-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="54c91-141">Laukā **Uz vienību** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="54c91-141">In the **To unit** field, enter or select a value.</span></span>
5. <span data-ttu-id="54c91-142">Laukā **Noapaļošana** atlasiet opciju.</span><span class="sxs-lookup"><span data-stu-id="54c91-142">In the **Rounding** field, select an option.</span></span> <span data-ttu-id="54c91-143">Nosakiet, kā pārveidotā vērtība ir jānoapaļo.</span><span class="sxs-lookup"><span data-stu-id="54c91-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="54c91-144">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="54c91-144">Click **OK**.</span></span>
7. <span data-ttu-id="54c91-145">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="54c91-145">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]