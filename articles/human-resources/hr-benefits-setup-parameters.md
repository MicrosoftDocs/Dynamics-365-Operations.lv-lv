---
title: Iestatīt atvieglojumu pārvaldības parametrus
description: Konfigurējiet parametrus atvieglojumu pārvaldībai risinājumā Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d6d463df08b9ae68047f09316f19e98740a8441
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229767"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="abc76-103">Iestatīt priekšrocību pārvaldības parametrus</span><span class="sxs-lookup"><span data-stu-id="abc76-103">Set Benefits management parameters</span></span>

<span data-ttu-id="abc76-104">Pirms varat iestatīt atvaļinājumu plānus risinājumā Microsoft Dynamics 365 Human Resources, ir jākonfigurē atvieglojumu pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="abc76-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="abc76-105">Šie parametri iestata noklusējuma vērtības, pamatojuma kodus un citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="abc76-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="abc76-106">Vispārējo parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="abc76-106">Configure general parameters</span></span>

1. <span data-ttu-id="abc76-107">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="abc76-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="abc76-108">Cilnē **Vispārīgi** norādiet vērtības šiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="abc76-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="abc76-109">Lauks</span><span class="sxs-lookup"><span data-stu-id="abc76-109">Field</span></span> | <span data-ttu-id="abc76-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="abc76-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="abc76-111">**Valsts/reģions**</span><span class="sxs-lookup"><span data-stu-id="abc76-111">**Country/region**</span></span> | <span data-ttu-id="abc76-112">Lauks **Valsts/reģions** nosaka pasta kodu/štatu rādīšanas secību.</span><span class="sxs-lookup"><span data-stu-id="abc76-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="abc76-113">Nolaižamajā sarakstā pirmā tiek parādīta atlasītā valsts.</span><span class="sxs-lookup"><span data-stu-id="abc76-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="abc76-114">**Reģistrācijas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="abc76-114">**Enrollment reason code**</span></span> | <span data-ttu-id="abc76-115">Atlasiet noklusēto pamatojuma kodu, ko izmantot, kad tiek izveidoti nodarbināto plāni atvērtās reģistrācijas apstrādes laikā.</span><span class="sxs-lookup"><span data-stu-id="abc76-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="abc76-116">**Atcelšanas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="abc76-116">**Cancellation reason code**</span></span> | <span data-ttu-id="abc76-117">Pamatojuma kods, kas jāizmanto nodarbinātā atvieglojumu plāna atcelšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="abc76-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="abc76-118">Atcelšanas laikā tas rāda dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="abc76-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="abc76-119">Ja nepieciešams, lietotāji var mainīt **Atcelšanas pamatojuma kodu**.</span><span class="sxs-lookup"><span data-stu-id="abc76-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="abc76-120">**Atkārtotas atvēršanas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="abc76-120">**Reopen reason code**</span></span> | <span data-ttu-id="abc76-121">Pamatojuma kods, kas jāizmanto nodarbinātā atvieglojumu plāna atkārtotas atvēršanas laikā.</span><span class="sxs-lookup"><span data-stu-id="abc76-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="abc76-122">Atcelšanas laikā tas rāda dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="abc76-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="abc76-123">Ja nepieciešams, lietotāji var mainīt **Atkārtotas atvēršanas pamatojuma kodu**.</span><span class="sxs-lookup"><span data-stu-id="abc76-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="abc76-124">**Dzīves notikuma iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="abc76-124">**Life event reason code**</span></span> | <span data-ttu-id="abc76-125">Pamatojuma kods, ko izmantot, kad notiek dzīves notikums.</span><span class="sxs-lookup"><span data-stu-id="abc76-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="abc76-126">**Likmju maiņas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="abc76-126">**Rate change reason code**</span></span> | <span data-ttu-id="abc76-127">Pamatojuma kods, ko izmantot, atceļot un atkārtoti atverot nodarbinātā atvieglojumu plānu likmes izmaiņu atjaunināšanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="abc76-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="abc76-128">Tas norāda, kuri ieraksti tika mainīti pēc likmes izmaiņu atjaunināšanas procesa.</span><span class="sxs-lookup"><span data-stu-id="abc76-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="abc76-129">**Piemērots jaunai pieņemšanai darbā**</span><span class="sxs-lookup"><span data-stu-id="abc76-129">**New hire eligible**</span></span> | <span data-ttu-id="abc76-130">Norāda vai ir iespējams veikt jaunu pieņemšanu darbā.</span><span class="sxs-lookup"><span data-stu-id="abc76-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="abc76-131">**Jauns pieņemšanas darbā reģistrācijas periods**</span><span class="sxs-lookup"><span data-stu-id="abc76-131">**New hire enrollment period**</span></span> | <span data-ttu-id="abc76-132">Laika periods, kurā atļauta jauna pieņemšanas darbā reģistrācija.</span><span class="sxs-lookup"><span data-stu-id="abc76-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="abc76-133">**Piezīme**: Šis iestatījums labo jebkuru jaunas darbā pieņemšanas reģistrācijas periodu, kuru iestatāt plāna piemērojamības kārtulai.</span><span class="sxs-lookup"><span data-stu-id="abc76-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="abc76-134">**Dzīves notikumi iespējoti**</span><span class="sxs-lookup"><span data-stu-id="abc76-134">**Life events enabled**</span></span> | <span data-ttu-id="abc76-135">Iespējo dzīves notikumus.</span><span class="sxs-lookup"><span data-stu-id="abc76-135">Enables life events.</span></span> |
   | <span data-ttu-id="abc76-136">**Paslēpt mantoto atvieglojumu veidlapas**</span><span class="sxs-lookup"><span data-stu-id="abc76-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="abc76-137">Ļauj slēpt mantotās atvieglojumu veidlapas.</span><span class="sxs-lookup"><span data-stu-id="abc76-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="abc76-138">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="abc76-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="abc76-139">Konfigurēt nodarbinātā patstāvīgi izmantojamo pakalpojumu parametrus</span><span class="sxs-lookup"><span data-stu-id="abc76-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="abc76-140">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="abc76-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="abc76-141">Cilnē **Nodarbinātā patstāvīgi izmantojamie pakalpojumi** norādiet vērtības šiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="abc76-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="abc76-142">Lauks</span><span class="sxs-lookup"><span data-stu-id="abc76-142">Field</span></span> | <span data-ttu-id="abc76-143">Apraksts</span><span class="sxs-lookup"><span data-stu-id="abc76-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="abc76-144">**Atvieglojuma pārbaude**</span><span class="sxs-lookup"><span data-stu-id="abc76-144">**Benefit verification**</span></span> | <span data-ttu-id="abc76-145">Pārbaudes teksts patstāvīgi izmantojamā pakalpojuma atvieglojumu izrakstīšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="abc76-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="abc76-146">**Automātiski atlasīt saņēmējus**</span><span class="sxs-lookup"><span data-stu-id="abc76-146">**Auto select designees**</span></span> | <span data-ttu-id="abc76-147">Norāda, vai automātiski atlasīt pakārtotos un saņēmējus, pamatojoties uz viņu piemērotību plāna opcijām.</span><span class="sxs-lookup"><span data-stu-id="abc76-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="abc76-148">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="abc76-148">Select **Save**.</span></span>
