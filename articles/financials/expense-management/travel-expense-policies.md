---
title: "Izdevumu politiku definēšana"
description: "Varat definēt izdevumu politikas, kuras jūsu darbiniekiem ir jāievēro, kad viņi izdevumu pārskatus un komandējumu pieprasījumus ievada un iesniedz programmatūrā Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: b0f9a5ca275944aeb27798a2f3377356319589c7
ms.contentlocale: lv-lv
ms.lasthandoff: 01/17/2018

---

# <a name="expense-policies"></a><span data-ttu-id="ac0f9-103">Izdevumu politikas</span><span class="sxs-lookup"><span data-stu-id="ac0f9-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ac0f9-104">Varat definēt politikas, kuras jūsu darbiniekiem ir jāievēro, kad viņi ievada un iesniedz izdevumu pārskatus un komandējumu pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="ac0f9-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span> <span data-ttu-id="ac0f9-105">Izdevumu politikas ieviešana var palīdzēt efektīgi pārvaldīt izdevumus.</span><span class="sxs-lookup"><span data-stu-id="ac0f9-105">Implementing expense policies can help you manage expenses effectively.</span></span> 

<span data-ttu-id="ac0f9-106">Varat iestatīt, piemēram, politiku attiecībā uz viesnīcas izdevumiem Ņujorkā, kurā ir norādīts, ka izdevumi par vienu nakti nedrīkst pārsniegt 250 USD.</span><span class="sxs-lookup"><span data-stu-id="ac0f9-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span> <span data-ttu-id="ac0f9-107">Ja darbinieks iesniedz izdevumu pārskatu vai komandējuma pieprasījumu, kurā maksa par istabu ir lielāka par šo summu, tad sistēma šo darbinieku informē, ka ir pārsniegta politikā norādītā šādu izdevumu summa.</span><span class="sxs-lookup"><span data-stu-id="ac0f9-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="ac0f9-108">Kad definējat politiku, varat konfigurēt ziņojumu, ko parādīt darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="ac0f9-108">You can configure the message that the worker will receive when you define the policy.</span></span> 

<span data-ttu-id="ac0f9-109">Varat definēt trīs tipu politikas.</span><span class="sxs-lookup"><span data-stu-id="ac0f9-109">You can define three types of policies:</span></span> 

 - <span data-ttu-id="ac0f9-110">Brīdinājums — ļauj darbiniekam iesniegt izdevumu pārskatu vai komandējuma pieprasījumu, bet izdevumi tiks atzīmēti visiem apstiprinātājiem un</span><span class="sxs-lookup"><span data-stu-id="ac0f9-110">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>  
 <span data-ttu-id="ac0f9-111">vēlākai ziņošanai.</span><span class="sxs-lookup"><span data-stu-id="ac0f9-111">for later reporting.</span></span> 
 - <span data-ttu-id="ac0f9-112">Kļūda — pirms izdevumu pārskata vai komandējuma pieprasījuma iesniegšanas liek darbiniekam pārskatīt izdevumus, lai tie atbilstu politikai.</span><span class="sxs-lookup"><span data-stu-id="ac0f9-112">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span> 
 - <span data-ttu-id="ac0f9-113">Pamatojums — pirms izdevumu pārskata vai komandējuma pieprasījuma iesniegšanas darbiniekam vai vadītājam liek ievadīt politikas summas pārsniegšanas pamatojumu.</span><span class="sxs-lookup"><span data-stu-id="ac0f9-113">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span> 

<span data-ttu-id="ac0f9-114">Varat iestatīt arī datumu diapazonu, kuram šīs izdevumu politikas ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="ac0f9-114">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="ac0f9-115">Lidojumiem, piemēram, starp Dāniju un Ņujorku, brīvdienu ceļojumu sezonā lidojumu maksa var būt dārga.</span><span class="sxs-lookup"><span data-stu-id="ac0f9-115">For example, airline fares for flights between Denmark and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="ac0f9-116">Varat definēt lidojumu izdevumu kārtulu, kas maksu par lidojumiem uz Ņujorku ierobežo līdz 5000 DKK, kā arī varat norādīt, ka šī kārtula ir spēkā no 15. marta līdz 15. septembrim.</span><span class="sxs-lookup"><span data-stu-id="ac0f9-116">You can define a flight expense rule that restricts the cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and September 15.</span></span> 

