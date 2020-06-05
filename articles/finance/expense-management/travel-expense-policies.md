---
title: Izdevumu politiku definēšana
description: Varat definēt izdevumu politikas, kuras jūsu darbiniekiem ir jāievēro, kad viņi ievada un iesniedz izdevumu pārskatus un komandējumu pieprasījumus programmā Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389719"
---
# <a name="define-expense-policies"></a><span data-ttu-id="e9c26-103">Izdevumu politiku definēšana</span><span class="sxs-lookup"><span data-stu-id="e9c26-103">Define expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9c26-104">Varat definēt politikas, kuras jūsu darbiniekiem ir jāievēro, kad viņi ievada un iesniedz izdevumu pārskatus un komandējumu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="e9c26-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="e9c26-105">Izdevumu politikas ieviešana var palīdzēt efektīgi pārvaldīt izdevumus.</span><span class="sxs-lookup"><span data-stu-id="e9c26-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="e9c26-106">Varat iestatīt, piemēram, politiku attiecībā uz viesnīcas izdevumiem Ņujorkā, kurā ir norādīts, ka izdevumi par vienu nakti nedrīkst pārsniegt 250 USD.</span><span class="sxs-lookup"><span data-stu-id="e9c26-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="e9c26-107">Ja darbinieks iesniedz izdevumu pārskatu vai komandējuma pieprasījumu, kurā maksa par naktsmītni ir lielāka par šo summu, sistēma informēs</span><span class="sxs-lookup"><span data-stu-id="e9c26-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="e9c26-108">darbinieku par to, ka tika pārsniegta izdevumu politikas summa.</span><span class="sxs-lookup"><span data-stu-id="e9c26-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="e9c26-109">Varat konfigurēt ziņojumu, ko parādīt darbiniekam,</span><span class="sxs-lookup"><span data-stu-id="e9c26-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="e9c26-110">kad definējat politiku.</span><span class="sxs-lookup"><span data-stu-id="e9c26-110">define the policy.</span></span>      
        
<span data-ttu-id="e9c26-111">Varat definēt trīs tipu politikas.</span><span class="sxs-lookup"><span data-stu-id="e9c26-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="e9c26-112">Brīdinājums — ļauj darbiniekam iesniegt izdevumu pārskatu vai komandējuma pieprasījumu, bet izdevumi tiks atzīmēti visiem apstiprinātājiem un</span><span class="sxs-lookup"><span data-stu-id="e9c26-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="e9c26-113">vēlākai ziņošanai.</span><span class="sxs-lookup"><span data-stu-id="e9c26-113">for later reporting.</span></span>        

- <span data-ttu-id="e9c26-114">Kļūda — pirms izdevumu pārskata vai komandējuma pieprasījuma iesniegšanas liek darbiniekam pārskatīt izdevumus, lai tie atbilstu politikai.</span><span class="sxs-lookup"><span data-stu-id="e9c26-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="e9c26-115">Pamatojums — pirms izdevumu pārskata vai komandējuma pieprasījuma iesniegšanas darbiniekam vai vadītājam liek ievadīt politikas summas pārsniegšanas pamatojumu.</span><span class="sxs-lookup"><span data-stu-id="e9c26-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="e9c26-116">Politiku padomi</span><span class="sxs-lookup"><span data-stu-id="e9c26-116">Policy tips</span></span>
<span data-ttu-id="e9c26-117">Tālāk ir minēti daži ieteikumi, kas var jums palīdzēt, veidojot jaunas politikas izmaksu pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="e9c26-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="e9c26-118">Politikām ir spēkā stāšanās datums, un tās nestāsies spēkā, ja politika tiek izveidota ar datumu pēc datuma, kad izdevumi radušies.</span><span class="sxs-lookup"><span data-stu-id="e9c26-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="e9c26-119">Piemēram, ja šodien veidojat jaunu politiku, lai ieviestu maksimālos ēdināšanas izdevumus 50 ASV dolāru, apmērā, visi esošie izdevumi, kas ievadīti kopš vakardienas, netiks pārbaudīti attiecībā pret šo politiku.</span><span class="sxs-lookup"><span data-stu-id="e9c26-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="e9c26-120">Veidojot politiku izdevumu kategorijai, kas var būt detalizēta, apsveriet iespēju pievienot izdevumu rindas tipa nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="e9c26-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="e9c26-121">Dažas politikas, piemēram, kvīts pieprasīšana, var būt neatbilstošas detalizētām rindām, un tās ieteicams piemērot tikai virsraksta rindai vai nedetalizētai rindai.</span><span class="sxs-lookup"><span data-stu-id="e9c26-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="e9c26-122">Izdevumu pārvaldības politikas tiek novērtētas attiecībā pret noklusējuma avota elementu.</span><span class="sxs-lookup"><span data-stu-id="e9c26-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="e9c26-123">Starpuzņēmumu scenārijos varat iestatīt politiku, kas ir jāizvērtē, salīdzinot ar mērķa elementu (piesaistīšanas juridiskā persona).</span><span class="sxs-lookup"><span data-stu-id="e9c26-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="e9c26-124">Lai palaistu ar mērķa elementu salīdzināmu politiku, **Līdzekļu pārvaldības** darbvietā ieslēdziet līdzekli "novērtēt izdevumu politiku salīdzinājumā ar piesaistīšanas juridisko personu".</span><span class="sxs-lookup"><span data-stu-id="e9c26-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="e9c26-125">Politiku novērtēšanas laiks</span><span class="sxs-lookup"><span data-stu-id="e9c26-125">When to evaluate policies</span></span>

<span data-ttu-id="e9c26-126">Izdevumu pārvaldības parametros ir iespēja novērtēt izdevumu pārvaldības politikas, kad rinda tiek saglabāta vai kad tiek iesniegts izdevumu pārskats.</span><span class="sxs-lookup"><span data-stu-id="e9c26-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="e9c26-127">Ja izvēlaties veikt novērtēšanu, kad rinda tiek saglabāta, tas nodrošina to, ka lietotājam agrāk tiek parādīts, kas jādara, lai pabeigtu izdevumu pārskatu uzreiz.</span><span class="sxs-lookup"><span data-stu-id="e9c26-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="e9c26-128">Pretējā gadījumā varat aizkavēt politikas novērtēšanu un ietaupīt laiku, ja validācija tiek veikta beigās, kad notiek iesniegšana darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="e9c26-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
