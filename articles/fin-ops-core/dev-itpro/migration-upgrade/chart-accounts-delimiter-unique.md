---
title: Unikāla kontu plāna norobežotāja iestatīšana
description: Šajā tēmā ir paskaidrots, kā kontu plānam un dimensijas vērtībām nevar izmantot vienu un to pašu norobežotāju. Pēc jaunināšanas ir jāmaina norobežotāja vērtības.
author: panolte
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: f4f89772dedb5433c3da3f0f7bf02106641f59a8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748111"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="5192c-104">Unikāla kontu plāna norobežotāja iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5192c-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5192c-105">Programmā Microsoft Dynamics AX 2012 kontu plānam un dimensijas vērtībām varēja izmantot vienu un to pašu norobežotāju.</span><span class="sxs-lookup"><span data-stu-id="5192c-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="5192c-106">Pašreizējās Finance and Operations versijās nevar būt tāds pats norobežotājs kontu plānam un dimensijas vērtībām.</span><span class="sxs-lookup"><span data-stu-id="5192c-106">In current versions of Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="5192c-107">Ja norobežotājam ir dublikāts, to var mainīt pēc jaunināšanas.</span><span class="sxs-lookup"><span data-stu-id="5192c-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="5192c-108">Šī funkcija ir pieejama tālāk minētajās versijās.</span><span class="sxs-lookup"><span data-stu-id="5192c-108">This feature is available in the following versions:</span></span>
- <span data-ttu-id="5192c-109">Finance and Operations versija 8.0</span><span class="sxs-lookup"><span data-stu-id="5192c-109">Finance and Operations version 8.0</span></span>
- <span data-ttu-id="5192c-110">Finance and Operations versija 7.1, KB 4094701 Nevar ievadīt finanšu dimensijas, ja dimensijas vērtības satur kontu plāna norobežotāju</span><span class="sxs-lookup"><span data-stu-id="5192c-110">Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="5192c-111">Finance and Operations versija 7.2, KB 4092967 Nevar izvēlēties apakšprojektu kā dimensiju, ja apakšprojekta formāts satur dimensijas norobežotāju</span><span class="sxs-lookup"><span data-stu-id="5192c-111">Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="5192c-112">Norobežotāja atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="5192c-112">Update delimiter</span></span>
<span data-ttu-id="5192c-113">Ja ir radies konflikts ar kontu plānu, var mainīt kontu plāna norobežotāju un projekta/apakšprojekta ID formātu.</span><span class="sxs-lookup"><span data-stu-id="5192c-113">If there is a conflict with the chart of accounts, the chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="5192c-114">Citus dimensiju norobežotājus nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="5192c-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="5192c-115">Kontu plāna norobežotāju var mainīt pēc jaunināšanas sadaļā **Virsgrāmatas parametri** > **Kontu plāns un dimensijas** > **Mainīt norobežotāju**.</span><span class="sxs-lookup"><span data-stu-id="5192c-115">You can change the chart of accounts delimiter after upgrade in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="5192c-116">Ja vienīgais konflikts ir ar projekta/apakšprojekta ID formātu, varat mainīt šo vērtību sadaļā **Projektu vadības un uzskaites parametri** > **Vispārīgi** > **Apakšprojektu formāta modificēšana**.</span><span class="sxs-lookup"><span data-stu-id="5192c-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="5192c-117">Kā noteikt, vai jūsu vidē ir nepieciešams atjaunināt norobežotājus</span><span class="sxs-lookup"><span data-stu-id="5192c-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="5192c-118">Ja norobežotāji jauninātajā vidē ir konfliktējoši, var veidoties nestabilitāte, ievadot vērtības segmentētas ievades vadīklā vai dimensiju ievades vadīklā.</span><span class="sxs-lookup"><span data-stu-id="5192c-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="5192c-119">Tas nozīmē, ka būs nepieciešams vienmēr izmantot meklēšanas rezultātus vai uznirstošo izvēlni, ievadot kontu un dimensiju kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="5192c-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]