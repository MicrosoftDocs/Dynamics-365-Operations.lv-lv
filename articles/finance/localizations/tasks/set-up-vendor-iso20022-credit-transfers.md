---
title: Kreditoru un kreditoru bankas kontu iestatīšana ISO20022 kredīta pārsūtījumiem
description: Šajā procedūrā parādīts, kā iestatīt kreditoru un informāciju par kreditora bankas kontu, kas nepieciešama ISO20022 kredīta pārskaitījumam, vai jebkura cita kreditora maksājumu faila izveidošanai.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4809a352f87cc3d88429461a06dfe36189ed5f31
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138973"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="3f91a-103">Kreditoru un kreditoru bankas kontu iestatīšana ISO20022 kredīta pārsūtījumiem</span><span class="sxs-lookup"><span data-stu-id="3f91a-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f91a-104">Šajā procedūrā parādīts, kā iestatīt kreditoru un informāciju par kreditora bankas kontu, kas nepieciešama ISO20022 kredīta pārskaitījumam, vai jebkura cita kreditora maksājumu faila izveidošanai.</span><span class="sxs-lookup"><span data-stu-id="3f91a-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="3f91a-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir DEMF.</span><span class="sxs-lookup"><span data-stu-id="3f91a-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="3f91a-106">Šī ir trešā procedūra no piecām, kas parāda kreditoru maksājumu procesu, izmantojot elektronisko pārskatu veidošanas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="3f91a-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="3f91a-107">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="3f91a-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="3f91a-108">Bankas informācijas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="3f91a-108">Set up bank details</span></span>
1. <span data-ttu-id="3f91a-109">Pārejiet uz sadaļu Kreditori > Kreditori > Visi kreditori.</span><span class="sxs-lookup"><span data-stu-id="3f91a-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="3f91a-110">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="3f91a-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3f91a-111">Piemēram, filtrējiet pēc lauka Kreditora konts, izmantojot vērtību DE-001.</span><span class="sxs-lookup"><span data-stu-id="3f91a-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="3f91a-112">Noklikšķiniet uz DE-001, lai apskatītu detalizētu informāciju par kreditoru.</span><span class="sxs-lookup"><span data-stu-id="3f91a-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="3f91a-113">Darbību rūtī noklikšķiniet uz Kreditors.</span><span class="sxs-lookup"><span data-stu-id="3f91a-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="3f91a-114">Noklikšķiniet uz Banku konti.</span><span class="sxs-lookup"><span data-stu-id="3f91a-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="3f91a-115">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="3f91a-115">Click Edit.</span></span>
    * <span data-ttu-id="3f91a-116">Ja bankas konts nav pieejams, nepieciešams izveidot jaunu.</span><span class="sxs-lookup"><span data-stu-id="3f91a-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="3f91a-117">Laukā SWIFT kods ierakstiet vērtību COBADEFFXXX.</span><span class="sxs-lookup"><span data-stu-id="3f91a-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="3f91a-118">Laukā IBAN ierakstiet DE36200400000628808808.</span><span class="sxs-lookup"><span data-stu-id="3f91a-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="3f91a-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="3f91a-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="3f91a-120">Kreditora maksāšanas metodes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="3f91a-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="3f91a-121">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="3f91a-121">Click Edit.</span></span>
2. <span data-ttu-id="3f91a-122">Izvērsiet vai sakļaujiet sadaļu Maksājums.</span><span class="sxs-lookup"><span data-stu-id="3f91a-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="3f91a-123">Laukā Maksāšanas metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="3f91a-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3f91a-124">Sarakstā noklikšķiniet uz saites SEPA CT rindā.</span><span class="sxs-lookup"><span data-stu-id="3f91a-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="3f91a-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="3f91a-125">Click Save.</span></span>

