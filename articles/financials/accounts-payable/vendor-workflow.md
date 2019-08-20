---
title: Kreditora darbplūsma
description: Modificējiet kreditora informāciju un izmantojiet darbplūsmu, lai to apstiprinātu.
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 112f9d6adeee583a63da8ab700d7adc179de2c1d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835314"
---
# <a name="vendor-workflow"></a><span data-ttu-id="1b7ce-103">Kreditora darbplūsma</span><span class="sxs-lookup"><span data-stu-id="1b7ce-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b7ce-104">Izmantojot kreditora darbplūsmu, konkrētos laukos veiktās izmaiņas pirms to pievienošanas kreditoram tiek nosūtītas apstiprināšanai uz darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="1b7ce-105">Kreditora darbplūsmas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1b7ce-105">Set up the vendor workflow</span></span>

<span data-ttu-id="1b7ce-106">Jums ir jāiespējo darbplūsmas līdzeklis, lai jūs varētu to izmantot.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="1b7ce-107">Dodieties uz **Parādi kreditoriem \> Iestatīšana \> Kreditoru moduļa parametri**.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="1b7ce-108">Cilnes **Vispārīgi** kopsavilkuma cilnē **Kreditoru apstiprināšana** iestatiet opcijas **Iespējot kreditoru apstiprināšanas** vērtību **Jā**.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="1b7ce-109">Laukā **Datu elementu uzvedība** atlasiet uzvedību, kura ir jāizmanto, importējot datus.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="1b7ce-110">**Atļaut izmaiņas bez apstiprinājuma** – datu elements var atjaunināt kreditora ierakstu, neveicot tā apstrādi darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="1b7ce-111">**Noraidīt izmaiņas** – kreditora ierakstam izmaiņas nevar veikt.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="1b7ce-112">Importēšana nebūs veiksmīga laukiem, kuri ir iespējoti darbplūsmai.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="1b7ce-113">**Izmaiņu piedāvājumu izveide** – visi lauki tiks mainīti, izņemot tos laukus, kuri ir iespējoti darbplūsmai.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="1b7ce-114">Šo lauku jaunās vērtības tiks pievienots kreditoram kā piedāvātās izmaiņas, un darbplūsma tiks sākta automātiski.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="1b7ce-115">Kreditora lauku sarakstā atlasiet izvēles rūtiņu **Iespējot** katram laukam, kas ir jāapstiprina, lai varētu veikt izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="1b7ce-116">Dodieties uz **Parādi kreditoriem \> Iestatīšana \> Kreditoru moduļa darbplūsmas**.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="1b7ce-117">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-117">Select **New**.</span></span>
7. <span data-ttu-id="1b7ce-118">Atlasiet **Piedāvāto kreditora izmaiņu darbplūsma**.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="1b7ce-119">Iestatiet darbplūsmu tā, lai tā atbilstu jūsu apstiprināšanas procesam.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="1b7ce-120">Darbplūsmas elements **Darbplūsmas apstiprināšana piedāvātajai kreditora izmaiņai** piemēros izmaiņas kreditoram.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="1b7ce-121">Kreditora informācijas maiņa un izmaiņu iesniegšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="1b7ce-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="1b7ce-122">Mainot lauku, kurš ir iespējots darbplūsmai, tiek parādīta lapa **Piedāvātās izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="1b7ce-123">Šajā lapā tiek rādīta lauka sākotnējā vērtība un jūsu ievadītā jaunā vērtība.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="1b7ce-124">Laukā, kurā veicāt izmaiņas, tiek atjaunota tā sākotnējā vērtība.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="1b7ce-125">Statusa ziņojums arī informē, ka jūsu veiktās izmaiņas nav iesniegtas.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="1b7ce-126">Katrreiz, kad maināt lauku, kurš ir iespējots darbplūsmai, šis lauks tiek pievienots sarakstam lapā **Piedāvātās izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="1b7ce-127">Lai atmestu laukam piedāvātās vērtības, izmantojiet pogu **Atmest** pie sarakstā esošā lauka.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="1b7ce-128">Lai atmestu visas izmaiņas, izmantojiet pogu **Atmest visas izmaiņas** pogas apakšdaļā.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="1b7ce-129">Atlasiet **Labi**, lai aizvērtu lapu.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="1b7ce-130">Ja ir vismaz viena piedāvātā izmaiņa, darbību rūtī tiek rādītas divas papildu cilnes: **Piedāvātās izmaiņas** un **Darbplūsma**.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="1b7ce-131">Atlasiet cilni **Piedāvātās izmaiņas**, lai atvērtu lapu **Piedāvātās izmaiņas**, un pārskatiet veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="1b7ce-132">Atlasiet cilni **Darbplūsma \> Iesniegt, lai iesniegtu izmaiņas darbplūsmā**.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="1b7ce-133">Lapas statuss tiek mainīts uz **Izmaiņas, kas gaida apstiprinājumu**.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="1b7ce-134">Darbplūsma atbilst standarta darbplūsmas procesam sistēmā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-134">The workflow follows the standard workflow process in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="1b7ce-135">Apstiprinātājs tiek novirzīts uz lapu **Kreditors**, kurā viņš vai viņa var pārskatīt izmaiņas lapā **Piedāvātās izmaiņas** lapu un pēc tam atlasīt cilni **Darbplūsma \>Apstiprināt**, lai apstiprinātu darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-135">The approver is directed to the **Vendor** page, where he or she can review the changes on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="1b7ce-136">Kad apstiprināšana ir pilnībā pabeigta, lauki tiek atjaunināti atbilstoši jūsu piedāvātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="1b7ce-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
