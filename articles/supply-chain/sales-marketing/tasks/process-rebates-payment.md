---
title: Maksājuma atlaižu apstrāde
description: Šajā procedūrā parādīts, kā pārvērst apstiprinātas un apstrādātas debitora atlaides par kredīta notām.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 981068d26d232b10efd8d7288daaf7358aee3728
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432903"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="f153a-103">Maksājuma atlaižu apstrāde</span><span class="sxs-lookup"><span data-stu-id="f153a-103">Process rebates for payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f153a-104">Šajā procedūrā parādīts, kā pārvērst apstiprinātas un apstrādātas debitora atlaides par kredīta notām.</span><span class="sxs-lookup"><span data-stu-id="f153a-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="f153a-105">Šo ceļvedi var lietot ar demonstrācijas uzņēmumu USMF.</span><span class="sxs-lookup"><span data-stu-id="f153a-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="f153a-106">Šajā ceļvedī priekšnoteikums ir viena vai vairākas atlaides prasības ar statusu Atzīmēt.</span><span class="sxs-lookup"><span data-stu-id="f153a-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="f153a-107">Ja izmantojat USMF, pirms šī ceļveža izpildes ieteicams palaist ceļvedi "Debitora atlaižu ģenerēšana un apstrāde".</span><span class="sxs-lookup"><span data-stu-id="f153a-107">If you're using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="f153a-108">Atlaides prasības pārveidošana kredīta notā</span><span class="sxs-lookup"><span data-stu-id="f153a-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="f153a-109">Dodieties uz Visi debitori.</span><span class="sxs-lookup"><span data-stu-id="f153a-109">Go to All customers.</span></span>
2. <span data-ttu-id="f153a-110">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f153a-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f153a-111">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f153a-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f153a-112">Darbību rūtī noklikšķiniet uz Iekasēt.</span><span class="sxs-lookup"><span data-stu-id="f153a-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="f153a-113">Noklikšķiniet uz Transakciju nosegšana.</span><span class="sxs-lookup"><span data-stu-id="f153a-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="f153a-114">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="f153a-114">Click Functions.</span></span>
7. <span data-ttu-id="f153a-115">Noklikšķiniet uz Atlaižu programma.</span><span class="sxs-lookup"><span data-stu-id="f153a-115">Click Rebate program.</span></span>
    * <span data-ttu-id="f153a-116">Lapā Atlaide uzskaitītas atlaižu prasības, kuras esat apstrādājis debitora atlaižu rīkā un kurām ir statuss Atzīmēt.</span><span class="sxs-lookup"><span data-stu-id="f153a-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="f153a-117">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="f153a-117">Click Edit.</span></span>
    * <span data-ttu-id="f153a-118">Iestatiet atzīmes laukā Atzīmēt prasībām, ko vēlaties iekļaut kredīta notā.</span><span class="sxs-lookup"><span data-stu-id="f153a-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="f153a-119">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="f153a-119">Click Functions.</span></span>
10. <span data-ttu-id="f153a-120">Noklikšķiniet uz Izveidot kredīta notu.</span><span class="sxs-lookup"><span data-stu-id="f153a-120">Click Create credit note.</span></span>
    * <span data-ttu-id="f153a-121">Tiek parādīts ziņojums, lai paziņotu, ka žurnāls ir iegrāmatots (tas ir Debitoru parādu patēriņa žurnāls, kā norādīts lapā Debitoru moduļa parametri).</span><span class="sxs-lookup"><span data-stu-id="f153a-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="f153a-122">Šī iemesla dēļ reāla pasīvu (kredīta) summa tiek pārvietota uz debitora bilanci.</span><span class="sxs-lookup"><span data-stu-id="f153a-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="f153a-123">Tas nozīmē, ka klients konts tika debetēts un Atlaižu uzkrājumu konts tiek kreditēts.</span><span class="sxs-lookup"><span data-stu-id="f153a-123">This means that the customer's account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="f153a-124">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f153a-124">Close the page.</span></span>
12. <span data-ttu-id="f153a-125">Noklikšķiniet uz Atcelt.</span><span class="sxs-lookup"><span data-stu-id="f153a-125">Click Cancel.</span></span>
    * <span data-ttu-id="f153a-126">Tas atsvaidzina lapu, lai varētu redzēt atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="f153a-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="f153a-127">Darbību rūtī noklikšķiniet uz Iekasēt.</span><span class="sxs-lookup"><span data-stu-id="f153a-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="f153a-128">Noklikšķiniet uz Transakciju nosegšana.</span><span class="sxs-lookup"><span data-stu-id="f153a-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="f153a-129">Ņemiet vērā, ka transakcija ar negatīvu summu, kas atspoguļo kopējo atlaižu summu, bez rēķina atsauces tika pievienota debitora bilancei.</span><span class="sxs-lookup"><span data-stu-id="f153a-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="f153a-130">Noklikšķiniet uz Atcelt.</span><span class="sxs-lookup"><span data-stu-id="f153a-130">Click Cancel.</span></span>

