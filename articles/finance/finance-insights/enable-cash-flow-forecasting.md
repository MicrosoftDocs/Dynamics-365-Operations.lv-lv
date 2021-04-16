---
title: Skaidras naudas plūsmas prognozēšanas iespējošana (priekšskatījums)
description: Šajā tēmā skaidrots, kā ieslēgt skaidras naudas plūsmas prognozēšanas līdzekli Finanšu ieskatos.
author: ShivamPandey-msft
ms.date: 07/24/2020
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
ms.openlocfilehash: f7c06eaeb79c1a2aa319cfa3d2ad8255bf716cd0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818732"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="edf35-103">Skaidras naudas plūsmas prognozēšanas iespējošana (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="edf35-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="edf35-104">Šajā tēmā skaidrots, kā ieslēgt skaidras naudas plūsmas prognozēšanas līdzekli Finanšu ieskatos.</span><span class="sxs-lookup"><span data-stu-id="edf35-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="edf35-105">Lai izmantotu maksājumu prognozes skaidras naudas plūsmā, jāiestata debitora maksājumu prognožu līdzeklis, kā tas aprakstīts [Debitora maksājumu prognožu iespējošana](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="edf35-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="edf35-106">Izmantojiet informāciju no vides lapas Microsoft Dynamics Lifecycle Services (LCS), lai izveidotu savienojumu ar Azure SQL primāro instanci šai videi.</span><span class="sxs-lookup"><span data-stu-id="edf35-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="edf35-107">Palaidiet tālāk norādīto Transact-SQL (T-SQL) komandu, lai ieslēgtu ierobežotos līdzekļus smilškastes videi.</span><span class="sxs-lookup"><span data-stu-id="edf35-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="edf35-108">(Iespējams, būs LCS jāieslēdz piekļuve savai IP adresei pirms varēsiet izveidot attilināto savienojumu ar programmas objektu serveri \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="edf35-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="edf35-109">Ja jūsu Microsoft Dynamics 365 Finance izvietošana ir Service Fabric izvietošana, varat izlaist šo darbību.</span><span class="sxs-lookup"><span data-stu-id="edf35-109">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="edf35-110">Finanšu ieskatu grupai jau vajadzētu ieslēgt jums šo ierobežoto līdzekli.</span><span class="sxs-lookup"><span data-stu-id="edf35-110">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="edf35-111">Ja neredzat līdzekļus darbvietā **Līdzekļu pārvaldība** vai ja rodas problēmas, mēģinot tos ieslēgt, sazinieties ar <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="edf35-111">If you don't see the features in the **Feature management** workspace, or if experience issues when you try to turn them on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="edf35-112">Atveriet darbvietu **Līdzekļu pārvaldība** un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="edf35-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="edf35-113">Atlasiet **Pārbaudīt atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="edf35-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="edf35-114">Ieslēdziet tālāk norādītos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="edf35-114">Turn on the following features:</span></span>

        - <span data-ttu-id="edf35-115">Jauna režģa vadīkla</span><span class="sxs-lookup"><span data-stu-id="edf35-115">New grid control</span></span>
        - <span data-ttu-id="edf35-116">Grupēšana režģos (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="edf35-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="edf35-117">Debitoru maksājumu prognozes (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="edf35-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="edf35-118">Skaidras naudas plūsmas prognozēšana (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="edf35-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="edf35-119">Dodieties uz **Skaidras naudas un bankas pārvaldība \> Skaidras naudas plūsmas prognozes iestatīšana** un pievienojiet likviditātes kontus, kas jāiekļauj prognozēs.</span><span class="sxs-lookup"><span data-stu-id="edf35-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="edf35-120">Ja likviditātes konti nav iestatīti, skaidras naudas plūsmu nevar ģenerēt.</span><span class="sxs-lookup"><span data-stu-id="edf35-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="edf35-121">Dodieties uz **Skaidras naudas un bankas pārvaldība \> Iestatīšana \> Finanšu ieskati (priekšskatījums) \> Skaidras naudas plūsmas prognozes (priekšskatījums)** un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="edf35-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="edf35-122">Cilnē **Skaidras naudas plūsmas prognoze** atlasiet **Iespējot līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="edf35-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="edf35-123">Atlasiet **Izveidot prognozēšanas modeli**.</span><span class="sxs-lookup"><span data-stu-id="edf35-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="edf35-124">Plašāku informāciju par to, kā iestatīt skaidras naudas plūsmas prognozēšanas iespēju, skatiet [Skaidras naudas plūsmas prognozēšana](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="edf35-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="edf35-125">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="edf35-125">Privacy notice</span></span>

<span data-ttu-id="edf35-126">Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.</span><span class="sxs-lookup"><span data-stu-id="edf35-126">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]