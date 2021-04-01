---
title: RCS uzlabota filtrēšana RCS/globālajā repozitorijā
description: Šajā tēmā ir aprakstītas uzlabotās filtrēšanas iespējas RCS globālajā repozitorijā, kas ir uzlabotas, lai iekļautu papildu filtrus.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 87ada5a97d2b716145082b3845fa87a12df57ef7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235601"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="73516-103">RCS uzlabotās filtrēšanas opcijas konfigurāciju atrašanai RCS/globālajā repozitorijā</span><span class="sxs-lookup"><span data-stu-id="73516-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73516-104">Šajā tēmā ir aprakstītas uzlabotās filtrēšanas iespējas Regulatory Configuration Services (RCS) globālajam repozitorijam, kas ir uzlabotas, lai iekļautu iespēju filtrēt ar šādiem kritērijiem:</span><span class="sxs-lookup"><span data-stu-id="73516-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="73516-105">**Valsts/reģions**, kura pamatā ir ISO valstu kodi</span><span class="sxs-lookup"><span data-stu-id="73516-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="73516-106">**Etiķešu** veidi:</span><span class="sxs-lookup"><span data-stu-id="73516-106">**Tags** types for:</span></span>
  - <span data-ttu-id="73516-107">Funkcionālais apgabals</span><span class="sxs-lookup"><span data-stu-id="73516-107">Functional area</span></span>
  - <span data-ttu-id="73516-108">Līdzekļu apgabals</span><span class="sxs-lookup"><span data-stu-id="73516-108">Feature area</span></span>
  - <span data-ttu-id="73516-109">Nozare</span><span class="sxs-lookup"><span data-stu-id="73516-109">Industry</span></span> 
  - <span data-ttu-id="73516-110">Biznesa dokuments</span><span class="sxs-lookup"><span data-stu-id="73516-110">Business document</span></span> 

<span data-ttu-id="73516-111">Lai vieglāk atklātu konkrētas vai saistītas konfigurācijas, jūs varat izmantot filtrus atsevišķi vai kā grupa.</span><span class="sxs-lookup"><span data-stu-id="73516-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="73516-112">Piemēram, lai atrastu viena veida konfigurējamus biznesa dokumentus, kas ir saistīti ar kreditora rēķiniem, varat izmantot **Biznesa dokumenta veida** filtru, lai meklētu šo dokumenta veidu.</span><span class="sxs-lookup"><span data-stu-id="73516-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="73516-113">[![Globālās krātuves filtra sadaļa](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="73516-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="73516-114">Varat turpināt precizēt meklēšanu, atlasot dokumenta veidu, piemēram, "kreditora rēķins", un noklikšķiniet uz **Lietot filtru**.</span><span class="sxs-lookup"><span data-stu-id="73516-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="73516-115">Šis piemērs parāda rezultātus, filtrējot **Biznesa dokumenta veidu** ar pievienotu dokumenta veidu.</span><span class="sxs-lookup"><span data-stu-id="73516-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="73516-116">[![Lietotais biznesa dokumenta tipa filtrs un imports](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="73516-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="73516-117">Filtrētus rezultātus var importēt lietotāju RCS repozitorijā vai Dynamics 365 Finance vidē atsevišķi vai kā kopu.</span><span class="sxs-lookup"><span data-stu-id="73516-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="73516-118">Lai to izdarītu, atlasiet konfigurāciju grupu un noklikšķiniet uz **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="73516-118">To do this, select the group of configurations, and click **Import**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]