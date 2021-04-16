---
title: Iestatīt Atvieglojumu pārvaldību un Darbinieku pašapkalpošanās parametrus visiem uzņēmumiem
description: Konfigurēt Atvieglojumu pārvaldības parametrus un Darbinieku pašapkalpošanos programmā Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 10f5310ba4feba4a196d02c406ff3217637e447e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791489"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="7dbee-103">Iestatīt Atvieglojumu pārvaldību un Darbinieku pašapkalpošanās parametrus visiem uzņēmumiem</span><span class="sxs-lookup"><span data-stu-id="7dbee-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7dbee-104">Pirms varat iestatīt atvieglojumu plānus risinājumā Microsoft Dynamics 365 Human Resources, ir jākonfigurē atvieglojumu pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="7dbee-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="7dbee-105">Šie parametri iestata noklusējuma vērtības, pamatojuma kodus un citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="7dbee-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="7dbee-106">Vispārējo parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="7dbee-106">Configure general parameters</span></span>

1. <span data-ttu-id="7dbee-107">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Personāla vadības kopīgie parametri**.</span><span class="sxs-lookup"><span data-stu-id="7dbee-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="7dbee-108">Cilnē **Atvieglojumu pārvaldība** norādiet vērtības šiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="7dbee-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="7dbee-109">Lauks</span><span class="sxs-lookup"><span data-stu-id="7dbee-109">Field</span></span> | <span data-ttu-id="7dbee-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="7dbee-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="7dbee-111">**Valsts/reģions**</span><span class="sxs-lookup"><span data-stu-id="7dbee-111">**Country/region**</span></span> | <span data-ttu-id="7dbee-112">Lauks **Valsts/reģions** nosaka pasta kodu/štatu rādīšanas secību.</span><span class="sxs-lookup"><span data-stu-id="7dbee-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="7dbee-113">Nolaižamajā sarakstā pirmā tiek parādīta atlasītā valsts.</span><span class="sxs-lookup"><span data-stu-id="7dbee-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="7dbee-114">**Reģistrācijas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="7dbee-114">**Enrollment reason code**</span></span> | <span data-ttu-id="7dbee-115">Atlasiet noklusēto pamatojuma kodu, ko izmantot, kad tiek izveidoti nodarbināto plāni atvērtās reģistrācijas apstrādes laikā.</span><span class="sxs-lookup"><span data-stu-id="7dbee-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="7dbee-116">**Atcelšanas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="7dbee-116">**Cancellation reason code**</span></span> | <span data-ttu-id="7dbee-117">Pamatojuma kods, kas jāizmanto nodarbinātā atvieglojumu plāna atcelšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="7dbee-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="7dbee-118">Atcelšanas laikā tas rāda dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="7dbee-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="7dbee-119">Ja nepieciešams, lietotāji var mainīt **Atcelšanas pamatojuma kodu**.</span><span class="sxs-lookup"><span data-stu-id="7dbee-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="7dbee-120">**Atkārtotas atvēršanas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="7dbee-120">**Reopen reason code**</span></span> | <span data-ttu-id="7dbee-121">Pamatojuma kods, kas jāizmanto nodarbinātā atvieglojumu plāna atkārtotas atvēršanas laikā.</span><span class="sxs-lookup"><span data-stu-id="7dbee-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="7dbee-122">Atcelšanas laikā tas rāda dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="7dbee-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="7dbee-123">Ja nepieciešams, lietotāji var mainīt **Atkārtotas atvēršanas pamatojuma kodu**.</span><span class="sxs-lookup"><span data-stu-id="7dbee-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="7dbee-124">**Dzīves notikuma iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="7dbee-124">**Life event reason code**</span></span> | <span data-ttu-id="7dbee-125">Pamatojuma kods, ko izmantot, kad notiek dzīves notikums.</span><span class="sxs-lookup"><span data-stu-id="7dbee-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="7dbee-126">**Likmju maiņas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="7dbee-126">**Rate change reason code**</span></span> | <span data-ttu-id="7dbee-127">Pamatojuma kods, ko izmantot, atceļot un atkārtoti atverot nodarbinātā atvieglojumu plānu likmes izmaiņu atjaunināšanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="7dbee-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="7dbee-128">Tas norāda, kuri ieraksti tika mainīti pēc likmes izmaiņu atjaunināšanas procesa.</span><span class="sxs-lookup"><span data-stu-id="7dbee-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="7dbee-129">**Atvieglojumu gada alga**</span><span class="sxs-lookup"><span data-stu-id="7dbee-129">**Benefits annual salary**</span></span> | <span data-ttu-id="7dbee-130">Ļauj iestatīt **Atvieglojumu gada alga** summu darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="7dbee-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="7dbee-131">Human Resources izmanto **Atvieglojumi gada algai** summu, nosakot vajadzību summas, nevis fiksētās atlīdzības gada summu.</span><span class="sxs-lookup"><span data-stu-id="7dbee-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="7dbee-132">**Piemērots jaunai pieņemšanai darbā**</span><span class="sxs-lookup"><span data-stu-id="7dbee-132">**New hire eligible**</span></span> | <span data-ttu-id="7dbee-133">Norāda vai ir iespējams veikt jaunu pieņemšanu darbā.</span><span class="sxs-lookup"><span data-stu-id="7dbee-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="7dbee-134">**Jauns pieņemšanas darbā reģistrācijas periods**</span><span class="sxs-lookup"><span data-stu-id="7dbee-134">**New hire enrollment period**</span></span> | <span data-ttu-id="7dbee-135">Laika periods, kurā atļauta jauna pieņemšanas darbā reģistrācija.</span><span class="sxs-lookup"><span data-stu-id="7dbee-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="7dbee-136">**Piezīme**: Šis iestatījums labo jebkuru jaunas darbā pieņemšanas reģistrācijas periodu, kuru iestatāt plāna piemērojamības kārtulai.</span><span class="sxs-lookup"><span data-stu-id="7dbee-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="7dbee-137">**Noklusējuma maksājumu biežums**</span><span class="sxs-lookup"><span data-stu-id="7dbee-137">**Default pay frequency**</span></span> | <span data-ttu-id="7dbee-138">Noklusējuma maksājumu biežums, kas jāizmanto, pievienojot jaunus darbiniekus.</span><span class="sxs-lookup"><span data-stu-id="7dbee-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="7dbee-139">**Dzīves notikumi iespējoti**</span><span class="sxs-lookup"><span data-stu-id="7dbee-139">**Life events enabled**</span></span> | <span data-ttu-id="7dbee-140">Iespējo dzīves notikumus.</span><span class="sxs-lookup"><span data-stu-id="7dbee-140">Enables life events.</span></span> |
   | <span data-ttu-id="7dbee-141">**Paslēpt mantoto atvieglojumu veidlapas**</span><span class="sxs-lookup"><span data-stu-id="7dbee-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="7dbee-142">Ļauj slēpt mantotās atvieglojumu veidlapas.</span><span class="sxs-lookup"><span data-stu-id="7dbee-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="7dbee-143">**Atvieglojuma pārbaude**</span><span class="sxs-lookup"><span data-stu-id="7dbee-143">**Benefit verification**</span></span> | <span data-ttu-id="7dbee-144">Pārbaudes teksts patstāvīgi izmantojamā pakalpojuma atvieglojumu izrakstīšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="7dbee-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="7dbee-145">**Automātiski atlasīt saņēmējus**</span><span class="sxs-lookup"><span data-stu-id="7dbee-145">**Auto select designees**</span></span> | <span data-ttu-id="7dbee-146">Norāda, vai automātiski atlasīt pakārtotos un saņēmējus, pamatojoties uz viņu piemērotību plāna opcijām.</span><span class="sxs-lookup"><span data-stu-id="7dbee-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="7dbee-147">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="7dbee-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="7dbee-148">Konfigurēt nodarbinātā patstāvīgi izmantojamo pakalpojumu parametrus</span><span class="sxs-lookup"><span data-stu-id="7dbee-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="7dbee-149">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Personāla vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="7dbee-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="7dbee-150">Cilnē **Atvieglojumu pārvaldība** norādiet vērtības šiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="7dbee-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="7dbee-151">Lauks</span><span class="sxs-lookup"><span data-stu-id="7dbee-151">Field</span></span> | <span data-ttu-id="7dbee-152">Apraksts</span><span class="sxs-lookup"><span data-stu-id="7dbee-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="7dbee-153">**Atvieglojuma pārbaude**</span><span class="sxs-lookup"><span data-stu-id="7dbee-153">**Benefit verification**</span></span> | <span data-ttu-id="7dbee-154">Pārbaudes teksts patstāvīgi izmantojamā pakalpojuma atvieglojumu izrakstīšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="7dbee-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="7dbee-155">**Automātiski atlasīt saņēmējus**</span><span class="sxs-lookup"><span data-stu-id="7dbee-155">**Auto select designees**</span></span> | <span data-ttu-id="7dbee-156">Norāda, vai automātiski atlasīt pakārtotos un saņēmējus, pamatojoties uz viņu piemērotību plāna opcijām.</span><span class="sxs-lookup"><span data-stu-id="7dbee-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="7dbee-157">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="7dbee-157">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]