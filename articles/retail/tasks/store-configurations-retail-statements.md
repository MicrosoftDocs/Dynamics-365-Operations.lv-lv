--- 
title: " Mazumtirdzniecības izrakstu veikala konfigurācijas"
description: "Šajā procedūra ir aprakstītas mazumtirdzniecības veikala konfigurācijas, kas ietekmē mazumtirdzniecības pārskatu izveides un grāmatošanas procesu."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: c2140afc869686ae3f6d6c73ddaa31a4954d4d72
ms.contentlocale: lv-lv
ms.lasthandoff: 01/19/2018

---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="c7bb6-103"> Mazumtirdzniecības izrakstu veikala konfigurācijas</span><span class="sxs-lookup"><span data-stu-id="c7bb6-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c7bb6-104">Šajā procedūra ir aprakstītas mazumtirdzniecības veikala konfigurācijas, kas ietekmē mazumtirdzniecības pārskatu izveides un grāmatošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="c7bb6-105">Finanšu dimensijas mazumtirdzniecības veikalos tiek ietvertas citā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="c7bb6-106">Procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="c7bb6-107">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Kanāli > Mazumtirdzniecības veikali > Visi mazumtirdzniecības veikali.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="c7bb6-108">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c7bb6-109">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c7bb6-110">Sadaļas Izraksts/slēgšana iestatījumi ietekmē veikala pārskata izveides, apstiprināšanas un grāmatošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="c7bb6-111">Atveriet sadaļu Izraksts/slēgšana.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="c7bb6-112">Atlasiet metodi, ko vēlaties izmantot izraksta rindu grupēšanai.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-112">Select the method you want to use to group the statement lines by.</span></span>  
    * <span data-ttu-id="c7bb6-113">Atlasiet Jā, ja, veidojot pārskatus no pārskata izveides pakešuzdevuma, dienā jāizveido tikai viens pārskats.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="c7bb6-114">Laukā Norēķinu uzskaites aprēķins nosaka, vai norēķinu deklarācijas jāpievieno kopā, vai arī jāizmanto pēdējā deklarācija.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="c7bb6-115">Atlasiet virsgrāmatas kontu, kur jāgrāmato noapaļošanas starpības.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="c7bb6-116">Laukā Maksimālā noapaļošanas starpība var ievadīt maksimālo atļauto noapaļošanas starpību.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="c7bb6-117">Laukā Grāmatošana var ievadīt maksimālo kopējo grāmatošanas starpību, kas atļauta pārskatam.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="c7bb6-118">Laukā Maiņa var ievadīt maksimālo kopējo maiņas starpību, kas atļauta pārskatam.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="c7bb6-119">Laukā Transakcija var ievadīt maksimālo kopējo starpību pārskata rindā.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="c7bb6-120">Laukā Slēguma metode var definēt, vai transakcijām, kas jāiekļauj pārskatā, jābūt daļai no slēgtas maiņas, vai arī tās var būt jebkuras transakcijas definētajā datuma/laika diapazonā.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="c7bb6-121">Laukā Darba dienas beigas var ievadīt laiku, kad transakcijas, kas tiek veiktas pēc pusnakts, ir jāgrāmato ar iepriekšējās dienas datumu.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="c7bb6-122">Atlasiet Jā, ja transakcijas, kas tiek veiktas pēc pusnakts, ir jāgrāmato ar iepriekšējās dienas datumu.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="c7bb6-123">Atlasiet Jā, lai iegūtu pārskatus, kas izveidoti katrai definētajai pārskatu izveides metodei.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="c7bb6-124">Tas var noderēt, ja ir jāuzlabo grāmatošanas veiktspēja veikaliem ar lielu transakciju apjomu, jo tādējādi tiks izveidots ievērojami mazāk pārskatu, ko var apstrādāt paralēli.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="c7bb6-125">Laukā Noklusējuma debitors var atlasiet debitora kontu, ko lietot pārdošanas procesā debitoriem.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  


