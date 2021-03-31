---
title: Datu integrētāja projekta izveide (priekšskatījums)
description: Šajā tēmā paskaidrots, kā izveidot datu integrētāja projektu.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 050c4f0fe1aea07c3866e2e9d7a6db6c758205ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208513"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="208c8-103">Datu integrētāja projekta izveide (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="208c8-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="208c8-104">Šajā tēmā paskaidrots, kā izveidot datu integrētāja projektu.</span><span class="sxs-lookup"><span data-stu-id="208c8-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="208c8-105">Pierakstieties programmā Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="208c8-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="208c8-106">Dodieties uz **Darbvietas \> Datu pārvaldība** un atlasiet **Datu entītijas**.</span><span class="sxs-lookup"><span data-stu-id="208c8-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="208c8-107">Pirms pārejat pie nākamās darbības, uzgaidiet, līdz visas datu entītijas ir atsvaidzinātas.</span><span class="sxs-lookup"><span data-stu-id="208c8-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="208c8-108">Atveriet [Power Apps portālu](https://make.powerapps.com/) un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="208c8-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="208c8-109">Atlasiet atbilstošo vidi.</span><span class="sxs-lookup"><span data-stu-id="208c8-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="208c8-110">Kreisās puses navigācijas rūtī atlasiet **Dati \> Savienojumi**.</span><span class="sxs-lookup"><span data-stu-id="208c8-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="208c8-111">Izveidojiet savienojumu ar tālāk norādīto vienumu atbilstošajām instancēm.</span><span class="sxs-lookup"><span data-stu-id="208c8-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="208c8-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="208c8-112">Dynamics 365</span></span>
        - <span data-ttu-id="208c8-113">Dynamics 365 finansēm un operācijām</span><span class="sxs-lookup"><span data-stu-id="208c8-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="208c8-114">Atveriet [Power Apps vides](https://admin.powerapps.com/environments) un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="208c8-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="208c8-115">Atlasiet **Datu integrētājs**.</span><span class="sxs-lookup"><span data-stu-id="208c8-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="208c8-116">Atlasiet **Savienojumu kopas**.</span><span class="sxs-lookup"><span data-stu-id="208c8-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="208c8-117">Atlasiet **Jauna savienojumu kopa**.</span><span class="sxs-lookup"><span data-stu-id="208c8-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="208c8-118">Ievadiet savienojuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="208c8-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="208c8-119">Atlasiet atbilstošos savienojumus tālāk norādītajiem vienumiem.</span><span class="sxs-lookup"><span data-stu-id="208c8-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="208c8-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="208c8-120">Dynamics 365</span></span>
        - <span data-ttu-id="208c8-121">Dynamics 365 finansēm un operācijām</span><span class="sxs-lookup"><span data-stu-id="208c8-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="208c8-122">Atlasiet atbilstošo organizācijas kartējumu.</span><span class="sxs-lookup"><span data-stu-id="208c8-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="208c8-123">Atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="208c8-123">Select **Create**.</span></span>

5. <span data-ttu-id="208c8-124">Atveriet [Power Apps vides](https://admin.powerapps.com/environments) un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="208c8-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="208c8-125">Izveidojiet datu integrācijas projektus tālāk norādītajām veidnēm, izmantojot savienojuma kopu, ko tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="208c8-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="208c8-126">Debitora maksājumu ieskatu rezultāti (CDS uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="208c8-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="208c8-127">Skaidras naudas plūsmas laika sērijas rezultāti (CDS uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="208c8-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="208c8-128">Budžeta laika sērijas rezultāti (CDS uz Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="208c8-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="208c8-129">Katram projektam iestatiet atbilstošo grafiku.</span><span class="sxs-lookup"><span data-stu-id="208c8-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="208c8-130">Ja CDS neredzat obligātās entītijas, lūdzu, dodieties uz **Kredīti un iekasēšana > Iestatījumi > Finanšu ieskati > Finanšu ieskatu parametri**, iespējojiet debitoru maksājumu prognožu līdzekli un noklikšķiniet uz pogas **Izveidot prognozēšanas modeli**.</span><span class="sxs-lookup"><span data-stu-id="208c8-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="208c8-131">Kad mākslīgā intelekta modeļa izvietošana ir pabeigta (veiksmīgi vai neveiksmīgi), CDS entītijas, kas nepieciešamas integrācijas izveidei, tiks izvietotas CDS.</span><span class="sxs-lookup"><span data-stu-id="208c8-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="208c8-132">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="208c8-132">Privacy notice</span></span>

<span data-ttu-id="208c8-133">Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.</span><span class="sxs-lookup"><span data-stu-id="208c8-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]