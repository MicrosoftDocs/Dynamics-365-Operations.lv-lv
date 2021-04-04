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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5afcb8171b674281faf8100d5c01fdff8d6ff764
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470789"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="46695-103">Veidnes MK izveide</span><span class="sxs-lookup"><span data-stu-id="46695-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="46695-104">Veidnes MK var izveidot, izmantojot jebkuru no tālāk aprakstītajām metodēm.</span><span class="sxs-lookup"><span data-stu-id="46695-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="46695-105">Visām metodēm lauki **Sākuma datums** un **Beigu datums** ir neobligāti un paredzēti tikai informācijai.</span><span class="sxs-lookup"><span data-stu-id="46695-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="46695-106">Manuāla veidnes MK izveide</span><span class="sxs-lookup"><span data-stu-id="46695-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="46695-107">Dodieties uz **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.</span><span class="sxs-lookup"><span data-stu-id="46695-107">Go to **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="46695-108">Atlasiet **Jauns**, lai atvērtu veidlapu **Izveidot MK veidni**.</span><span class="sxs-lookup"><span data-stu-id="46695-108">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="46695-109">Sadaļā **Kopēt MK rindas no atsauces** atlasiet opciju **Manuāli**.</span><span class="sxs-lookup"><span data-stu-id="46695-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="46695-110">Laukā **Krājuma kods** ievadiet **MK** tipa krājumu.</span><span class="sxs-lookup"><span data-stu-id="46695-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="46695-111">Laukā **Nosaukums** ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="46695-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="46695-112">Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="46695-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="46695-113">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="46695-113">Select **OK**.</span></span>

<span data-ttu-id="46695-114">Tiek izveidots jauns, tukšs veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="46695-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="46695-115">Veidnes MK izveide uz citas veidnes MK pamata</span><span class="sxs-lookup"><span data-stu-id="46695-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="46695-116">Atlasiet **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.</span><span class="sxs-lookup"><span data-stu-id="46695-116">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="46695-117">Atlasiet **Jauns**, lai atvērtu veidlapu **Izveidot MK veidni**.</span><span class="sxs-lookup"><span data-stu-id="46695-117">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="46695-118">Sadaļā **Kopēt MK rindas no atsauces** atlasiet opciju **Veidnes MK**.</span><span class="sxs-lookup"><span data-stu-id="46695-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="46695-119">Laukā **Atsauces numurs** atlasiet jau izveidotu veidnes MK, kuru kopēt uz jauno veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="46695-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="46695-120">Laukā **Nosaukums** ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="46695-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="46695-121">Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="46695-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="46695-122">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="46695-122">Select **OK**.</span></span>

<span data-ttu-id="46695-123">Tiek izveidots jauns veidnes MK, izmantojot rindas, kas atbilst rindām oriģinālajā veidnes MK.</span><span class="sxs-lookup"><span data-stu-id="46695-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="46695-124">Veidnes MK izveide uz krājuma MK pamata</span><span class="sxs-lookup"><span data-stu-id="46695-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="46695-125">Atlasiet **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.</span><span class="sxs-lookup"><span data-stu-id="46695-125">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="46695-126">Atlasiet **Jauns**, lai atvērtu veidlapu **Izveidot MK veidni**.</span><span class="sxs-lookup"><span data-stu-id="46695-126">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="46695-127">Sadaļā **Kopēt MK rindas no atsauces** atlasiet **MK**.</span><span class="sxs-lookup"><span data-stu-id="46695-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="46695-128">Laukā **Atsauces numurs** atlasiet MK versiju.</span><span class="sxs-lookup"><span data-stu-id="46695-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="46695-129">Krājums ar tipu MK tiek kopēts laukā **Krājuma kods**.</span><span class="sxs-lookup"><span data-stu-id="46695-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="46695-130">Laukā **Nosaukums** ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="46695-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="46695-131">Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="46695-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="46695-132">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="46695-132">Select **OK**.</span></span>

<span data-ttu-id="46695-133">Tiek izveidots jauns veidnes MK, izmantojot rindas, kas atbilst sarakstā **Materiālu komplekti** esošajām MK rindām.</span><span class="sxs-lookup"><span data-stu-id="46695-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="46695-134">Veidnes MK izveide uz ražošanas MK pamata</span><span class="sxs-lookup"><span data-stu-id="46695-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="46695-135">Atlasiet **Pakalpojumu pārvaldība** \> **Iestatījumi** \> **Pakalpojumu objekti** \> **Veidņu MK**.</span><span class="sxs-lookup"><span data-stu-id="46695-135">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="46695-136">Atlasiet **Jauns**, lai atvērtu veidlapu **Izveidot MK veidni**.</span><span class="sxs-lookup"><span data-stu-id="46695-136">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="46695-137">Sadaļā **Kopēt MK rindas no atsauces** atlasiet **Ražošana**.</span><span class="sxs-lookup"><span data-stu-id="46695-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="46695-138">Laukā **Atsauces numurs** atlasiet ražošanas MK.</span><span class="sxs-lookup"><span data-stu-id="46695-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="46695-139">Laukā **Nosaukums** ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="46695-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="46695-140">Laukos **Sākuma datums** un **Beigu datums** ievadiet datumu intervālu, kurā veidnes MK ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="46695-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="46695-141">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="46695-141">Select **OK**.</span></span>

<span data-ttu-id="46695-142">Tiek izveidots jauns veidnes MK, izmantojot rindas, kas atbilst sarakstā **MK** esošajām MK rindām.</span><span class="sxs-lookup"><span data-stu-id="46695-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="46695-143">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="46695-143">See also</span></span>

[<span data-ttu-id="46695-144">Veidnes MK</span><span class="sxs-lookup"><span data-stu-id="46695-144">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]