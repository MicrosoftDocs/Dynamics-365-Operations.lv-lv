---
title: Debitora darbplūsma
description: Šajā tēmā ir sniegta informācija par debitora darbplūsmu. Jūs maināt noteiktus debitora informācijas laukus un pēc tam, izmantojot darbplūsmu, nosūtāt izmaiņas apstiprināšanai, pirms tās tiek pievienotas debitora informācijai.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 5998a492e12cb93aeec029c6e56f811f8b90055a
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2020
ms.locfileid: "4459511"
---
# <a name="customer-workflow"></a><span data-ttu-id="9ff84-104">Debitora darbplūsma</span><span class="sxs-lookup"><span data-stu-id="9ff84-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ff84-105">Šī debitora darbplūsma ir pievienota versijai 8.0.4.</span><span class="sxs-lookup"><span data-stu-id="9ff84-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="9ff84-106">Varat mainīt noteiktus debitora informācijas laukus un pēc tam, izmantojot darbplūsmu, nosūtīt izmaiņas apstiprināšanai, pirms tās tiek pievienotas debitora informācijai.</span><span class="sxs-lookup"><span data-stu-id="9ff84-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="9ff84-107">Iestatīt debitora darbplūsmu</span><span class="sxs-lookup"><span data-stu-id="9ff84-107">Set up the customer workflow</span></span>

<span data-ttu-id="9ff84-108">Lai varētu izmantot debitora darbplūsmas līdzekli, tas vispirms ir jāiespējo.</span><span class="sxs-lookup"><span data-stu-id="9ff84-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="9ff84-109">Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru parādu parametri**.</span><span class="sxs-lookup"><span data-stu-id="9ff84-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="9ff84-110">Lai iespējotu līdzekli, atveriet cilnes **Vispārīgie iestatījumi** kopsavilkuma cilni **Debitora apstiprinājums** un opcijai **Iespējot klienta apstiprinājumus** iestatiet opciju **Jā**.</span><span class="sxs-lookup"><span data-stu-id="9ff84-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="9ff84-111">Laukā **Datu elementa režīms** atlasiet datu elementu vēlamo izturēšanos datu importēšanas brīdī. Ir pieejamas šādas iespējas.</span><span class="sxs-lookup"><span data-stu-id="9ff84-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="9ff84-112">**Atļaut izmaiņas bez apstiprinājuma** – elements var atjaunināt klienta ierakstu, neapstrādājot to ar darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="9ff84-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="9ff84-113">**Noraidīt izmaiņas** – klienta ierakstā nevar veikt izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="9ff84-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="9ff84-114">Laukos, kam ir iespējota darbplūsma, importēšana neizdosies.</span><span class="sxs-lookup"><span data-stu-id="9ff84-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="9ff84-115">**Izveidot izmaiņu priekšlikumus** – tiks mainīti visi lauki, izņemot laukus, kam ir iespējota darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="9ff84-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="9ff84-116">Šo lauku jaunās vērtības tiks pievienotas debitora informācijai kā piedāvātās izmaiņas, un tiks automātiski sākta darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="9ff84-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="9ff84-117">Pēc tam debitora lauku sarakstā atlasiet izvēles rūtiņu **Iespējot** pie katra lauka, kas jāapstiprina pirms izmaiņu veikšanas.</span><span class="sxs-lookup"><span data-stu-id="9ff84-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="9ff84-118">Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru parādu darbplūsmas**.</span><span class="sxs-lookup"><span data-stu-id="9ff84-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="9ff84-119">Atlasiet **Jauna**.</span><span class="sxs-lookup"><span data-stu-id="9ff84-119">Select **New**.</span></span>
7. <span data-ttu-id="9ff84-120">Atlasiet **Piedāvāto klienta izmaiņu darbplūsma**.</span><span class="sxs-lookup"><span data-stu-id="9ff84-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="9ff84-121">Iestatiet darbplūsmu atbilstoši jūsu apstiprināšanas procesam.</span><span class="sxs-lookup"><span data-stu-id="9ff84-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="9ff84-122">Izmaiņas tiks piemērotas debitora informācijai, izmantojot darbplūsmas apstiprināšanas elementu **Darbplūsmas apstiprinājums piedāvātajām klienta izmaiņām**.</span><span class="sxs-lookup"><span data-stu-id="9ff84-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="9ff84-123">Debitora informācijas mainīšana un izmaiņu iesniegšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="9ff84-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="9ff84-124">Mainot lauku, kam ir iespējota darbplūsma, tiek parādīta lapa **Piedāvātās izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="9ff84-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="9ff84-125">Šajā lapā tiek rādīta lauka sākotnējā vērtība un jūsu ievadītā jaunā vērtība.</span><span class="sxs-lookup"><span data-stu-id="9ff84-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="9ff84-126">Jūsu izmainītajam laukam tiek atjaunota sākotnējā vērtība.</span><span class="sxs-lookup"><span data-stu-id="9ff84-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="9ff84-127">Lapā tiek parādīts statusa ziņojums, informējot, ka jūsu veiktās izmaiņas nav iesniegtas.</span><span class="sxs-lookup"><span data-stu-id="9ff84-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="9ff84-128">Mainot lauku, kam ir iespējota darbplūsma, attiecīgais lauks katru reizi tiek pievienots piedāvāto izmaiņu sarakstam.</span><span class="sxs-lookup"><span data-stu-id="9ff84-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="9ff84-129">Lai atmestu lauka piedāvāto vērtību, izmantojiet pogu **Atmest**, kas sarakstā ir blakus laukam.</span><span class="sxs-lookup"><span data-stu-id="9ff84-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="9ff84-130">Lai atmestu visas izmaiņas, izmantojiet pogu **Atmest visas izmaiņas**, kas atrodas lapas apakšā.</span><span class="sxs-lookup"><span data-stu-id="9ff84-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="9ff84-131">Atlasiet **Labi**, lai aizvērtu lapu.</span><span class="sxs-lookup"><span data-stu-id="9ff84-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="9ff84-132">Ja ir piedāvātas vismaz vienas izmaiņas, darbību rūtī tiek rādītas divas papildu izvēlnes: **Piedāvātās izmaiņas** un **Darbplūsma**.</span><span class="sxs-lookup"><span data-stu-id="9ff84-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="9ff84-133">Lai atvērtu lapu **Piedāvātās izmaiņas** un pārskatītu izmaiņas, atlasiet **Piedāvātās izmaiņas**.</span><span class="sxs-lookup"><span data-stu-id="9ff84-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="9ff84-134">Lai iesniegtu izmaiņas darbplūsmā, atlasiet **Darbplūsma \> Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="9ff84-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="9ff84-135">Lapas statuss tiek mainīts uz **Izmaiņas, kas gaida apstiprinājumu**.</span><span class="sxs-lookup"><span data-stu-id="9ff84-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="9ff84-136">Darbplūsma atbilst programmas standarta darbplūsmu procesam.</span><span class="sxs-lookup"><span data-stu-id="9ff84-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="9ff84-137">Apstiprinātājs tiek virzīts uz lapu **Debitors**, kurā var pārskatīt izmaiņas lapā **Piedāvātās izmaiņas** un pēc tam atlasīt **Darbplūsma \> Apstiprināt**, lai apstiprinātu darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="9ff84-137">The approver is directed to the **Customer** page where the changes can be reviewed on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="9ff84-138">Kad apstiprināšana ir pilnībā pabeigta, lauki tiek atjaunināti atbilstoši jūsu piedāvātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="9ff84-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
