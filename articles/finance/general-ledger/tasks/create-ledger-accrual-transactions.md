---
title: Virsgrāmatas uzkrājumu darbību izveide
description: Šajā uzdevumā ir aprakstīts, kā ģenerēt virsgrāmatas uzkrājuma transakcijas, kuras nosaka uzkrāšanas shēmas.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6cbda1c535aad63df55d40bcbadccffc3f35b455
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994644"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="88e14-103">Virsgrāmatas uzkrājumu darbību izveide</span><span class="sxs-lookup"><span data-stu-id="88e14-103">Create ledger accrual transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="88e14-104">Šajā uzdevuma ceļvedī aprakstīts, kā ģenerēt Virsgrāmatas uzkrāšanas transakcijas, kas balstītas uz uzkrāšanas shēmām.</span><span class="sxs-lookup"><span data-stu-id="88e14-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="88e14-105">Pārejiet uz sadaļu Virsgrāmata > Žurnāla ieraksti > Virsgrāmatas žurnāli.</span><span class="sxs-lookup"><span data-stu-id="88e14-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="88e14-106">Sarakstā atrodiet un atlasiet vēlamo žurnālu vai izveidojiet to.</span><span class="sxs-lookup"><span data-stu-id="88e14-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="88e14-107">Noklikšķiniet, lai sekotu saitei laukā Žurnāla iedaļas numurs.</span><span class="sxs-lookup"><span data-stu-id="88e14-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="88e14-108">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="88e14-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="88e14-109">Laukā Konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="88e14-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="88e14-110">Šajā piemērā mēs nosakām apdrošināšanas izdevumus.</span><span class="sxs-lookup"><span data-stu-id="88e14-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="88e14-111">Tie kļūs par periodisko izdevumu summu.</span><span class="sxs-lookup"><span data-stu-id="88e14-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="88e14-112">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="88e14-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="88e14-113">Laukā Debets ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="88e14-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="88e14-114">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="88e14-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="88e14-115">Noklikšķiniet uz Funkcijas.</span><span class="sxs-lookup"><span data-stu-id="88e14-115">Click Functions.</span></span>
10. <span data-ttu-id="88e14-116">Noklikšķiniet uz Virsgrāmatas uzkrājumi.</span><span class="sxs-lookup"><span data-stu-id="88e14-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="88e14-117">Laukā Uzkrāšanas identifikācija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="88e14-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="88e14-118">Sarakstā atrodiet un atlasiet uzkrāšanas shēmu, kuru vēlaties lietot.</span><span class="sxs-lookup"><span data-stu-id="88e14-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="88e14-119">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="88e14-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="88e14-120">Laukā Sākuma datums ievadiet kādu datumu.</span><span class="sxs-lookup"><span data-stu-id="88e14-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="88e14-121">Noklikšķiniet uz Transakcijas.</span><span class="sxs-lookup"><span data-stu-id="88e14-121">Click Transactions.</span></span>
16. <span data-ttu-id="88e14-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="88e14-122">Close the page.</span></span>
17. <span data-ttu-id="88e14-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="88e14-123">Click OK.</span></span>
18. <span data-ttu-id="88e14-124">Noklikšķiniet uz Grāmatot.</span><span class="sxs-lookup"><span data-stu-id="88e14-124">Click Post.</span></span>

