--- 
title: "Bankas iestādes līguma izveide akreditīvam"
description: "Šajā uzdevumā ir parādīta bankas iestādes līguma izveidošana, lai apstrādātu akreditīvu."
author: ShylaThompson
manager: AnnBe
ms.date: 02/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ac3394a40bff3aaee6a76448633e4f36c4049612
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="42c5a-103">Bankas iestādes līguma izveide akreditīvam</span><span class="sxs-lookup"><span data-stu-id="42c5a-103">Create a bank facility agreement for a letter of credit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="42c5a-104">Šajā uzdevumā ir parādīta bankas iestādes līguma izveidošana, lai apstrādātu akreditīvu.</span><span class="sxs-lookup"><span data-stu-id="42c5a-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="42c5a-105">Pirms šī uzdevuma veikšanas ir jāizveido bankas iestādes un grāmatošanas metodes.</span><span class="sxs-lookup"><span data-stu-id="42c5a-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="42c5a-106">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums “USMF”.</span><span class="sxs-lookup"><span data-stu-id="42c5a-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="42c5a-107">Izveidot bankas iestādes līgumu</span><span class="sxs-lookup"><span data-stu-id="42c5a-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="42c5a-108">Pārejiet uz sadaļu Kases un bankas pārvaldība > Akreditīvi > Bankas iestādes līgumi.</span><span class="sxs-lookup"><span data-stu-id="42c5a-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="42c5a-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="42c5a-109">Click New.</span></span>
3. <span data-ttu-id="42c5a-110">Laukā Līguma numurs ievadiet līguma numuru saskaņā ar līgumu, kas noslēgts ar banku.</span><span class="sxs-lookup"><span data-stu-id="42c5a-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="42c5a-111">Laukā Bankas konts ievadiet konta numuru izdevējbankā.</span><span class="sxs-lookup"><span data-stu-id="42c5a-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="42c5a-112">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="42c5a-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="42c5a-113">Laukā Sākuma datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="42c5a-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="42c5a-114">Laukā Beigu datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="42c5a-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="42c5a-115">Izvērsiet vai sakļaujiet sadaļu Vispārīgi.</span><span class="sxs-lookup"><span data-stu-id="42c5a-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="42c5a-116">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="42c5a-116">Click Add line.</span></span>
10. <span data-ttu-id="42c5a-117">Laukā Iestādes tips noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="42c5a-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="42c5a-118">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="42c5a-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="42c5a-119">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="42c5a-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="42c5a-120">Laukā Limits ievadiet iestādes summu, par kuru esat ar šo banku vienojies.</span><span class="sxs-lookup"><span data-stu-id="42c5a-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="42c5a-121">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="42c5a-121">Click Save.</span></span>
15. <span data-ttu-id="42c5a-122">Noklikšķiniet uz Paplašināt, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="42c5a-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="42c5a-123">Laukā Jauns līguma numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="42c5a-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="42c5a-124">Laukā Beigu datums ievadiet datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="42c5a-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="42c5a-125">Noklikšķiniet uz Paplašināt.</span><span class="sxs-lookup"><span data-stu-id="42c5a-125">Click Extend.</span></span>
19. <span data-ttu-id="42c5a-126">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="42c5a-126">Close the page.</span></span>


