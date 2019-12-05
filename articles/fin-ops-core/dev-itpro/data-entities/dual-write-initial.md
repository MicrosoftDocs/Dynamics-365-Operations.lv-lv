---
title: Izpildes pasūtījums programmu Finance and Operations un Common Data Service sākotnējai sinhronizācijai.
description: Šajā tēmā ir norādīta sinhronizācijas kārtība, kura ir jāievēro sākotnējo datu izveidei.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: cf444ef1192fed3a6a49282da37374dd8c443356
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769641"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="4c146-103">Izpildes pasūtījums programmu Finance and Operations un Common Data Service sākotnējai sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="4c146-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c146-104">Pirms datu integrācijas izmantošanas izveidojiet sākotnējos datus, kas nepieciešami klientiem, piegādātājiem un kontaktpersonām.</span><span class="sxs-lookup"><span data-stu-id="4c146-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="4c146-105">Piemēram, jūs vēlaties izveidot jaunu vienumu **Piegādātāju grupa** un iestatīt tās vērtību **Apmaksas nosacījumi** uz **Net30**.</span><span class="sxs-lookup"><span data-stu-id="4c146-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="4c146-106">Šajā gadījumā pirms mēģināt izveidot vienumu **Piegādātāju grupa**, nodrošiniet, lai **Net30** ir atrodams gan programmā, gan Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4c146-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="4c146-107">(Nākotnē korporācija Microsoft izlaidīs duālās rakstīšanas funkcionalitāti ar nosaukumu Sākotnējā sinhronizācija. Šī funkcionalitāte veiks vienreizēju datu sinhronizāciju starp programmu un Common Data Service duālās rakstīšanas iestatīšanas gaitā.)</span><span class="sxs-lookup"><span data-stu-id="4c146-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="4c146-108">Korporācija Microsoft izlaiž duālās rakstīšanas kartējumu visiem atsauces datiem, tostarp **Apmaksas nosacījumiem** (maksājuma nosacījumiem).</span><span class="sxs-lookup"><span data-stu-id="4c146-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="4c146-109">Ja jums jau ir sākotnējie dati vienā sistēmā, neliela atjaunināšanas operācija ierakstā var izraisīt duālu ierakstu par šo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="4c146-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="4c146-110">Jums ir jāievēro šāda prioritārā secība, lai nodrošinātu, ka sākotnējie dati ir pieejami gan programmā, gan Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4c146-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="4c146-111">Kreditors</span><span class="sxs-lookup"><span data-stu-id="4c146-111">Vendor</span></span>

<span data-ttu-id="4c146-112">Izpildes secība entītijai **Piegādātājs**:</span><span class="sxs-lookup"><span data-stu-id="4c146-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="4c146-113">Kreditoru grupa</span><span class="sxs-lookup"><span data-stu-id="4c146-113">Vendor group</span></span>

    1. <span data-ttu-id="4c146-114">Apmaksas nosacījumi</span><span class="sxs-lookup"><span data-stu-id="4c146-114">Terms of payment</span></span>

        1. <span data-ttu-id="4c146-115">Maksāšanas diena un rindas</span><span class="sxs-lookup"><span data-stu-id="4c146-115">Payment day and lines</span></span>
        2. <span data-ttu-id="4c146-116">Maksājumu grafiks</span><span class="sxs-lookup"><span data-stu-id="4c146-116">Payment schedule</span></span>

2. <span data-ttu-id="4c146-117">Piegādātāja maksāšanas metode</span><span class="sxs-lookup"><span data-stu-id="4c146-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="4c146-118">Debitors (Organizācija)</span><span class="sxs-lookup"><span data-stu-id="4c146-118">Customer (Organization)</span></span>

<span data-ttu-id="4c146-119">Izpildes secība entītijai **Klients**:</span><span class="sxs-lookup"><span data-stu-id="4c146-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="4c146-120">Debitoru grupa</span><span class="sxs-lookup"><span data-stu-id="4c146-120">Customer group</span></span>

    1. <span data-ttu-id="4c146-121">Apmaksas nosacījumi</span><span class="sxs-lookup"><span data-stu-id="4c146-121">Terms of payment</span></span>

        1. <span data-ttu-id="4c146-122">Maksāšanas diena un rindas</span><span class="sxs-lookup"><span data-stu-id="4c146-122">Payment day and lines</span></span>
        2. <span data-ttu-id="4c146-123">Maksājums</span><span class="sxs-lookup"><span data-stu-id="4c146-123">Payment</span></span> 

2. <span data-ttu-id="4c146-124">Debitora maksāšanas metode</span><span class="sxs-lookup"><span data-stu-id="4c146-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="4c146-125">Kontaktpersona</span><span class="sxs-lookup"><span data-stu-id="4c146-125">Contact (Person)</span></span>

<span data-ttu-id="4c146-126">Izpildes secība entītijai **Kontaktpersona**:</span><span class="sxs-lookup"><span data-stu-id="4c146-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="4c146-127">Debitors</span><span class="sxs-lookup"><span data-stu-id="4c146-127">Customer</span></span>
2. <span data-ttu-id="4c146-128">Kreditors</span><span class="sxs-lookup"><span data-stu-id="4c146-128">Vendor</span></span>
