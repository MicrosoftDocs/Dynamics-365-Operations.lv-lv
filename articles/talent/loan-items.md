---
title: "Darbiniekiem aizdotu krājumu pārvaldīšana"
description: "Patapinājuma priekšmeti ir ieraksti, kas vadītājiem palīdz izsekot fiziskos priekšmetus, kurus jūsu uzņēmums patapina saviem darbiniekiem."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fe8d8812aaa78c7b5558615f586940488f2dc1b2
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="manage-items-lent-to-workers"></a><span data-ttu-id="8e497-103">Darbiniekiem aizdotu krājumu pārvaldīšana</span><span class="sxs-lookup"><span data-stu-id="8e497-103">Manage items lent to workers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8e497-104">Patapinājuma priekšmeti ir ieraksti, kas vadītājiem palīdz izsekot fiziskos priekšmetus, kurus jūsu uzņēmums patapina saviem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="8e497-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="8e497-105">Tālāk ir uzskaitīti tādu priekšmetu piemēri, ko uzņēmums var aizdot saviem darbiniekiem:</span><span class="sxs-lookup"><span data-stu-id="8e497-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="8e497-106">Mobilie tālruņi</span><span class="sxs-lookup"><span data-stu-id="8e497-106">Mobile telephones</span></span>
-   <span data-ttu-id="8e497-107">Automašīnas</span><span class="sxs-lookup"><span data-stu-id="8e497-107">Automobiles</span></span>
-   <span data-ttu-id="8e497-108">Datortehnika</span><span class="sxs-lookup"><span data-stu-id="8e497-108">Computer equipment</span></span>

<span data-ttu-id="8e497-109">Katram fiziskajam priekšmetam ir nepieciešams atbilstošs patapinājuma priekšmets.</span><span class="sxs-lookup"><span data-stu-id="8e497-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="8e497-110">Katrā patapinājuma priekšmeta ierakstā ir jāapraksta, kas tiek aizdots, kurš ir atbildīgs par patapinājumu un cik dienas šo priekšmetu darbiniekam var patapināt.</span><span class="sxs-lookup"><span data-stu-id="8e497-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="8e497-111">Vienlaikus varat izveidot vairākus patapinājuma priekšmetus, piemēram, tādiem priekšmetiem kā atslēgas, piekļuves kartes vai formastērpi.</span><span class="sxs-lookup"><span data-stu-id="8e497-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="8e497-112">Kad priekšmets tiek patapināts, ievadiet datumu, kad tas ticis patapināts, un plānoto atpakaļatdošanas datumu.</span><span class="sxs-lookup"><span data-stu-id="8e497-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="8e497-113">Kad priekšmets tiek atdots atpakaļ, ievadiet faktisko atpakaļatdošanas datumu.</span><span class="sxs-lookup"><span data-stu-id="8e497-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="8e497-114">Izmantojot darbvietu Darbinieku patstāvīgi izmantojamais pakalpojums, darbinieki var skatīt patapinājuma priekšmetu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="8e497-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="8e497-115">Viņi var arī rediģēt esošos ierakstus vai ievadīt jaunus patapinājuma priekšmetus, ja viņi ir saņēmuši papildu fiziskos priekšmetus.</span><span class="sxs-lookup"><span data-stu-id="8e497-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="8e497-116">Darbplūsmu var iestatīt tā, lai jauno vai esošo patapinājuma priekšmetu izmaiņas novirzītu uz apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="8e497-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="8e497-117">Vadītāji var skatīt patapinājuma priekšmetus savām tiešajām atskaitēm.</span><span class="sxs-lookup"><span data-stu-id="8e497-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="8e497-118">Tāpat viņiem var piešķirt atļauju pievienot jaunus patapinājuma priekšmetus savu darbinieku vārdā.</span><span class="sxs-lookup"><span data-stu-id="8e497-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="8e497-119"> Ziņošana par nozaudētiem vai laikā neatdotiem patapinājuma priekšmetiem</span><span class="sxs-lookup"><span data-stu-id="8e497-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="8e497-120">Ja priekšmets ir bojāts vai netiek atdots laikā, ievadiet fiktīvu atdošanas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="8e497-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="8e497-121">Pēc tam dzēsiet priekšmetu vai paturiet to apskatā un mainiet aprakstu, lai norādītu, ka priekšmets nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="8e497-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="8e497-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="8e497-122">Additional resources</span></span>
--------

[<span data-ttu-id="8e497-123">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="8e497-123">Human resources</span></span>](index.md)




