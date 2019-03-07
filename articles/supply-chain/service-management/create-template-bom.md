---
title: Veidnes MK izveide
description: Veidnes MK var izveidot, izmantojot vairākas metodes.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89c5d45ac27a8678c51fb63c0326c2802a094596
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "320999"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="6c8b1-103">Veidnes MK izveide</span><span class="sxs-lookup"><span data-stu-id="6c8b1-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6c8b1-104">Veidnes MK var izveidot, izmantojot jebkuru no tālāk aprakstītajām metodēm.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="6c8b1-105">Visām metodēm lauki **Sākuma datums** un **Beigu datums** ir neobligāti un paredzēti tikai informācijai.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="6c8b1-106">Manuāla veidnes MK izveide</span><span class="sxs-lookup"><span data-stu-id="6c8b1-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="6c8b1-107">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="6c8b1-108">Nospiediet taustiņu kombināciju CTRL + N, lai atvērtu veidlapu **Veidnes MK izveide**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="6c8b1-109">Sadaļā **Kopēt MK rindas no atsauces** atlasiet opciju **Manuāli**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="6c8b1-110">Laukā **Krājuma kods** ievadiet **MK** tipa krājumu.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="6c8b1-111">Laukā **Nosaukums** ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="6c8b1-112">Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="6c8b1-113">Noklikšķiniet uz **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-113">Click **OK**.</span></span>

<span data-ttu-id="6c8b1-114">Tiek izveidots jauns, tukšs veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="6c8b1-115">Veidnes MK izveide uz citas veidnes MK pamata</span><span class="sxs-lookup"><span data-stu-id="6c8b1-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="6c8b1-116">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="6c8b1-117">Nospiediet taustiņu kombināciju CTRL + N, lai atvērtu veidlapu **Veidnes MK izveide**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="6c8b1-118">Sadaļā **Kopēt MK rindas no atsauces** atlasiet opciju **Veidnes MK**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="6c8b1-119">Laukā **Atsauces numurs** atlasiet jau izveidotu veidnes MK, kuru kopēt uz jauno veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="6c8b1-120">Laukā **Nosaukums** ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="6c8b1-121">Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="6c8b1-122">Noklikšķiniet uz **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-122">Click **OK**.</span></span>

<span data-ttu-id="6c8b1-123">Tiek izveidots jauns veidnes MK, izmantojot rindas, kas atbilst rindām oriģinālajā veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="6c8b1-124">Veidnes MK izveide uz krājuma MK pamata</span><span class="sxs-lookup"><span data-stu-id="6c8b1-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="6c8b1-125">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="6c8b1-126">Nospiediet taustiņu kombināciju CTRL + N, lai atvērtu veidlapu **Veidnes MK izveide**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="6c8b1-127">Sadaļā **Kopēt MK rindas no atsauces** atlasiet **MK**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="6c8b1-128">Laukā **Atsauces numurs** atlasiet MK versiju.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="6c8b1-129">Krājums ar tipu MK tiek kopēts laukā **Krājuma kods**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="6c8b1-130">Laukā **Nosaukums** ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="6c8b1-131">Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="6c8b1-132">Noklikšķiniet uz **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-132">Click **OK**.</span></span>

<span data-ttu-id="6c8b1-133">Tiek izveidots jauns veidnes MK, izmantojot rindas, kas atbilst sarakstā**Materiālu komplekti** esošajām MK rindām.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="6c8b1-134">Veidnes MK izveide uz ražošanas MK pamata</span><span class="sxs-lookup"><span data-stu-id="6c8b1-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="6c8b1-135">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="6c8b1-136">Nospiediet taustiņu kombināciju CTRL + N, lai atvērtu veidlapu **Veidnes MK izveide**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="6c8b1-137">Sadaļā **Kopēt MK rindas no atsauces** atlasiet **Ražošana**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="6c8b1-138">Laukā **Atsauces numurs** atlasiet ražošanas MK.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="6c8b1-139">Laukā **Nosaukums** ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="6c8b1-140">Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="6c8b1-141">Noklikšķiniet uz **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-141">Click **OK**.</span></span>

<span data-ttu-id="6c8b1-142">Tiek izveidots jauns veidnes MK, izmantojot rindas, kas atbilst sarakstā **MK** esošajām MK rindām.</span><span class="sxs-lookup"><span data-stu-id="6c8b1-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c8b1-143">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="6c8b1-143">See also</span></span>

[<span data-ttu-id="6c8b1-144">Veidnes MK </span><span class="sxs-lookup"><span data-stu-id="6c8b1-144">Template BOMs</span></span>](template-boms.md)

  


