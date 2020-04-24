---
title: Veidnes MK izveide
description: Veidnes MK var izveidot, izmantojot vairākas metodes.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 815b6b726e9a76a9294995bc5689b030cf623ec0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202587"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="48c05-103">Veidnes MK izveide</span><span class="sxs-lookup"><span data-stu-id="48c05-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="48c05-104">Veidnes MK var izveidot, izmantojot jebkuru no tālāk aprakstītajām metodēm.</span><span class="sxs-lookup"><span data-stu-id="48c05-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="48c05-105">Visām metodēm lauki **Sākuma datums** un **Beigu datums** ir neobligāti un paredzēti tikai informācijai.</span><span class="sxs-lookup"><span data-stu-id="48c05-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="48c05-106">Manuāla veidnes MK izveide</span><span class="sxs-lookup"><span data-stu-id="48c05-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="48c05-107">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.</span><span class="sxs-lookup"><span data-stu-id="48c05-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="48c05-108">Nospiediet taustiņu kombināciju CTRL + N, lai atvērtu veidlapu **Veidnes MK izveide**.</span><span class="sxs-lookup"><span data-stu-id="48c05-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="48c05-109">Sadaļā **Kopēt MK rindas no atsauces** atlasiet opciju **Manuāli**.</span><span class="sxs-lookup"><span data-stu-id="48c05-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="48c05-110">Laukā **Krājuma kods** ievadiet **MK** tipa krājumu.</span><span class="sxs-lookup"><span data-stu-id="48c05-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="48c05-111">Laukā **Nosaukums** ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="48c05-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="48c05-112">Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="48c05-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="48c05-113">Noklikšķiniet uz **OK**.</span><span class="sxs-lookup"><span data-stu-id="48c05-113">Click **OK**.</span></span>

<span data-ttu-id="48c05-114">Tiek izveidots jauns, tukšs veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="48c05-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="48c05-115">Veidnes MK izveide uz citas veidnes MK pamata</span><span class="sxs-lookup"><span data-stu-id="48c05-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="48c05-116">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.</span><span class="sxs-lookup"><span data-stu-id="48c05-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="48c05-117">Nospiediet taustiņu kombināciju CTRL + N, lai atvērtu veidlapu **Veidnes MK izveide**.</span><span class="sxs-lookup"><span data-stu-id="48c05-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="48c05-118">Sadaļā **Kopēt MK rindas no atsauces** atlasiet opciju **Veidnes MK**.</span><span class="sxs-lookup"><span data-stu-id="48c05-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="48c05-119">Laukā **Atsauces numurs** atlasiet jau izveidotu veidnes MK, kuru kopēt uz jauno veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="48c05-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="48c05-120">Laukā **Nosaukums** ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="48c05-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="48c05-121">Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="48c05-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="48c05-122">Noklikšķiniet uz **OK**.</span><span class="sxs-lookup"><span data-stu-id="48c05-122">Click **OK**.</span></span>

<span data-ttu-id="48c05-123">Tiek izveidots jauns veidnes MK, izmantojot rindas, kas atbilst rindām oriģinālajā veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="48c05-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="48c05-124">Veidnes MK izveide uz krājuma MK pamata</span><span class="sxs-lookup"><span data-stu-id="48c05-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="48c05-125">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.</span><span class="sxs-lookup"><span data-stu-id="48c05-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="48c05-126">Nospiediet taustiņu kombināciju CTRL + N, lai atvērtu veidlapu **Veidnes MK izveide**.</span><span class="sxs-lookup"><span data-stu-id="48c05-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="48c05-127">Sadaļā **Kopēt MK rindas no atsauces** atlasiet **MK**.</span><span class="sxs-lookup"><span data-stu-id="48c05-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="48c05-128">Laukā **Atsauces numurs** atlasiet MK versiju.</span><span class="sxs-lookup"><span data-stu-id="48c05-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="48c05-129">Krājums ar tipu MK tiek kopēts laukā **Krājuma kods**.</span><span class="sxs-lookup"><span data-stu-id="48c05-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="48c05-130">Laukā **Nosaukums** ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="48c05-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="48c05-131">Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="48c05-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="48c05-132">Noklikšķiniet uz **OK**.</span><span class="sxs-lookup"><span data-stu-id="48c05-132">Click **OK**.</span></span>

<span data-ttu-id="48c05-133">Tiek izveidots jauns veidnes MK, izmantojot rindas, kas atbilst sarakstā**Materiālu komplekti** esošajām MK rindām.</span><span class="sxs-lookup"><span data-stu-id="48c05-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="48c05-134">Veidnes MK izveide uz ražošanas MK pamata</span><span class="sxs-lookup"><span data-stu-id="48c05-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="48c05-135">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.</span><span class="sxs-lookup"><span data-stu-id="48c05-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="48c05-136">Nospiediet taustiņu kombināciju CTRL + N, lai atvērtu veidlapu **Veidnes MK izveide**.</span><span class="sxs-lookup"><span data-stu-id="48c05-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="48c05-137">Sadaļā **Kopēt MK rindas no atsauces** atlasiet **Ražošana**.</span><span class="sxs-lookup"><span data-stu-id="48c05-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="48c05-138">Laukā **Atsauces numurs** atlasiet ražošanas MK.</span><span class="sxs-lookup"><span data-stu-id="48c05-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="48c05-139">Laukā **Nosaukums** ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="48c05-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="48c05-140">Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="48c05-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="48c05-141">Noklikšķiniet uz **OK**.</span><span class="sxs-lookup"><span data-stu-id="48c05-141">Click **OK**.</span></span>

<span data-ttu-id="48c05-142">Tiek izveidots jauns veidnes MK, izmantojot rindas, kas atbilst sarakstā **MK** esošajām MK rindām.</span><span class="sxs-lookup"><span data-stu-id="48c05-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="48c05-143">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="48c05-143">See also</span></span>

[<span data-ttu-id="48c05-144">Veidnes MK </span><span class="sxs-lookup"><span data-stu-id="48c05-144">Template BOMs</span></span>](template-boms.md)

  


