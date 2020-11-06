---
title: Iestatīt atvieglojumu pārvaldības parametrus
description: Konfigurējiet parametrus atvieglojumu pārvaldībai risinājumā Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 07/16/2020
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
ms.openlocfilehash: cb9dd6eb8ef840dab54eabab8526200a3a8e21f0
ms.sourcegitcommit: e100c1c7c8dcdacf066defc206dd2f44b8ce6100
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/20/2020
ms.locfileid: "4057032"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="50d6f-103">Iestatīt priekšrocību pārvaldības parametrus</span><span class="sxs-lookup"><span data-stu-id="50d6f-103">Set Benefits management parameters</span></span>

<span data-ttu-id="50d6f-104">Pirms varat iestatīt atvaļinājumu plānus risinājumā Microsoft Dynamics 365 Human Resources, ir jākonfigurē atvieglojumu pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="50d6f-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="50d6f-105">Šie parametri iestata noklusējuma vērtības, pamatojuma kodus un citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="50d6f-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="50d6f-106">Vispārējo parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="50d6f-106">Configure general parameters</span></span>

1. <span data-ttu-id="50d6f-107">Darbvietā **Atvieglojumu pārvaldība** , sadaļā **Iestatījumi** atlasiet **Personāla vadības kopīgie parametri**.</span><span class="sxs-lookup"><span data-stu-id="50d6f-107">In the **Benefits management** workspace, under **Setup** , select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="50d6f-108">Cilnē **Vispārīgi** norādiet vērtības šiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="50d6f-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="50d6f-109">Lauks</span><span class="sxs-lookup"><span data-stu-id="50d6f-109">Field</span></span> | <span data-ttu-id="50d6f-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="50d6f-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="50d6f-111">**Valsts/reģions**</span><span class="sxs-lookup"><span data-stu-id="50d6f-111">**Country/region**</span></span> | <span data-ttu-id="50d6f-112">Lauks **Valsts/reģions** nosaka pasta kodu/štatu rādīšanas secību.</span><span class="sxs-lookup"><span data-stu-id="50d6f-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="50d6f-113">Nolaižamajā sarakstā pirmā tiek parādīta atlasītā valsts.</span><span class="sxs-lookup"><span data-stu-id="50d6f-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="50d6f-114">**Reģistrācijas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="50d6f-114">**Enrollment reason code**</span></span> | <span data-ttu-id="50d6f-115">Atlasiet noklusēto pamatojuma kodu, ko izmantot, kad tiek izveidoti nodarbināto plāni atvērtās reģistrācijas apstrādes laikā.</span><span class="sxs-lookup"><span data-stu-id="50d6f-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="50d6f-116">**Atcelšanas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="50d6f-116">**Cancellation reason code**</span></span> | <span data-ttu-id="50d6f-117">Pamatojuma kods, kas jāizmanto nodarbinātā atvieglojumu plāna atcelšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="50d6f-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="50d6f-118">Atcelšanas laikā tas rāda dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50d6f-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="50d6f-119">Ja nepieciešams, lietotāji var mainīt **Atcelšanas pamatojuma kodu**.</span><span class="sxs-lookup"><span data-stu-id="50d6f-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="50d6f-120">**Atkārtotas atvēršanas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="50d6f-120">**Reopen reason code**</span></span> | <span data-ttu-id="50d6f-121">Pamatojuma kods, kas jāizmanto nodarbinātā atvieglojumu plāna atkārtotas atvēršanas laikā.</span><span class="sxs-lookup"><span data-stu-id="50d6f-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="50d6f-122">Atcelšanas laikā tas rāda dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="50d6f-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="50d6f-123">Ja nepieciešams, lietotāji var mainīt **Atkārtotas atvēršanas pamatojuma kodu**.</span><span class="sxs-lookup"><span data-stu-id="50d6f-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="50d6f-124">**Dzīves notikuma iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="50d6f-124">**Life event reason code**</span></span> | <span data-ttu-id="50d6f-125">Pamatojuma kods, ko izmantot, kad notiek dzīves notikums.</span><span class="sxs-lookup"><span data-stu-id="50d6f-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="50d6f-126">**Likmju maiņas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="50d6f-126">**Rate change reason code**</span></span> | <span data-ttu-id="50d6f-127">Pamatojuma kods, ko izmantot, atceļot un atkārtoti atverot nodarbinātā atvieglojumu plānu likmes izmaiņu atjaunināšanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="50d6f-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="50d6f-128">Tas norāda, kuri ieraksti tika mainīti pēc likmes izmaiņu atjaunināšanas procesa.</span><span class="sxs-lookup"><span data-stu-id="50d6f-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="50d6f-129">**Atvieglojumu gada alga**</span><span class="sxs-lookup"><span data-stu-id="50d6f-129">**Benefits annual salary**</span></span> | <span data-ttu-id="50d6f-130">Ļauj iestatīt **Atvieglojumu gada alga** summu darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="50d6f-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="50d6f-131">Human Resources izmanto **Atvieglojumu gada alga** summu, nosakot vajadzību summas, nevis fiksētās atlīdzības gada summu.</span><span class="sxs-lookup"><span data-stu-id="50d6f-131">Human Resources will use the **Benefits annual salary** amount when determing coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="50d6f-132">**Piemērots jaunai pieņemšanai darbā**</span><span class="sxs-lookup"><span data-stu-id="50d6f-132">**New hire eligible**</span></span> | <span data-ttu-id="50d6f-133">Norāda vai ir iespējams veikt jaunu pieņemšanu darbā.</span><span class="sxs-lookup"><span data-stu-id="50d6f-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="50d6f-134">**Jauns pieņemšanas darbā reģistrācijas periods**</span><span class="sxs-lookup"><span data-stu-id="50d6f-134">**New hire enrollment period**</span></span> | <span data-ttu-id="50d6f-135">Laika periods, kurā atļauta jauna pieņemšanas darbā reģistrācija.</span><span class="sxs-lookup"><span data-stu-id="50d6f-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="50d6f-136">**Piezīme** : Šis iestatījums labo jebkuru jaunas darbā pieņemšanas reģistrācijas periodu, kuru iestatāt plāna piemērojamības kārtulai.</span><span class="sxs-lookup"><span data-stu-id="50d6f-136">**Note** : This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="50d6f-137">**Noklusējuma maksājumu biežums**</span><span class="sxs-lookup"><span data-stu-id="50d6f-137">**Default pay frequency**</span></span> | <span data-ttu-id="50d6f-138">Noklusējuma maksājumu biežums, kas jāizmanto, pievienojot jaunus darbiniekus.</span><span class="sxs-lookup"><span data-stu-id="50d6f-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="50d6f-139">**Dzīves notikumi iespējoti**</span><span class="sxs-lookup"><span data-stu-id="50d6f-139">**Life events enabled**</span></span> | <span data-ttu-id="50d6f-140">Iespējo dzīves notikumus.</span><span class="sxs-lookup"><span data-stu-id="50d6f-140">Enables life events.</span></span> |
   | <span data-ttu-id="50d6f-141">**Paslēpt mantoto atvieglojumu veidlapas**</span><span class="sxs-lookup"><span data-stu-id="50d6f-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="50d6f-142">Ļauj slēpt mantotās atvieglojumu veidlapas.</span><span class="sxs-lookup"><span data-stu-id="50d6f-142">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="50d6f-143">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="50d6f-143">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="50d6f-144">Konfigurēt nodarbinātā patstāvīgi izmantojamo pakalpojumu parametrus</span><span class="sxs-lookup"><span data-stu-id="50d6f-144">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="50d6f-145">Darbvietā **Atvieglojumu pārvaldība** , sadaļā **Iestatījumi** atlasiet **Personāla vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="50d6f-145">In the **Benefits management** workspace, under **Setup** , select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="50d6f-146">Cilnē **Atvieglojumu pārvaldība** norādiet vērtības šiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="50d6f-146">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="50d6f-147">Lauks</span><span class="sxs-lookup"><span data-stu-id="50d6f-147">Field</span></span> | <span data-ttu-id="50d6f-148">Apraksts</span><span class="sxs-lookup"><span data-stu-id="50d6f-148">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="50d6f-149">**Atvieglojuma pārbaude**</span><span class="sxs-lookup"><span data-stu-id="50d6f-149">**Benefit verification**</span></span> | <span data-ttu-id="50d6f-150">Pārbaudes teksts patstāvīgi izmantojamā pakalpojuma atvieglojumu izrakstīšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="50d6f-150">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="50d6f-151">**Automātiski atlasīt saņēmējus**</span><span class="sxs-lookup"><span data-stu-id="50d6f-151">**Auto select designees**</span></span> | <span data-ttu-id="50d6f-152">Norāda, vai automātiski atlasīt pakārtotos un saņēmējus, pamatojoties uz viņu piemērotību plāna opcijām.</span><span class="sxs-lookup"><span data-stu-id="50d6f-152">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="50d6f-153">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="50d6f-153">Select **Save**.</span></span>
