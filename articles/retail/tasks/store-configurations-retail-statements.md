---
title: " Mazumtirdzniecības izrakstu veikala konfigurācijas"
description: Šajā procedūra ir aprakstītas mazumtirdzniecības veikala konfigurācijas, kas ietekmē mazumtirdzniecības pārskatu izveides un grāmatošanas procesu.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbedcda59f503b103d5448e59038e4ed8ca0b51d
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916534"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="c099c-103"> Mazumtirdzniecības izrakstu veikala konfigurācijas</span><span class="sxs-lookup"><span data-stu-id="c099c-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c099c-104">Šajā procedūra ir aprakstītas mazumtirdzniecības veikala konfigurācijas, kas ietekmē mazumtirdzniecības pārskatu izveides un grāmatošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="c099c-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="c099c-105">Finanšu dimensijas mazumtirdzniecības veikalos tiek ietvertas citā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="c099c-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="c099c-106">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="c099c-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="c099c-107">**Navigācijas rūtī** dodieties uz **Moduļi > Mazumtirdzniecība un komercija > Kanāli > Mazumtirdzniecības veikali > Visi mazumtirdzniecības veikali**.</span><span class="sxs-lookup"><span data-stu-id="c099c-107">In the **Navgiation pane**, go to **Modules > Retail and commerce > Channels > Retail stores > All retail stores**.</span></span>
2. <span data-ttu-id="c099c-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c099c-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c099c-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c099c-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c099c-110">Noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="c099c-110">Click **Edit**.</span></span>
5. <span data-ttu-id="c099c-111">Kopsavilkuma cilnes **Izraksts/slēgšana** iestatījumi ietekmē veikala pārskata izveides, apstiprināšanas un grāmatošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="c099c-111">The settings in the **Statement/closing** fastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="c099c-112">Paplašiniet kopsavilkuma cilni **Izraksts/slēgšana**.</span><span class="sxs-lookup"><span data-stu-id="c099c-112">Expand the **Statement/closing** fastTab.</span></span>  
6. <span data-ttu-id="c099c-113">Laukā **Izraksta metode** atlasiet metodi, kuru vēlaties izmantot pārskata rindu grupēšanai.</span><span class="sxs-lookup"><span data-stu-id="c099c-113">In the **Statement method** field, select the method you want to use to to group the statement lines by.</span></span>  
7. <span data-ttu-id="c099c-114">Atlasiet “Jā” sadaļā **Viens izraksts dienā**, ja, veidojot pārskatus no pārskata izveides pakešuzdevuma, dienā jāizveido tikai viens pārskats.</span><span class="sxs-lookup"><span data-stu-id="c099c-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="c099c-115">Lauks **Norēķinu uzskaites aprēķins** nosaka, vai norēķinu deklarācijas jāpievieno kopā, vai arī jāizmanto pēdējā deklarācija.</span><span class="sxs-lookup"><span data-stu-id="c099c-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="c099c-116">Laukā **Noapaļošana** atlasiet virsgrāmatas kontu, kur jāgrāmato noapaļošanas starpības.</span><span class="sxs-lookup"><span data-stu-id="c099c-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="c099c-117">Laukā **Maksimālā noapaļošanas starpība** var ievadīt maksimālo atļauto noapaļošanas starpību.</span><span class="sxs-lookup"><span data-stu-id="c099c-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="c099c-118">Laukā **Grāmatošana** var ievadīt maksimālo kopējo grāmatošanas starpību, kas atļauta pārskatam.</span><span class="sxs-lookup"><span data-stu-id="c099c-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="c099c-119">Laukā **Maiņa** var ievadīt maksimālo kopējo maiņas starpību, kas atļauta pārskatam.</span><span class="sxs-lookup"><span data-stu-id="c099c-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="c099c-120">Laukā **Transakcija** var ievadīt maksimālo kopējo starpību pārskata rindā.</span><span class="sxs-lookup"><span data-stu-id="c099c-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="c099c-121">Laukā **Slēguma metode** var definēt, vai transakcijām, kas jāiekļauj pārskatā, jābūt daļai no slēgtas maiņas, vai arī tās var būt jebkuras transakcijas definētajā datuma/laika diapazonā.</span><span class="sxs-lookup"><span data-stu-id="c099c-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="c099c-122">Laukā **Darba dienas beigas** var ievadīt laiku, kad transakcijas, kas tiek veiktas pēc pusnakts, ir jāgrāmato ar iepriekšējās dienas datumu.</span><span class="sxs-lookup"><span data-stu-id="c099c-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="c099c-123">Atlasiet “Jā” laukā **Grāmatot kā darba dienu**, ja transakcijas, kas tiek veiktas pēc pusnakts, ir jāgrāmato ar iepriekšējās dienas datumu.</span><span class="sxs-lookup"><span data-stu-id="c099c-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="c099c-124">Atlasiet “Jā” laukā **Sadalīt pēc izraksta metodes**, lai iegūtu pārskatus, kas izveidoti katrai definētajai pārskatu izveides metodei.</span><span class="sxs-lookup"><span data-stu-id="c099c-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="c099c-125">Tas var noderēt, ja ir jāuzlabo grāmatošanas veiktspēja veikaliem ar lielu transakciju apjomu, jo tādējādi tiks izveidots ievērojami mazāk pārskatu, ko var apstrādāt paralēli.</span><span class="sxs-lookup"><span data-stu-id="c099c-125">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="c099c-126">Kopsavilkuma cilnes **Vispārīgi** laukā **Noklusējuma debitors** var atlasiet debitora kontu, ko lietot pārdošanas procesā debitoriem.</span><span class="sxs-lookup"><span data-stu-id="c099c-126">In the **General** fastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  

