---
title: "Izdevumu darbplūsma"
description: "Šajā tēmā ir skaidrots, kā programmatūrā Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition varat izmantot darbplūsmu sistēmu, lai modulī Izdevumu pārvaldība iestatītu pārskatīšanas procesu izdevumu pārskatiem."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
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
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 25fc9b5bac4a63cdf24cca10ef3a683a3b02b527
ms.contentlocale: lv-lv
ms.lasthandoff: 01/19/2018

---

# <a name="expense-workflow"></a><span data-ttu-id="db4d3-103">Izdevumu darbplūsma</span><span class="sxs-lookup"><span data-stu-id="db4d3-103">Expense workflow</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="db4d3-104">Programmatūrā Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition varat izmantot darbplūsmu sistēmu, lai modulī Izdevumu pārvaldība iestatītu pārskatīšanas procesu izdevumu pārskatiem.</span><span class="sxs-lookup"><span data-stu-id="db4d3-104">You can use the workflow system in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="db4d3-105">Varat iestatīt darbplūsmu, kas izmanto tālāk norādītos kritērijus, lai noteiktu, kurš apstiprina izdevumu pārskatus.</span><span class="sxs-lookup"><span data-stu-id="db4d3-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="db4d3-106">Darbinieku pārskatu veidošanas hierarhija un sākotnēji definētu apstiprinājumu ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="db4d3-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="db4d3-107">Vairāku līmeņu apstiprinājums, kas atbalsta pagaidu apstiprinātājus un galīgo apstiprinātāju</span><span class="sxs-lookup"><span data-stu-id="db4d3-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="db4d3-108">Finanšu dimensijas un projekta atbildība</span><span class="sxs-lookup"><span data-stu-id="db4d3-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="db4d3-109">Piešķire noteiktiem lietotājiem vai lietotāju grupām</span><span class="sxs-lookup"><span data-stu-id="db4d3-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="db4d3-110">Darbplūsmu apstiprinājumus var izveidot izdevumu pārskatiem, komandējumu pieprasījumiem, skaidras naudas avansiem un pievienotās vērtības nodokļa (PVN) atgūšanai.</span><span class="sxs-lookup"><span data-stu-id="db4d3-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="db4d3-111">**Piemērs**</span><span class="sxs-lookup"><span data-stu-id="db4d3-111">**Example**</span></span>

<span data-ttu-id="db4d3-112">Nākamais process ir izdevumu pārskatam paredzētas izdevumu pārvaldības darbplūsmas piemērs.</span><span class="sxs-lookup"><span data-stu-id="db4d3-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="db4d3-113">Darbinieks izveido un saglabā izdevumu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="db4d3-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="db4d3-114">Šis darbinieks izdevumu pārskatu iesniedz apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="db4d3-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="db4d3-115">Apstiprinātājs tiek identificēts, balstoties uz kārtulām, kuras tika definētas darbplūsmas iestatīšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="db4d3-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="db4d3-116">Apstiprinātājs saņem paziņojumu par to, ka izdevumu pārskats ir gatavs apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="db4d3-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="db4d3-117">Apstiprinātājs pārskata izdevumu pārskatu un apstiprina, ka ir izpildīti tālāk norādītie nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="db4d3-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="db4d3-118">Izdevumi nepārkāpj izdevumu politikas.</span><span class="sxs-lookup"><span data-stu-id="db4d3-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="db4d3-119">Ja izdevumi pārkāpj politiku, tad apstiprinātājs apstiprina, ka izdevumu pārskats ietver derīgu darījuma pamatojumu.</span><span class="sxs-lookup"><span data-stu-id="db4d3-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="db4d3-120">Izdevumu pārskatam ir pievienotas elektroniskās kvītis.</span><span class="sxs-lookup"><span data-stu-id="db4d3-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="db4d3-121">Apstiprinātājs apstiprina izdevumu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="db4d3-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="db4d3-122">Izdevumu pārskats tiek nodots parādu kreditoriem koordinatoram iegrāmatošanai.</span><span class="sxs-lookup"><span data-stu-id="db4d3-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="db4d3-123">Atkarībā no tā, vai ir konfigurēta automātiskā grāmatošana, notiek viena no tālāk norādītajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="db4d3-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="db4d3-124">Ja automātiskā grāmatošana ir konfigurēta, tad izdevumu pārskats tiek apstrādāts maksājuma veikšanai un izdevumu pārskata statuss tiek atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="db4d3-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="db4d3-125">Ja automātiskā grāmatošana nav konfigurēta, tad parādu kreditoriem koordinators pārbauda, vai ir iesniegtas visas sākotnējās kvītis un vai kvītis saskan ar izdevumu pārskatā norādītajiem izdevumiem.</span><span class="sxs-lookup"><span data-stu-id="db4d3-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="db4d3-126">Ir arī jāpārbauda, vai ir pareizi visi izdevumu pārskatā ievadītie nodokļu kodi.</span><span class="sxs-lookup"><span data-stu-id="db4d3-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="db4d3-127">Kad atbilstība šīm prasībām ir pārbaudīta, izdevumu pārskats tiek grāmatots.</span><span class="sxs-lookup"><span data-stu-id="db4d3-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="db4d3-128">Kad izdevumu pārskats ir iegrāmatots, tiek autorizēts maksājums par šo izdevumu pārskatu un darbinieks saņem kompensāciju.</span><span class="sxs-lookup"><span data-stu-id="db4d3-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>

