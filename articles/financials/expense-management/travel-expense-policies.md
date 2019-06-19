---
title: Izdevumu politiku definēšana
description: Varat definēt izdevumu politikas, kuras jūsu darbiniekiem ir jāievēro, kad viņi ievada un iesniedz izdevumu pārskatus un komandējumu pieprasījumus programmā Microsoft Dynamics 365 for Finance and Operations.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6923a4d5420cd768d1b0da24eab406033c17fd67
ms.sourcegitcommit: 06c8dc5bc4e1c41f68e1cda141d61529768be958
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/22/2019
ms.locfileid: "1594940"
---
# <a name="expense-policies"></a><span data-ttu-id="550d7-103">Izdevumu ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="550d7-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="550d7-104">Varat definēt politikas, kuras jūsu darbiniekiem ir jāievēro, kad viņi ievada un iesniedz izdevumu pārskatus un komandējumu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="550d7-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="550d7-105">Izdevumu politikas ieviešana var palīdzēt efektīgi pārvaldīt izdevumus.</span><span class="sxs-lookup"><span data-stu-id="550d7-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="550d7-106">Varat iestatīt, piemēram, politiku attiecībā uz viesnīcas izdevumiem Ņujorkā, kurā ir norādīts, ka izdevumi par vienu nakti nedrīkst pārsniegt 250 USD.</span><span class="sxs-lookup"><span data-stu-id="550d7-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="550d7-107">Ja darbinieks iesniedz izdevumu pārskatu vai komandējuma pieprasījumu, kurā maksa par naktsmītni ir lielāka par šo summu, sistēma informēs</span><span class="sxs-lookup"><span data-stu-id="550d7-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="550d7-108">darbinieku par to, ka tika pārsniegta izdevumu politikas summa.</span><span class="sxs-lookup"><span data-stu-id="550d7-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="550d7-109">Varat konfigurēt ziņojumu, ko parādīt darbiniekam,</span><span class="sxs-lookup"><span data-stu-id="550d7-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="550d7-110">kad definējat politiku.</span><span class="sxs-lookup"><span data-stu-id="550d7-110">define the policy.</span></span>      
        
<span data-ttu-id="550d7-111">Varat definēt trīs tipu politikas.</span><span class="sxs-lookup"><span data-stu-id="550d7-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="550d7-112">Brīdinājums — ļauj darbiniekam iesniegt izdevumu pārskatu vai komandējuma pieprasījumu, bet izdevumi tiks atzīmēti visiem apstiprinātājiem un</span><span class="sxs-lookup"><span data-stu-id="550d7-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="550d7-113">vēlākai ziņošanai.</span><span class="sxs-lookup"><span data-stu-id="550d7-113">for later reporting.</span></span>        

- <span data-ttu-id="550d7-114">Kļūda — pirms izdevumu pārskata vai komandējuma pieprasījuma iesniegšanas liek darbiniekam pārskatīt izdevumus, lai tie atbilstu politikai.</span><span class="sxs-lookup"><span data-stu-id="550d7-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="550d7-115">Pamatojums — pirms izdevumu pārskata vai komandējuma pieprasījuma iesniegšanas darbiniekam vai vadītājam liek ievadīt politikas summas pārsniegšanas pamatojumu.</span><span class="sxs-lookup"><span data-stu-id="550d7-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="550d7-116">Politiku padomi</span><span class="sxs-lookup"><span data-stu-id="550d7-116">Policy tips</span></span>
<span data-ttu-id="550d7-117">Tālāk ir minēti daži ieteikumi, kas var jums palīdzēt, izveidojot jaunas politikas izmaksu pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="550d7-117">Here are a few suggestions that can assist you whe creating new policies for expense management.</span></span> 
* <span data-ttu-id="550d7-118">Politikām ir spēkā stāšanās datums, un tās nestāsies spēkā, ja politika tiek izveidota ar datumu pēc datuma, kad izdevumi radušies.</span><span class="sxs-lookup"><span data-stu-id="550d7-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="550d7-119">Piemēram, ja šodien veidojat jaunu politiku, lai ieviestu maksimālos ēdināšanas izdevumus 50 ASV dolāru, apmērā, visi esošie izdevumi, kas ievadīti kopš vakardienas, netiks pārbaudīti attiecībā pret šo politiku.</span><span class="sxs-lookup"><span data-stu-id="550d7-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="550d7-120">Veidojot politiku izdevumu kategorijai, kas var būt detalizēta, apsveriet iespēju pievienot izdevumu rindas tipa nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="550d7-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="550d7-121">Dažas politikas, piemēram, kvīts pieprasīšana, var būt neatbilstošas detalizētām rindām, un tās ieteicams piemērot tikai virsraksta rindai vai nedetalizētai rindai.</span><span class="sxs-lookup"><span data-stu-id="550d7-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="550d7-122">Politiku novērtēšanas laiks</span><span class="sxs-lookup"><span data-stu-id="550d7-122">When to evaluate policies</span></span>

<span data-ttu-id="550d7-123">Izdevumu pārvaldības parametros ir iespēja novērtēt izdevumu pārvaldības politikas, kad rinda tiek saglabāta vai kad tiek iesniegts izdevumu pārskats.</span><span class="sxs-lookup"><span data-stu-id="550d7-123">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="550d7-124">Ja izvēlaties veikt novērtēšanu, kad rinda tiek saglabāta, tas nodrošina to, ka lietotājam agrāk tiek parādīts, kas jādara, lai pabeigtu izdevumu pārskatu uzreiz.</span><span class="sxs-lookup"><span data-stu-id="550d7-124">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="550d7-125">Pretējā gadījumā varat aizkavēt politikas novērtēšanu un ietaupīt laiku, ja validācija tiek veikta beigās, kad notiek iesniegšana darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="550d7-125">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
