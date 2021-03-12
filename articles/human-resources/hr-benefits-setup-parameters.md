---
title: Iestatīt Atvieglojumu pārvaldību un Darbinieku pašapkalpošanās parametrus visiem uzņēmumiem
description: Konfigurēt Atvieglojumu pārvaldības parametrus un Darbinieku pašapkalpošanos programmā Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
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
ms.openlocfilehash: b50c4f71789c34f08ce810312f3c3198303b031e
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2021
ms.locfileid: "4962444"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="9a137-103">Iestatīt Atvieglojumu pārvaldību un Darbinieku pašapkalpošanās parametrus visiem uzņēmumiem</span><span class="sxs-lookup"><span data-stu-id="9a137-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

<span data-ttu-id="9a137-104">Pirms varat iestatīt atvieglojumu plānus risinājumā Microsoft Dynamics 365 Human Resources, ir jākonfigurē atvieglojumu pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="9a137-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="9a137-105">Šie parametri iestata noklusējuma vērtības, pamatojuma kodus un citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="9a137-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="9a137-106">Vispārējo parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="9a137-106">Configure general parameters</span></span>

1. <span data-ttu-id="9a137-107">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Personāla vadības kopīgie parametri**.</span><span class="sxs-lookup"><span data-stu-id="9a137-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="9a137-108">Cilnē **Atvieglojumu pārvaldība** norādiet vērtības šiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="9a137-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="9a137-109">Lauks</span><span class="sxs-lookup"><span data-stu-id="9a137-109">Field</span></span> | <span data-ttu-id="9a137-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="9a137-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9a137-111">**Valsts/reģions**</span><span class="sxs-lookup"><span data-stu-id="9a137-111">**Country/region**</span></span> | <span data-ttu-id="9a137-112">Lauks **Valsts/reģions** nosaka pasta kodu/štatu rādīšanas secību.</span><span class="sxs-lookup"><span data-stu-id="9a137-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="9a137-113">Nolaižamajā sarakstā pirmā tiek parādīta atlasītā valsts.</span><span class="sxs-lookup"><span data-stu-id="9a137-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="9a137-114">**Reģistrācijas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="9a137-114">**Enrollment reason code**</span></span> | <span data-ttu-id="9a137-115">Atlasiet noklusēto pamatojuma kodu, ko izmantot, kad tiek izveidoti nodarbināto plāni atvērtās reģistrācijas apstrādes laikā.</span><span class="sxs-lookup"><span data-stu-id="9a137-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="9a137-116">**Atcelšanas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="9a137-116">**Cancellation reason code**</span></span> | <span data-ttu-id="9a137-117">Pamatojuma kods, kas jāizmanto nodarbinātā atvieglojumu plāna atcelšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="9a137-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="9a137-118">Atcelšanas laikā tas rāda dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9a137-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="9a137-119">Ja nepieciešams, lietotāji var mainīt **Atcelšanas pamatojuma kodu**.</span><span class="sxs-lookup"><span data-stu-id="9a137-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="9a137-120">**Atkārtotas atvēršanas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="9a137-120">**Reopen reason code**</span></span> | <span data-ttu-id="9a137-121">Pamatojuma kods, kas jāizmanto nodarbinātā atvieglojumu plāna atkārtotas atvēršanas laikā.</span><span class="sxs-lookup"><span data-stu-id="9a137-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="9a137-122">Atcelšanas laikā tas rāda dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="9a137-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="9a137-123">Ja nepieciešams, lietotāji var mainīt **Atkārtotas atvēršanas pamatojuma kodu**.</span><span class="sxs-lookup"><span data-stu-id="9a137-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="9a137-124">**Dzīves notikuma iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="9a137-124">**Life event reason code**</span></span> | <span data-ttu-id="9a137-125">Pamatojuma kods, ko izmantot, kad notiek dzīves notikums.</span><span class="sxs-lookup"><span data-stu-id="9a137-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="9a137-126">**Likmju maiņas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="9a137-126">**Rate change reason code**</span></span> | <span data-ttu-id="9a137-127">Pamatojuma kods, ko izmantot, atceļot un atkārtoti atverot nodarbinātā atvieglojumu plānu likmes izmaiņu atjaunināšanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="9a137-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="9a137-128">Tas norāda, kuri ieraksti tika mainīti pēc likmes izmaiņu atjaunināšanas procesa.</span><span class="sxs-lookup"><span data-stu-id="9a137-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="9a137-129">**Atvieglojumu gada alga**</span><span class="sxs-lookup"><span data-stu-id="9a137-129">**Benefits annual salary**</span></span> | <span data-ttu-id="9a137-130">Ļauj iestatīt **Atvieglojumu gada alga** summu darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="9a137-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="9a137-131">Human Resources izmanto **Atvieglojumi gada algai** summu, nosakot vajadzību summas, nevis fiksētās atlīdzības gada summu.</span><span class="sxs-lookup"><span data-stu-id="9a137-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="9a137-132">**Piemērots jaunai pieņemšanai darbā**</span><span class="sxs-lookup"><span data-stu-id="9a137-132">**New hire eligible**</span></span> | <span data-ttu-id="9a137-133">Norāda vai ir iespējams veikt jaunu pieņemšanu darbā.</span><span class="sxs-lookup"><span data-stu-id="9a137-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="9a137-134">**Jauns pieņemšanas darbā reģistrācijas periods**</span><span class="sxs-lookup"><span data-stu-id="9a137-134">**New hire enrollment period**</span></span> | <span data-ttu-id="9a137-135">Laika periods, kurā atļauta jauna pieņemšanas darbā reģistrācija.</span><span class="sxs-lookup"><span data-stu-id="9a137-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="9a137-136">**Piezīme**: Šis iestatījums labo jebkuru jaunas darbā pieņemšanas reģistrācijas periodu, kuru iestatāt plāna piemērojamības kārtulai.</span><span class="sxs-lookup"><span data-stu-id="9a137-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="9a137-137">**Noklusējuma maksājumu biežums**</span><span class="sxs-lookup"><span data-stu-id="9a137-137">**Default pay frequency**</span></span> | <span data-ttu-id="9a137-138">Noklusējuma maksājumu biežums, kas jāizmanto, pievienojot jaunus darbiniekus.</span><span class="sxs-lookup"><span data-stu-id="9a137-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="9a137-139">**Dzīves notikumi iespējoti**</span><span class="sxs-lookup"><span data-stu-id="9a137-139">**Life events enabled**</span></span> | <span data-ttu-id="9a137-140">Iespējo dzīves notikumus.</span><span class="sxs-lookup"><span data-stu-id="9a137-140">Enables life events.</span></span> |
   | <span data-ttu-id="9a137-141">**Paslēpt mantoto atvieglojumu veidlapas**</span><span class="sxs-lookup"><span data-stu-id="9a137-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="9a137-142">Ļauj slēpt mantotās atvieglojumu veidlapas.</span><span class="sxs-lookup"><span data-stu-id="9a137-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="9a137-143">**Atvieglojuma pārbaude**</span><span class="sxs-lookup"><span data-stu-id="9a137-143">**Benefit verification**</span></span> | <span data-ttu-id="9a137-144">Pārbaudes teksts patstāvīgi izmantojamā pakalpojuma atvieglojumu izrakstīšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="9a137-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="9a137-145">**Automātiski atlasīt saņēmējus**</span><span class="sxs-lookup"><span data-stu-id="9a137-145">**Auto select designees**</span></span> | <span data-ttu-id="9a137-146">Norāda, vai automātiski atlasīt pakārtotos un saņēmējus, pamatojoties uz viņu piemērotību plāna opcijām.</span><span class="sxs-lookup"><span data-stu-id="9a137-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="9a137-147">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="9a137-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="9a137-148">Konfigurēt nodarbinātā patstāvīgi izmantojamo pakalpojumu parametrus</span><span class="sxs-lookup"><span data-stu-id="9a137-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="9a137-149">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Personāla vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="9a137-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="9a137-150">Cilnē **Atvieglojumu pārvaldība** norādiet vērtības šiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="9a137-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="9a137-151">Lauks</span><span class="sxs-lookup"><span data-stu-id="9a137-151">Field</span></span> | <span data-ttu-id="9a137-152">Apraksts</span><span class="sxs-lookup"><span data-stu-id="9a137-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9a137-153">**Atvieglojuma pārbaude**</span><span class="sxs-lookup"><span data-stu-id="9a137-153">**Benefit verification**</span></span> | <span data-ttu-id="9a137-154">Pārbaudes teksts patstāvīgi izmantojamā pakalpojuma atvieglojumu izrakstīšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="9a137-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="9a137-155">**Automātiski atlasīt saņēmējus**</span><span class="sxs-lookup"><span data-stu-id="9a137-155">**Auto select designees**</span></span> | <span data-ttu-id="9a137-156">Norāda, vai automātiski atlasīt pakārtotos un saņēmējus, pamatojoties uz viņu piemērotību plāna opcijām.</span><span class="sxs-lookup"><span data-stu-id="9a137-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="9a137-157">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="9a137-157">Select **Save**.</span></span>


