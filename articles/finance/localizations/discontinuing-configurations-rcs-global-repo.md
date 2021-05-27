---
title: Konfigurāciju pārtraukšana RCS globālajā repozitorijā
description: Šajā tēmā aprakstīts, kā pārtraukt RCS globālā repozitorija konfigurācijas.
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2bd22e991de376cfd93f75158f1f29716d2559e1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018737"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="c871c-103">Konfigurāciju pārtraukšana RCS globālajā repozitorijā</span><span class="sxs-lookup"><span data-stu-id="c871c-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c871c-104">Šajā tēmā aprakstīts, kā pārtraukt RCS globālā repozitorija konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="c871c-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="c871c-105">Iepriekš bija iespējams dzēst tikai tās konfigurācijas, kuras vairāk nebija nepieciešamas.</span><span class="sxs-lookup"><span data-stu-id="c871c-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="c871c-106">Taču tagad varat RCS globālajā repozitorijā atzīmēt konfigurāciju kā **Pārtrauktu**.</span><span class="sxs-lookup"><span data-stu-id="c871c-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="c871c-107">Ar šo funkcionalitāti jūs varat arī:</span><span class="sxs-lookup"><span data-stu-id="c871c-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="c871c-108">Nodrošināt iepriekšējus paziņojumus, ja tiek plānots pārtraukt konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="c871c-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="c871c-109">Iekļaut saistošu informāciju par maiņas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="c871c-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="c871c-110">Konkrētai konfigurācijai iestatīt datumu **Atbalstīta līdz**, lai informētu lietotāju par laiku, kad tā tiks pārtraukta.</span><span class="sxs-lookup"><span data-stu-id="c871c-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="c871c-111">Pārtraucot konfigurācijas versiju, varat neobligāti norādīt šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="c871c-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="c871c-112">**Aizstāšanas konfigurācija**</span><span class="sxs-lookup"><span data-stu-id="c871c-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="c871c-113">**Maiņas konfigurācijas versija**</span><span class="sxs-lookup"><span data-stu-id="c871c-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="c871c-114">**Brīvā teksta piezīme**: Izmantojiet šo lauku, lai sniegtu saites uz dokumentiem vai atsauces</span><span class="sxs-lookup"><span data-stu-id="c871c-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="c871c-115">**Atbalstīta līdz**: Šis lauks nodrošina piedāvāto datumu, līdz kuram pašreizējā konfigurācija/versija tiks atbalstīta.</span><span class="sxs-lookup"><span data-stu-id="c871c-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="c871c-116">Šis datums ir jāatjaunina manuāli.</span><span class="sxs-lookup"><span data-stu-id="c871c-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="c871c-117">Lai pārtrauktu konfigurāciju, izpildiet šīs darbības:</span><span class="sxs-lookup"><span data-stu-id="c871c-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="c871c-118">Atlasiet, vai vēlaties pārtraukt vienu vai visas versijas ar tiem pašiem iestatījumiem vienā darbībā, iestatot opciju **Visas versijas** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c871c-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="c871c-119">Iestatiet parametru **Pārtraukt** uz opciju **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c871c-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="c871c-120">Atlasiet **Labi**, lai pārtrauktu konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="c871c-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="c871c-121">Lauks **Pārtraukšanas datums** tiks aizpildīts, kad saglabāsit izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="c871c-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![Konfigurācijas pārtraukšanas informācija](media/Discontinue-details-2.png)
  
<span data-ttu-id="c871c-123">Jebkurā laikā varat atgriezt konfigurāciju statusā **Kopīgota** vai pielāgot konfigurācijas informāciju.</span><span class="sxs-lookup"><span data-stu-id="c871c-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="c871c-124">Kopīgojot informāciju, norādiet datumu **Atbalstīta līdz** un citu informāciju, kas ir saistīta ar pārtraukšanu, lai norādītu savus plānus attiecībā uz pārtraukšanu nākotnē.</span><span class="sxs-lookup"><span data-stu-id="c871c-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="c871c-125">Ja vēlaties kopīgot informāciju par plānoto pārtraukšanu pirms faktiskās konfigurācijas pārtraukšanas, lietotājs var iepriekš aizpildīt visus laukus, kas saistīti ar nomaiņu, bet atstāt parametru **Pārtraukt** iestatītu uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="c871c-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="c871c-126">Pārtraukšana neierobežo darbības ar konfigurācijām.</span><span class="sxs-lookup"><span data-stu-id="c871c-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="c871c-127">Varat turpināt importēt, palaist vai atvasināt konfigurācijas, šie lauki ir informatīvi.</span><span class="sxs-lookup"><span data-stu-id="c871c-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="c871c-128">Finance atbalsta šīs informācijas rādīšanu, sākot ar versiju 10.0.14</span><span class="sxs-lookup"><span data-stu-id="c871c-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="c871c-129">Sākot ar versiju 10.0.14., Dynamics 365 Finance atbalsta pārtraukšanas informācijas rādīšanu.</span><span class="sxs-lookup"><span data-stu-id="c871c-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="c871c-130">Lapā **Globālais repozitorijs** varat skatīt jaunāko informāciju, kas saistīta ar pārtraukšanu.</span><span class="sxs-lookup"><span data-stu-id="c871c-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="c871c-131">Konfigurācijas tiek pēc noklusējuma pārtrauktas un filtrētas.</span><span class="sxs-lookup"><span data-stu-id="c871c-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="c871c-132">Lapā **Importētās konfigurācijas** (ERSolutionTable) tiek rādītas konfigurācijas, kuras jau tika pārtrauktas importēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="c871c-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="c871c-133">Informāciju par konfigurācijām, kuras tika pārtrauktas pēc importēšanas, var sinhronizēt, palaižot darbu **Importēt konfigurāciju atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="c871c-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


