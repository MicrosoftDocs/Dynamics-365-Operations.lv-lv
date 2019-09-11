---
title: Tādu mazumtirdzniecības parametru konfigurēšana, kas ietekmē mazumtirdzniecības pārskatus
description: Šajā tēmā parādītas konfigurācijas tiem mazumtirdzniecības parametriem, kuri ietekmē to, kā tiek izveidoti un grāmatoti mazumtirdzniecības pārskati.
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
ms.openlocfilehash: b9a0386a4d61395903e82d988244dd131c1febaf
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867275"
---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a><span data-ttu-id="41787-103">Tādu mazumtirdzniecības parametru konfigurēšana, kas ietekmē mazumtirdzniecības pārskatus</span><span class="sxs-lookup"><span data-stu-id="41787-103">Configure Retail parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="41787-104">Šajā tēmā parādītas konfigurācijas tiem mazumtirdzniecības parametriem, kuri ietekmē to, kā tiek izveidoti un grāmatoti mazumtirdzniecības pārskati.</span><span class="sxs-lookup"><span data-stu-id="41787-104">This topic demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="41787-105">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="41787-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="41787-106">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Mazumtirdzniecība un komercija > Headquarters iestatīšana > Parametri > Mazumtirdzniecības parametri**.</span><span class="sxs-lookup"><span data-stu-id="41787-106">In the navigation pane, go to **Modules > Retail and commerce > Headquarters setup  > Parameters > Retail parameters**.</span></span>
2. <span data-ttu-id="41787-107">Atlasiet cilni **Grāmatošana**.</span><span class="sxs-lookup"><span data-stu-id="41787-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="41787-108">Atlasiet **Jā**, ja vēlaties grāmatot konkrētus periodiskus atlaižu apjomus.</span><span class="sxs-lookup"><span data-stu-id="41787-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="41787-109">Atlasiet **Standarta**, lai izmantotu noklusējuma uzņēmumus vai atlasiet **Periodiski**, ja vēlaties definēt, kuru uzņēmumu izmantot katrai periodiskajai atlaidei.</span><span class="sxs-lookup"><span data-stu-id="41787-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="41787-110">Atlasiet **Kopsavilkums**, ja krājumu rindas vajadzētu, kad vien iespējams, apkopot.</span><span class="sxs-lookup"><span data-stu-id="41787-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="41787-111">Atlasiet **Jā**, ja rēķinus un maksājumus vajadzētu automātiski veikt kā daļu no pārskatu grāmatošanas procesa.</span><span class="sxs-lookup"><span data-stu-id="41787-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="41787-112">Atlasiet **Jā**, ja vajadzētu apkopot noguldījuma seifā darījumus.</span><span class="sxs-lookup"><span data-stu-id="41787-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="41787-113">Atlasiet **Jā**, ja vajadzētu apkopot noguldījuma bankā darījumus.</span><span class="sxs-lookup"><span data-stu-id="41787-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="41787-114">Atlasiet **Jā**, lai ieslēgtu apkopošanu pārskata grāmatošanai. </span><span class="sxs-lookup"><span data-stu-id="41787-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="41787-115">Atlasiet **Jā**, lai paralēli izveidotu un apstrādātu pasūtījumus, kad tiek grāmatoti pārskati.</span><span class="sxs-lookup"><span data-stu-id="41787-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="41787-116">Ievadiet maksimālo apstrādājamo pasūtījumu skaitu katram pakešuzdevumā darbam.</span><span class="sxs-lookup"><span data-stu-id="41787-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="41787-117">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="41787-117">Select **Save**.</span></span>

