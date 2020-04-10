---
title: Darbplūsmu iestatīšana izdevumu pārvaldībai
description: Varat iestatīt darbplūsmas procesu, kas tiek izmantots komandējumu un izdevumu dokumentu pārskatīšanai un apstiprināšanai.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdd4d69cb86da12e4a265f89c021c238d00cad08
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153998"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="78c92-103">Darbplūsmu iestatīšana izdevumu pārvaldībai</span><span class="sxs-lookup"><span data-stu-id="78c92-103">Set up workflows for Expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78c92-104">Varat iestatīt darbplūsmas procesu, kas tiek izmantots komandējumu un izdevumu dokumentu pārskatīšanai un apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="78c92-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="78c92-105">Dokumenti, kuriem var definēt darbplūsmas, ietver izdevumu pārskatus, komandējumu pieprasījumus un skaidras naudas avansa pieprasījumus.</span><span class="sxs-lookup"><span data-stu-id="78c92-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="78c92-106">Darbplūsma attēlo biznesa procesu.</span><span class="sxs-lookup"><span data-stu-id="78c92-106">A workflow represents a business process.</span></span> <span data-ttu-id="78c92-107">Izmantojot darbplūsmu, tiek noteikta dokumenta plūsma caur sistēmu un norādīts, kuram ir jāpabeidz uzdevums vai jāapstiprina dokuments.</span><span class="sxs-lookup"><span data-stu-id="78c92-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="78c92-108">Darbplūsmas sistēmas lietošanai organizācijā ir vairākas priekšrocības.</span><span class="sxs-lookup"><span data-stu-id="78c92-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="78c92-109">**Saskaņoti procesi** — varat definēt noteiktu dokumentiem, piemēram, pirkšanas pieprasījumu un izdevumu pārskatu, apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="78c92-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="78c92-110">Izmantojot darbplūsmas sistēmu, varat nodrošināt saskaņotu un efektīvu dokumentu apstrādes un apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="78c92-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="78c92-111">Procesa pārskatāmība — varat sekot līdzi noteiktas darbplūsmas instances statusa, vēsturiskajiem un veiktspējas rādītājiem.</span><span class="sxs-lookup"><span data-stu-id="78c92-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="78c92-112">Tādējādi varat noteikt, vai ir jāveic darbplūsmas izmaiņas, lai uzlabotu efektivitāti.</span><span class="sxs-lookup"><span data-stu-id="78c92-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="78c92-113">Centralizēts darbu saraksts — lietotāji var apskatīt centralizētu darbu sarakstu, lai uzzinātu, kuri darbplūsmas uzdevumi un apstiprinājumi ir viņiem piešķirti.</span><span class="sxs-lookup"><span data-stu-id="78c92-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="78c92-114">**Izveidojamo darbplūsmu veidi**</span><span class="sxs-lookup"><span data-stu-id="78c92-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="78c92-115">Nākamajā tabulā ir uzskaitīti darbplūsmu tipi, ko varat izveidot sadaļā **Izdevumi**.</span><span class="sxs-lookup"><span data-stu-id="78c92-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="78c92-116"><strong>Tips</strong></span><span class="sxs-lookup"><span data-stu-id="78c92-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="78c92-117"><strong>Šī tipa lietošanas nolūks</strong></span><span class="sxs-lookup"><span data-stu-id="78c92-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="78c92-118"><strong>Izdevumu pārskats</strong></span><span class="sxs-lookup"><span data-stu-id="78c92-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="78c92-119">Izveidot apstiprinājuma darbplūsmas izdevumu pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="78c92-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="78c92-120"><strong>Izdevumu pārskata automātiska grāmatošana</strong></span><span class="sxs-lookup"><span data-stu-id="78c92-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="78c92-121">Izveidot automātiskas grāmatošanas darbplūsmas izdevumu pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="78c92-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="78c92-122"><strong>Izdevumu dokumenta rinda</strong></span><span class="sxs-lookup"><span data-stu-id="78c92-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="78c92-123">Izveidot apstiprinājuma darbplūsmas izdevumu pārskatu rindu vienumiem.</span><span class="sxs-lookup"><span data-stu-id="78c92-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="78c92-124"><strong>Izdevumu rindas krājuma automātiskā grāmatošana</strong></span><span class="sxs-lookup"><span data-stu-id="78c92-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="78c92-125">Izveidot automātiskas grāmatošanas darbplūsmas izdevumu pārskatu rindu vienumiem.</span><span class="sxs-lookup"><span data-stu-id="78c92-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="78c92-126"><strong>Komandējuma pieprasījums</strong></span><span class="sxs-lookup"><span data-stu-id="78c92-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="78c92-127">Izveidot apstiprināšanas darbplūsmas komandējumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="78c92-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="78c92-128"><strong>Avansa pieprasījumi</strong></span><span class="sxs-lookup"><span data-stu-id="78c92-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="78c92-129">Izveidot apstiprināšanas darbplūsmas skaidras naudas avansa pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="78c92-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="78c92-130"><strong>PVN nodokļu atgūšana</strong></span><span class="sxs-lookup"><span data-stu-id="78c92-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="78c92-131">Izveidot apstiprināšanas darbplūsmas pievienotās vērtības nodokļa (PVN) atgūšanai.</span><span class="sxs-lookup"><span data-stu-id="78c92-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

