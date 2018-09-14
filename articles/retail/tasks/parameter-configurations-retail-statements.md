--- 
title: " Mazumtirdzniecības izrakstu parametru konfigurācijas"
description: "Šajā procedūra ir aprakstītas mazumtirdzniecības parametru konfigurācijas, kas ietekmē mazumtirdzniecības pārskatu izveides un grāmatošanas procesu."
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6dacd2b80ca0d51d81d2bdf5bc2636b47da621ee
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="90765-103"> Mazumtirdzniecības izrakstu parametru konfigurācijas</span><span class="sxs-lookup"><span data-stu-id="90765-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="90765-104">Šajā procedūra ir aprakstītas mazumtirdzniecības parametru konfigurācijas, kas ietekmē mazumtirdzniecības pārskatu izveides un grāmatošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="90765-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="90765-105">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="90765-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="90765-106">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Centrālā biroja iestatīšana > Parametri > Mazumtirdzniecības parametri.</span><span class="sxs-lookup"><span data-stu-id="90765-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="90765-107">Noklikšķiniet uz cilnes Grāmatošana.</span><span class="sxs-lookup"><span data-stu-id="90765-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="90765-108">Atlasiet Jā, ja vēlaties grāmatot tikai periodiskās atlaižu summas.</span><span class="sxs-lookup"><span data-stu-id="90765-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="90765-109">Atlasiet Standarta, lai izmantotu noklusējuma kontus, vai atlasiet Periodisks, ja vēlaties definēt, kuru kontu lietot katrai periodiskajai atlaidei.</span><span class="sxs-lookup"><span data-stu-id="90765-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="90765-110">Atlasiet Kopsavilkums, ja krājuma rindas jāapkopo, kad vien tas ir iespējams.</span><span class="sxs-lookup"><span data-stu-id="90765-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="90765-111">Atlasiet Jā, ja rēķini un maksājumi ir automātiski jāapmaksā kā daļa no pārskata grāmatošanas procesa.</span><span class="sxs-lookup"><span data-stu-id="90765-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="90765-112">Atlasiet Jā, ja seifa noguldījuma transakcijas ir jāapkopo.</span><span class="sxs-lookup"><span data-stu-id="90765-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="90765-113">Atlasiet Jā, ja bankas noguldījuma transakcijas ir jāapkopo.</span><span class="sxs-lookup"><span data-stu-id="90765-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="90765-114">Atlasiet Jā, lai lieslēgtu apkopojumu parskatu grāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="90765-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="90765-115">Atlasiet Jā, lai izveidotu un apstrādātu pasūtījumus, vienlaicīgi grāmatojot pārskatus.</span><span class="sxs-lookup"><span data-stu-id="90765-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="90765-116">Ievadiet maksimālo apstrādājamo pasūtījumu skaitu katram pakešuzdevumā darbam.</span><span class="sxs-lookup"><span data-stu-id="90765-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="90765-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="90765-117">Click Save.</span></span>


