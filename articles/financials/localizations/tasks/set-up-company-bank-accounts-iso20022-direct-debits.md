---
title: Uzņēmuma bankas kontu iestatīšana ISO20022 tiešajiem debetiem
description: Šajā uzdevumā parādīts, kā iestatīt informāciju par uzņēmuma bankas kontu, kas nepieciešama debitora maksājumu failu ģenerēšanai.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 290d0eeb383dc3808935809e21b1bf6c99a8550a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552398"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="1a72a-103">Uzņēmuma bankas kontu iestatīšana ISO20022 tiešajiem debetiem</span><span class="sxs-lookup"><span data-stu-id="1a72a-103">Set up company bank accounts for ISO20022 direct debits</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1a72a-104">Šajā uzdevumā parādīts, kā iestatīt informāciju par uzņēmuma bankas kontu, kas nepieciešama debitora maksājumu failu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="1a72a-104">This task walks you through setting up the company specific bank account information that is required for generating customer payment files.</span></span> <span data-ttu-id="1a72a-105">Šī procedūra izmanto ISO 20022 tiešā debeta formātu kā piemēru.</span><span class="sxs-lookup"><span data-stu-id="1a72a-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> <span data-ttu-id="1a72a-106">Citos formātos, iespējams, ir nepieciešamu papildu iestatījumu informācija, piemēram, uzņēmuma ID un kārtošanas kods.</span><span class="sxs-lookup"><span data-stu-id="1a72a-106">Other formats might require additional setup information like the Company ID or the Sort code.</span></span>



<span data-ttu-id="1a72a-107">Šis uzdevums tika izveidots, izmantojot demonstrācijas datu uzņēmumu DEMF.</span><span class="sxs-lookup"><span data-stu-id="1a72a-107">This task was created using the demo data company DEMF.</span></span>



<span data-ttu-id="1a72a-108">Šī ir otrā no piecām procedūrām, kas demonstrē debitora maksājuma procesu, izmantojot elektronisko atskaišu konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="1a72a-108">This is the second of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-the-iban-and-swift-codes"></a><span data-ttu-id="1a72a-109">IBAN un SWIFT kodu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1a72a-109">Set up the IBAN and SWIFT codes</span></span>
1. <span data-ttu-id="1a72a-110">Pārejiet uz sadaļu Skaidras naudas un banku pārvaldība > Banku konti.</span><span class="sxs-lookup"><span data-stu-id="1a72a-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="1a72a-111">Izmantojiet ātro filtru, lai filtrētu pēc lauka Bankas konts vērtības DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="1a72a-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="1a72a-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1a72a-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1a72a-113">Piemēram, noklikšķiniet uz DEMF OPER, lai atvērtu informāciju par bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="1a72a-113">For example, click 'DEMF OPER' to open the bank account details.</span></span>  
4. <span data-ttu-id="1a72a-114">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="1a72a-114">Click Edit.</span></span>
5. <span data-ttu-id="1a72a-115">Izvērsiet vai sakļaujiet sadaļu Papildu identifikācija.</span><span class="sxs-lookup"><span data-stu-id="1a72a-115">Expand or collapse the Additional identification section.</span></span>
6. <span data-ttu-id="1a72a-116">Ievadiet vērtību laukā IBAN.</span><span class="sxs-lookup"><span data-stu-id="1a72a-116">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="1a72a-117">Piemēram, ievadiet 'DE89370400440532013000'.</span><span class="sxs-lookup"><span data-stu-id="1a72a-117">For example, enter 'DE89370400440532013000'.</span></span>  
7. <span data-ttu-id="1a72a-118">Ierakstiet vērtību laukā SWIFT kods.</span><span class="sxs-lookup"><span data-stu-id="1a72a-118">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="1a72a-119">Piemēram, ievadiet DEUTDEFF.</span><span class="sxs-lookup"><span data-stu-id="1a72a-119">For example, enter 'DEUTDEFF'.</span></span>    <span data-ttu-id="1a72a-120">Lūdzu, ņemiet vērā, ka SWIFT\BIC nav nepieciešami daudziem maksājumu formātiem, tomēr ir ieteicams reģistrēt to bankas kontam.</span><span class="sxs-lookup"><span data-stu-id="1a72a-120">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="1a72a-121">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="1a72a-121">Click Save.</span></span>

## <a name="set-up-a-bank-account-for-the-legal-entity"></a><span data-ttu-id="1a72a-122">Juridiskas personas bankas konta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1a72a-122">Set up a bank account for the legal entity</span></span>
1. <span data-ttu-id="1a72a-123">Pārejiet uz sadaļu Organizācijas administrēšana > Organizācijas > Juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="1a72a-123">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="1a72a-124">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="1a72a-124">Click Edit.</span></span>
3. <span data-ttu-id="1a72a-125">Izvērsiet vai sakļaujiet sadaļu Bankas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="1a72a-125">Expand or collapse the Bank account information section.</span></span>
4. <span data-ttu-id="1a72a-126">Laukā Bankas konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="1a72a-126">In the Bank account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="1a72a-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1a72a-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1a72a-128">Piemēram, atlasiet "DEMF OPER" bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="1a72a-128">For example, select the "DEMF OPER" bank account.</span></span>  
6. <span data-ttu-id="1a72a-129">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="1a72a-129">Click Save.</span></span>

