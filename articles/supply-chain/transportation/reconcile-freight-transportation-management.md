---
title: "Saskaņot kravu transportēšanas pārvaldībā"
description: "Šajā rakstā ir izklāstīts kravas saskaņošanas process."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0e9dd669ff08c02a8bbb1f83e19dfa62298f317b
ms.contentlocale: lv-lv
ms.lasthandoff: 07/18/2017

---

# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="515f3-103">Saskaņot kravu transportēšanas pārvaldībā</span><span class="sxs-lookup"><span data-stu-id="515f3-103">Reconcile freight in transportation management</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="515f3-104">Šajā rakstā ir izklāstīts kravas saskaņošanas process.</span><span class="sxs-lookup"><span data-stu-id="515f3-104">This article describes the freight reconciliation process.</span></span>

<span data-ttu-id="515f3-105">Kravas saskaņošanu var izpildīt manuāli vai to var iestatīt automātiskai izpildīšanai.</span><span class="sxs-lookup"><span data-stu-id="515f3-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="515f3-106">Lai izmantotu automātisko kravas saskaņošanu, ir jāiestata audita šablons, kur varat definēt kritērijus, kuri nosaka, kādi kravas rēķini tiek saskaņoti automātiski.</span><span class="sxs-lookup"><span data-stu-id="515f3-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="515f3-107">Kravas saskaņošanas process</span><span class="sxs-lookup"><span data-stu-id="515f3-107">The freight reconciliation process</span></span>
<span data-ttu-id="515f3-108">Kravas pārvadāšanas likmes aprēķina likmes noteikšanas programma, kas ir saistīta ar attiecīgo sūtījumu pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="515f3-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="515f3-109">Ja krava ir apstiprināta, tiek ģenerēta kravas pavadzīme un uz to tiek pārsūtītas kravas pārvadāšanas likmes.</span><span class="sxs-lookup"><span data-stu-id="515f3-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="515f3-110">Kravas pārvadāšanas likmes tiek iedalītas kā papildmaksas attiecīgajam pirmdokumentam (pirkšanas pasūtījumam, pārdošanas pasūtījumam un/vai pārsūtīšanas pasūtījumam) atkarībā no regulārajam norēķinu procesam izmantotajiem iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="515f3-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="515f3-111">Kravas saskaņošanas process (kas tiek saukts arī par salīdzināšanas procesu) var sākties, tiklīdz tiek saņemts kravas rēķins no sūtījumu pārvadātāja.</span><span class="sxs-lookup"><span data-stu-id="515f3-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="515f3-112">Rēķinu var saņemt elektroniski vai papīra formātā.</span><span class="sxs-lookup"><span data-stu-id="515f3-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="515f3-113">Ja rēķins tiek saņemts papīra formātā, varat ģenerēt elektronisku rēķinu, izmantojot kravas pavadzīmi kā veidni.</span><span class="sxs-lookup"><span data-stu-id="515f3-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="515f3-114">[![Kravas saskaņošanas process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="515f3-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="515f3-115">Manuāla saskaņošana</span><span class="sxs-lookup"><span data-stu-id="515f3-115">Manual reconciliation</span></span>
<span data-ttu-id="515f3-116">Ja kravu saskaņojat manuāli, tad rēķinā iekļautajai kravai katra rēķina rinda ir jāsalīdzina ar kravas pavadzīmes rindu vai rindām.</span><span class="sxs-lookup"><span data-stu-id="515f3-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="515f3-117">Šo salīdzināšanu jūs veicat lapā **Kravas pavadzīmes un rēķina salīdzināšana**.</span><span class="sxs-lookup"><span data-stu-id="515f3-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="515f3-118">Ja rēķina rindas summa neatbilst kravas pavadzīmes summai, jums ir jāatlasa saskaņošanas iemesls šai atšķirībai.</span><span class="sxs-lookup"><span data-stu-id="515f3-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="515f3-119">Ja saskaņošanai pastāv vairāki iemesli, neatbilstošo summu varat sadalīt starp tiem.</span><span class="sxs-lookup"><span data-stu-id="515f3-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="515f3-120">Saskaņošanas iemesls nosaka, kā šīs starpību summas tiek grāmatotas virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="515f3-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="515f3-121">Kad ir izpildīta visa rēķina summas saskaņošana, tā tiek iesniegta apstiprināšanai, un pēc tam žurnāls tiek grāmatots.</span><span class="sxs-lookup"><span data-stu-id="515f3-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="515f3-122">Nākamajā attēlā ir parādīts, kā ģenerēt kravas rēķinu un izpildīt kravas saskaņošanu programmatūrā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="515f3-122">The following illustration shows how to generate a freight invoice and do freight reconciliation in Microsoft Dynamics 365 for Finance and Operations.</span></span> 
<span data-ttu-id="515f3-123">[![Kravas saskaņošanas uzdevumi programmatūrā Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="515f3-123">[![Freight reconcilation tasks in Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="515f3-124">Automātiska saskaņošana</span><span class="sxs-lookup"><span data-stu-id="515f3-124">Automatic reconciliation</span></span>
<span data-ttu-id="515f3-125">Lai izmantotu automātisko saskaņošanu, jums ir jānorāda saskaņošanas grafiks, kā arī izmantojamie rēķini un sūtījumu pārvadātāji.</span><span class="sxs-lookup"><span data-stu-id="515f3-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="515f3-126">Rēķinu rindu un kravu pavadzīmju salīdzināšana tiek veikta atbilstoši audita šablona iestatījumiem un kravas pavadzīmes tipam.</span><span class="sxs-lookup"><span data-stu-id="515f3-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="515f3-127">Kad esat izpildījis automātisko saskaņošanu, jums ir jāapstrādā visi rēķini, kurus sistēma nespēj saskaņot.</span><span class="sxs-lookup"><span data-stu-id="515f3-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="515f3-128">Pēc tam jums šie rēķini ir jāpārstrādā manuāli, pirms visus rēķinus varat grāmatot maksājumam.</span><span class="sxs-lookup"><span data-stu-id="515f3-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>




