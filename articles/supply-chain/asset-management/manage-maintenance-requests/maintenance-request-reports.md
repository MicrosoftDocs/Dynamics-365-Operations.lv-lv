---
title: Pārskati par uzturēšanas pieprasījumu
description: Šajā tēmā paskaidrots, kā izveidot pārskatus par uzturēšanas pieprasījumu Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5abb62e7f92f62d4635309625d765e1c081052eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432836"
---
# <a name="maintenance-request-reports"></a><span data-ttu-id="7e31f-103">Pārskati par uzturēšanas pieprasījumu</span><span class="sxs-lookup"><span data-stu-id="7e31f-103">Maintenance request reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="7e31f-104">Līdzekļu pārvaldībā varat ģenerēt divus pārskatus, kas saistīti ar uzturēšanas pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="7e31f-104">In Asset Management, you can generate two reports that are related to maintenance requests.</span></span> <span data-ttu-id="7e31f-105">Vienā pārskatā tiek rādīta detalizēta informācija, bet otrā pārskatā ir sniegts saraksts, ko var izmantot plānošanai un turpmākajiem pasākumiem.</span><span class="sxs-lookup"><span data-stu-id="7e31f-105">One report shows details, and the other report provides a list that can be used for planning and follow-up.</span></span>

## <a name="create-a-maintenance-request-details-report"></a><span data-ttu-id="7e31f-106">Detalizētas informācijas pārskata par uzturēšanas pieprasījumu izveide</span><span class="sxs-lookup"><span data-stu-id="7e31f-106">Create a Maintenance request details report</span></span>

<span data-ttu-id="7e31f-107">Pārskatā **Detalizēta informācija par uzturēšanas pieprasījumu** ir parādīta dažāda informāciju, kas saistīta ar uzturēšanas pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="7e31f-107">The **Maintenance request details** report shows various information that is related to maintenance requests.</span></span>

1. <span data-ttu-id="7e31f-108">Atlasiet **Līdzekļu pārvaldība** \> **Pārskati** \> **Uzturēšanas pieprasījumi** \> **Detalizēta informācija par uzturēšanas pieprasījumiem**.</span><span class="sxs-lookup"><span data-stu-id="7e31f-108">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request details**.</span></span>
2. <span data-ttu-id="7e31f-109">Kopsavilkuma cilnē **Iekļaujamie ieraksti** varat atlasīt konkrētus uzturēšanas pieprasījumus, lai tos iekļautu pārskatā.</span><span class="sxs-lookup"><span data-stu-id="7e31f-109">On the **Records to include** FastTab, you can select specific maintenance requests to include on the report.</span></span>
3. <span data-ttu-id="7e31f-110">Kopsavilkuma cilnē **Palaist fonā** vajadzības gadījumā varat iestatīt pārskatu veidošanu kā pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="7e31f-110">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="7e31f-111">Atlasiet **Labi**, lai izveidotu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="7e31f-111">Select **OK** to generate the report.</span></span>

<span data-ttu-id="7e31f-112">Nākamajā attēlā ir parādīts pārskata **Detalizēta informācija par uzturēšanas pieprasījumu** piemērs.</span><span class="sxs-lookup"><span data-stu-id="7e31f-112">The following illustration shows an example of the **Maintenance request details** report.</span></span>

![Informācijas atskaite par uzturēšanas pieprasījumu](media/09-manage-maintenance-requests.png)

## <a name="create-a-maintenance-request-list-report"></a><span data-ttu-id="7e31f-114">Uzturēšanas pieprasījumu saraksta pārskata izveide</span><span class="sxs-lookup"><span data-stu-id="7e31f-114">Create a Maintenance request list report</span></span>

<span data-ttu-id="7e31f-115">Pārskatā **Uzturēšanas pieprasījumu saraksts** tiek parādīts visu viena veida uzturēšanas pieprasījumu saraksts.</span><span class="sxs-lookup"><span data-stu-id="7e31f-115">The **Maintenance request list** report shows a list of all maintenance requests of the same request type.</span></span>

1. <span data-ttu-id="7e31f-116">Atlasiet **Līdzekļu pārvaldība** \> **Pārskati** \> **Uzturēšanas pieprasījumi** \> **Uzturēšanas pieprasījumu saraksts**.</span><span class="sxs-lookup"><span data-stu-id="7e31f-116">Select **Asset management** \> **Reports** \> **Maintenance requests** \> **Maintenance request list**.</span></span>
2. <span data-ttu-id="7e31f-117">Kopsavilkuma cilnē **Iekļaujamie ieraksti** varat veikt atlases, lai definētu, kuri uzturēšanas pieprasījumi ir iekļauti pārskatā.</span><span class="sxs-lookup"><span data-stu-id="7e31f-117">On the **Records to include** FastTab, you can make selections to define which maintenance requests are included on the report.</span></span>
3. <span data-ttu-id="7e31f-118">Kopsavilkuma cilnē **Palaist fonā** vajadzības gadījumā varat iestatīt pārskatu veidošanu kā pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="7e31f-118">On the **Run in the background** FastTab, you can set up report generation as a batch job, as you require.</span></span>
4. <span data-ttu-id="7e31f-119">Atlasiet **Labi**, lai izveidotu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="7e31f-119">Select **OK** to generate the report.</span></span>

<span data-ttu-id="7e31f-120">Nākamajā attēlā ir parādīts **Uzturēšanas pieprasījumu saraksta** pārskata par visiem aktīvajiem uzturēšanas pieprasījumiem piemērs.</span><span class="sxs-lookup"><span data-stu-id="7e31f-120">The following illustration shows an example of the **Maintenance request list** report for all active maintenance requests.</span></span>

![Uzturēšanas pieprasījumu saraksta pārskats](media/10-manage-maintenance-requests.png)
