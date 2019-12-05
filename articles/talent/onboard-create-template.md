---
title: Pievienošanas veidnes izveide, izmantojot Dynamics 365 Talent - Onboard
description: Šajā tēmā ir paskaidrots, kā izmantot programmu Microsoft Dynamics 365 Talent - Onboard, lai izveidotu pievienošanas ceļveža veidni nesen nolīgtajiem darbiniekiem. Šis uzdevums ir būtisks pirmais solis cilvēkkapitāla pārvaldības (HCM) no pieņemšanas darbā līdz aiziešanai pensijā stratēģijā.
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 55853418eacd179b7bb50b7e4385300bdcb27abe
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812906"
---
# <a name="create-an-onboarding-template-by-using-dynamics-365-talent---onboard"></a><span data-ttu-id="b4318-104">Pievienošanas veidnes izveide, izmantojot Dynamics 365 Talent - Onboard</span><span class="sxs-lookup"><span data-stu-id="b4318-104">Create an onboarding template by using Dynamics 365 Talent - Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b4318-105">Microsoft Dynamics 365 Talent: Onboard nodrošina dažādas veidnes, kas var palīdzēt iespējami ātri izveidot pievienošanas ceļvedi.</span><span class="sxs-lookup"><span data-stu-id="b4318-105">Microsoft Dynamics 365 Talent: Onboard provides various templates that can help you create an onboarding guide as quickly as possible.</span></span> <span data-ttu-id="b4318-106">Varat izmantot vienu vai vairākas no šīm veidnēm, vai varat izveidot savas veidnes.</span><span class="sxs-lookup"><span data-stu-id="b4318-106">You can use one or more of these templates, or you can create your own templates.</span></span> <span data-ttu-id="b4318-107">Onboard nodrošina teksta paraugu, ko varat izmantot, veidojot savas veidnes.</span><span class="sxs-lookup"><span data-stu-id="b4318-107">Onboard provides sample text that you can use when you create your own templates.</span></span> <span data-ttu-id="b4318-108">Tāpēc process ir viegls, pat ja sākat no nulles.</span><span class="sxs-lookup"><span data-stu-id="b4318-108">Therefore, the process is easy even if you start from scratch.</span></span>

## <a name="create-an-onboarding-template-from-an-existing-template"></a><span data-ttu-id="b4318-109">Pievienošanas veidnes izveide no esošas veidnes</span><span class="sxs-lookup"><span data-stu-id="b4318-109">Create an onboarding template from an existing template</span></span>

1. <span data-ttu-id="b4318-110">Kreisās puses izvēlnē atlasiet **Veidnes**.</span><span class="sxs-lookup"><span data-stu-id="b4318-110">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="b4318-111">Sadaļā **Populāras veidnes no galerijas** vai **Manas veidnes** atlasiet veidni.</span><span class="sxs-lookup"><span data-stu-id="b4318-111">Under **Popular templates from the gallery** or **My templates**, select a template.</span></span> <span data-ttu-id="b4318-112">Lai skatītu vairāk veidņu atlasiet **Vairāk veidņu galerijā**.</span><span class="sxs-lookup"><span data-stu-id="b4318-112">To view more templates, select **More in template gallery**.</span></span>
3. <span data-ttu-id="b4318-113">Izpildiet kādu no norādītajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="b4318-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="b4318-114">Ja veidne ir no galerijas, atlasiet **Saglabāt kā manu veidni**, ievadiet jauno veidnes nosaukumu un atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b4318-114">If the template is from the gallery, select **Save as my template**, enter a new name for the template, and select **Save**.</span></span>
    - <span data-ttu-id="b4318-115">Ja veidne ir no **Manas veidnes**, atlasiet **Saglabāt kā veidni**, ievadiet jauno veidnes nosaukumu un atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b4318-115">If the template is from **My templates**, select **Save as template**, enter a new name for the template, and select **Save**.</span></span>

    <span data-ttu-id="b4318-116">[![Veidnes izveide no esošas veidnes](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span><span class="sxs-lookup"><span data-stu-id="b4318-116">[![Creating a template from an existing template](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span></span>

## <a name="create-a-new-onboarding-template"></a><span data-ttu-id="b4318-117">Jaunas pievienošanas veidnes izveide</span><span class="sxs-lookup"><span data-stu-id="b4318-117">Create a new onboarding template</span></span>

1. <span data-ttu-id="b4318-118">Kreisās puses izvēlnē atlasiet **Veidnes**.</span><span class="sxs-lookup"><span data-stu-id="b4318-118">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="b4318-119">Sadaļā **Manas veidnes**atlasiet elementu **Pievienot** (pluszīme \[**+**\]).</span><span class="sxs-lookup"><span data-stu-id="b4318-119">Under **My templates**, select the **Add** (plus sign \[**+**\]) tile.</span></span>

    <span data-ttu-id="b4318-120">[![Jaunas veidnes izveide](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span><span class="sxs-lookup"><span data-stu-id="b4318-120">[![Creating a new template](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span></span>

3. <span data-ttu-id="b4318-121">Dialoglodziņā **Izveidot ceļveža veidni** ievadiet nosaukumu šai veidnei un pēc tam atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b4318-121">In the **Create a guide template** dialog box, enter a name for the template, and then select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b4318-122">Nākamās darbības</span><span class="sxs-lookup"><span data-stu-id="b4318-122">Next steps</span></span>

- [<span data-ttu-id="b4318-123">Pievienošanas ceļvežu un veidņu rediģēšana</span><span class="sxs-lookup"><span data-stu-id="b4318-123">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="b4318-124">Satura kopīgošana ar citiem ieguldītājiem</span><span class="sxs-lookup"><span data-stu-id="b4318-124">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="b4318-125">Uzdevumu un pievienoto darbinieku statusa skatīšana</span><span class="sxs-lookup"><span data-stu-id="b4318-125">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="b4318-126">Par pieņemšanu darbā atbildīgo grupu izveide Onboard</span><span class="sxs-lookup"><span data-stu-id="b4318-126">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="b4318-127">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="b4318-127">See also</span></span>

- [<span data-ttu-id="b4318-128">Programmas Onboard izmēģināšana vai iegāde</span><span class="sxs-lookup"><span data-stu-id="b4318-128">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="b4318-129">Jaunumi un izmaiņas Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="b4318-129">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="b4318-130">Nodošanas izpildei plāni</span><span class="sxs-lookup"><span data-stu-id="b4318-130">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="b4318-131">Atbalsta saņemšana saistībā ar Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="b4318-131">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)
