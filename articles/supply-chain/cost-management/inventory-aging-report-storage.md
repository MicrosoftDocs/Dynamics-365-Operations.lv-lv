---
title: Krājumu vecumstruktūru pārskata glabāšana
description: Šajā tēmā aprakstīta funkcionalitāte, kas ļauj palaist krājuma novecošanas pārskatu un padarīt rezultātu pieejamu veidlapas un diagrammas veidā.
author: AndersGirke
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 17ca0a105521f3216dfefcc170d60c1eb7137bf6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809762"
---
# <a name="inventory-aging-report-storage"></a><span data-ttu-id="dcc81-103">Krājumu vecumstruktūru pārskata glabāšana</span><span class="sxs-lookup"><span data-stu-id="dcc81-103">Inventory aging report storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dcc81-104">Programmā Microsoft Dynamics 365 Supply Chain Management var palaist **Krājumu vecumstruktūru pārskata glabāšanas** rezultātus un padarīt tos pieejamus veidlapas un diagrammas veidā.</span><span class="sxs-lookup"><span data-stu-id="dcc81-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging report storage** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="dcc81-105">Veidlapā kolonnas un uzkrātās bilances tiek dinamiski pielāgotas atkarībā no konfigurētā izkārtojuma.</span><span class="sxs-lookup"><span data-stu-id="dcc81-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="dcc81-106">Diagramma sniedz vizuālu apskatu, kas atbalsta filtrēšanu, un ļauj detalizēti apskatīt detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="dcc81-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="dcc81-107">Turklāt datu elements, kura nosaukums ir **Krājumu vecumstruktūru pārskats**, ļauj eksportēt **Krājumu vecumstruktūru pārskata glabāšana** rezultātus, kas tiek palaisti, piemēram, Microsoft Excel faila vai PDF faila formātā.</span><span class="sxs-lookup"><span data-stu-id="dcc81-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging report storage** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="dcc81-108">Šī **Krājumu vecumstruktūru pārskata glabāšanas** rezultātu palaišanas metode pārskatam noder gadījumos, ja izlaidē ir daudz rindu.</span><span class="sxs-lookup"><span data-stu-id="dcc81-108">This method of running an **Inventory aging report storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="dcc81-109">Piemēram, izlaide saturēs daudzas rindas, ja jums ir 50 000 preces un 300 veikali, kas ir izveidoti kā noliktavas, un jūs pieprasāt krājumu novecošanu pēc preces, vietas un noliktavas.</span><span class="sxs-lookup"><span data-stu-id="dcc81-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="enable-the-inventory-value-storage-report-feature"></a><span data-ttu-id="dcc81-110">Iespējot Krājumu vērtības uzglabāšanas pārskata līdzekli</span><span class="sxs-lookup"><span data-stu-id="dcc81-110">Enable the Inventory value storage report feature</span></span>

<span data-ttu-id="dcc81-111">Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo sistēmā.</span><span class="sxs-lookup"><span data-stu-id="dcc81-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="dcc81-112">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un iespējotu to pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="dcc81-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="dcc81-113">Šeit līdzeklis tiek norādīts kā:</span><span class="sxs-lookup"><span data-stu-id="dcc81-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="dcc81-114">**Modulis** - Izmaksu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="dcc81-114">**Module** - Cost management</span></span>
- <span data-ttu-id="dcc81-115">**Līdzekļa nosaukums** - krājumu vecumstruktūru pārskata uzglabāšana</span><span class="sxs-lookup"><span data-stu-id="dcc81-115">**Feature name** - Inventory aging report storage</span></span>

## <a name="run-an-inventory-aging-report-storage"></a><span data-ttu-id="dcc81-116">Palaist Krājumu vecumstruktūru pārskata glabāšanu</span><span class="sxs-lookup"><span data-stu-id="dcc81-116">Run an Inventory aging report storage</span></span>

1. <span data-ttu-id="dcc81-117">Dodieties uz **Izmaksu pārvaldība \> Vaicājumi un pārskati \> Krājuma novecošanas ziņojuma glabātuve**.</span><span class="sxs-lookup"><span data-stu-id="dcc81-117">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="dcc81-118">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="dcc81-118">Select **New**.</span></span>
1. <span data-ttu-id="dcc81-119">Laukā **Procesa identifikators - nosaukums** ievadiet unikālu pārskata apstiprināšanas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="dcc81-119">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="dcc81-120">Atlasiet pārskatu **Identifikācija – ID** un pēc vajadzības to filtrējiet.</span><span class="sxs-lookup"><span data-stu-id="dcc81-120">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="dcc81-121">Pārskata izpilde vienmēr tiek veikta pakešuzdevumā.</span><span class="sxs-lookup"><span data-stu-id="dcc81-121">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="dcc81-122">Kad pakešuzdevums ir pabeigts, izvade tiek rādīta lapā **Krājumu novecošanas pārskata glabātuve**.</span><span class="sxs-lookup"><span data-stu-id="dcc81-122">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="dcc81-123">Lai skatītu izlaidi kā formu, kurai ir tradicionāls režģa izkārtojums, atlasiet **Skatīt papildinformāciju**.</span><span class="sxs-lookup"><span data-stu-id="dcc81-123">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="dcc81-124">Lai skatītu izlaidi kā apkopotu diagrammu, atlasiet **Skatīt diagrammu.**</span><span class="sxs-lookup"><span data-stu-id="dcc81-124">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dcc81-125">Veidlapā netiek iekļautas starpsummas, kas definētas pārskata izkārtojumā.</span><span class="sxs-lookup"><span data-stu-id="dcc81-125">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="dcc81-126">Datu elements **Krājumu novecošanas pārskats** ļauj eksportēt **Krājumu vecumstruktūru pārskata glabāšana** pārskatu, lietojot filtru laukam **Procesa identifikators – nosaukums** jebkurā formātā, ko atbalsta datu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="dcc81-126">The **Inventory aging report** data entity lets you export the output of an **Inventory aging report storage** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]