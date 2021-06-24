---
title: Datu integrētāja projekta izveide (priekšskatījums)
description: Šajā tēmā paskaidrots, kā izveidot datu integrētāja projektu.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 59f85c64ea7b1f539a245e08b76bd6a34797b0ca
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186472"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="4e9fc-103">Datu integrētāja projekta izveide (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="4e9fc-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="4e9fc-104">Šajā tēmā paskaidrots, kā izveidot datu integrētāja projektu.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="4e9fc-105">Pierakstieties programmā Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="4e9fc-106">Dodieties uz **Darbvietas \> Datu pārvaldība** un atlasiet **Datu entītijas**.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="4e9fc-107">Pirms pārejat pie nākamās darbības, uzgaidiet, līdz visas datu entītijas ir atsvaidzinātas.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="4e9fc-108">Atveriet [Power Apps portālu](https://make.powerapps.com/) un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="4e9fc-109">Atlasiet atbilstošo vidi.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="4e9fc-110">Kreisās puses navigācijas rūtī atlasiet **Dati \> Savienojumi**.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="4e9fc-111">Izveidojiet savienojumu ar tālāk norādīto vienumu atbilstošajām instancēm.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="4e9fc-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4e9fc-112">Dynamics 365</span></span>
        - <span data-ttu-id="4e9fc-113">Dynamics 365 finansēm un operācijām</span><span class="sxs-lookup"><span data-stu-id="4e9fc-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="4e9fc-114">Atveriet [Power Apps vides](https://admin.powerapps.com/environments) un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="4e9fc-115">Atlasiet **Datu integrētājs**.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="4e9fc-116">Atlasiet **Savienojumu kopas**.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="4e9fc-117">Atlasiet **Jauna savienojumu kopa**.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="4e9fc-118">Ievadiet savienojuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="4e9fc-119">Atlasiet atbilstošos savienojumus tālāk norādītajiem vienumiem.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="4e9fc-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="4e9fc-120">Dynamics 365</span></span>
        - <span data-ttu-id="4e9fc-121">Dynamics 365 finansēm un operācijām</span><span class="sxs-lookup"><span data-stu-id="4e9fc-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="4e9fc-122">Atlasiet atbilstošo organizācijas kartējumu.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="4e9fc-123">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-123">Select **Create**.</span></span>

5. <span data-ttu-id="4e9fc-124">Atveriet [Power Apps vides](https://admin.powerapps.com/environments) un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="4e9fc-125">Izveidojiet datu integrācijas projektus tālāk norādītajām veidnēm, izmantojot savienojuma kopu, ko tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="4e9fc-126">Debitora maksājumu ieskatu rezultāti (CDS uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="4e9fc-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
            - <span data-ttu-id="4e9fc-127">Ja izmantojat versiju 10.0.17 vai jaunāku versiju, ir jāizmanto veidne ar nosaukumu Debitoru maksājumu ieskatu rezultāts (CDS uz Fin un Ops 10.0.17+).</span><span class="sxs-lookup"><span data-stu-id="4e9fc-127">If you are using version 10.0.17 or later, you need to use the template named, Customer payment insights result (CDS to Fin and Ops 10.0.17+).</span></span>
        - <span data-ttu-id="4e9fc-128">Skaidras naudas plūsmas laika sērijas rezultāti (CDS uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="4e9fc-128">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="4e9fc-129">Budžeta laika sērijas rezultāti (CDS uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="4e9fc-129">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="4e9fc-130">Katram projektam iestatiet atbilstošo grafiku.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-130">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="4e9fc-131">Ja CDS neredzat obligātās entītijas, lūdzu, dodieties uz **Kredīti un iekasēšana > Iestatījumi > Finanšu ieskati > Finanšu ieskatu parametri**, iespējojiet debitoru maksājumu prognožu līdzekli un noklikšķiniet uz pogas **Izveidot prognozēšanas modeli**.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-131">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="4e9fc-132">Kad mākslīgā intelekta modeļa izvietošana ir pabeigta (veiksmīgi vai neveiksmīgi), CDS entītijas, kas nepieciešamas integrācijas izveidei, tiks izvietotas CDS.</span><span class="sxs-lookup"><span data-stu-id="4e9fc-132">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
