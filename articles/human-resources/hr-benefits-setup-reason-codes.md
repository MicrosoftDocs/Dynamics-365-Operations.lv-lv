---
title: Iestatiet cēloņa kodus
description: Dynamics 365 Human Resources izmanto pamatojuma kodus, lai izskaidrotu, kāpēc nodarbinātā atvieglojumi mainās.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c799a81f38a5dbd5996afbda9529fa83d7fe5cf9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468399"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="17864-103">Iestatiet cēloņa kodus</span><span class="sxs-lookup"><span data-stu-id="17864-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="17864-104">Dynamics 365 Human Resources izmanto pamatojuma kodus, lai izskaidrotu, kāpēc nodarbinātā atvieglojumi mainās.</span><span class="sxs-lookup"><span data-stu-id="17864-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="17864-105">No 2021. gada janvāra iemeslu kodi tiek migrēti uz darbvietu **Personāla vadība**, nevis uz darbvietu **Atvieglojumu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="17864-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="17864-106">Papildinformāciju skatiet sadaļā [Iemesla kodu manuāla migrēšana uz Personāla pārvaldību](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span><span class="sxs-lookup"><span data-stu-id="17864-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="17864-107">Iemeslu kodu izveide</span><span class="sxs-lookup"><span data-stu-id="17864-107">Create reason codes</span></span>

1. <span data-ttu-id="17864-108">Darbvietā **Personāla pārvaldība** (vai darbvietā **Atvieglojumu pārvaldība**, ja iemeslu kodi vēl nav migrēti), atlasiet **Saites** un pēc tam atlasiet **Iemeslu kodi**.</span><span class="sxs-lookup"><span data-stu-id="17864-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="17864-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="17864-109">Select **New**.</span></span>

3. <span data-ttu-id="17864-110">Norādiet vērtības tālāk minētajos laukos.</span><span class="sxs-lookup"><span data-stu-id="17864-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="17864-111">Lauks</span><span class="sxs-lookup"><span data-stu-id="17864-111">Field</span></span> | <span data-ttu-id="17864-112">Apraksts</span><span class="sxs-lookup"><span data-stu-id="17864-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="17864-113">**Pamatojuma kods**</span><span class="sxs-lookup"><span data-stu-id="17864-113">**Reason code**</span></span> | <span data-ttu-id="17864-114">Unikālais nosaukums, lai identificētu iemeslu, kāpēc nodarbinātais varētu mainīt atvieglojumu plāna reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="17864-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="17864-115">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="17864-115">**Description**</span></span> | <span data-ttu-id="17864-116">Pamatojuma koda apraksts.</span><span class="sxs-lookup"><span data-stu-id="17864-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="17864-117">Sadaļā **Piemērojamie scenāriji** iestatiet **Atvieglojumu pārvaldība** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="17864-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="17864-118">(Nav piemērojams, ja iemeslu kodi vēl nav migrēti uz darbvietu **Personāla pārvaldība**.)</span><span class="sxs-lookup"><span data-stu-id="17864-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="17864-119">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="17864-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="17864-120">Iemesla kodu manuāla migrēšana uz Personāla pārvaldību</span><span class="sxs-lookup"><span data-stu-id="17864-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="17864-121">2021. gada janvārī iemeslu kodi tiek migrēti uz darbvietu **Personāla vadība**, nevis uz darbvietu **Atvieglojumu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="17864-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="17864-122">Vairums iemesla koda datu tiks automātiski migrēti jūsu vidē.</span><span class="sxs-lookup"><span data-stu-id="17864-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="17864-123">Daži iemesla koda dati, iespējams, netiks migrēti.</span><span class="sxs-lookup"><span data-stu-id="17864-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="17864-124">Piemēram, iemeslu kodiem tagad ir maksimālais 15 rakstzīmju skaits, tāpēc visi iemeslu kodi, kas pārsniedz 15 rakstzīmes, netiks migrēti automātiski.</span><span class="sxs-lookup"><span data-stu-id="17864-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="17864-125">Jūs redzēsit reklāmkarogu darbvietas **Atvieglojumu pārvaldība** lapā **Saites**, kurā būs sniegta informācija par migrāciju un to, vai kādi iemeslu kodi netika migrēti.</span><span class="sxs-lookup"><span data-stu-id="17864-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="17864-126">Atlasiet **Iemeslu kodi**, lai skatītu detalizētu informāciju par migrācijas statusu.</span><span class="sxs-lookup"><span data-stu-id="17864-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="17864-127">[![Iemeslu kodi](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="17864-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="17864-128">Atlasiet iemeslu kodu, kas netika migrēts.</span><span class="sxs-lookup"><span data-stu-id="17864-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="17864-129">[![Iemesla koda migrācijas statuss](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="17864-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="17864-130">Atlasiet **Migrēt iemesla kodu**.</span><span class="sxs-lookup"><span data-stu-id="17864-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="17864-131">[![Migrēt iemesla kodu](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="17864-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="17864-132">Rūtī **Atvieglojuma iemesla koda migrācija** jums ir divas opcijas kartēšanai uz Personāla pārvaldības iemesla kodu:</span><span class="sxs-lookup"><span data-stu-id="17864-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="17864-133">Lai Personāla pārvaldībā izmantotu esošu iemesla kodu, izvēlieties vienu kodu nolaižamajā sarakstā **Izmantot esošo iemesla kodu**.</span><span class="sxs-lookup"><span data-stu-id="17864-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="17864-134">Personāla pārvaldībā varat izmantot esošu iemesla kodu tikai tad, ja cits Atvieglojumu pārvaldības iemesla kods vēl nav migrēts uz to.</span><span class="sxs-lookup"><span data-stu-id="17864-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="17864-135">Lai Personāla pārvaldībā izveidotu jaunu iemesla kodu, ievadiet jaunu iemesla kodu sadaļā **Jauns iemesla kods** un tam ievadiet aprakstu sadaļā **Jauns apraksts**.</span><span class="sxs-lookup"><span data-stu-id="17864-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="17864-136">[![Kartēt uz Personāla pārvaldības iemesla kodu](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="17864-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="17864-137">Kad iemeslu kodi ir migrēti uz Personāla pārvaldību, opcija tos izmantot Atvieglojumu pārvaldībā tiek automātiski iestatīta uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="17864-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="17864-138">[![Izmantot iemesla kodu Atvieglojumu pārvaldībā](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="17864-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]