--- 
title: "Uzņēmuma bankas kontu iestatīšana ISO20022 kredīta pārsūtījumiem"
description: "Šajā procedūrā parādīts, kā iestatīt uzņēmumam specifiskus bankas konta informāciju, kas ir nepieciešama maksājuma faila izveidošanai."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1d0eabdfdeb5ed7d0bdb6df87ebdfa0d41e87492
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="b9eea-103">Uzņēmuma bankas kontu iestatīšana ISO20022 kredīta pārsūtījumiem</span><span class="sxs-lookup"><span data-stu-id="b9eea-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9eea-104">Šajā procedūrā parādīts, kā iestatīt uzņēmumam specifiskus bankas konta informāciju, kas ir nepieciešama maksājuma faila izveidošanai.</span><span class="sxs-lookup"><span data-stu-id="b9eea-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="b9eea-105">Iestatiet informāciju, kas nepieciešama, lai izveidotu ISO 20022 kredīta pārskaitījuma formātu, taču atkarībā no formāta var būt nepieciešama cita informācija, piemēram, uzņēmuma ID un kārtošanas kods.</span><span class="sxs-lookup"><span data-stu-id="b9eea-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="b9eea-106">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DEMF.</span><span class="sxs-lookup"><span data-stu-id="b9eea-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="b9eea-107">Šī ir otrā procedūra no piecām, kas parāda kreditoru maksājumu procesu, izmantojot elektronisko pārskatu veidošanas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="b9eea-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="b9eea-108">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="b9eea-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="b9eea-109">IBAN un SWIFT koda iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b9eea-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="b9eea-110">Pārejiet uz sadaļu Skaidras naudas un banku pārvaldība > Banku konti.</span><span class="sxs-lookup"><span data-stu-id="b9eea-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="b9eea-111">Izmantojiet ātro filtru, lai filtrētu pēc lauka Bankas konts vērtības DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="b9eea-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="b9eea-112">Noklikšķiniet uz DEMF OPER, lai apskatītu informāciju par bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="b9eea-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="b9eea-113">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="b9eea-113">Click Edit.</span></span>
5. <span data-ttu-id="b9eea-114">Izvērsiet sadaļu Papildu identifikācija.</span><span class="sxs-lookup"><span data-stu-id="b9eea-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="b9eea-115">Laukā IBAN ierakstiet DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="b9eea-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="b9eea-116">Laukā SWIFT kods ierakstiet vērtību DEUTDEFF.</span><span class="sxs-lookup"><span data-stu-id="b9eea-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="b9eea-117">Ņemiet vērā, ka SWIFT\BIC nav nepieciešami daudziem maksājumu formātiem, tomēr ir ieteicams reģistrēt to bankas kontam.</span><span class="sxs-lookup"><span data-stu-id="b9eea-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="b9eea-118">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b9eea-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="b9eea-119">Juridiskas personas bankas konta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b9eea-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="b9eea-120">Pārejiet uz sadaļu Organizācijas administrēšana > Organizācijas > Juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="b9eea-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="b9eea-121">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="b9eea-121">Click Edit.</span></span>
3. <span data-ttu-id="b9eea-122">Izvērsiet sadaļu Bankas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="b9eea-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="b9eea-123">Ievadiet vai atlasiet vērtību laukā Bankas konts.</span><span class="sxs-lookup"><span data-stu-id="b9eea-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="b9eea-124">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="b9eea-124">Click Save.</span></span>


