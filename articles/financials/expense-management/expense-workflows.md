---
title: "Darbplūsmu iestatīšana izdevumiem"
description: "Varat iestatīt darbplūsmas procesu, kas tiek izmantots komandējumu un izdevumu dokumentu pārskatīšanai un apstiprināšanai."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: ef60fbab0f75ff70206d954e3d098a3866c467b6
ms.contentlocale: lv-lv
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="bcc25-103">Darbplūsmu iestatīšana izdevumiem</span><span class="sxs-lookup"><span data-stu-id="bcc25-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="bcc25-104"> Varat iestatīt darbplūsmas procesu, kas tiek izmantots komandējumu un izdevumu dokumentu pārskatīšanai un apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="bcc25-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="bcc25-105">Dokumenti, kuriem var definēt darbplūsmas, ietver izdevumu pārskatus, komandējumu pieprasījumus un skaidras naudas avansa pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="bcc25-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="bcc25-106">Darbplūsma attēlo biznesa procesu.</span><span class="sxs-lookup"><span data-stu-id="bcc25-106">A workflow represents a business process.</span></span> <span data-ttu-id="bcc25-107">Izmantojot darbplūsmu, tiek noteikta dokumenta plūsma caur sistēmu un norādīts, kuram ir jāpabeidz uzdevums vai jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="bcc25-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="bcc25-108">Darbplūsmas sistēmas lietošanai organizācijā ir vairākas priekšrocības.</span><span class="sxs-lookup"><span data-stu-id="bcc25-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="bcc25-109">**Saskaņoti procesi** — varat definēt noteiktu dokumentiem, piemēram, pirkšanas pieprasījumu un izdevumu pārskatu, apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="bcc25-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="bcc25-110">Izmantojot darbplūsmas sistēmu, varat nodrošināt saskaņotu un efektīvu dokumentu apstrādes un apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="bcc25-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="bcc25-111">Procesa pārskatāmība — varat sekot līdzi noteiktas darbplūsmas instances statusa, vēsturiskajiem un veiktspējas rādītājiem.</span><span class="sxs-lookup"><span data-stu-id="bcc25-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="bcc25-112">Tādējādi varat noteikt, vai ir jāveic darbplūsmas izmaiņas, lai uzlabotu efektivitāti.</span><span class="sxs-lookup"><span data-stu-id="bcc25-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="bcc25-113">Centralizēts darbu saraksts — lietotāji var apskatīt centralizētu darbu sarakstu, lai uzzinātu, kuri darbplūsmas uzdevumi un apstiprinājumi ir viņiem piešķirti.</span><span class="sxs-lookup"><span data-stu-id="bcc25-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="bcc25-114">**Izveidojamo darbplūsmu veidi**</span><span class="sxs-lookup"><span data-stu-id="bcc25-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="bcc25-115">Nākamajā tabulā ir uzskaitīti darbplūsmu tipi, ko varat izveidot sadaļā **Izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="bcc25-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="bcc25-116">**Tips**</span><span class="sxs-lookup"><span data-stu-id="bcc25-116">**Type**</span></span>                           | <span data-ttu-id="bcc25-117">**Šī tipa lietošanas nolūks**</span><span class="sxs-lookup"><span data-stu-id="bcc25-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="bcc25-118">**Izdevumu pārskats**</span><span class="sxs-lookup"><span data-stu-id="bcc25-118">**Expense report**</span></span>                 | <span data-ttu-id="bcc25-119">Izveidot apstiprinājuma darbplūsmas izdevumu pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="bcc25-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="bcc25-120">**Izdevumu pārskata automātiska grāmatošana**</span><span class="sxs-lookup"><span data-stu-id="bcc25-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="bcc25-121">Izveidot automātiskas grāmatošanas darbplūsmas izdevumu pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="bcc25-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="bcc25-122">**Izdevumu dokumenta rinda**</span><span class="sxs-lookup"><span data-stu-id="bcc25-122">**Expense line item**</span></span>              | <span data-ttu-id="bcc25-123">Izveidot apstiprinājuma darbplūsmas izdevumu pārskatu rindu vienumiem.</span><span class="sxs-lookup"><span data-stu-id="bcc25-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="bcc25-124">**Izdevumu rindas krājuma automātiskā grāmatošana**</span><span class="sxs-lookup"><span data-stu-id="bcc25-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="bcc25-125">Izveidot automātiskas grāmatošanas darbplūsmas izdevumu pārskatu rindu vienumiem.</span><span class="sxs-lookup"><span data-stu-id="bcc25-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="bcc25-126">**Komandējuma pieprasījums**</span><span class="sxs-lookup"><span data-stu-id="bcc25-126">**Travel requisition**</span></span>             | <span data-ttu-id="bcc25-127">Izveidot apstiprināšanas darbplūsmas komandējumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="bcc25-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="bcc25-128">**Avansa pieprasījumi**</span><span class="sxs-lookup"><span data-stu-id="bcc25-128">**Cash advance request**</span></span>           | <span data-ttu-id="bcc25-129">Izveidot apstiprināšanas darbplūsmas skaidras naudas avansa pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="bcc25-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="bcc25-130">**PVN nodokļu atgūšana**</span><span class="sxs-lookup"><span data-stu-id="bcc25-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="bcc25-131">Izveidot apstiprināšanas darbplūsmas pievienotās vērtības nodokļa (PVN) atgūšanai.</span><span class="sxs-lookup"><span data-stu-id="bcc25-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

