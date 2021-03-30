---
title: Uzkrāšanas shēmu izveide
description: Šajā tēmā ir paskaidrots, kā izveidot uzkrāšanas shēmu.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c021f71735e63c270e8f1998d77d4e4abcc5506
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236702"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="10c3f-103">Uzkrāšanas shēmu izveide</span><span class="sxs-lookup"><span data-stu-id="10c3f-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="10c3f-104">Šajā tēmā ir paskaidrots, kā izveidot uzkrāšanas shēmu.</span><span class="sxs-lookup"><span data-stu-id="10c3f-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="10c3f-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="10c3f-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="10c3f-106">Ejiet uz **Navigācijas rūts > Moduļi > Virsgrāmata > Žurnāla iestatīšana > Uzkrāšanas shēmas**.</span><span class="sxs-lookup"><span data-stu-id="10c3f-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="10c3f-107">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="10c3f-107">Select **New**.</span></span>
3. <span data-ttu-id="10c3f-108">Laukā **Uzkrājuma identifikācija** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="10c3f-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="10c3f-109">Laukā **Uzkrāšanas shēmas apraksts** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="10c3f-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="10c3f-110">Laukā **Debets** norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="10c3f-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="10c3f-111">Definētais galvenais konts aizstās debeta galveno kontu žurnāla dokumenta rindā un tas tiks izmantots arī atlikto maksājumu anulēšanai, pamatojoties uz Virsgrāmatas uzkrājumu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="10c3f-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="10c3f-112">Laukā **Kredīts** norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="10c3f-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="10c3f-113">Definētais galvenais konts aizstās kredīta galveno kontu žurnāla dokumenta rindā un tas tiks izmantots arī atlikto maksājumu anulēšanai, pamatojoties uz Virsgrāmatas uzkrājumu transakcijām.</span><span class="sxs-lookup"><span data-stu-id="10c3f-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="10c3f-114">Laukā **Vaučeris** norādiet, kā vēlaties noteikt vaučeri, kad darījumi tiek publicēti.</span><span class="sxs-lookup"><span data-stu-id="10c3f-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="10c3f-115">Laukā **Apraksts** ierakstiet vērtību, lai aprakstītu darījumus, kas tiks publicēti.</span><span class="sxs-lookup"><span data-stu-id="10c3f-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="10c3f-116">Laukā **Perioda biežums** atlasiet, cik bieži darījumiem jānotiek.</span><span class="sxs-lookup"><span data-stu-id="10c3f-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="10c3f-117">Laukā **Notikumu skaits periodā** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="10c3f-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="10c3f-118">Laukā **Publicēt darījumus** atlasiet, kad darījumi tiek publicēti, piemēram **Ik mēnesi**.</span><span class="sxs-lookup"><span data-stu-id="10c3f-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]