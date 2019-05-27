---
title: Transakcijas aizturēšana vai atsākšana pārdošanas punktā (POS)
description: Šajā tēmā ir paskaidrots, kā lietotāji var aizturēt notiekošas transakcijas un tās atsākt vēlāk vai citā kases sistēmā, izmantojot Microsoft Dynamics 365 for Retail.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ffb04609318c7de4b9ef729a8e03a7f9395806b8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569548"
---
# <a name="suspend-and-resume-transactions-in-the-point-of-sale-pos"></a><span data-ttu-id="cba81-103">Transakciju aizturēšana vai atsākšana pārdošanas punktā (POS)</span><span class="sxs-lookup"><span data-stu-id="cba81-103">Suspend and resume transactions in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="cba81-104">Pārdošanas punkta (POS) lietotāji var aizturēt notiekošas transakcijas un pēc tam atsākt tās vēlāk vai citā reģistrā.</span><span class="sxs-lookup"><span data-stu-id="cba81-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="cba81-105">Transakcijas bieži tiek aizturētas, lai ātri atbrīvotu reģistru citam uzdevumam, nezaudējot pašreizējās transakcijas progresu.</span><span class="sxs-lookup"><span data-stu-id="cba81-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="cba81-106">Piemēram, veikala speciālists sāk apstrādāt debitora transakciju mobilajā ierīcē, taču apstrāde ir jāpabeidz reģistrā, kam ir naudas kaste.</span><span class="sxs-lookup"><span data-stu-id="cba81-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="cba81-107">Šajā gadījumā veikala speciālists var aizturēt transakciju mobilajā ierīcē un pēc tam atsaukt to un atsākt reģistrā.</span><span class="sxs-lookup"><span data-stu-id="cba81-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="cba81-108">Aizturēšanas un atsākšanas funkcijas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="cba81-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="cba81-109">POS operācijas</span><span class="sxs-lookup"><span data-stu-id="cba81-109">POS operations</span></span>

<span data-ttu-id="cba81-110">Divas [POS operācijas](pos-operations.md) ļauj POS atbalstīt aizturēšanas un atsākšanas scenārijus.</span><span class="sxs-lookup"><span data-stu-id="cba81-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="cba81-111">Varat piešķirt šīs operācijas [pogu režģiem](pos-screen-layouts.md) transakciju lapā vai sveiciena lapā.</span><span class="sxs-lookup"><span data-stu-id="cba81-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="cba81-112">503: Aizturēt transakciju</span><span class="sxs-lookup"><span data-stu-id="cba81-112">503: Suspend transaction</span></span>
- <span data-ttu-id="cba81-113">504: Atsaukt transakciju</span><span class="sxs-lookup"><span data-stu-id="cba81-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="cba81-114">Kvīts veidne</span><span class="sxs-lookup"><span data-stu-id="cba81-114">Receipt template</span></span>

<span data-ttu-id="cba81-115">POS var konfigurēt, lai ģenerētu drukātās pavadzīmes, kad transakcija ir aizturēta.</span><span class="sxs-lookup"><span data-stu-id="cba81-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="cba81-116">Šo pavadzīmi var izmantot, lai vēlāk ātri noteiktu un atsauktu transakciju.</span><span class="sxs-lookup"><span data-stu-id="cba81-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="cba81-117">Lai iespējotu kvīts drukāšanau POS, veikala kvīts profilam ir jāpievieno kvīts formāts **Aizturēta transakcija**.</span><span class="sxs-lookup"><span data-stu-id="cba81-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="cba81-118">Kvīts formātu var izveidot tā, lai tajā tiktu vai netiktu iekļauti noteikti transakcijas dati.</span><span class="sxs-lookup"><span data-stu-id="cba81-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="cba81-119">Piemēram, formāts var iekļaut svītrkodu skenēšanas nodrošināšanai.</span><span class="sxs-lookup"><span data-stu-id="cba81-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="cba81-120">Kvīšu numerācija</span><span class="sxs-lookup"><span data-stu-id="cba81-120">Receipt numbering</span></span>

<span data-ttu-id="cba81-121">Tāpat kā citiem POS transakciju tipiem, kuri ģenerē drukātas kvītis, veikala funkcionalitātes profila sadaļā **Kvīšu numerācija** varat definēt numerāciju aizturētajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="cba81-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="cba81-122">Anulēt, noslēdzot maiņu</span><span class="sxs-lookup"><span data-stu-id="cba81-122">Void when closing shift</span></span>

