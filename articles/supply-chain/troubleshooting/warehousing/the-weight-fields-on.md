---
title: Kravas rindu svara lauki neatbilst kravas svara laukiem
description: Kravas rindu svara lauki neatbilst kravas svara laukiem
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924355"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="5958d-103">Kravas rindu svara lauki neatbilst kravas svara laukiem</span><span class="sxs-lookup"><span data-stu-id="5958d-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="5958d-104">Kļūdas kods: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span><span class="sxs-lookup"><span data-stu-id="5958d-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="5958d-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="5958d-105">Symptoms</span></span>

<span data-ttu-id="5958d-106">Sistēma parāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="5958d-106">The system shows the following error message:</span></span>

> <span data-ttu-id="5958d-107">Kravas rindu svara lauki neatbilst kravas svara laukiem %1.</span><span class="sxs-lookup"><span data-stu-id="5958d-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="5958d-108">Palaidiet noliktavas kravas svara konsekvences pārbaudi, lai pārrēķinātu svara laukus.</span><span class="sxs-lookup"><span data-stu-id="5958d-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="5958d-109">Iemesls</span><span class="sxs-lookup"><span data-stu-id="5958d-109">Cause</span></span>

<span data-ttu-id="5958d-110">Lauki **Neto svars** un **Taras svars** kravas rindā ir iestatīti uz *0* (nulli).</span><span class="sxs-lookup"><span data-stu-id="5958d-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="5958d-111">Tomēr svara lauki nav iestatīti uz *0* preces svara mērījumiem.</span><span class="sxs-lookup"><span data-stu-id="5958d-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="5958d-112">Ja kravas rindā nav iestatīti svara lauki, visas kravas rindā iestatītā daudzuma korekcijas var radīt nepareizu kravas svara aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="5958d-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="5958d-113">Šī problēma var rasties, ja pēc kravas rindas izveidošanas preces svars ir mainīts.</span><span class="sxs-lookup"><span data-stu-id="5958d-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="5958d-114">Novēršana</span><span class="sxs-lookup"><span data-stu-id="5958d-114">Resolution</span></span>

<span data-ttu-id="5958d-115">Pēc noklusējuma, veidojot kravas rindu, tajā tiek ievadīti preces svara lauki.</span><span class="sxs-lookup"><span data-stu-id="5958d-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="5958d-116">Ja svars ir nulle, to var pārrēķināt, izmantojot funkcionalitāti *Noliktavas kravas konsekvences pārbaude*.</span><span class="sxs-lookup"><span data-stu-id="5958d-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="5958d-117">Dodieties uz **Sistēmas administrēšana \> Periodiskie uzdevumi \> Datu bāze \> Konsekvences pārbaude**.</span><span class="sxs-lookup"><span data-stu-id="5958d-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="5958d-118">Izvēles rūtiņā **Konsekvences pārbaude** iestatiet lauku **Modulis** uz *Noliktavas pārvaldība*.</span><span class="sxs-lookup"><span data-stu-id="5958d-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="5958d-119">Lauku **Pārbaudīt/Labot** iestatiet uz *Labot kļūdu*.</span><span class="sxs-lookup"><span data-stu-id="5958d-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="5958d-120">Izvēles rūtiņu sarakstā atzīmējiet izvēles rūtiņu **Noliktavas kravas svara konsekvences pārdaude** un pārliecinieties, vai ir iezīmēta tikai rinda šai izvēles rūtiņai.</span><span class="sxs-lookup"><span data-stu-id="5958d-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="5958d-121">Izvēles rūtiņas saraksta augšpusē atlasiet daudzpunktes pogu (**...**) un pēc tam izvēlnē atlasiet **Dialogs**.</span><span class="sxs-lookup"><span data-stu-id="5958d-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="5958d-122">Lai norādītu kritērijus, kuriem jāpalaiž konsekvences pārbaude, dialoglodziņā **Noliktavas kravas svara konsekvences pārbaude** iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="5958d-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="5958d-123">**Kravas ID:** norādiet kravas ID.</span><span class="sxs-lookup"><span data-stu-id="5958d-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="5958d-124">Atstājiet šo tukšu, lai pārbaudītu visus kravas ID.</span><span class="sxs-lookup"><span data-stu-id="5958d-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="5958d-125">**Krājuma kods:** norādiet krājuma kodu.</span><span class="sxs-lookup"><span data-stu-id="5958d-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="5958d-126">Atstājiet šo tukšu, lai pārbaudītu visas kravas.</span><span class="sxs-lookup"><span data-stu-id="5958d-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="5958d-127">**Vienmēr pārrēķināt kravu svaru:** iestatiet šo opciju kā *Jā*.</span><span class="sxs-lookup"><span data-stu-id="5958d-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="5958d-128">**Atļaut pārrakstīt svaru kravas rindās:** iestatiet šo opciju kā *Jā*.</span><span class="sxs-lookup"><span data-stu-id="5958d-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="5958d-129">Atlasiet **Labi**, lai aizvērtu dialoglodziņu **Noliktavas noslodzes svara konsekvences pārbaude**.</span><span class="sxs-lookup"><span data-stu-id="5958d-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="5958d-130">Atlasiet daudzpunktes pogu un pēc tam izvēlnē atlasiet **Izpildīt**.</span><span class="sxs-lookup"><span data-stu-id="5958d-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="5958d-131">Svars tiek pārrēķināts, ņemot vērā norādītos kritērijus.</span><span class="sxs-lookup"><span data-stu-id="5958d-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="5958d-132">Atlasiet saiti **Ziņojuma detaļas**, lai skatītu konsekvences pārbaudes rezultātus.</span><span class="sxs-lookup"><span data-stu-id="5958d-132">Select the **Message details** link to view the result of the consistency check.</span></span>
