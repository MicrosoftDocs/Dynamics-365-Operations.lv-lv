---
title: Iestatīt atvieglojumu pārvaldības parametrus
description: Konfigurējiet parametrus atvieglojumu pārvaldībai risinājumā Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009815"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="d4d1a-103">Iestatīt atvieglojumu pārvaldības parametrus</span><span class="sxs-lookup"><span data-stu-id="d4d1a-103">Set Benefits management parameters</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="d4d1a-104">Pirms varat iestatīt atvaļinājumu plānus risinājumā Microsoft Dynamics 365 Human Resources, ir jākonfigurē atvieglojumu pārvaldības parametri.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you need to configure Benefits management parameters.</span></span> <span data-ttu-id="d4d1a-105">Šie parametri iestata noklusējuma vērtības, pamatojuma kodus un citas opcijas.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="d4d1a-106">Vispārējo parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="d4d1a-106">Configure general parameters</span></span>

1. <span data-ttu-id="d4d1a-107">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="d4d1a-108">Cilnē **Vispārīgi** norādiet vērtības šiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="d4d1a-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="d4d1a-109">Lauks</span><span class="sxs-lookup"><span data-stu-id="d4d1a-109">Field</span></span> | <span data-ttu-id="d4d1a-110">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d4d1a-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d4d1a-111">**Valsts/reģions**</span><span class="sxs-lookup"><span data-stu-id="d4d1a-111">**Country/region**</span></span> | <span data-ttu-id="d4d1a-112">Lauks **Valsts/reģions** nosaka pasta kodu/štatu rādīšanas secību.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="d4d1a-113">Nolaižamajā sarakstā pirmā tiek parādīta atlasītā valsts.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="d4d1a-114">**Reģistrācijas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="d4d1a-114">**Enrollment reason code**</span></span> | <span data-ttu-id="d4d1a-115">Atlasiet noklusēto pamatojuma kodu, ko izmantot, kad tiek izveidoti nodarbināto plāni atvērtās reģistrācijas apstrādes laikā.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="d4d1a-116">**Atcelšanas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="d4d1a-116">**Cancellation reason code**</span></span> | <span data-ttu-id="d4d1a-117">Pamatojuma kods, kas jāizmanto nodarbinātā atvieglojumu plāna atcelšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="d4d1a-118">Atcelšanas laikā tas rāda dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="d4d1a-119">Ja nepieciešams, lietotāji var mainīt **Atcelšanas pamatojuma kodu**.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="d4d1a-120">**Atkārtotas atvēršanas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="d4d1a-120">**Reopen reason code**</span></span> | <span data-ttu-id="d4d1a-121">Pamatojuma kods, kas jāizmanto nodarbinātā atvieglojumu plāna atkārtotas atvēršanas laikā.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="d4d1a-122">Atcelšanas laikā tas rāda dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="d4d1a-123">Ja nepieciešams, lietotāji var mainīt **Atkārtotas atvēršanas pamatojuma kodu**.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="d4d1a-124">**Dzīves notikuma iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="d4d1a-124">**Life event reason code**</span></span> | <span data-ttu-id="d4d1a-125">Pamatojuma kods, ko izmantot, kad notiek dzīves notikums.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="d4d1a-126">**Likmju maiņas iemesla kods**</span><span class="sxs-lookup"><span data-stu-id="d4d1a-126">**Rate change reason code**</span></span> | <span data-ttu-id="d4d1a-127">Pamatojuma kods, ko izmantot, atceļot un atkārtoti atverot nodarbinātā atvieglojumu plānu likmes izmaiņu atjaunināšanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="d4d1a-128">Tas norāda, kuri ieraksti tika mainīti pēc likmes izmaiņu atjaunināšanas procesa.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="d4d1a-129">**Piemērots jaunai pieņemšanai darbā**</span><span class="sxs-lookup"><span data-stu-id="d4d1a-129">**New hire eligible**</span></span> | <span data-ttu-id="d4d1a-130">Norāda vai ir iespējams veikt jaunu pieņemšanu darbā.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="d4d1a-131">**Jauns pieņemšanas darbā reģistrācijas periods**</span><span class="sxs-lookup"><span data-stu-id="d4d1a-131">**New hire enrollment period**</span></span> | <span data-ttu-id="d4d1a-132">Laika periods, kurā atļauta jauna pieņemšanas darbā reģistrācija.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="d4d1a-133">**Piezīme**: Šis iestatījums labo jebkuru jaunas darbā pieņemšanas reģistrācijas periodu, kuru iestatāt plāna piemērojamības kārtulai.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="d4d1a-134">**Gada algas uzlabojums**</span><span class="sxs-lookup"><span data-stu-id="d4d1a-134">**Annual salary enhancement**</span></span> | <span data-ttu-id="d4d1a-135">Norāda, vai automātiski aprēķināt **Gada atvieglojumu algas** summu **Nodarbinātības atvieglojumu informācijā**.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-135">Specifies whether to automatically calculate the **Annual benefit salary** amount in **Employment Benefit Details**.</span></span> <span data-ttu-id="d4d1a-136">Tas ir balstīts uz nodarbinātā **Fiksētās atlīdzības algas likmi**,**Vidējo laiku** un **Maksājuma biežumu**.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-136">It's based on the employee’s **Fixed compensation pay rate**, **Average hours**, and **Payment frequency**.</span></span></br></br><span data-ttu-id="d4d1a-137">**Vidējais laiks** x **Fiksētās algas likme** x **Maksājuma biežums** (# no apmaksas periodiem) = **Gada atvieglojumu alga**</span><span class="sxs-lookup"><span data-stu-id="d4d1a-137">**Average hours** x **Fixed pay rate** x **Payment frequency** (# of pay periods) = **Annual benefit salary**</span></span> </br></br><span data-ttu-id="d4d1a-138">Ja kāda no vērtībām laukos **Vidējais laiks**, **Fiksētās atlīdzības izmaksas likme** vai **Maksājumu biežums** lauki mainās, sistēma automātiski pārrēķinās nodarbinātā **Gada atvieglojumu algas** summu, pamatojoties uz mainītajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-138">If any of the values in the **Average hours**, **Fixed compensation pay rate**, or **Payment frequency** fields change, the system automatically recalculates the employee’s **Annual benefit salary** amount based on the changed values.</span></span> <span data-ttu-id="d4d1a-139">Sistēma izveido ierakstu **Spēkā stāšanās datums**, lai noteiktu precīzu datumu un laiku, kad izmaiņas notikušas.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-139">The system creates a **Date effective** record to identify the exact date and time the change occurred.</span></span> <span data-ttu-id="d4d1a-140">Ja nepieciešams, varat manuāli rediģēt **Gada atvieglojumu algas** summu.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-140">You can manually edit the **Annual benefit salary** amount if necessary.</span></span> |
   | <span data-ttu-id="d4d1a-141">**Dzīves notikumi iespējoti**</span><span class="sxs-lookup"><span data-stu-id="d4d1a-141">**Life events enabled**</span></span> | <span data-ttu-id="d4d1a-142">Iespējo dzīves notikumus.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-142">Enables life events.</span></span> |
   | <span data-ttu-id="d4d1a-143">**Paslēpt mantoto atvieglojumu veidlapas**</span><span class="sxs-lookup"><span data-stu-id="d4d1a-143">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="d4d1a-144">Ļauj slēpt mantotās atvieglojumu veidlapas.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-144">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="d4d1a-145">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-145">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="d4d1a-146">Konfigurēt nodarbinātā patstāvīgi izmantojamo pakalpojumu parametrus</span><span class="sxs-lookup"><span data-stu-id="d4d1a-146">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="d4d1a-147">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-147">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="d4d1a-148">Cilnē **Nodarbinātā patstāvīgi izmantojamie pakalpojumi** norādiet vērtības šiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="d4d1a-148">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="d4d1a-149">Lauks</span><span class="sxs-lookup"><span data-stu-id="d4d1a-149">Field</span></span> | <span data-ttu-id="d4d1a-150">Apraksts</span><span class="sxs-lookup"><span data-stu-id="d4d1a-150">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d4d1a-151">**Atvieglojuma pārbaude**</span><span class="sxs-lookup"><span data-stu-id="d4d1a-151">**Benefit verification**</span></span> | <span data-ttu-id="d4d1a-152">Pārbaudes teksts patstāvīgi izmantojamā pakalpojuma atvieglojumu izrakstīšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-152">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="d4d1a-153">**Automātiski atlasīt saņēmējus**</span><span class="sxs-lookup"><span data-stu-id="d4d1a-153">**Auto select designees**</span></span> | <span data-ttu-id="d4d1a-154">Norāda, vai automātiski atlasīt pakārtotos un saņēmējus, pamatojoties uz viņu piemērotību plāna opcijām.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-154">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="d4d1a-155">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="d4d1a-155">Select **Save**.</span></span>