<span data-ttu-id="cba81-123">Varat izmantot opciju **Anulēt, noslēdzot maiņu**, lai pieprasītu, ka lietotāji pabeidz vai anulē jebkuru aizturētu transakciju pirms savas maiņas slēgšanas.</span><span class="sxs-lookup"><span data-stu-id="cba81-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="cba81-124">Operācijas **Maiņas slēgšana** laikā, POS piedāvās lietotājiem skatīt vai anulēt visas nenokārtotās aizturētās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="cba81-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="cba81-125">Transakcijas aizturēšana un atsākšana</span><span class="sxs-lookup"><span data-stu-id="cba81-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="cba81-126">Transakcijas aizturēšana</span><span class="sxs-lookup"><span data-stu-id="cba81-126">Suspend a transaction</span></span>

<span data-ttu-id="cba81-127">Lietotāji, kuriem ir atbilstošas privilēģijas un kuru ekrāna izkārtojumā ir ietverta operācija **Transkacijas aizturēšana**, var aizturēt transakciju, lai to atsaukttu vēlāk vai citā reģistrā.</span><span class="sxs-lookup"><span data-stu-id="cba81-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="cba81-128">Transakcijas var aizturēt tikai tad, ja tajās **nav** tālāk norādīto tipu rindu:</span><span class="sxs-lookup"><span data-stu-id="cba81-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="cba81-129">Aktīvā maksājuma rindas</span><span class="sxs-lookup"><span data-stu-id="cba81-129">Active payment lines</span></span>
- <span data-ttu-id="cba81-130">Dāvanu kartes rindas (dāvanu kartes izsniegšana vai dāvanu kartes bilances papildināšana)</span><span class="sxs-lookup"><span data-stu-id="cba81-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="cba81-131">Aizturēta transakcija neietekmē pārdošanas informāciju vai krājumu pieejamības informāciju veikalā.</span><span class="sxs-lookup"><span data-stu-id="cba81-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="cba81-132">Aizturētas transakcijas atsākšana</span><span class="sxs-lookup"><span data-stu-id="cba81-132">Resume a suspended transaction</span></span>

<span data-ttu-id="cba81-133">Aizturētās transakcijas var atsaukt un atsākt vienā veikalā jebkurš lietotājs, kuram ir atbilstošas privilēģijas un kuram ir arī izkārtojums, kas ietver operāciju **Transakcijas atsākšana**.</span><span class="sxs-lookup"><span data-stu-id="cba81-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="cba81-134">Lai ātri un viegli atsauktu aizturētu transakciju, noskenējiet drukātās pavadzīmes svītrkodu, kamēr skatāt operācijas **Transakcijas atsākšana** transakciju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="cba81-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="cba81-135">Apsvērumi bezsaistes režīmā</span><span class="sxs-lookup"><span data-stu-id="cba81-135">Considerations for offline mode</span></span>

- <span data-ttu-id="cba81-136">Transakcijas, kas ir aizturētas, kamēr POS ir tiešsaistes režīmā, nevar atsākt bezsaistes režīmā, jo dati nav sinhronizēti ar bezsaistes datu bāzi.</span><span class="sxs-lookup"><span data-stu-id="cba81-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="cba81-137">Ja aizturat transakciju, kamēr POS ir bezsaistes režīmā, varat atsaukt to bezsaistes režīmā, ja ir zināms, ka POS nevienā brīdī pēc transakcijas aizturēšanas nav bijis pārslēgts atpakaļ tiešsaistes režīmā.</span><span class="sxs-lookup"><span data-stu-id="cba81-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="cba81-138">Pārslēdzot POS atpakaļ tiešsaistes režīmā, dati par aizturētajām transakcijām tiek pārvietoti uz tiešsaistes datu bāzi un noņemti no bezsaistes datu bāzes.</span><span class="sxs-lookup"><span data-stu-id="cba81-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="cba81-139">Tāpēc transakcijas var atsākt tikai tiešsaistes režīmā.</span><span class="sxs-lookup"><span data-stu-id="cba81-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="cba81-140">Ja pārslēgsiet POS atpakaļ bezsaistes režīmā, aizturētās transakcijas nevarēsiet atsākt, jo tās jau būs noņemtas no bezsaistes datu bāzes.</span><span class="sxs-lookup"><span data-stu-id="cba81-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="cba81-141">Aizturētas transakcijas anulēšana</span><span class="sxs-lookup"><span data-stu-id="cba81-141">Void a suspended transaction</span></span>

<span data-ttu-id="cba81-142">Aizturētās transakcijas varat anulēt, vai nu atsaucot transakciju un pēc tam veicot operāciju **Transakcijas anulēšana**, vai atlasot transakciju sarakstā **Transakcijas atsaukšana** un programmas joslā atlasot **Anulēt**.</span><span class="sxs-lookup"><span data-stu-id="cba81-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="cba81-143">Var arī konfigurēt veikalu tā, lai lietotājiem piedāvātu anulēt aizturētās transakcijas, kad lietotāji slēdz maiņu.</span><span class="sxs-lookup"><span data-stu-id="cba81-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>
