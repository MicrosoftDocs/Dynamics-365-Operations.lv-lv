---
title: Duālās rakstīšanas iestatījums no Lifecycle Services
description: Šajā tēmā skaidrots, kā iestatīt divu rakstīšanas savienojumu starp jaunu Finance and Operations vidi un jaunu Common Data Service vidi no Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f49eba1748861af6ee3353a6c58005ee84ccae23
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998112"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="97ba3-103">Duālās rakstīšanas iestatījums no Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="97ba3-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="97ba3-104">Šajā tēmā skaidrots, kā iestatīt divu rakstīšanas savienojumu starp jaunu Finance and Operations vidi un jaunu Common Data Service vidi no Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="97ba3-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Common Data Service environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="97ba3-105">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="97ba3-105">Prerequisites</span></span>

<span data-ttu-id="97ba3-106">Jums ir jābūt administratoram, lai iestatītu duālās rakstīšanas savienojumu.</span><span class="sxs-lookup"><span data-stu-id="97ba3-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="97ba3-107">Jums ir nepieciešama piekļuve nomniekam.</span><span class="sxs-lookup"><span data-stu-id="97ba3-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="97ba3-108">Jums ir jābūt administratoram gan Finance and Operations, gan Common Data Service vidēs.</span><span class="sxs-lookup"><span data-stu-id="97ba3-108">You must be an admin in both Finance and Operations environments and Common Data Service environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="97ba3-109">Izveidot duālās rakstīšanas savienojumu</span><span class="sxs-lookup"><span data-stu-id="97ba3-109">Set up a dual-write connection</span></span>

<span data-ttu-id="97ba3-110">Sekojiet šīm darbībām, lai iestatītu duālās rakstīšanas savienojumu.</span><span class="sxs-lookup"><span data-stu-id="97ba3-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="97ba3-111">Dodieties uz savu projektu portālā LCS.</span><span class="sxs-lookup"><span data-stu-id="97ba3-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="97ba3-112">Atlasiet **Konfigurēt** , lai izvietotu jaunu vidi.</span><span class="sxs-lookup"><span data-stu-id="97ba3-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="97ba3-113">Atlasiet versiju.</span><span class="sxs-lookup"><span data-stu-id="97ba3-113">Select the version.</span></span> 
4. <span data-ttu-id="97ba3-114">Atlasiet topoloģiju.</span><span class="sxs-lookup"><span data-stu-id="97ba3-114">Select the topology.</span></span> <span data-ttu-id="97ba3-115">Ja ir pieejama tikai viena topoloģija, tā tiek automātiski atlasīta.</span><span class="sxs-lookup"><span data-stu-id="97ba3-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="97ba3-116">Pabeidziet pirmās darbības **Izvietošanas iestatījumu** vednī.</span><span class="sxs-lookup"><span data-stu-id="97ba3-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="97ba3-117">**Common Data Service** cilnē sekojiet šīm darbībām:</span><span class="sxs-lookup"><span data-stu-id="97ba3-117">On the **Common Data Service** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="97ba3-118">Ja Common Data Service vide jau ir nodrošināta jūsu nomniekam, varat to atlasīt.</span><span class="sxs-lookup"><span data-stu-id="97ba3-118">If a Common Data Service environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="97ba3-119">Iestatiet **Konfigurēt Common Data Service** opciju uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="97ba3-119">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="97ba3-120">Laukā **Pieejamās vides** atlasiet vidi, ko integrēt ar jūsu Finance and Operations datiem.</span><span class="sxs-lookup"><span data-stu-id="97ba3-120">In the **Available environments** field, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="97ba3-121">Saraksts ietver visas vides, kurās ir administratora privilēģijas.</span><span class="sxs-lookup"><span data-stu-id="97ba3-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="97ba3-122">Atzīmējiet izvēles rūtiņu **Piekrītu** , lai norādītu, ka piekrītat noteikumiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="97ba3-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Common Data Service cilne, kad Common Data Service vide jau ir nodrošināta jūsu nomniekam](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="97ba3-124">Ja nomniekam vēl nav Common Data Service vide, tiks nodrošināta jauna vide.</span><span class="sxs-lookup"><span data-stu-id="97ba3-124">If your tenant doesn't already have a Common Data Service environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="97ba3-125">Iestatiet **Konfigurēt Common Data Service** opciju uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="97ba3-125">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="97ba3-126">Ievadiet Common Data Service vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="97ba3-126">Enter a name for the Common Data Service environment.</span></span>
        3. <span data-ttu-id="97ba3-127">Atlasiet reģionu, kurā izvietot vidi.</span><span class="sxs-lookup"><span data-stu-id="97ba3-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="97ba3-128">Atlasiet noklusējuma valodu un valūtu videi.</span><span class="sxs-lookup"><span data-stu-id="97ba3-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="97ba3-129">Vēlāk nevarēs mainīt valodu un valūtu.</span><span class="sxs-lookup"><span data-stu-id="97ba3-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="97ba3-130">Atzīmējiet izvēles rūtiņu **Piekrītu** , lai norādītu, ka piekrītat noteikumiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="97ba3-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Common Data Service cilne, kad jūsu nomniekam vēl nav Common Data Service vides](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="97ba3-132">Pabeidziet atlikušās darbības **Izvietošanas iestatījumu** vednī.</span><span class="sxs-lookup"><span data-stu-id="97ba3-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="97ba3-133">Pēc tam, kad vides statuss ir **Izvietots** , atveriet vides informācijas lapu.</span><span class="sxs-lookup"><span data-stu-id="97ba3-133">After the environment has a status of **Deployed** , open the environment details page.</span></span> <span data-ttu-id="97ba3-134">**Common Data Service vides informācijas** sadaļā ir redzami saistīto Finance and Operations vides un Common Data Service vides nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="97ba3-134">The **Common Data Service environment information** section shows the names of the Finance and Operations environment and the Common Data Service environment that are linked.</span></span>

    ![Common Data Service vides informācijas sadaļa](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="97ba3-136">Finance and Operations vides administratoram ir jāpiesakās portālā LCS un jāatlasa **Saite uz kompaktdiskiem lietojumprogrammām** , lai izveidotu saites.</span><span class="sxs-lookup"><span data-stu-id="97ba3-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="97ba3-137">Vides informācijas lapa rāda administratora kontaktinformāciju.</span><span class="sxs-lookup"><span data-stu-id="97ba3-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="97ba3-138">Pēc tam, kad saite ir pabeigta, statuss tiek atjaunināts uz **Vides saistīšana ir veiksmīgi pabeigta**.</span><span class="sxs-lookup"><span data-stu-id="97ba3-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="97ba3-139">Lai atvērtu **Datu integrācijas** darbvietu Finance and Operations vidē un kontrolētu pieejamās veidnes, izvēlieties **Saistīt ar kompaktdiskiem lietojumprogrammās**.</span><span class="sxs-lookup"><span data-stu-id="97ba3-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![¨Saite uz kompaktdiskiem lietojumprogrammām¨ poga Common Data Service vides informācijas sadaļā](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="97ba3-141">Jūs nevarat atsaistīt vides, izmantojot portālu LCS.</span><span class="sxs-lookup"><span data-stu-id="97ba3-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="97ba3-142">Lai noņemtu saiti videi, atveriet **Datu integrācijas** darbvietu Finance and Operations vidē un pēc tam atlasiet **Noņemt saiti**.</span><span class="sxs-lookup"><span data-stu-id="97ba3-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>
