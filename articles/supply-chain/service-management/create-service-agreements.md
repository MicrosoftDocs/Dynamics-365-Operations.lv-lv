---
title: "Pakalpojumu līgumu izveide"
description: "Šajā tēmā ir aprakstīts, kā lietot līdzekļus moduļos Pakalpojumu pārvaldība un Projektu pārvaldība un uzskaite, lai izveidotu pakalpojumu līgumus."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a3d848b0cfebd190f1aa1d8aa6717d9cf3b80685
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-agreements"></a><span data-ttu-id="213af-103">Pakalpojumu līgumu izveide</span><span class="sxs-lookup"><span data-stu-id="213af-103">Create service agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="213af-104">Šajā tēmā ir aprakstīts, kā lietot līdzekļus moduļos Pakalpojumu pārvaldība un Projektu pārvaldība un uzskaite, lai izveidotu pakalpojumu līgumus.</span><span class="sxs-lookup"><span data-stu-id="213af-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="213af-105">Izveidot pakalpojumu līgumu no pakalpojumu pārvaldības</span><span class="sxs-lookup"><span data-stu-id="213af-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="213af-106">Pārejiet uz **Pakalpojumu vadība**.</span><span class="sxs-lookup"><span data-stu-id="213af-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="213af-107">Noklikšķiniet uz **Pakalpojumu līgumi**, lai izveidotu jaunu pakalpojumu līguma rindu lapas galvenē.</span><span class="sxs-lookup"><span data-stu-id="213af-107">Click **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="213af-108">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="213af-108">Click **New**.</span></span> <span data-ttu-id="213af-109">Ievadiet aprakstu, atlasiet atsauci uz projektu laukā **Projekta ID** un aizpildiet atlikušos laukus un rindas pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="213af-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="213af-110">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="213af-110">Click **Save**.</span></span>
4. <span data-ttu-id="213af-111">Cilnē **Relācijas** atlasiet **Pakalpojumu objekti** vai **Pakalpojumu uzdevumi**, lai izveidotu pakalpojumu objektu relācijas vai pakalpojumu uzdevumu relācijas pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="213af-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="213af-112">Pakalpojuma objekti un uzdevumi ar izveidotām saistībām var tikt pievienoti pakalpojumu līguma rindām.</span><span class="sxs-lookup"><span data-stu-id="213af-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="213af-113">Lapas apakšējā pusē izveidojiet pakalpojumu līguma rindas nokopējot rindas no pakalpojuma veidnes vai arī pašrocīgi izveidojot pakalpojumu līguma rindas.</span><span class="sxs-lookup"><span data-stu-id="213af-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="213af-114">Ja pakalpojumu līgumā rindas tiek iekopētas no cita pakalpojumu līguma, ir iespējams norādīt vai vēlaties kopēt arī pakalpojuma objekta un pakalpojuma uzdevumu relācijas.</span><span class="sxs-lookup"><span data-stu-id="213af-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="213af-115">Ja šīs saistības tiek kopētas, tās tiek pievienotas esošajām saistībām pakalpojumu līgumā.</span><span class="sxs-lookup"><span data-stu-id="213af-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="213af-116">Ja pakalpojumu līguma rindas tiek kopētas no pakalpojuma veidnes, tad pakalpojuma objekta un pakalpojumu uzdevuma saistības tiek automātiski pārkopētas kā pakalpojumu objekta saistības un pakalpojumu uzdevuma saistības jaunā pakalpojumu līguma rindās.</span><span class="sxs-lookup"><span data-stu-id="213af-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="213af-117">Pakalpojuma līguma rindu manuāla izveide</span><span class="sxs-lookup"><span data-stu-id="213af-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="213af-118">Lapā **Pakalpojumu līgumi** rindu režģī pievienojiet pakalpojumu līguma rindu.</span><span class="sxs-lookup"><span data-stu-id="213af-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="213af-119">Ievadiet attiecīgu informāciju par pakalpojumu līgumu rindu.</span><span class="sxs-lookup"><span data-stu-id="213af-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="213af-120">Lai saglabātu rindu un aizvērtu lapu, nospiediet taustiņu kombināciju **CTRL+S**.</span><span class="sxs-lookup"><span data-stu-id="213af-120">Press **CTRL+S** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="213af-121">Pakalpojumu līguma izveide no formas Projekts</span><span class="sxs-lookup"><span data-stu-id="213af-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="213af-122">Noklikšķiniet uz **Projektu pārvaldība un uzskaite**.</span><span class="sxs-lookup"><span data-stu-id="213af-122">Click **Project management and accounting**.</span></span>
2. <span data-ttu-id="213af-123">Noklikšķiniet uz **Visi projekti**.</span><span class="sxs-lookup"><span data-stu-id="213af-123">Click **All projects**.</span></span>
3. <span data-ttu-id="213af-124">Atlasiet projektu no saraksta.</span><span class="sxs-lookup"><span data-stu-id="213af-124">Select the project from the list.</span></span>
4. <span data-ttu-id="213af-125">**Darbību rūtī** noklikšķiniet uz **Pārvaldīt**.</span><span class="sxs-lookup"><span data-stu-id="213af-125">On the **Action Pane**, click **Manage**.</span></span> <span data-ttu-id="213af-126">**Jaunajā** darbību grupā noklikšķiniet uz **Pakalpojums** un atlasiet **Pakalpojuma līgums**.</span><span class="sxs-lookup"><span data-stu-id="213af-126">In the **New** Action group, click **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="213af-127">Lai ievadītu projekta atsauci, izpildiet sadaļā **Pakalpojumu līguma izveidošana** sniegtos norādījumus, kā tika aprakstīts iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="213af-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="213af-128">Saistītās tēmas</span><span class="sxs-lookup"><span data-stu-id="213af-128">Related topics</span></span>

[<span data-ttu-id="213af-129">Pakalpojumu līgumi</span><span class="sxs-lookup"><span data-stu-id="213af-129">Service agreements</span></span>](service-agreements.md)



