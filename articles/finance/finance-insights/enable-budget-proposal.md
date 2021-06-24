---
title: Budžeta priekšlikuma iespējošana (priekšskatījums)
description: Šajā tēmā skaidrots, kā ieslēgt budžeta priekšlikuma līdzekli Finanšu ieskatos.
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
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222538"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="8e20c-103">Budžeta priekšlikuma iespējošana (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="8e20c-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8e20c-104">Šajā tēmā skaidrots, kā ieslēgt budžeta priekšlikuma līdzekli Finanšu ieskatos.</span><span class="sxs-lookup"><span data-stu-id="8e20c-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="8e20c-105">Izmantojiet informāciju no vides lapas Microsoft Dynamics Lifecycle Services (LCS), lai izveidotu savienojumu ar Azure SQL primāro instanci šai videi.</span><span class="sxs-lookup"><span data-stu-id="8e20c-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="8e20c-106">Palaidiet tālāk norādīto Transact-SQL (T-SQL) komandu, lai ieslēgtu ierobežotos līdzekļus smilškastes videi.</span><span class="sxs-lookup"><span data-stu-id="8e20c-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="8e20c-107">(Iespējams, būs LCS jāieslēdz piekļuve savai IP adresei pirms varēsiet izveidot attilināto savienojumu ar programmas objektu serveri \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="8e20c-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="8e20c-108">Izlaidiet šo darbību, ja izmantojat versiju 10.0.20 vai jaunāku versiju, vai, ja izmantojat Service Fabric izvietojumu.</span><span class="sxs-lookup"><span data-stu-id="8e20c-108">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="8e20c-109">Finanšu ieskatu grupai jau vajadzētu ieslēgt jums šo ierobežoto līdzekli.</span><span class="sxs-lookup"><span data-stu-id="8e20c-109">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="8e20c-110">Ja neredzat līdzekli darbvietā **Līdzekļu pārvaldība** vai ja rodas problēmas, mēģinot to ieslēgt, sazinieties ar <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="8e20c-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="8e20c-111">Atveriet darbvietu **Līdzekļu pārvaldība** un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8e20c-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="8e20c-112">Atlasiet **Pārbaudīt atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="8e20c-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="8e20c-113">Sameklējiet **Budžeta priekšlikums** un ieslēdziet šo līdzekli.</span><span class="sxs-lookup"><span data-stu-id="8e20c-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="8e20c-114">Doties uz **Budžeta veidošana \> Iestatīšana \> Pamata budžeta veidošana \> Budžeta priekšlikums (priekšskatījums)** un atlasiet **Iespējot līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="8e20c-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
