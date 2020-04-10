---
title: Procentu koda ar diapazonu izveide
description: Procentu kodus var iestatīt, lai tiktu aprēķinātas dažādas procentu summas, balstoties uz vērtību diapazonu.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c0c5b20ff6fff2bc62daca68c46e949a38df8d92
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140279"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="71334-103">Procentu koda ar diapazonu izveide</span><span class="sxs-lookup"><span data-stu-id="71334-103">Create an interest code with a range</span></span>

[!include [banner](../../includes/banner.md)]
<span data-ttu-id="71334-104">Procentu kodus var iestatīt, lai tiktu aprēķinātas dažādas procentu summas, balstoties uz vērtību diapazonu.</span><span class="sxs-lookup"><span data-stu-id="71334-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="71334-105">Šajā procedūrā ir parādīts, kā pievienot procentu kodu un tam pievienot diapazonu.</span><span class="sxs-lookup"><span data-stu-id="71334-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="71334-106">Pārejiet uz sadaļu Kredīts un iekasēšana > Procenti > Iestatīt procentu kodus.</span><span class="sxs-lookup"><span data-stu-id="71334-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="71334-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="71334-107">Click New.</span></span>
3. <span data-ttu-id="71334-108">Laukā Procentu kodi ievadiet procentu koda nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="71334-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="71334-109">Laukā Apraksts ievadiet procentu koda aprakstu.</span><span class="sxs-lookup"><span data-stu-id="71334-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="71334-110">Atlasiet Mēnesis.</span><span class="sxs-lookup"><span data-stu-id="71334-110">Select Month.</span></span>
6. <span data-ttu-id="71334-111">Paplašiniet sadaļu Ienākumi.</span><span class="sxs-lookup"><span data-stu-id="71334-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="71334-112">Izvērsiet Ieņēmumus, atlasot valūtu.</span><span class="sxs-lookup"><span data-stu-id="71334-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="71334-113">Laukā Virsgrāmatas grāmatošanas konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="71334-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="71334-114">Laukā Procenti pēc diapazona atlasiet Mēneši.</span><span class="sxs-lookup"><span data-stu-id="71334-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="71334-115">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="71334-115">Click Add.</span></span>
11. <span data-ttu-id="71334-116">Laukā Apraksts ievadiet šīs valūtas un diapazona aprakstu.</span><span class="sxs-lookup"><span data-stu-id="71334-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="71334-117">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="71334-117">Click Save.</span></span>
13. <span data-ttu-id="71334-118">Noklikšķiniet uz Diapazoni.</span><span class="sxs-lookup"><span data-stu-id="71334-118">Click Ranges.</span></span>
14. <span data-ttu-id="71334-119">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="71334-119">Click New.</span></span>
15. <span data-ttu-id="71334-120">Kā vērtību No ievadiet 0 un pēc tam ievadiet procentu likmi mēnesī, kas tiks izmantota, lai aprēķinātu procentus.</span><span class="sxs-lookup"><span data-stu-id="71334-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="71334-121">Mūsu piemērā tā ir 1,5.</span><span class="sxs-lookup"><span data-stu-id="71334-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="71334-122">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="71334-122">Click New.</span></span>
17. <span data-ttu-id="71334-123">Kā nākamo vērtību No ievadiet 4, kas ir pirmais mēnesis, kurā tiks aprēķināta jauna procentu summa.</span><span class="sxs-lookup"><span data-stu-id="71334-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="71334-124">Ievadiet procentu likmi mēnesī, kas tiks izmantota, lai aprēķinātu procentus, sākot ar 4. mēnesi.</span><span class="sxs-lookup"><span data-stu-id="71334-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="71334-125">Šajā piemērā atlasiet vērtību 2.0.</span><span class="sxs-lookup"><span data-stu-id="71334-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="71334-126">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="71334-126">Click New.</span></span>
20. <span data-ttu-id="71334-127">Kā nākamo vērtību No ievadiet 7, kas ir nākamais mēnesis, kurā tiks aprēķināta jauna procentu summa.</span><span class="sxs-lookup"><span data-stu-id="71334-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="71334-128">Ievadiet procentu likmi mēnesī, kas tiks izmantota, lai aprēķinātu procentus, sākot ar 7. mēnesi.</span><span class="sxs-lookup"><span data-stu-id="71334-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="71334-129">Šajā piemērā atlasiet vērtību 2.5.</span><span class="sxs-lookup"><span data-stu-id="71334-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="71334-130">Noklikšķiniet uz Aizvērt, lai pabeigtu iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="71334-130">Click Close to complete the setup.</span></span>

