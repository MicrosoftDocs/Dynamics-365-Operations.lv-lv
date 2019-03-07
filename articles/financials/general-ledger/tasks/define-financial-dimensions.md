---
title: Finanšu dimensiju definēšana
description: Šajā uzdevumu ceļvedī parādīts, kā pievienot uz elementu balstītu finanšu dimensiju un pielāgoto finanšu dimensiju.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20a7781486c6e0612c27af02a1bccbc48c55a932
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "353797"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="edd97-103">Finanšu dimensiju definēšana</span><span class="sxs-lookup"><span data-stu-id="edd97-103">Define financial dimensions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="edd97-104">Šajā uzdevumu ceļvedī parādīts, kā pievienot uz elementu balstītu finanšu dimensiju un pielāgoto finanšu dimensiju.</span><span class="sxs-lookup"><span data-stu-id="edd97-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="edd97-105">Ceļvedī tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="edd97-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="edd97-106">Uz elementu balstītas finanšu dimensijas izveide</span><span class="sxs-lookup"><span data-stu-id="edd97-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="edd97-107">Pārejiet uz sadaļu Virsgrāmata > Kontu plāns > Dimensijas > Finanšu dimensijas.</span><span class="sxs-lookup"><span data-stu-id="edd97-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="edd97-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="edd97-108">Click New.</span></span>
3. <span data-ttu-id="edd97-109">Laukā Lietotāja vērtības no atlasiet sistēmas definētu elementu, uz kuru balstīt finanšu dimensiju.</span><span class="sxs-lookup"><span data-stu-id="edd97-109">In the User values from field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="edd97-110">Laukā Dimensijas nosaukums ievadiet vērtību, lai aprakstītu finanšu dimensiju.</span><span class="sxs-lookup"><span data-stu-id="edd97-110">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="edd97-111">Nosaukums var atšķirties no sistēmas definētā elementa nosaukuma, bet nedrīkst saturēt atstarpes vai īpašas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="edd97-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>  
5. <span data-ttu-id="edd97-112">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="edd97-112">Click Activate.</span></span>
    * <span data-ttu-id="edd97-113">Aktivizējot finanšu dimensiju, tabulā tiek atjaunināts finanšu dimensijas nosaukums un tiek noņemtas dzēstās dimensijas.</span><span class="sxs-lookup"><span data-stu-id="edd97-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="edd97-114">Pirms aktivizēt finanšu dimensiju var ievadīt dimensijas vērtības, taču finanšu dimensiju nevar izmantot, kamēr tā netiks aktivizēta.</span><span class="sxs-lookup"><span data-stu-id="edd97-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="edd97-115">Aktivizācijas paziņojumā noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="edd97-115">Click Close on the activation message.</span></span>
7. <span data-ttu-id="edd97-116">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="edd97-116">Click Activate.</span></span>
    * <span data-ttu-id="edd97-117">Dimensijas aktivizāciju var ieplānot kā pakešuzdevumu noteiktā datumā un laikā.</span><span class="sxs-lookup"><span data-stu-id="edd97-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="edd97-118">Noklikšķiniet uz Dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="edd97-118">Click Dimension values.</span></span>
    * <span data-ttu-id="edd97-119">Dažas dimensijas vērtības attiecas tikai uz konkrētu uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="edd97-119">Some dimension values are company specific.</span></span> <span data-ttu-id="edd97-120">Jūs varat pārliecināties, vai tās attiecas tikai uz konkrētu uzņēmumu, pārbaudot, vai uzņēmuma nosaukums parādās dimensiju vērtību sarakstā.</span><span class="sxs-lookup"><span data-stu-id="edd97-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="edd97-121">Pielāgotās finanšu dimensijas izveide</span><span class="sxs-lookup"><span data-stu-id="edd97-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="edd97-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="edd97-122">Close the page.</span></span>
2. <span data-ttu-id="edd97-123">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="edd97-123">Click New.</span></span>
3. <span data-ttu-id="edd97-124">Laukā "Izmantot vērtības no" atlasiet <Custom dimension>.</span><span class="sxs-lookup"><span data-stu-id="edd97-124">In the Use values from field, select <Custom dimension>.</span></span>
4. <span data-ttu-id="edd97-125">Laukā Dimensijas nosaukums ievadiet vērtību, lai aprakstītu finanšu dimensiju.</span><span class="sxs-lookup"><span data-stu-id="edd97-125">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="edd97-126">Nosaukumā nedrīkst būt atstarpes vai īpašas rakstzīmes.</span><span class="sxs-lookup"><span data-stu-id="edd97-126">The name cannot contain spaces or special characters.</span></span>  
    * <span data-ttu-id="edd97-127">Lai ierobežotu summas un tipa informāciju, ko var ievadīt dimensiju vērtībām, var norādīt arī konta masku.</span><span class="sxs-lookup"><span data-stu-id="edd97-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    * <span data-ttu-id="edd97-128">Jūs varat ievadīt rakstzīmes, kas paliek vienādas katrai dimensijas vērtībai, piemēram, burtus vai pārnesumzīmi.</span><span class="sxs-lookup"><span data-stu-id="edd97-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="edd97-129">Varat arī ievadīt numura zīmes (#) un zīmes & kā vietturi burtiem un cipariem, kas mainīsies ikreiz, kad tiks izveidota dimensijas vērtība.</span><span class="sxs-lookup"><span data-stu-id="edd97-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="edd97-130">Izmantojiet numura zīmi (#) kā vietturi cipariem un zīmi & kā vietturi burtiem.</span><span class="sxs-lookup"><span data-stu-id="edd97-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="edd97-131">Piemērs: lai dimensijas vērtību noteiktu kā burtus CC un trīs ciparus, kā formāta maska ir jāieraksta CC-###.</span><span class="sxs-lookup"><span data-stu-id="edd97-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="edd97-132">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="edd97-132">Click Activate.</span></span>
    * <span data-ttu-id="edd97-133">Aktivizējot finanšu dimensiju, tabulā tiek atjaunināts finanšu dimensijas nosaukums un tiek noņemtas dzēstās dimensijas.</span><span class="sxs-lookup"><span data-stu-id="edd97-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="edd97-134">Pirms aktivizēt finanšu dimensiju var ievadīt dimensijas vērtības, taču finanšu dimensiju nevar izmantot, kamēr tā netiks aktivizēta.</span><span class="sxs-lookup"><span data-stu-id="edd97-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="edd97-135">Noklikšķiniet uz Aktivizēt.</span><span class="sxs-lookup"><span data-stu-id="edd97-135">Click Activate.</span></span>
    * <span data-ttu-id="edd97-136">Dimensijas aktivizāciju var ieplānot kā pakešuzdevumu noteiktā datumā un laikā.</span><span class="sxs-lookup"><span data-stu-id="edd97-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
7. <span data-ttu-id="edd97-137">Noklikšķiniet uz Dimensiju vērtības.</span><span class="sxs-lookup"><span data-stu-id="edd97-137">Click Dimension values.</span></span>
8. <span data-ttu-id="edd97-138">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="edd97-138">Click New.</span></span>
9. <span data-ttu-id="edd97-139">Laukā Dimensijas vērtība ievadiet nosaukumu, lai aprakstītu savu finanšu dimensijas vērtību.</span><span class="sxs-lookup"><span data-stu-id="edd97-139">In the Dimension value field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="edd97-140">Laukā Apraksts ierakstiet aprakstu, kas apraksta jūsu finanšu dimensijas vērtību.</span><span class="sxs-lookup"><span data-stu-id="edd97-140">In the Description field, type a description that describes your financial dimension value.</span></span>

