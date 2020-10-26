---
title: Eksperimenta statusa pārskatīšana
description: Šajā tēmā ir paskaidrots, kāds ir eksperimenta statuss eksperimenta dzīves ciklā pakalpojumā Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 097206c0aa487e14499bdf3907465e17b7d337e2
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930241"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="15368-103">Eksperimenta statusa pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="15368-103">Review the status of an experiment</span></span>
<span data-ttu-id="15368-104">Eksperimenta iestatīšana un izpildīšana pakalpojumā Dynamics 365 Commerce ir saistīta ar daudzām darbībām.</span><span class="sxs-lookup"><span data-stu-id="15368-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="15368-105">Informāciju par eksperimenta dzīves ciklu skatiet sadaļā [Eksperimentēšana pakalpojumā Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="15368-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="15368-106">Lai uzzinātu, kur dzīves ciklā šobrīd atrodas eksperiments, dodieties uz cilni **Eksperimenti** vietnes veidotājā.</span><span class="sxs-lookup"><span data-stu-id="15368-106">To learn where an experiment is in the lifecycle, go to the **Experiments** tab in site builder.</span></span> <span data-ttu-id="15368-107">Tiks parādīts eksperimentu saraksts ar katra eksperimenta statusu gan pakalpojumā Commerce, gan trešās puses pakalpojumā, kas tiek izmantots, lai iespējotu eksperimentu veidošanu, variantu piešķiršanu un datu analizēšanu.</span><span class="sxs-lookup"><span data-stu-id="15368-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="15368-108">Kolonnā **Commerce statuss** var tikt parādītas tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="15368-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="15368-109">**Melnraksts** – eksperiments ir pievienots lapai vai fragmentam pakalpojumā Commerce un tiek rediģēts.</span><span class="sxs-lookup"><span data-stu-id="15368-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="15368-110">**Publicēts** – eksperimenta varianti ir gatavi parādīšanai tīmekļa vietnē.</span><span class="sxs-lookup"><span data-stu-id="15368-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="15368-111">Ja eksperiments tiek izpildīts trešās puses pakalpojumā, tīmekļa vietnes lietotāji redzēs lapas vai fragmenta variantu, kuru atlasījis trešās puses pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="15368-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="15368-112">**Nepublicēts** – eksperiments vairs nav pieejams vietnē.</span><span class="sxs-lookup"><span data-stu-id="15368-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="15368-113">Pat ja eksperiments tiek izpildīts trešās puses pakalpojumā, tīmekļa vietnes lietotāji redzēs tikai lapas vai fragmenta noklusējuma versiju.</span><span class="sxs-lookup"><span data-stu-id="15368-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="15368-114">**Pabeigts** – eksperiments ir izpildīts un variants tika publicēts visu tīmekļa vietnes lietotāju pieejamībai.</span><span class="sxs-lookup"><span data-stu-id="15368-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="15368-115">Līdzīgi **trešās puses statusa** kolonnā var tikt parādītas tālāk esošās vērtības, lai norādītu, kāds ir eksperimentu statuss trešās puses pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="15368-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="15368-116">**Melnraksts** – eksperiments ir iestatīts trešās puses pakalpojumā, bet nav sākts.</span><span class="sxs-lookup"><span data-stu-id="15368-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="15368-117">**Izpilde** – eksperiments tika sākts trešās puses pakalpojumā un veic datu apkopošanu.</span><span class="sxs-lookup"><span data-stu-id="15368-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="15368-118">**Apturēts** – eksperiments ir apturēts un nenotiek datu apkopošana.</span><span class="sxs-lookup"><span data-stu-id="15368-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="15368-119">Jums ir jāatsāk eksperiments, lai tas atkal apkopotu datus.</span><span class="sxs-lookup"><span data-stu-id="15368-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="15368-120">**Arhivēts** – eksperiments ir izpildīts un tas ir kataloģizēts trešās puses pakalpojumā turpmākai atsaucei.</span><span class="sxs-lookup"><span data-stu-id="15368-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="15368-121">Diagrammā ir parādītas abas statusu kopas un kā tās ir savstarpēji saistītas.</span><span class="sxs-lookup"><span data-stu-id="15368-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="15368-122">[ ![Eksperimentu statusi](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="15368-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>