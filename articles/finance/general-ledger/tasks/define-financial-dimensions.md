---
title: Finanšu dimensiju definēšana
description: Šajā uzdevumu ceļvedī parādīts, kā pievienot uz elementu balstītu finanšu dimensiju un pielāgoto finanšu dimensiju.
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6fbe739eec0cfa1e7b0276872640bd4f82be3ef7
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138340"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="5a305-103">Finanšu dimensiju definēšana</span><span class="sxs-lookup"><span data-stu-id="5a305-103">Define financial dimensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5a305-104">Šajā uzdevumu ceļvedī parādīts, kā pievienot uz elementu balstītu finanšu dimensiju un pielāgoto finanšu dimensiju.</span><span class="sxs-lookup"><span data-stu-id="5a305-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="5a305-105">Ceļvedī tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="5a305-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="5a305-106">Uz elementu balstītas finanšu dimensijas izveide</span><span class="sxs-lookup"><span data-stu-id="5a305-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="5a305-107">Dodieties uz **Navigācijas rūts > Moduļi > Virsgrāmata > Kontu plāns > Dimensijas > Finanšu dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="5a305-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Dimensions > Financial dimensions**.</span></span>
2. <span data-ttu-id="5a305-108">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5a305-108">Click **New**.</span></span>
3. <span data-ttu-id="5a305-109">Laukā **Lietotāja vērtību veidlapa** atlasiet sistēmas definētu elementu, uz kuru balstīt finanšu dimensiju.</span><span class="sxs-lookup"><span data-stu-id="5a305-109">In the **User values form** field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="5a305-110">Laukā **Dimensijas nosaukums** ievadiet vērtību, lai aprakstītu finanšu dimensiju.</span><span class="sxs-lookup"><span data-stu-id="5a305-110">In the **Dimension name** field, type a value to describe the financial dimension.</span></span> <span data-ttu-id="5a305-111">Nosaukums var atšķirties no sistēmas definētā elementa nosaukuma, bet nedrīkst saturēt atstarpes vai īpašas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="5a305-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>
5. <span data-ttu-id="5a305-112">Noklikšķiniet uz **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="5a305-112">Click **Activate**.</span></span> <span data-ttu-id="5a305-113">Aktivizējot finanšu dimensiju, tabulā tiek atjaunināts finanšu dimensijas nosaukums un tiek noņemtas dzēstās dimensijas.</span><span class="sxs-lookup"><span data-stu-id="5a305-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="5a305-114">Pirms aktivizēt finanšu dimensiju var ievadīt dimensijas vērtības, taču finanšu dimensiju nevar izmantot, kamēr tā netiks aktivizēta.</span><span class="sxs-lookup"><span data-stu-id="5a305-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="5a305-115">Aktivizēšanas ziņojumā noklikšķiniet uz **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="5a305-115">Click **Close** on the activation message.</span></span>
7. <span data-ttu-id="5a305-116">Noklikšķiniet uz **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="5a305-116">Click **Activate**.</span></span> <span data-ttu-id="5a305-117">Dimensijas aktivizāciju var ieplānot kā pakešuzdevumu noteiktā datumā un laikā.</span><span class="sxs-lookup"><span data-stu-id="5a305-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="5a305-118">**Darbību rūtī** noklikšķiniet uz **Dimensiju vērtības**.</span><span class="sxs-lookup"><span data-stu-id="5a305-118">On **Action pane**, click **Dimension values**.</span></span> <span data-ttu-id="5a305-119">Dažas dimensijas vērtības attiecas tikai uz konkrētu uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="5a305-119">Some dimension values are company specific.</span></span> <span data-ttu-id="5a305-120">Jūs varat pārliecināties, vai tās attiecas tikai uz konkrētu uzņēmumu, pārbaudot, vai uzņēmuma nosaukums parādās dimensiju vērtību sarakstā.</span><span class="sxs-lookup"><span data-stu-id="5a305-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="5a305-121">Pielāgotās finanšu dimensijas izveide</span><span class="sxs-lookup"><span data-stu-id="5a305-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="5a305-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="5a305-122">Close the page.</span></span>
2. <span data-ttu-id="5a305-123">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5a305-123">Click **New**.</span></span>
3. <span data-ttu-id="5a305-124">Laukā **Izmantot vērtības no** atlasiet **Pielāgota dimensija**.</span><span class="sxs-lookup"><span data-stu-id="5a305-124">In the **Use values from** field, select **Custom dimension**.</span></span>
4. <span data-ttu-id="5a305-125">Laukā **Dimensijas nosaukums** ievadiet vērtību, lai aprakstītu finanšu dimensiju.</span><span class="sxs-lookup"><span data-stu-id="5a305-125">In the **Dimension name** field, type a value to describe the financial dimension.</span></span>
    - <span data-ttu-id="5a305-126">Nosaukumā nedrīkst būt atstarpes vai īpašas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="5a305-126">The name cannot contain spaces or special characters.</span></span>  
    - <span data-ttu-id="5a305-127">Lai ierobežotu summas un tipa informāciju, ko var ievadīt dimensiju vērtībām, var norādīt arī konta masku.</span><span class="sxs-lookup"><span data-stu-id="5a305-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    - <span data-ttu-id="5a305-128">Jūs varat ievadīt rakstzīmes, kas paliek vienādas katrai dimensijas vērtībai, piemēram, burtus vai pārnesumzīmi.</span><span class="sxs-lookup"><span data-stu-id="5a305-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="5a305-129">Varat arī ievadīt numura zīmes (#) un zīmes & kā vietturi burtiem un cipariem, kas mainīsies ikreiz, kad tiks izveidota dimensijas vērtība.</span><span class="sxs-lookup"><span data-stu-id="5a305-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="5a305-130">Izmantojiet numura zīmi (#) kā vietturi cipariem un zīmi & kā vietturi burtiem.</span><span class="sxs-lookup"><span data-stu-id="5a305-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="5a305-131">Piemērs: lai dimensijas vērtību noteiktu kā burtus CC un trīs ciparus, kā formāta maska ir jāieraksta CC-###.</span><span class="sxs-lookup"><span data-stu-id="5a305-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="5a305-132">Noklikšķiniet uz **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="5a305-132">Click **Activate**.</span></span> <span data-ttu-id="5a305-133">Aktivizējot finanšu dimensiju, tabulā tiek atjaunināts finanšu dimensijas nosaukums un tiek noņemtas dzēstās dimensijas.</span><span class="sxs-lookup"><span data-stu-id="5a305-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="5a305-134">Pirms aktivizēt finanšu dimensiju var ievadīt dimensijas vērtības, taču finanšu dimensiju nevar izmantot, kamēr tā netiks aktivizēta.</span><span class="sxs-lookup"><span data-stu-id="5a305-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>     
6. <span data-ttu-id="5a305-135">Noklikšķiniet uz **Aktivizēt**.</span><span class="sxs-lookup"><span data-stu-id="5a305-135">Click **Activate**.</span></span> <span data-ttu-id="5a305-136">Dimensijas aktivizāciju var ieplānot kā pakešuzdevumu noteiktā datumā un laikā.</span><span class="sxs-lookup"><span data-stu-id="5a305-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>      
7. <span data-ttu-id="5a305-137">**Darbību rūtī** noklikšķiniet uz **Dimensiju vērtības**.</span><span class="sxs-lookup"><span data-stu-id="5a305-137">On **Action pane**, click **Dimension values**.</span></span>
8. <span data-ttu-id="5a305-138">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="5a305-138">Click **New**.</span></span>
9. <span data-ttu-id="5a305-139">Laukā **Dimensijas vērtība** ievadiet nosaukumu, lai aprakstītu savu finanšu dimensijas vērtību.</span><span class="sxs-lookup"><span data-stu-id="5a305-139">In the **Dimension value** field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="5a305-140">Laukā **Apraksts** ierakstiet aprakstu, kas apraksta jūsu finanšu dimensijas vērtību.</span><span class="sxs-lookup"><span data-stu-id="5a305-140">In the **Description** field, type a description that describes your financial dimension value.</span></span>

