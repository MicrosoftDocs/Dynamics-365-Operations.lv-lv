---
title: Skaidras naudas plūsmas prognozēšanas iespējošana (priekšskatījums)
description: Šajā tēmā skaidrots, kā ieslēgt skaidras naudas plūsmas prognozēšanas līdzekli Finanšu ieskatos.
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
ms.openlocfilehash: ba8acb2191291e2abed5cabf234c19fe09e6c8ff
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222562"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="d8e92-103">Skaidras naudas plūsmas prognozēšanas iespējošana (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="d8e92-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d8e92-104">Šajā tēmā skaidrots, kā ieslēgt skaidras naudas plūsmas prognozēšanas līdzekli Finanšu ieskatos.</span><span class="sxs-lookup"><span data-stu-id="d8e92-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="d8e92-105">Lai izmantotu maksājumu prognozes skaidras naudas plūsmā, jāiestata debitora maksājumu prognožu līdzeklis, kā tas aprakstīts [Debitora maksājumu prognožu iespējošana](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="d8e92-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="d8e92-106">Izmantojiet informāciju no vides lapas Microsoft Dynamics Lifecycle Services (LCS), lai izveidotu savienojumu ar Azure SQL primāro instanci šai videi.</span><span class="sxs-lookup"><span data-stu-id="d8e92-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="d8e92-107">Palaidiet tālāk norādīto Transact-SQL (T-SQL) komandu, lai ieslēgtu ierobežotos līdzekļus smilškastes videi.</span><span class="sxs-lookup"><span data-stu-id="d8e92-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="d8e92-108">(Iespējams, būs LCS jāieslēdz piekļuve savai IP adresei pirms varēsiet izveidot attilināto savienojumu ar programmas objektu serveri \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="d8e92-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="d8e92-109">Izlaidiet šo darbību, ja izmantojat versiju 10.0.20 vai jaunāku versiju, vai, ja izmantojat Service Fabric izvietojumu.</span><span class="sxs-lookup"><span data-stu-id="d8e92-109">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="d8e92-110">Finanšu ieskatu grupai jau vajadzētu ieslēgt jums šo ierobežoto līdzekli.</span><span class="sxs-lookup"><span data-stu-id="d8e92-110">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="d8e92-111">Ja neredzat līdzekli darbvietā **Līdzekļu pārvaldība** vai ja rodas problēmas, mēģinot to ieslēgt, sazinieties ar <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="d8e92-111">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="d8e92-112">Atveriet darbvietu **Līdzekļu pārvaldība** un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d8e92-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="d8e92-113">Atlasiet **Pārbaudīt atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="d8e92-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="d8e92-114">Ieslēdziet tālāk norādītos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="d8e92-114">Turn on the following features:</span></span>

        - <span data-ttu-id="d8e92-115">Jauna režģa vadīkla</span><span class="sxs-lookup"><span data-stu-id="d8e92-115">New grid control</span></span>
        - <span data-ttu-id="d8e92-116">Grupēšana režģos (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="d8e92-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="d8e92-117">Debitoru maksājumu prognozes (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="d8e92-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="d8e92-118">Skaidras naudas plūsmas prognozēšana (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="d8e92-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="d8e92-119">Dodieties uz **Skaidras naudas un bankas pārvaldība \> Skaidras naudas plūsmas prognozes iestatīšana** un pievienojiet likviditātes kontus, kas jāiekļauj prognozēs.</span><span class="sxs-lookup"><span data-stu-id="d8e92-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d8e92-120">Ja likviditātes konti nav iestatīti, skaidras naudas plūsmu nevar ģenerēt.</span><span class="sxs-lookup"><span data-stu-id="d8e92-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="d8e92-121">Dodieties uz **Skaidras naudas un bankas pārvaldība \> Iestatīšana \> Finanšu ieskati (priekšskatījums) \> Skaidras naudas plūsmas prognozes (priekšskatījums)** un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d8e92-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="d8e92-122">Cilnē **Skaidras naudas plūsmas prognoze** atlasiet **Iespējot līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="d8e92-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="d8e92-123">Atlasiet **Izveidot prognozēšanas modeli**.</span><span class="sxs-lookup"><span data-stu-id="d8e92-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="d8e92-124">Plašāku informāciju par to, kā iestatīt skaidras naudas plūsmas prognozēšanas iespēju, skatiet [Skaidras naudas plūsmas prognozēšana](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="d8e92-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
