--- 
title: Procentu koda ar diapazonu izveide
description: "Procentu kodus var iestatīt, lai tiktu aprēķinātas dažādas procentu summas, balstoties uz vērtību diapazonu."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e7b6cbc70058c9b9a8edaf3c3303fa7ba0e9da44
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="2c43a-103">Procentu koda ar diapazonu izveide</span><span class="sxs-lookup"><span data-stu-id="2c43a-103">Create an interest code with a range</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2c43a-104">Procentu kodus var iestatīt, lai tiktu aprēķinātas dažādas procentu summas, balstoties uz vērtību diapazonu.</span><span class="sxs-lookup"><span data-stu-id="2c43a-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="2c43a-105">Šajā procedūrā ir parādīts, kā pievienot procentu kodu un tam pievienot diapazonu.</span><span class="sxs-lookup"><span data-stu-id="2c43a-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="2c43a-106">Pārejiet uz sadaļu Kredīts un iekasēšana > Procenti > Iestatīt procentu kodus.</span><span class="sxs-lookup"><span data-stu-id="2c43a-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="2c43a-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2c43a-107">Click New.</span></span>
3. <span data-ttu-id="2c43a-108">Laukā Procentu kodi ievadiet procentu koda nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="2c43a-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="2c43a-109">Laukā Apraksts ievadiet procentu koda aprakstu.</span><span class="sxs-lookup"><span data-stu-id="2c43a-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="2c43a-110">Atlasiet Mēnesis.</span><span class="sxs-lookup"><span data-stu-id="2c43a-110">Select Month.</span></span>
6. <span data-ttu-id="2c43a-111">Paplašiniet sadaļu Ienākumi.</span><span class="sxs-lookup"><span data-stu-id="2c43a-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="2c43a-112">Izvērsiet Ieņēmumus, atlasot valūtu.</span><span class="sxs-lookup"><span data-stu-id="2c43a-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="2c43a-113">Laukā Virsgrāmatas grāmatošanas konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="2c43a-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="2c43a-114">Laukā Procenti pēc diapazona atlasiet Mēneši.</span><span class="sxs-lookup"><span data-stu-id="2c43a-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="2c43a-115">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="2c43a-115">Click Add.</span></span>
11. <span data-ttu-id="2c43a-116">Laukā Apraksts ievadiet šīs valūtas un diapazona aprakstu.</span><span class="sxs-lookup"><span data-stu-id="2c43a-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="2c43a-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="2c43a-117">Click Save.</span></span>
13. <span data-ttu-id="2c43a-118">Noklikšķiniet uz Diapazoni.</span><span class="sxs-lookup"><span data-stu-id="2c43a-118">Click Ranges.</span></span>
14. <span data-ttu-id="2c43a-119">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="2c43a-119">Click New.</span></span>
15. <span data-ttu-id="2c43a-120">Kā vērtību No ievadiet 0 un pēc tam ievadiet procentu likmi mēnesī, kas tiks izmantota, lai aprēķinātu procentus.</span><span class="sxs-lookup"><span data-stu-id="2c43a-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="2c43a-121">Mūsu piemērā tā ir 1,5.</span><span class="sxs-lookup"><span data-stu-id="2c43a-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="2c43a-122">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="2c43a-122">Click New.</span></span>
17. <span data-ttu-id="2c43a-123">Kā nākamo vērtību No ievadiet 4, kas ir pirmais mēnesis, kurā tiks aprēķināta jauna procentu summa.</span><span class="sxs-lookup"><span data-stu-id="2c43a-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="2c43a-124">Ievadiet procentu likmi mēnesī, kas tiks izmantota, lai aprēķinātu procentus, sākot ar 4. mēnesi.</span><span class="sxs-lookup"><span data-stu-id="2c43a-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="2c43a-125">Šajā piemērā atlasiet vērtību 2.0.</span><span class="sxs-lookup"><span data-stu-id="2c43a-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="2c43a-126">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="2c43a-126">Click New.</span></span>
20. <span data-ttu-id="2c43a-127">Kā nākamo vērtību No ievadiet 7, kas ir nākamais mēnesis, kurā tiks aprēķināta jauna procentu summa.</span><span class="sxs-lookup"><span data-stu-id="2c43a-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="2c43a-128">Ievadiet procentu likmi mēnesī, kas tiks izmantota, lai aprēķinātu procentus, sākot ar 7. mēnesi.</span><span class="sxs-lookup"><span data-stu-id="2c43a-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="2c43a-129">Šajā piemērā atlasiet vērtību 2.5.</span><span class="sxs-lookup"><span data-stu-id="2c43a-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="2c43a-130">Noklikšķiniet uz Aizvērt, lai pabeigtu iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="2c43a-130">Click Close to complete the setup.</span></span>


