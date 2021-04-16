---
title: Līdzekļu pakalpojumu līmeņi
description: Šajā tēmā ir paskaidroti līdzekļu pakalpojumu līmeņi Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4163d059fda4ae0120d5c989e744c5a5fe0f5892
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808298"
---
# <a name="asset-service-levels"></a><span data-ttu-id="e0788-103">Līdzekļu pakalpojumu līmeņi</span><span class="sxs-lookup"><span data-stu-id="e0788-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e0788-104">Šajā tēmā ir paskaidroti līdzekļu pakalpojumu līmeņi Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="e0788-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="e0788-105">Līdzekļu pakalpojumu līmeņi ir saistīti ar līdzekļiem, un tiek pārsūtīti uz uzturēšanas pieprasījumiem un darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="e0788-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="e0788-106">Tos izmanto, lai darba pasūtījumu plānošanas laikā aprēķinātu darba uzdevumu prioritāti.</span><span class="sxs-lookup"><span data-stu-id="e0788-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="e0788-107">Līdzekļu pakalpojumu līmeni var mainīt, ja ir nepieciešamas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="e0788-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="e0788-108">Plašāku informāciju par iestatījumiem, kas ir saistīti ar vērtējuma rezultātu aprēķināšanu darba pasūtījumu plānošanai, skatiet nodaļā [Līdzekļu pārvaldības parametri](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e0788-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="e0788-109">Līdzekļu pakalpojumu līmenim jāiestata vismaz viens noklusējuma ieraksts.</span><span class="sxs-lookup"><span data-stu-id="e0788-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="e0788-110">Šo noklusējuma ierakstu izmanto, ja darba pasūtījuma plānošanas laikā netiek atrasta neviena cita atbilstība.</span><span class="sxs-lookup"><span data-stu-id="e0788-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="e0788-111">**1. piemērs:** noklusējuma pakalpojumu līmenis, kas tiek izmantots, ja netiek atrasta neviena cita atbilstība.</span><span class="sxs-lookup"><span data-stu-id="e0788-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="e0788-112">Šajā ierakstā atlasiet tikai pakalpojumu līmeni.</span><span class="sxs-lookup"><span data-stu-id="e0788-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="e0788-113">**2. piemērs** : augsts pakalpojumu līmenis, ko izmanto, lai plānotu darbus Volvo kravas automašīnas dzinējam.</span><span class="sxs-lookup"><span data-stu-id="e0788-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="e0788-114">Šajā ierakstā atlasiet atbilstošo līdzekļa veidu **(piemēram, kravas automašīnas dzinēju**), ražotāju (**Volvo**) un pakalpojumu līmeni.</span><span class="sxs-lookup"><span data-stu-id="e0788-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="e0788-115">Līdzekļu pakalpojumu līmeņu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e0788-115">Set up asset service levels</span></span>

1. <span data-ttu-id="e0788-116">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļa pakalpojumu līmeņi**.</span><span class="sxs-lookup"><span data-stu-id="e0788-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="e0788-117">Atlasiet **Jauns**, lai izveidotu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e0788-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="e0788-118">Atkarībā no detalizācijas līmeņa, kas nepieciešams līdzekļu pakalpojumu līmenim, veiciet atbilstošo atlasi laukos **Funkcionālais novietojums**, **Līdzekļa veids**, **Ražotājs**, **Modelis**, **Līdzeklis**, **Darba pasūtījuma veids** un **Pakalpojumu līmenis**.</span><span class="sxs-lookup"><span data-stu-id="e0788-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e0788-119">Ja līdzekļa pakalpojumu līmenis tiek izmantots uzturēšanas pieprasījumiem un darba pasūtījumiem, Līdzekļu pārvaldība iziet cauri visiem līdzekļu pakalpojumu līmeņu ierakstiem, lai pārbaudītu iespējamo atbilstību.</span><span class="sxs-lookup"><span data-stu-id="e0788-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="e0788-120">Tā vienmēr vispirms pārbauda visraksturīgāko kombināciju.</span><span class="sxs-lookup"><span data-stu-id="e0788-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="e0788-121">Citiem vārdiem sakot, Līdzekļu pārvaldība vispirms pārbauda atbilstību laukam **Darba pasūtījuma veids**.</span><span class="sxs-lookup"><span data-stu-id="e0788-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="e0788-122">Ja atbilstība netiek atrasta, tā meklē atbilstību laukam **Līdzeklis** un tā tālāk.</span><span class="sxs-lookup"><span data-stu-id="e0788-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="e0788-123">Kā jūs varat redzēt lapas **Līdzekļa pakalpojumu līmeņi** zkārtojumā, šī uzvedība nozīmē, ka, lai atrastu visspecifiskāko kombināciju, Līdzekļu pārvaldība atbilstības meklēšanai pārbauda katru ierakstu no labās puses uz kreiso.</span><span class="sxs-lookup"><span data-stu-id="e0788-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="e0788-124">Ja atbilstība netiek atrasta, šajos laukos tiek izmantots "noklusējuma" ieraksts, kam nav atlases iespēju.</span><span class="sxs-lookup"><span data-stu-id="e0788-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="e0788-125">Laukā **Pakalpojumu līmenis** atlasiet skaitli, kas norāda pakalpojumu līmeni (prioritāti).</span><span class="sxs-lookup"><span data-stu-id="e0788-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="e0788-126">Ja maināt līdzekļu pakalpojumu līmeņa ierakstu lapā **Līdzekļu pakalpojumu līmeņi** pēc tam, kad esat to jau izmantojis darba pasūtījumā, pakalpojumu līmenis uzturēšanas pieprasījumiem un darba pasūtījumiem netiek atbilstoši atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="e0788-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]