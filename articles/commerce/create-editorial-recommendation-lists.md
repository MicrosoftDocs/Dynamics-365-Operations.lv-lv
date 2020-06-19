---
title: Manuāli izveidot pārraudzītus ieteikumus
description: Šajā tēmā izskaidrots, kā prečzinis var manuāli izveidot un pārvaldīt preču sarakstus Microsoft Dynamics 365 Commerce klientiem.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0b866704b419fb07dcf1ddd386af2f7d6cfa02e2
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404120"
---
# <a name="manually-create-curated-recommendations"></a><span data-ttu-id="70030-103">Manuāli izveidot pārraudzītus ieteikumus</span><span class="sxs-lookup"><span data-stu-id="70030-103">Manually create curated recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="70030-104">Šajā tēmā izskaidrots, kā prečzinis var manuāli izveidot un pārvaldīt preču ieteikumu sarakstus Microsoft Dynamics 365 Commerce klientiem.</span><span class="sxs-lookup"><span data-stu-id="70030-104">This topic explains how merchandizers can manually create and manage product recommendations lists for Microsoft Dynamics 365 Commerce customers.</span></span>

<span data-ttu-id="70030-105">Pārraudzīti saraksti ir atsevišķa satura kolekcijas, ko veido un pārrauga cilvēki.</span><span class="sxs-lookup"><span data-stu-id="70030-105">Curated lists are collections of individual content, created and curated by people.</span></span>  

## <a name="create-a-new-list"></a><span data-ttu-id="70030-106">Jauna saraksta izveide</span><span class="sxs-lookup"><span data-stu-id="70030-106">Create a new list</span></span>

<span data-ttu-id="70030-107">Lai izveidotu pārvaldītu preču rekomendāciju sarakstu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="70030-107">To create a curated product recommendation list, follow these steps.</span></span>

1. <span data-ttu-id="70030-108">Pärejiet uz **Mazumtirdzniecība un komercija &gt; Preču ieteikumi &gt; Ieteikumu saraksti**.</span><span class="sxs-lookup"><span data-stu-id="70030-108">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation lists**.</span></span>
1. <span data-ttu-id="70030-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="70030-109">Select **New**.</span></span>
1. <span data-ttu-id="70030-110">Ievadiet vērtību laukā **Saraksta ID**.</span><span class="sxs-lookup"><span data-stu-id="70030-110">In the **List Id** field, enter a value.</span></span>
1. <span data-ttu-id="70030-111">Ievadiet vērtību laukā **Saraksta nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="70030-111">In the **List name** field, enter a value.</span></span>
    - <span data-ttu-id="70030-112">**Saraksta nosaukums** ir tā saraksta nosaukums, kas parādīsies moduļa **Preču kolekcijas** pārraudzītu sarakstu sadaļā.</span><span class="sxs-lookup"><span data-stu-id="70030-112">The **List name** is the title of the list that will appear in the curated lists section of the **Product collection** module.</span></span>
1. <span data-ttu-id="70030-113">Lai pievienotu preces sarakstam , atlasiet **Pievienot preces**.</span><span class="sxs-lookup"><span data-stu-id="70030-113">To add products to the list, select **Add products**.</span></span>
1. <span data-ttu-id="70030-114">Lai sarakstā mainītu preču secību, ievadiet vērtību kolonnā **Rādīšanas secība**.</span><span class="sxs-lookup"><span data-stu-id="70030-114">To change the order of the products in the list, enter a value in the **Display order** column.</span></span>
    - <span data-ttu-id="70030-115">Ja divām precēm ir tāda pati rādīšanas secības vērtība, tad šo divu rezultātu gala secība var atšķirties no tās, kas ir operāciju uzskaites daļā.</span><span class="sxs-lookup"><span data-stu-id="70030-115">If two products have the same display order value, then the final order of those two results may differ from the back office.</span></span>
1. <span data-ttu-id="70030-116">Atlasiet **Saglabāt**, lai saglabātu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="70030-116">Select **Save** to save the list.</span></span>

## <a name="example-list"></a><span data-ttu-id="70030-117">Saraksta piemērs</span><span class="sxs-lookup"><span data-stu-id="70030-117">Example List</span></span>

![Pārraudzīta saraksta piemērs operāciju uzskaites daļā](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a><span data-ttu-id="70030-119">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="70030-119">Additional resources</span></span>

[<span data-ttu-id="70030-120">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="70030-120">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="70030-121">Iespējojiet Azure Data Lake Storage vidē Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="70030-121">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="70030-122">Iespējot preču ieteikumus</span><span class="sxs-lookup"><span data-stu-id="70030-122">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="70030-123">Personalizētu ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="70030-123">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="70030-124">Atteikšanās no personalizētiem ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="70030-124">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="70030-125">Pievienot preču ieteikumus punktā POS</span><span class="sxs-lookup"><span data-stu-id="70030-125">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="70030-126">Ieteikumu pievienošana transakciju ekrānam</span><span class="sxs-lookup"><span data-stu-id="70030-126">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="70030-127">AI-ML ieteikumu rezultātu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="70030-127">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="70030-128">Izveidot ieteikumus ar demonstrācijas datiem</span><span class="sxs-lookup"><span data-stu-id="70030-128">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="70030-129">Bieži uzdotie jautājumi par preču ieteikumiem</span><span class="sxs-lookup"><span data-stu-id="70030-129">Product recommendations FAQ</span></span>](faq-recommendations.md)
