---
title: "Izdevumu politiku definēšana"
description: "Varat definēt izdevumu politikas, kas ir jāievēro jūsu darbiniekiem, kad viņi ievada un iesniedz izdevumu pārskatus un komandējumu pieprasījumus programmatūrā Microsoft Dynamics 365 for Finance and Operations."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 04eaff110fea021ddee32be650be540894eb703b
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---

# <a name="expense-policies"></a><span data-ttu-id="0c845-103">Izdevumu ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="0c845-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c845-104">Varat definēt politikas, kuras jūsu darbiniekiem ir jāievēro, kad viņi ievada un iesniedz izdevumu pārskatus un komandējumu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="0c845-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="0c845-105">Izdevumu politikas ieviešana var palīdzēt efektīgi pārvaldīt izdevumus.</span><span class="sxs-lookup"><span data-stu-id="0c845-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="0c845-106">Varat iestatīt, piemēram, politiku attiecībā uz viesnīcas izdevumiem Ņujorkā, kurā ir norādīts, ka izdevumi par vienu nakti nedrīkst pārsniegt 250 USD.</span><span class="sxs-lookup"><span data-stu-id="0c845-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="0c845-107">Ja darbinieks iesniedz izdevumu pārskatu vai komandējuma pieprasījumu, kurā maksa par naktsmītni ir lielāka par šo summu, sistēma informēs</span><span class="sxs-lookup"><span data-stu-id="0c845-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="0c845-108">darbinieku par to, ka tika pārsniegta izdevumu politikas summa.</span><span class="sxs-lookup"><span data-stu-id="0c845-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="0c845-109">Varat konfigurēt ziņojumu, ko parādīt darbiniekam,</span><span class="sxs-lookup"><span data-stu-id="0c845-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="0c845-110">kad definējat politiku.</span><span class="sxs-lookup"><span data-stu-id="0c845-110">define the policy.</span></span>      
        
<span data-ttu-id="0c845-111">Varat definēt trīs tipu politikas.</span><span class="sxs-lookup"><span data-stu-id="0c845-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="0c845-112">Brīdinājums — ļauj darbiniekam iesniegt izdevumu pārskatu vai komandējuma pieprasījumu, bet izdevumi tiks atzīmēti visiem apstiprinātājiem un</span><span class="sxs-lookup"><span data-stu-id="0c845-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="0c845-113">vēlākai ziņošanai.</span><span class="sxs-lookup"><span data-stu-id="0c845-113">for later reporting.</span></span>        

- <span data-ttu-id="0c845-114">Kļūda — pirms izdevumu pārskata vai komandējuma pieprasījuma iesniegšanas liek darbiniekam pārskatīt izdevumus, lai tie atbilstu politikai.</span><span class="sxs-lookup"><span data-stu-id="0c845-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
  - <span data-ttu-id="0c845-115">Pamatojums — pirms izdevumu pārskata vai komandējuma pieprasījuma iesniegšanas darbiniekam vai vadītājam liek ievadīt politikas summas pārsniegšanas pamatojumu.</span><span class="sxs-lookup"><span data-stu-id="0c845-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        
 
  <span data-ttu-id="0c845-116">Varat iestatīt arī datumu diapazonu, kuram šīs izdevumu politikas ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="0c845-116">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="0c845-117">Piemēram, maksa par lidojumiem starp Dāniju</span><span class="sxs-lookup"><span data-stu-id="0c845-117">For example, airline fares for flights between Denmark</span></span>      
  <span data-ttu-id="0c845-118">un Ņujorku var būt dārgāka populārākajā brīvdienu ceļojumu sezonā.</span><span class="sxs-lookup"><span data-stu-id="0c845-118">and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="0c845-119">Varat definēt lidojuma izdevumu kārtulu, kas ierobežo</span><span class="sxs-lookup"><span data-stu-id="0c845-119">You can define a flight expense rule that restricts the</span></span>      
  <span data-ttu-id="0c845-120">maksu lidojumiem uz Ņujorku ierobežojumu DKK 5000, un varat norādīt, ka šī kārtula ir spēkā no 15. marta līdz</span><span class="sxs-lookup"><span data-stu-id="0c845-120">cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and</span></span>      
  <span data-ttu-id="0c845-121">15. septembrim.</span><span class="sxs-lookup"><span data-stu-id="0c845-121">September 15.</span></span>

