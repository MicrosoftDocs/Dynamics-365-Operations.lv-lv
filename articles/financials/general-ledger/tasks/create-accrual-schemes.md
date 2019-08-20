---
title: Uzkrāšanas shēmu izveide
description: Šajā uzdevumu ceļvedī aprakstīts, kā radīt uzkrāšanas shēmu.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0ae55000a5cf1593d057d940dc3dbbf9e5cb3f3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834893"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="45ee4-103">Uzkrāšanas shēmu izveide</span><span class="sxs-lookup"><span data-stu-id="45ee4-103">Create accrual schemes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="45ee4-104">Šajā uzdevumu ceļvedī aprakstīts, kā radīt uzkrāšanas shēmu.</span><span class="sxs-lookup"><span data-stu-id="45ee4-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="45ee4-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="45ee4-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="45ee4-106">Pārejiet uz sadaļu Virsgrāmata > Žurnāla iestatīšana > Uzkrāšanas shēmas.</span><span class="sxs-lookup"><span data-stu-id="45ee4-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="45ee4-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="45ee4-107">Click New.</span></span>
3. <span data-ttu-id="45ee4-108">Laukā Uzkrāšanas shēmas ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="45ee4-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="45ee4-109">Laukā Uzkrājuma shēmas apraksts ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="45ee4-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="45ee4-110">Laukā Debets norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="45ee4-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="45ee4-111">Definētais galvenais konts aizstās debeta galveno kontu žurnāla dokumenta rindā un tas tiks izmantots arī atlikto maksājumu anulēšanai, pamatojoties uz Virsgrāmatas uzkrājumu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="45ee4-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="45ee4-112">Laukā Kredīts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="45ee4-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="45ee4-113">Definētais galvenais konts aizstās kredīta galveno kontu žurnāla dokumenta rindā un tas tiks izmantots arī atlikto maksājumu anulēšanai, pamatojoties uz Virsgrāmatas uzkrājumu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="45ee4-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="45ee4-114">Laukā dokuments atlasiet, kā jānosaka dokuments transakciju grāmatošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="45ee4-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="45ee4-115">Laukā Apraksts ievadiet vērtību, lai aprakstītu grāmatojamās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="45ee4-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="45ee4-116">Laukā Perioda biežums atlasiet, cik bieži vajadzētu notikt transakcijām.</span><span class="sxs-lookup"><span data-stu-id="45ee4-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="45ee4-117">Laukā Gadījumu skaits pēc perioda ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="45ee4-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="45ee4-118">Laukā Grāmatot transakcijas atlasiet, kad transakcijas ir jāgrāmato, piemēram, katru mēnesi.</span><span class="sxs-lookup"><span data-stu-id="45ee4-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>

