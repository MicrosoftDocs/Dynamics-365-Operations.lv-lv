---
title: "Ražošanas kontroles un projekta pārvaldības uzskaitē izmantojamās izmaksu kategorijas"
description: "Dažus ražošanas darba veidus var saistīt ar projekta laika aprēķiniem un pārskatu sagatavošanu. Šajā rakstā ir sniegta informācija par izmaksu kategorijām, kas jānorāda šādiem ražošanas un projekta nolūkiem paredzētiem ražošanas darba veidiem."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1f4c03d886a7a6e98276422cd954954fe6e8a12e
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="78f0b-104">Ražošanas kontroles un projekta pārvaldības uzskaitē izmantojamās izmaksu kategorijas</span><span class="sxs-lookup"><span data-stu-id="78f0b-104">Cost categories used in Production control and Project management accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78f0b-105">Dažus ražošanas darba veidus var saistīt ar projekta laika aprēķiniem un pārskatu sagatavošanu.</span><span class="sxs-lookup"><span data-stu-id="78f0b-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="78f0b-106">Šajā rakstā ir sniegta informācija par izmaksu kategorijām, kas jānorāda šādiem ražošanas un projekta nolūkiem paredzētiem ražošanas darba veidiem.</span><span class="sxs-lookup"><span data-stu-id="78f0b-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="78f0b-107">Dažus ražošanas darba veidus var saistīt ar projekta laika aprēķiniem un pārskatu sagatavošanu.</span><span class="sxs-lookup"><span data-stu-id="78f0b-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="78f0b-108">Šajā gadījumā izmaksu kategorija ir nepieciešama ražošanas un projekta mērķiem.</span><span class="sxs-lookup"><span data-stu-id="78f0b-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="78f0b-109">Ja ražošanā un projektos tiek izmantota izmaksu kategorija, ir jānorāda ar projektu saistīta papildu informācija.</span><span class="sxs-lookup"><span data-stu-id="78f0b-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="78f0b-110">Piemēram, ar projektiem saistītās stundu izmaksas var atšķirties no ar ražošanu saistītajām stundu izmaksām.</span><span class="sxs-lookup"><span data-stu-id="78f0b-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="78f0b-111">Lai noteiktu izmaksu kategoriju, ko izmanto lapā Ražošanas kontrole un Projekta pārvaldības uzskaite, var izmantot lapu **Izmaksu kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="78f0b-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> 

<span data-ttu-id="78f0b-112">**Piezīme.** Izmaksu uzskaite ir pieejama lapā **Projektu kategorijas**, bet šī lapa nav saistīta ar šajā tēmā aprakstīto funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="78f0b-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="78f0b-113">Izmantojot projektos izmaksu kategoriju, lapā **Izmaksu kategorijas** ir pieejamas papildu cilnes, kurās ir redzama ar projektu saistīta papildu informācija.</span><span class="sxs-lookup"><span data-stu-id="78f0b-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="78f0b-114">Šajā informācijā ir iekļauta izmaksu kategorijai piešķirtā kategoriju grupa, rindas rekvizīts un virsgrāmatas konti.</span><span class="sxs-lookup"><span data-stu-id="78f0b-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="78f0b-115">Izmaksu kategorija ir jāpiešķir kategoriju grupai, kas atbalsta transakcijas tipu **Stundas**.</span><span class="sxs-lookup"><span data-stu-id="78f0b-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="78f0b-116">Rindas rekvizīts norāda noklusējuma informāciju par to, kā pārskatā iekļautās laika izmaksas var piešķirt projektam.</span><span class="sxs-lookup"><span data-stu-id="78f0b-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="78f0b-117">Parasti izmaksu kategorijai piešķirtajai kategoriju grupai tiek definēti ar izmaksām un pārdošanu saistītie virsgrāmatas konti.</span><span class="sxs-lookup"><span data-stu-id="78f0b-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="78f0b-118">Tomēr atsevišķai izmaksu kategorijai var norādīt noteiktus kontus.</span><span class="sxs-lookup"><span data-stu-id="78f0b-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="78f0b-119">Papildu pogas lapā **Izmaksu kategorijas** ļauj piekļūt ar projektu saistītai informācijai par atlasīto izmaksu kategoriju.</span><span class="sxs-lookup"><span data-stu-id="78f0b-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="78f0b-120">Piemēram, var skatīt ar projektu saistītas transakcijas, definēt darbiniekus vai projektus, noteikt stundu izmaksas un pārdošanas cenas un skatīt pārskatus.</span><span class="sxs-lookup"><span data-stu-id="78f0b-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>




