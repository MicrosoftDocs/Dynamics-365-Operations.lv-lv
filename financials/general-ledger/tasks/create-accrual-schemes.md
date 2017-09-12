--- 
title: "Uzkrāšanas shēmu izveide"
description: "Šajā uzdevumu ceļvedī aprakstīts, kā radīt uzkrāšanas shēmu."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 324be23a1e26de0d05c7cf6a61567f7260d0c390
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-accrual-schemes"></a><span data-ttu-id="38689-103">Uzkrāšanas shēmu izveide</span><span class="sxs-lookup"><span data-stu-id="38689-103">Create accrual schemes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38689-104">Šajā uzdevumu ceļvedī aprakstīts, kā radīt uzkrāšanas shēmu.</span><span class="sxs-lookup"><span data-stu-id="38689-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="38689-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="38689-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="38689-106">Pārejiet uz sadaļu Virsgrāmata > Žurnāla iestatīšana > Uzkrāšanas shēmas.</span><span class="sxs-lookup"><span data-stu-id="38689-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="38689-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="38689-107">Click New.</span></span>
3. <span data-ttu-id="38689-108">Laukā Uzkrāšanas shēmas ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="38689-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="38689-109">Laukā Uzkrājuma shēmas apraksts ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="38689-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="38689-110">Laukā Debets norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="38689-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="38689-111">Definētais galvenais konts aizstās debeta galveno kontu žurnāla dokumenta rindā un tas tiks izmantots arī atlikto maksājumu anulēšanai, pamatojoties uz Virsgrāmatas uzkrājumu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="38689-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="38689-112">Laukā Kredīts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="38689-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="38689-113">Definētais galvenais konts aizstās kredīta galveno kontu žurnāla dokumenta rindā un tas tiks izmantots arī atlikto maksājumu anulēšanai, pamatojoties uz Virsgrāmatas uzkrājumu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="38689-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="38689-114">Laukā dokuments atlasiet, kā jānosaka dokuments transakciju grāmatošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="38689-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="38689-115">Laukā Apraksts ievadiet vērtību, lai aprakstītu grāmatojamās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="38689-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="38689-116">Laukā Perioda biežums atlasiet, cik bieži vajadzētu notikt transakcijām.</span><span class="sxs-lookup"><span data-stu-id="38689-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="38689-117">Laukā Gadījumu skaits pēc perioda ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="38689-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="38689-118">Laukā Grāmatot transakcijas atlasiet, kad transakcijas ir jāgrāmato, piemēram, katru mēnesi.</span><span class="sxs-lookup"><span data-stu-id="38689-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>


