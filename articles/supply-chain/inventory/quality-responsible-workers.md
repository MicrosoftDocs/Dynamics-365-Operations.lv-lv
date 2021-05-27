---
title: Par neatbilstību apstiprināšanu atbildīgie darbinieki
description: Šajā tēmā ir aprakstīts, kā konfigurēt darbiniekus, kas ir atbildīgi par neatbilstību apstiprināšanu.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d3f647de2c188661c2c9c5f31e2642c3f8ca0b5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021784"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="53d79-103">Par neatbilstību apstiprināšanu atbildīgie darbinieki</span><span class="sxs-lookup"><span data-stu-id="53d79-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53d79-104">Šajā tēmā ir aprakstīts, kā konfigurēt darbiniekus, kas ir atbildīgi par neatbilstību apstiprināšanu.</span><span class="sxs-lookup"><span data-stu-id="53d79-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="53d79-105">Neatbilstības ir jāapstiprina, pirms lietotāji var sākt ievadīt tādu detalizētu informāciju kā labojumi vai operācijas.</span><span class="sxs-lookup"><span data-stu-id="53d79-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="53d79-106">Pirms lietotāji var apstiprināt vai noraidīt neatbilstības, viņu lietotāja ID (lietotāja ierakstam) jābūt saistītam ar darbinieka ierakstu.</span><span class="sxs-lookup"><span data-stu-id="53d79-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="53d79-107">Pēc izvēles varat konfigurēt darbiniekus, kuri ir atbildīgi par kvalitāti, un pēc tam vienam darbiniekam ļaut apstiprināt darbu cita darbinieka vārdā.</span><span class="sxs-lookup"><span data-stu-id="53d79-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="53d79-108">Iespējojiet lietotājam neatbilstību apstrādi</span><span class="sxs-lookup"><span data-stu-id="53d79-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="53d79-109">Pirms lietotājs var apstiprināt vai noraidīt neatbilstības, viņu lietotāja ieraksts ir jāsaista ar darbinieka ierakstu.</span><span class="sxs-lookup"><span data-stu-id="53d79-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="53d79-110">Apstiprinājuma laukus pēc tam var iestatīt automātiski, un pašreizējo lietotāju var automātiski aizpildīt darba laika uzskaites tabulā.</span><span class="sxs-lookup"><span data-stu-id="53d79-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="53d79-111">Lai lietotājs varētu izmantot dokumenta piezīmes, jums jāaktivizē dokumentu apstrāde lietotāja opcijās.</span><span class="sxs-lookup"><span data-stu-id="53d79-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="53d79-112">Dodieties uz **Sistēmas administrēšana \> Lietotāji \> Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="53d79-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="53d79-113">Atrodiet un atveriet lietotāju, kuram jābūt iespējai apstiprināt vai noraidīt neatbilstības.</span><span class="sxs-lookup"><span data-stu-id="53d79-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="53d79-114">Laukā **Persona** iestatiet darbinieka vārdu, kas ir saistīts ar pašreizējo lietotāja ierakstu.</span><span class="sxs-lookup"><span data-stu-id="53d79-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="53d79-115">Darbību rūtī atlasiet **Lietotāja opcijas**.</span><span class="sxs-lookup"><span data-stu-id="53d79-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="53d79-116">Pašreizējā lietotāja ieraksta lapā **Opcijas** cilnē **Preferences** iestatiet opciju **Iespējot dokumentu apstrādi** uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="53d79-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="53d79-117">Aizveriet lapas.</span><span class="sxs-lookup"><span data-stu-id="53d79-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="53d79-118">Definēt par kvalitāti atbildīgos darbiniekus</span><span class="sxs-lookup"><span data-stu-id="53d79-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="53d79-119">Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Kvalitātes kontrole \> Par kvalitāti atbildīgie darbinieki**.</span><span class="sxs-lookup"><span data-stu-id="53d79-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="53d79-120">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="53d79-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="53d79-121">Laukā **Darbinieks** atlasiet darbinieku, kas ievada kvalitātes datus.</span><span class="sxs-lookup"><span data-stu-id="53d79-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="53d79-122">Laukā **Atbildīgais darbinieks** atlasiet darbinieku, kura vārdā atlasītais darbinieks ievada darbu.</span><span class="sxs-lookup"><span data-stu-id="53d79-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="53d79-123">Kad neatbilstības ir izveidotas un atjauninātas, darbinieks laukos **Darbinieks** tiks ievadīts pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="53d79-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53d79-124">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="53d79-124">Additional resources</span></span>

- [<span data-ttu-id="53d79-125">Kvalitātes pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="53d79-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="53d79-126">Iespējot kvalitātes un neatbilstības pārvaldību</span><span class="sxs-lookup"><span data-stu-id="53d79-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="53d79-127">Kvalitātes papildmaksas</span><span class="sxs-lookup"><span data-stu-id="53d79-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="53d79-128">Karantīnas zonas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="53d79-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="53d79-129">Neatbilstību diagnostikas tipi</span><span class="sxs-lookup"><span data-stu-id="53d79-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="53d79-130">Kvalitātes maksa par neatbilstībām</span><span class="sxs-lookup"><span data-stu-id="53d79-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="53d79-131">Operācijas neatbilstībai</span><span class="sxs-lookup"><span data-stu-id="53d79-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="53d79-132">Kvalitātes pārvaldība noliktavas procesiem</span><span class="sxs-lookup"><span data-stu-id="53d79-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
