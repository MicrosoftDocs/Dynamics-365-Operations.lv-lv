---
title: Tādu parametru konfigurēšana, kas ietekmē mazumtirdzniecības pārskatus
description: Šajā tēmā parādītas konfigurācijas tiem Commerce parametriem, kuri ietekmē to, kā tiek izveidoti un grāmatoti mazumtirdzniecības pārskati.
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023274"
---
# <a name="configure-parameters-that-affect-retail-statements"></a><span data-ttu-id="c3ad8-103">Tādu parametru konfigurēšana, kas ietekmē mazumtirdzniecības pārskatus</span><span class="sxs-lookup"><span data-stu-id="c3ad8-103">Configure parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c3ad8-104">Šajā tēmā parādītas konfigurācijas tiem Commerce parametriem, kuri ietekmē to, kā tiek izveidoti un grāmatoti mazumtirdzniecības pārskati.</span><span class="sxs-lookup"><span data-stu-id="c3ad8-104">This topic demonstrates configurations for Commerce parameters that affect how statements get created and posted.</span></span> <span data-ttu-id="c3ad8-105">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="c3ad8-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="c3ad8-106">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Retail un Commerce > Headquarters iestatīšana > Parametri > Commerce parametri**.</span><span class="sxs-lookup"><span data-stu-id="c3ad8-106">In the navigation pane, go to **Modules > Retail and Commerce > Headquarters setup  > Parameters > Commerce parameters**.</span></span>
2. <span data-ttu-id="c3ad8-107">Atlasiet cilni **Grāmatošana**.</span><span class="sxs-lookup"><span data-stu-id="c3ad8-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="c3ad8-108">Atlasiet **Jā**, ja vēlaties grāmatot konkrētus periodiskus atlaižu apjomus.</span><span class="sxs-lookup"><span data-stu-id="c3ad8-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="c3ad8-109">Atlasiet **Standarta**, lai izmantotu noklusējuma uzņēmumus vai atlasiet **Periodiski**, ja vēlaties definēt, kuru uzņēmumu izmantot katrai periodiskajai atlaidei.</span><span class="sxs-lookup"><span data-stu-id="c3ad8-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="c3ad8-110">Atlasiet **Kopsavilkums**, ja krājumu rindas vajadzētu, kad vien iespējams, apkopot.</span><span class="sxs-lookup"><span data-stu-id="c3ad8-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="c3ad8-111">Atlasiet **Jā**, ja rēķinus un maksājumus vajadzētu automātiski veikt kā daļu no pārskatu grāmatošanas procesa.</span><span class="sxs-lookup"><span data-stu-id="c3ad8-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="c3ad8-112">Atlasiet **Jā**, ja vajadzētu apkopot noguldījuma seifā darījumus.</span><span class="sxs-lookup"><span data-stu-id="c3ad8-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="c3ad8-113">Atlasiet **Jā**, ja vajadzētu apkopot noguldījuma bankā darījumus.</span><span class="sxs-lookup"><span data-stu-id="c3ad8-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="c3ad8-114">Atlasiet **Jā**, lai ieslēgtu apkopošanu pārskata grāmatošanai. </span><span class="sxs-lookup"><span data-stu-id="c3ad8-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="c3ad8-115">Atlasiet **Jā**, lai paralēli izveidotu un apstrādātu pasūtījumus, kad tiek grāmatoti pārskati.</span><span class="sxs-lookup"><span data-stu-id="c3ad8-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="c3ad8-116">Ievadiet maksimālo apstrādājamo pasūtījumu skaitu katram pakešuzdevumā darbam.</span><span class="sxs-lookup"><span data-stu-id="c3ad8-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="c3ad8-117">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c3ad8-117">Select **Save**.</span></span>

