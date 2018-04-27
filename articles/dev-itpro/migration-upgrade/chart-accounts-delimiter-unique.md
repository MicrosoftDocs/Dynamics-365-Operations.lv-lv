---
title: "Kontu plāna norobežotājam ir jābūt unikālam"
description: "Risinājumā Dynamics 365 for Finance and Operations nevar būt tāds pats norobežotājs kontu plānam un dimensijas vērtībām. Pēc jaunināšanas ir jāmaina norobežotāja vērtības."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c9728714944b54f3bff1e2a8b43c7adcf5200f08
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="chart-of-accounts-delimiter-must-be-unique"></a><span data-ttu-id="a0a8e-104">Kontu plāna norobežotājam ir jābūt unikālam</span><span class="sxs-lookup"><span data-stu-id="a0a8e-104">Chart of accounts delimiter must be unique</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="a0a8e-105">Programmā Microsoft Dynamics AX 2012 varēja izmantot tādu pašu norobežotāju kontu plānam un dimensijas vērtībām.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="a0a8e-106">Risinājumā Dynamics 365 for Finance and Operations nevar būt tāds pats norobežotājs kontu plānam un dimensijas vērtībām.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="a0a8e-107">Ja norobežotājam ir dublikāts, to var mainīt pēc jaunināšanas.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="a0a8e-108">Šī funkcija ir pieejama:</span><span class="sxs-lookup"><span data-stu-id="a0a8e-108">This feature is available in:</span></span>
- <span data-ttu-id="a0a8e-109">Dynamics 365 for Finance and Operations versijā 8.0</span><span class="sxs-lookup"><span data-stu-id="a0a8e-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="a0a8e-110">Dynamics 365 for Finance and Operations versijā 7.1, KB 4094701 Nevar ievadīt finanšu dimensijas, ja dimensijas vērtības satur kontu plāna norobežotāju</span><span class="sxs-lookup"><span data-stu-id="a0a8e-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="a0a8e-111">Dynamics 365 for Finance and Operations versijā 7.2, KB 4092967 Nevar izvēlēties apakšprojektu kā dimensiju, ja apakšprojekta formātā ir dimensiju norobežotājs</span><span class="sxs-lookup"><span data-stu-id="a0a8e-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="a0a8e-112">Norobežotāja atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="a0a8e-112">Update delimiter</span></span>
<span data-ttu-id="a0a8e-113">Ja ir radies konflikts ar kontu plānu, var mainīt kontu plāna norobežotāju un projekta/apakšprojekta ID formātu.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="a0a8e-114">Citus dimensiju norobežotājus nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="a0a8e-115">Kontu plāna norobežotāju var mainīt pēc jaunināšanas uz Finance and Operations sadaļā **Virsgrāmatas parametri** > **Kontu plāns un dimensijas** > **Mainīt norobežotāju**.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="a0a8e-116">Ja vienīgais konflikts ir ar projekta/apakšprojekta ID formātu, varat mainīt šo vērtību sadaļā **Projektu vadības un uzskaites parametri** > **Vispārīgi** > **Apakšprojektu formāta modificēšana**.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="a0a8e-117">Kā noteikt, vai jūsu vidē ir nepieciešams atjaunināt norobežotājus</span><span class="sxs-lookup"><span data-stu-id="a0a8e-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="a0a8e-118">Ja norobežotāji jauninātajā vidē ir konfliktējoši, var veidoties nestabilitāte, ievadot vērtības segmentētas ievades vadīklā vai dimensiju ievades vadīklā.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="a0a8e-119">Tas nozīmē, ka būs nepieciešams vienmēr izmantot meklēšanas rezultātus vai uznirstošo izvēlni, ievadot kontu un dimensiju kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="a0a8e-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>

