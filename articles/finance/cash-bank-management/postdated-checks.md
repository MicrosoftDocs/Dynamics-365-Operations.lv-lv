---
title: Ar iepriekšēju datumu datēti čeki
description: Šajā rakstā ir sniegta informācija par ar iepriekšēju datumu datētu čeku atbalstu programmā Microsoft Dynamics 365 Finance. Ar iepriekšēju datumu datēti čeki ir čeki, kas tiek izsniegti, lai veiktu vai saņemtu maksājumus nākotnes datumā. Tāpēc šādu čeku nevar iekasēt pirms norādītā datuma.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38ee6c5b3d258c313a2066b388a83330bf696d39
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178869"
---
# <a name="postdated-checks"></a><span data-ttu-id="880ba-105">Ar iepriekšēju datumu datēti čeki</span><span class="sxs-lookup"><span data-stu-id="880ba-105">Postdated checks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="880ba-106">Šajā rakstā ir sniegta informācija par ar iepriekšēju datumu datētu čeku atbalstu.</span><span class="sxs-lookup"><span data-stu-id="880ba-106">This article provides information about support for postdated checks.</span></span> <span data-ttu-id="880ba-107">Ar iepriekšēju datumu datēti čeki ir čeki, kas tiek izsniegti, lai veiktu vai saņemtu maksājumus nākotnes datumā.</span><span class="sxs-lookup"><span data-stu-id="880ba-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="880ba-108">Tāpēc šādu čeku nevar iekasēt pirms norādītā datuma.</span><span class="sxs-lookup"><span data-stu-id="880ba-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="880ba-109">Programma Dynamics 365 Finance atbalsta pilnu pārvaldības ciklu ar iepriekšēju datumu datētiem čekiem gan modulī, Debitori, gan modulī Kreditori, kā tas ir parādīts tālāk redzamajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="880ba-109">Dynamics 365 Finance supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="880ba-110">Scenārijs</span><span class="sxs-lookup"><span data-stu-id="880ba-110">Scenario</span></span></th>
<th><span data-ttu-id="880ba-111">Detalizēta</span><span class="sxs-lookup"><span data-stu-id="880ba-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="880ba-112">Iestatīt ar iepriekšēju datumu datētus čekus</span><span class="sxs-lookup"><span data-stu-id="880ba-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="880ba-113">Jums ir jāiestata jauna maksājuma metode un jānorāda maksājuma procedūra klīringa kontiem saistībā ar izsniegtajiem čekiem, saņemtajiem čekiem un ieturētajiem nodokļiem.</span><span class="sxs-lookup"><span data-stu-id="880ba-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="880ba-114">Reģistrēt un grāmatot čeku kreditoram, kas datēts ar iepriekšēju datumu</span><span class="sxs-lookup"><span data-stu-id="880ba-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="880ba-115">Reģistrējiet informāciju par kreditoram izsniegto čeku, kas datēts ar iepriekšēju datumu.</span><span class="sxs-lookup"><span data-stu-id="880ba-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="880ba-116">Grāmatojot maksājumu, tiek atzītas kreditora saistības, taču vēl netiek kreditēts bankas konts.</span><span class="sxs-lookup"><span data-stu-id="880ba-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="880ba-117">Tā vietā šim nolūkam tiek lietots klīringa konts.</span><span class="sxs-lookup"><span data-stu-id="880ba-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="880ba-118">Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana debitoram</span><span class="sxs-lookup"><span data-stu-id="880ba-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="880ba-119">Reģistrējiet informāciju par no debitora saņemtu čeku, kurš datēts ar iepriekšēju datumu.</span><span class="sxs-lookup"><span data-stu-id="880ba-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="880ba-120">Grāmatojot maksājumu, tiek kreditēta no debitora saņemamā summa, taču vēl netiek debitēts bankas konts.</span><span class="sxs-lookup"><span data-stu-id="880ba-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="880ba-121">Tā vietā šim nolūkam tiek lietots klīringa konts.</span><span class="sxs-lookup"><span data-stu-id="880ba-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="880ba-122">Reģistrējiet un grāmatojiet ar iepriekšēju datumu datētu debitora vai kreditora aizstāšanas čeku.</span><span class="sxs-lookup"><span data-stu-id="880ba-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="880ba-123">Ja jūsu sākotnējais kreditoram izsniegtais vai no debitora saņemtais čeks ir pazaudēts vai bojāts, varat izsniegt ar iepriekšēju datumu datētu aizstāšanas čeku.</span><span class="sxs-lookup"><span data-stu-id="880ba-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="880ba-124">Kad reģistrējot čeka informāciju, norādiet atsauci uz sākotnējo čeku un norādiet, ka jaunais čeks aizstāj sākotnējo.</span><span class="sxs-lookup"><span data-stu-id="880ba-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="880ba-125">Varat arī grāmatot šo aizstāšanas čeku.</span><span class="sxs-lookup"><span data-stu-id="880ba-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="880ba-126">Pārsūtīt debitora ar iepriekšējo datumu datēto čeku kreditoram</span><span class="sxs-lookup"><span data-stu-id="880ba-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="880ba-127">Kad no debitora saņemat ar iepriekšēju datumu datētu čeku, šo čeku varat pārsūtīt kreditoram kā maksājumu.</span><span class="sxs-lookup"><span data-stu-id="880ba-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="880ba-128">Segt ar iepriekšēju datumu datētu debitora vai kreditora čeku</span><span class="sxs-lookup"><span data-stu-id="880ba-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="880ba-129">Sedziet ar iepriekšēju datumu datētu čeku, kas debitoram vai kreditoram ir grāmatots pagaidu kontam, kad šim čekam beidzot pienāk beigu termiņš.</span><span class="sxs-lookup"><span data-stu-id="880ba-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="880ba-130">Kad čeks ir segts, banka beidzot veic debitēšanu vai kreditēšanu pret klīringa kontu, kas tika izmantots iepriekš.</span><span class="sxs-lookup"><span data-stu-id="880ba-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="880ba-131">Atcelt kreditora čeku, kas datēts ar iepriekšēju datumu</span><span class="sxs-lookup"><span data-stu-id="880ba-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="880ba-132">Varat atcelt ar iepriekšēju datumu datētu čeku tālāk norādītajās situācijās: - Banka ir atgriezusi čeku.</span><span class="sxs-lookup"><span data-stu-id="880ba-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="880ba-133">- Čeks ir lietots nepareizam rēķinam.</span><span class="sxs-lookup"><span data-stu-id="880ba-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="880ba-134">- Čeks ir apmaksāts skaidrā naudā.</span><span class="sxs-lookup"><span data-stu-id="880ba-134">- A cash payment is made against the check.</span></span>
  </td>
  </tr>
  <tr class="even">
  <td><span data-ttu-id="880ba-135">Apturiet ar iepriekšēju datumu datēta čeka maksājumu.</span><span class="sxs-lookup"><span data-stu-id="880ba-135">Stop payment for a postdated check</span></span></td>
  <td><span data-ttu-id="880ba-136">Kreditoram izsniegtam ar iepriekšēju datumu datētam čekam maksājumu varat apturēt tādu iemeslu dēļ kā nepietiekami naudas līdzekļi, ar kreditoru noslēgtā līguma izmaiņas, kreditors piegādā preces ar defektiem vai kreditoram preces tiek atgrieztas.</span><span class="sxs-lookup"><span data-stu-id="880ba-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="880ba-137">Varat apturēt tikai tādu čeku maksājumu, kam nav veikts klīrings.</span><span class="sxs-lookup"><span data-stu-id="880ba-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
  </tr>
  </tbody>
  </table>



<span data-ttu-id="880ba-138">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="880ba-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="880ba-139">Ar iepriekšēju datumu datētu čeku iestatīšana</span><span class="sxs-lookup"><span data-stu-id="880ba-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="880ba-140">Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana debitoram</span><span class="sxs-lookup"><span data-stu-id="880ba-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="880ba-141">Ar iepriekšēju datumu datētu čeku no debitora apmaksa</span><span class="sxs-lookup"><span data-stu-id="880ba-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="880ba-142">Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana kreditoram</span><span class="sxs-lookup"><span data-stu-id="880ba-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="880ba-143">Ar iepriekšēju datumu datētu čeku no kreditora apmaksa</span><span class="sxs-lookup"><span data-stu-id="880ba-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)



