---
title: "Unikāla kontu plāna norobežotāja nodrošināšana"
description: "Risinājumā Dynamics 365 for Finance and Operations nevar būt tāds pats norobežotājs kontu plānam un dimensijas vērtībām. Pēc jaunināšanas ir jāmaina norobežotāja vērtības."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="1adaa-104">Unikāla kontu plāna norobežotāja nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="1adaa-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1adaa-105">Programmā Microsoft Dynamics AX 2012 varēja izmantot tādu pašu norobežotāju kontu plānam un dimensijas vērtībām.</span><span class="sxs-lookup"><span data-stu-id="1adaa-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="1adaa-106">Risinājumā Dynamics 365 for Finance and Operations nevar būt tāds pats norobežotājs kontu plānam un dimensijas vērtībām.</span><span class="sxs-lookup"><span data-stu-id="1adaa-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="1adaa-107">Ja norobežotājam ir dublikāts, to var mainīt pēc jaunināšanas.</span><span class="sxs-lookup"><span data-stu-id="1adaa-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="1adaa-108">Šī funkcija ir pieejama:</span><span class="sxs-lookup"><span data-stu-id="1adaa-108">This feature is available in:</span></span>
- <span data-ttu-id="1adaa-109">Dynamics 365 for Finance and Operations versijā 8.0</span><span class="sxs-lookup"><span data-stu-id="1adaa-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="1adaa-110">Dynamics 365 for Finance and Operations versijā 7.1, KB 4094701 Nevar ievadīt finanšu dimensijas, ja dimensijas vērtības satur kontu plāna norobežotāju</span><span class="sxs-lookup"><span data-stu-id="1adaa-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="1adaa-111">Dynamics 365 for Finance and Operations versijā 7.2, KB 4092967 Nevar izvēlēties apakšprojektu kā dimensiju, ja apakšprojekta formātā ir dimensiju norobežotājs</span><span class="sxs-lookup"><span data-stu-id="1adaa-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="1adaa-112">Norobežotāja atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="1adaa-112">Update delimiter</span></span>
<span data-ttu-id="1adaa-113">Ja ir radies konflikts ar kontu plānu, var mainīt kontu plāna norobežotāju un projekta/apakšprojekta ID formātu.</span><span class="sxs-lookup"><span data-stu-id="1adaa-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="1adaa-114">Citus dimensiju norobežotājus nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="1adaa-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="1adaa-115">Kontu plāna norobežotāju var mainīt pēc jaunināšanas uz Finance and Operations sadaļā **Virsgrāmatas parametri** > **Kontu plāns un dimensijas** > **Mainīt norobežotāju**.</span><span class="sxs-lookup"><span data-stu-id="1adaa-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="1adaa-116">Ja vienīgais konflikts ir ar projekta/apakšprojekta ID formātu, varat mainīt šo vērtību sadaļā **Projektu vadības un uzskaites parametri** > **Vispārīgi** > **Apakšprojektu formāta modificēšana**.</span><span class="sxs-lookup"><span data-stu-id="1adaa-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="1adaa-117">Kā noteikt, vai jūsu vidē ir nepieciešams atjaunināt norobežotājus</span><span class="sxs-lookup"><span data-stu-id="1adaa-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="1adaa-118">Ja norobežotāji jauninātajā vidē ir konfliktējoši, var veidoties nestabilitāte, ievadot vērtības segmentētas ievades vadīklā vai dimensiju ievades vadīklā.</span><span class="sxs-lookup"><span data-stu-id="1adaa-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="1adaa-119">Tas nozīmē, ka būs nepieciešams vienmēr izmantot meklēšanas rezultātus vai uznirstošo izvēlni, ievadot kontu un dimensiju kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="1adaa-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>

