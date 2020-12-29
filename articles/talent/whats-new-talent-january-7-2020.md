---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2020. gada 7. janvāris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461883"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="11534-103">Jaunumi un izmaiņas programmā Dynamics 365 Talent (2020. gada 7. janvāris)</span><span class="sxs-lookup"><span data-stu-id="11534-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="11534-104">Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="11534-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="11534-105">Izmaiņas programmā Attract</span><span class="sxs-lookup"><span data-stu-id="11534-105">Changes in Attract</span></span>

<span data-ttu-id="11534-106">Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="11534-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="11534-107">Izmaiņas programmā Onboard</span><span class="sxs-lookup"><span data-stu-id="11534-107">Changes in Onboard</span></span>

<span data-ttu-id="11534-108">Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="11534-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="11534-109">Izmaiņas programmā Core HR</span><span class="sxs-lookup"><span data-stu-id="11534-109">Changes in Core HR</span></span>

<span data-ttu-id="11534-110">Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2697.</span><span class="sxs-lookup"><span data-stu-id="11534-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="11534-111">Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="11534-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="11534-112">Nevar dzēst darbiniekus, kuriem nav nodarbinātības ierakstu – (386157)</span><span class="sxs-lookup"><span data-stu-id="11534-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="11534-113">Šī izmaiņa pievieno dzēšanas opciju veidlapā **Darbinieki bez nodarbinātības**.</span><span class="sxs-lookup"><span data-stu-id="11534-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="11534-114">Darbinieki parādās šajā veidlapā, kad darbiniekam nepastāv nākotnes, aktīva vai vēsturiska nodarbinātība.</span><span class="sxs-lookup"><span data-stu-id="11534-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="11534-115">Šajā laidienā dzēšana ir aktivizēta tikai sistēmas administratoriem.</span><span class="sxs-lookup"><span data-stu-id="11534-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="11534-116">Tomēr nākamās nedēļas laidienā drošība tiks atjaunināta, lai ļautu visiem lietotājiem ar personāla vadības asistenta lomu noņemt darbiniekus bez nodarbinātības.</span><span class="sxs-lookup"><span data-stu-id="11534-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="11534-117">Šīs izmaiņas var veikt arī manuāli, veicot šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="11534-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="11534-118">Ejiet uz **Drošības konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="11534-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="11534-119">Cilnē **Privilēģijas** filtrējiet sarakstu **Privilēģijas** **Uzturēt darbiniekus**.</span><span class="sxs-lookup"><span data-stu-id="11534-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="11534-120">Kolonnā **Atsauces** atlasiet **Displeja izvēlnes elementi**.</span><span class="sxs-lookup"><span data-stu-id="11534-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="11534-121">Kolonnā **Displeja izvēlnes vienumi** atlasiet **HcmWOrkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="11534-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="11534-122">Iestatiet **Dzēšanas** atļauju uz Piešķirt.</span><span class="sxs-lookup"><span data-stu-id="11534-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="11534-123">Atlasiet cilni **Nepublicētie objekti**.</span><span class="sxs-lookup"><span data-stu-id="11534-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="11534-124">Atlasiet **Publicēt visus**.</span><span class="sxs-lookup"><span data-stu-id="11534-124">Select **Publish all**.</span></span>
