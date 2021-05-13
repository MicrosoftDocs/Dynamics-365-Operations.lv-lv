---
title: Nodarbinātie bez nodarbinātības
description: Darbinieki, kuriem nav turpmākas, aktīvas vai vēsturiskas nodarbinātības jūsu organizācijā, parādās veidlapā Darbinieki bez nodarbinātības.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1a137de25924f4c4ec6f6b1fe70f9d21af591c0
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924575"
---
# <a name="workers-without-employment"></a><span data-ttu-id="89bd9-103">Nodarbinātie bez nodarbinātības</span><span class="sxs-lookup"><span data-stu-id="89bd9-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="89bd9-104">Darbinieki, kuriem nav turpmākas, aktīvas vai vēsturiskas nodarbinātības jūsu organizācijā, parādās veidlapā **Darbinieki bez nodarbinātības**.</span><span class="sxs-lookup"><span data-stu-id="89bd9-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="89bd9-105">Darbinieki ar šādu statusu var parādīties, ja importējat darbiniekus bez nodarbinātības ieraksta vai ja dzēšat darbinieka nodarbinātību, izmantojot **Darbinieki > Nodarbinātības vēsture**.</span><span class="sxs-lookup"><span data-stu-id="89bd9-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="89bd9-106">Pēc noklusējuma veidlapa **Darbinieki bez nodarbinātības** ir pieejama ar šādām lomām:</span><span class="sxs-lookup"><span data-stu-id="89bd9-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="89bd9-107">Personāla vadības asistents</span><span class="sxs-lookup"><span data-stu-id="89bd9-107">Human Resources Assistant</span></span>
- <span data-ttu-id="89bd9-108">Personāla vadības vadītājs</span><span class="sxs-lookup"><span data-stu-id="89bd9-108">Human Resources Manager</span></span>
- <span data-ttu-id="89bd9-109">Personāla atlases darbinieks</span><span class="sxs-lookup"><span data-stu-id="89bd9-109">Recruiter</span></span>
- <span data-ttu-id="89bd9-110">Atlīdzību un atvieglojumu vadītājs</span><span class="sxs-lookup"><span data-stu-id="89bd9-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="89bd9-111">Algu administrators</span><span class="sxs-lookup"><span data-stu-id="89bd9-111">Payroll Administrator</span></span>
- <span data-ttu-id="89bd9-112">Algu vadītājs</span><span class="sxs-lookup"><span data-stu-id="89bd9-112">Payroll Manager</span></span>
- <span data-ttu-id="89bd9-113">Apmācības vadītājs</span><span class="sxs-lookup"><span data-stu-id="89bd9-113">Training Manager</span></span>

<span data-ttu-id="89bd9-114">Sarakstā **Darbinieki bez nodarbinātības** varat dzēst uzskaitītās personas.</span><span class="sxs-lookup"><span data-stu-id="89bd9-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="89bd9-115">Pēc noklusējuma šī privilēģija tiek piešķirta Human Resources asistenta lomai.</span><span class="sxs-lookup"><span data-stu-id="89bd9-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="89bd9-116">Varat piešķirt šo privilēģiju citām lomām, izmantojot šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="89bd9-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="89bd9-117">Atlasiet **Sistēmas administrēšana** un pēc tam atlasiet **Drošības konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="89bd9-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="89bd9-118">Cilnē **Privilēģijas** filtrējiet sarakstu **Privilēģijas** **Uzturēt darbiniekus**.</span><span class="sxs-lookup"><span data-stu-id="89bd9-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="89bd9-119">[![Filtrēt privilēģiju sarakstu](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="89bd9-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="89bd9-120">Kolonnā **Atsauces** atlasiet **Displeja izvēlnes elementi**.</span><span class="sxs-lookup"><span data-stu-id="89bd9-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="89bd9-121">Kolonnā **Displeja izvēlnes vienumi** atlasiet **HcmWorkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="89bd9-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="89bd9-122">[![Atlasīt formu](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="89bd9-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="89bd9-123">Iestatiet **Dzēšanas** atļauju uz **Piešķirt**.</span><span class="sxs-lookup"><span data-stu-id="89bd9-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="89bd9-124">Atlasiet cilni **Nepublicētie objekti**.</span><span class="sxs-lookup"><span data-stu-id="89bd9-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="89bd9-125">Atlasiet **Publicēt visus**.</span><span class="sxs-lookup"><span data-stu-id="89bd9-125">Select **Publish all**.</span></span>

   <span data-ttu-id="89bd9-126">[![Publicēt izmaiņas](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="89bd9-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]