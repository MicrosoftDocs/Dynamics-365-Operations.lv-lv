---
title: Maksājuma atlaižu apstrāde
description: Šajā procedūrā parādīts, kā pārvērst apstiprinātas un apstrādātas debitora atlaides par kredīta notām.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a05565d220c53d0f860a2c0569622b55c4021d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833883"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="b0f72-103">Maksājuma atlaižu apstrāde</span><span class="sxs-lookup"><span data-stu-id="b0f72-103">Process rebates for payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0f72-104">Šajā procedūrā parādīts, kā pārvērst apstiprinātas un apstrādātas debitora atlaides par kredīta notām.</span><span class="sxs-lookup"><span data-stu-id="b0f72-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="b0f72-105">Šo ceļvedi var lietot ar demonstrācijas uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="b0f72-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="b0f72-106">Šajā ceļvedī priekšnoteikums ir viena vai vairākas atlaides prasības ar statusu Atzīmēt.</span><span class="sxs-lookup"><span data-stu-id="b0f72-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="b0f72-107">Ja jūs izmantojat USMF, pirms šī ceļveža izpildes ieteicams palaist ceļvedi "Debitora atlaižu ģenerēšana un apstrāde".</span><span class="sxs-lookup"><span data-stu-id="b0f72-107">If you’re using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="b0f72-108">Atlaides prasības pārveidošana kredīta notā</span><span class="sxs-lookup"><span data-stu-id="b0f72-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="b0f72-109">Dodieties uz Visi debitori.</span><span class="sxs-lookup"><span data-stu-id="b0f72-109">Go to All customers.</span></span>
2. <span data-ttu-id="b0f72-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b0f72-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b0f72-111">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b0f72-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b0f72-112">Darbību rūtī noklikšķiniet uz Iekasēt.</span><span class="sxs-lookup"><span data-stu-id="b0f72-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="b0f72-113">Noklikšķiniet uz Transakciju nosegšana.</span><span class="sxs-lookup"><span data-stu-id="b0f72-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="b0f72-114">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="b0f72-114">Click Functions.</span></span>
7. <span data-ttu-id="b0f72-115">Noklikšķiniet uz Atlaižu programma.</span><span class="sxs-lookup"><span data-stu-id="b0f72-115">Click Rebate program.</span></span>
    * <span data-ttu-id="b0f72-116">Lapā Atlaide uzskaitītas atlaižu prasības, kuras esat apstrādājis debitora atlaižu rīkā un kurām ir statuss Atzīmēt.</span><span class="sxs-lookup"><span data-stu-id="b0f72-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="b0f72-117">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="b0f72-117">Click Edit.</span></span>
    * <span data-ttu-id="b0f72-118">Iestatiet atzīmes laukā Atzīmēt prasībām, ko vēlaties iekļaut kredīta notā.</span><span class="sxs-lookup"><span data-stu-id="b0f72-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="b0f72-119">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="b0f72-119">Click Functions.</span></span>
10. <span data-ttu-id="b0f72-120">Noklikšķiniet uz Izveidot kredīta notu.</span><span class="sxs-lookup"><span data-stu-id="b0f72-120">Click Create credit note.</span></span>
    * <span data-ttu-id="b0f72-121">Tiek parādīts ziņojums, lai paziņotu, ka žurnāls ir iegrāmatots (tas ir Debitoru parādu patēriņa žurnāls, kā norādīts lapā Debitoru moduļa parametri.</span><span class="sxs-lookup"><span data-stu-id="b0f72-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="b0f72-122">Šī iemesla dēļ reāla pasīvu (kredīta) summa tiek pārvietota uz debitora bilanci.</span><span class="sxs-lookup"><span data-stu-id="b0f72-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="b0f72-123">Tas nozīmē, ka debitora konts tika debetēts un Atlaižu uzkrājumu konts tiek kreditēts.</span><span class="sxs-lookup"><span data-stu-id="b0f72-123">This means that the customer’s account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="b0f72-124">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b0f72-124">Close the page.</span></span>
12. <span data-ttu-id="b0f72-125">Noklikšķiniet uz Atcelt.</span><span class="sxs-lookup"><span data-stu-id="b0f72-125">Click Cancel.</span></span>
    * <span data-ttu-id="b0f72-126">Tas atsvaidzina lapu, lai varētu redzēt atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="b0f72-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="b0f72-127">Darbību rūtī noklikšķiniet uz Iekasēt.</span><span class="sxs-lookup"><span data-stu-id="b0f72-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="b0f72-128">Noklikšķiniet uz Transakciju nosegšana.</span><span class="sxs-lookup"><span data-stu-id="b0f72-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="b0f72-129">Ņemiet vērā, ka transakcija ar negatīvu summu, kas atspoguļo kopējo atlaižu summu, bez rēķina atsauces tika pievienota debitora bilancei.</span><span class="sxs-lookup"><span data-stu-id="b0f72-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="b0f72-130">Noklikšķiniet uz Atcelt.</span><span class="sxs-lookup"><span data-stu-id="b0f72-130">Click Cancel.</span></span>

