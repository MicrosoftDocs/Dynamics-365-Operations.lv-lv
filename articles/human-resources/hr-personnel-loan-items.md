---
title: Nodarbinātajiem aizdotu priekšmetu pārvaldīšana
description: Patapinājuma priekšmeti ir ieraksti, kas vadītājiem palīdz izsekot fiziskos priekšmetus, kurus jūsu uzņēmums patapina saviem darbiniekiem.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 5915df388da7ce8b90cdcb0e859268c00003110c
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429317"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="d67cf-103">Nodarbinātajiem aizdotu priekšmetu pārvaldīšana</span><span class="sxs-lookup"><span data-stu-id="d67cf-103">Manage items that are lent to workers</span></span>

<span data-ttu-id="d67cf-104">Patapinājuma priekšmeti ir ieraksti, kas vadītājiem palīdz izsekot fiziskos priekšmetus, kurus jūsu uzņēmums patapina saviem darbiniekiem.</span><span class="sxs-lookup"><span data-stu-id="d67cf-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="d67cf-105">Tālāk ir uzskaitīti tādu priekšmetu piemēri, ko uzņēmums var aizdot saviem darbiniekiem:</span><span class="sxs-lookup"><span data-stu-id="d67cf-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="d67cf-106">Mobilie tālruņi</span><span class="sxs-lookup"><span data-stu-id="d67cf-106">Mobile telephones</span></span>
-   <span data-ttu-id="d67cf-107">Automašīnas</span><span class="sxs-lookup"><span data-stu-id="d67cf-107">Automobiles</span></span>
-   <span data-ttu-id="d67cf-108">Datortehnika</span><span class="sxs-lookup"><span data-stu-id="d67cf-108">Computer equipment</span></span>

<span data-ttu-id="d67cf-109">Katram fiziskajam priekšmetam ir nepieciešams atbilstošs patapinājuma priekšmets.</span><span class="sxs-lookup"><span data-stu-id="d67cf-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="d67cf-110">Katrā patapinājuma priekšmeta ierakstā ir jāapraksta, kas tiek aizdots, kurš ir atbildīgs par patapinājumu un cik dienas šo priekšmetu darbiniekam var patapināt.</span><span class="sxs-lookup"><span data-stu-id="d67cf-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="d67cf-111">Vienlaikus varat izveidot vairākus patapinājuma priekšmetus, piemēram, tādiem priekšmetiem kā atslēgas, piekļuves kartes vai formastērpi.</span><span class="sxs-lookup"><span data-stu-id="d67cf-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="d67cf-112">Kad priekšmets tiek patapināts, ievadiet datumu, kad tas ticis patapināts, un plānoto atpakaļatdošanas datumu.</span><span class="sxs-lookup"><span data-stu-id="d67cf-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="d67cf-113">Kad priekšmets tiek atdots atpakaļ, ievadiet faktisko atpakaļatdošanas datumu.</span><span class="sxs-lookup"><span data-stu-id="d67cf-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="d67cf-114">Izmantojot darbvietu Darbinieku patstāvīgi izmantojamais pakalpojums, darbinieki var skatīt patapinājuma priekšmetu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="d67cf-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="d67cf-115">Viņi var arī rediģēt esošos ierakstus vai ievadīt jaunus patapinājuma priekšmetus, ja viņi ir saņēmuši papildu fiziskos priekšmetus.</span><span class="sxs-lookup"><span data-stu-id="d67cf-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="d67cf-116">Darbplūsmu var iestatīt tā, lai jauno vai esošo patapinājuma priekšmetu izmaiņas novirzītu uz apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="d67cf-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="d67cf-117">Vadītāji var skatīt patapinājuma priekšmetus savām tiešajām atskaitēm.</span><span class="sxs-lookup"><span data-stu-id="d67cf-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="d67cf-118">Tāpat viņiem var piešķirt atļauju pievienot jaunus patapinājuma priekšmetus savu darbinieku vārdā.</span><span class="sxs-lookup"><span data-stu-id="d67cf-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="d67cf-119"> Ziņošana par nozaudētiem vai laikā neatdotiem patapinājuma priekšmetiem</span><span class="sxs-lookup"><span data-stu-id="d67cf-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="d67cf-120">Ja priekšmets ir bojāts vai netiek atdots laikā, ievadiet fiktīvu atdošanas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d67cf-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="d67cf-121">Pēc tam dzēsiet priekšmetu vai paturiet to apskatā un mainiet aprakstu, lai norādītu, ka priekšmets nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="d67cf-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="d67cf-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d67cf-122">Additional resources</span></span>
--------

[<span data-ttu-id="d67cf-123">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="d67cf-123">Human resources</span></span>](index.md)



