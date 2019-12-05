---
title: Krājumu vecumstruktūru pārskats
description: Šajā tēmā aprakstīta funkcionalitāte, kas ļauj palaist krājuma novecošanas pārskatu un padarīt rezultātu pieejamu veidlapas un diagrammas veidā.
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810255"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="e66be-103">Krājumu vecumstruktūru pārskats</span><span class="sxs-lookup"><span data-stu-id="e66be-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="e66be-104">Programmā Microsoft Dynamics 365 Supply Chain Management var palaist **Krājumu novecošanas ziņojumu** un padarīt rezultātu pieejamu veidlapas un diagrammas veidā.</span><span class="sxs-lookup"><span data-stu-id="e66be-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="e66be-105">Veidlapā kolonnas un uzkrātās bilances tiek dinamiski pielāgotas atkarībā no konfigurētā izkārtojuma.</span><span class="sxs-lookup"><span data-stu-id="e66be-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="e66be-106">Diagramma sniedz vizuālu apskatu, kas atbalsta filtrēšanu, un ļauj detalizēti apskatīt detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="e66be-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="e66be-107">Turklāt datu elements, kura nosaukums ir **Krājumu novecošanas pārskats**, ļauj eksportēt **Krājumu novecošanas pārskata** rezultātus, kas tiek palaisti, piemēram, Microsoft Excel faila vai PDF faila formātā.</span><span class="sxs-lookup"><span data-stu-id="e66be-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="e66be-108">Šī **Krājumu novecošanas** palaišanas metode pārskatam noder gadījumos, ja izlaidē ir daudz rindu.</span><span class="sxs-lookup"><span data-stu-id="e66be-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="e66be-109">Piemēram, izlaide saturēs daudzas rindas, ja jums ir 50 000 preces un 300 veikali, kas ir izveidoti kā noliktavas, un jūs pieprasāt krājumu novecošanu pēc preces, vietas un noliktavas.</span><span class="sxs-lookup"><span data-stu-id="e66be-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="e66be-110">Krājuma novecošanas pārskats</span><span class="sxs-lookup"><span data-stu-id="e66be-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="e66be-111">Dodieties uz **Izmaksu pārvaldība \>Vaicājumi un pārskati\>Krājuma novecošanas ziņojuma glabātuve**.</span><span class="sxs-lookup"><span data-stu-id="e66be-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="e66be-112">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e66be-112">Select **New**.</span></span>
1. <span data-ttu-id="e66be-113">Laukā **Procesa identifikators - nosaukums** ievadiet unikālu pārskata apstiprināšanas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="e66be-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="e66be-114">Atlasiet pārskatu **Identifikācija – ID** un pēc vajadzības to filtrējiet.</span><span class="sxs-lookup"><span data-stu-id="e66be-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="e66be-115">Pārskata izpilde vienmēr tiek veikta pakešuzdevumā.</span><span class="sxs-lookup"><span data-stu-id="e66be-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="e66be-116">Kad pakešuzdevums ir pabeigts, izvade tiek rādīta lapā **Krājumu novecošanas pārskata glabātuve**.</span><span class="sxs-lookup"><span data-stu-id="e66be-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="e66be-117">Lai skatītu izlaidi kā formu, kurai ir tradicionāls režģa izkārtojums, atlasiet **Skatīt papildinformāciju**.</span><span class="sxs-lookup"><span data-stu-id="e66be-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="e66be-118">Lai skatītu izlaidi kā apkopotu diagrammu, atlasiet **Skatīt diagrammu.**</span><span class="sxs-lookup"><span data-stu-id="e66be-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e66be-119">Veidlapā netiek iekļautas starpsummas, kas definētas pārskata izkārtojumā.</span><span class="sxs-lookup"><span data-stu-id="e66be-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="e66be-120">Datu elements **Krājumu novecošanas pārskats** ļauj eksportēt **Krājuma novecošanas** pārskata rezultātu, lietojot filtru laukam **Procesa identifikators – nosaukums** jebkurā formātā, ko atbalsta datu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="e66be-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
