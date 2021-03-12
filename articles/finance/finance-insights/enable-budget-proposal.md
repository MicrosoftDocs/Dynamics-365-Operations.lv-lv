---
title: Budžeta priekšlikuma iespējošana (priekšskatījums)
description: Šajā tēmā skaidrots, kā ieslēgt budžeta priekšlikuma līdzekli Finanšu ieskatos.
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
ms.openlocfilehash: 59cf40e8bf69734c5f3645997ff0b07c29d4f40e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995144"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="ae174-103">Budžeta priekšlikuma iespējošana (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="ae174-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ae174-104">Šajā tēmā skaidrots, kā ieslēgt budžeta priekšlikuma līdzekli Finanšu ieskatos.</span><span class="sxs-lookup"><span data-stu-id="ae174-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="ae174-105">Izmantojiet informāciju no vides lapas Microsoft Dynamics Lifecycle Services (LCS), lai izveidotu savienojumu ar Azure SQL primāro instanci šai videi.</span><span class="sxs-lookup"><span data-stu-id="ae174-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="ae174-106">Palaidiet tālāk norādīto Transact-SQL (T-SQL) komandu, lai ieslēgtu ierobežotos līdzekļus smilškastes videi.</span><span class="sxs-lookup"><span data-stu-id="ae174-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="ae174-107">(Iespējams, būs LCS jāieslēdz piekļuve savai IP adresei pirms varēsiet izveidot attilināto savienojumu ar programmas objektu serveri \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="ae174-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="ae174-108">Ja jūsu Microsoft Dynamics 365 Finance izvietošana ir Service Fabric izvietošana, varat izlaist šo darbību.</span><span class="sxs-lookup"><span data-stu-id="ae174-108">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="ae174-109">Finanšu ieskatu grupai jau vajadzētu ieslēgt jums šo ierobežoto līdzekli.</span><span class="sxs-lookup"><span data-stu-id="ae174-109">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="ae174-110">Ja neredzat šo līdzekli darbvietā **Līdzekļu pārvaldība** vai ja rodas problēmas, kad mēģināt to ieslēgt, nosūtiet e-pasta ziņojumu [Finanšu ieskatu programmas priekšskatījuma grupai](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="ae174-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, send email to the [Finance Insights App Preview team](mailto:fiap@microsoft.com).</span></span>

2. <span data-ttu-id="ae174-111">Atveriet darbvietu **Līdzekļu pārvaldība** un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ae174-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="ae174-112">Atlasiet **Pārbaudīt atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="ae174-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="ae174-113">Sameklējiet **Budžeta priekšlikums** un ieslēdziet šo līdzekli.</span><span class="sxs-lookup"><span data-stu-id="ae174-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="ae174-114">Doties uz **Budžeta veidošana \> Iestatīšana \> Pamata budžeta veidošana \> Budžeta priekšlikums (priekšskatījums)** un atlasiet **Iespējot līdzekli**.</span><span class="sxs-lookup"><span data-stu-id="ae174-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="ae174-115">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="ae174-115">Privacy notice</span></span>
<span data-ttu-id="ae174-116">Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.</span><span class="sxs-lookup"><span data-stu-id="ae174-116">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
