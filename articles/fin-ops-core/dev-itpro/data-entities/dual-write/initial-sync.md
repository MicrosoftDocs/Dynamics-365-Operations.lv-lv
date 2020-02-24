---
title: Izpildes pasūtījums Finance and Operations programmu un Common Data Service sākotnējai sinhronizācijai.
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
ms.openlocfilehash: befe4e12a10f4a39b90bcb4faba6431a063a40e2
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019900"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="0ce64-103">Izpildes pasūtījums Finance and Operations programmu un Common Data Service sākotnējai sinhronizācijai.</span><span class="sxs-lookup"><span data-stu-id="0ce64-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="0ce64-104">Pirms datu integrācijas izmantošanas izveidojiet sākotnējos datus, kas nepieciešami klientiem, piegādātājiem un kontaktpersonām.</span><span class="sxs-lookup"><span data-stu-id="0ce64-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="0ce64-105">Piemēram, jūs vēlaties izveidot jaunu vienumu **Piegādātāju grupa** un iestatīt tās vērtību **Apmaksas nosacījumi** uz **Net30**.</span><span class="sxs-lookup"><span data-stu-id="0ce64-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="0ce64-106">Šajā gadījumā pirms mēģināt izveidot vienumu **Piegādātāju grupa**, nodrošiniet, lai **Net30** ir atrodams gan programmā, gan Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0ce64-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="0ce64-107">(Nākotnē korporācija Microsoft izlaidīs duālās rakstīšanas funkcionalitāti ar nosaukumu Sākotnējā sinhronizācija. Šī funkcionalitāte veiks vienreizēju datu sinhronizāciju starp programmu un Common Data Service duālās rakstīšanas iestatīšanas gaitā.)</span><span class="sxs-lookup"><span data-stu-id="0ce64-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="0ce64-108">Korporācija Microsoft izlaiž duālās rakstīšanas kartējumu visiem atsauces datiem, tostarp **Apmaksas nosacījumiem** (maksājuma nosacījumiem).</span><span class="sxs-lookup"><span data-stu-id="0ce64-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="0ce64-109">Ja jums jau ir sākotnējie dati vienā sistēmā, neliela atjaunināšanas operācija ierakstā var izraisīt duālu ierakstu par šo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="0ce64-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="0ce64-110">Jums ir jāievēro šāda prioritārā secība, lai nodrošinātu, ka sākotnējie dati ir pieejami gan programmā, gan Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0ce64-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="0ce64-111">Kreditors</span><span class="sxs-lookup"><span data-stu-id="0ce64-111">Vendor</span></span>

<span data-ttu-id="0ce64-112">Izpildes secība entītijai **Piegādātājs**:</span><span class="sxs-lookup"><span data-stu-id="0ce64-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="0ce64-113">Kreditoru grupa</span><span class="sxs-lookup"><span data-stu-id="0ce64-113">Vendor group</span></span>

    1. <span data-ttu-id="0ce64-114">Apmaksas nosacījumi</span><span class="sxs-lookup"><span data-stu-id="0ce64-114">Terms of payment</span></span>

        1. <span data-ttu-id="0ce64-115">Maksāšanas diena un rindas</span><span class="sxs-lookup"><span data-stu-id="0ce64-115">Payment day and lines</span></span>
        2. <span data-ttu-id="0ce64-116">Maksājumu grafiks</span><span class="sxs-lookup"><span data-stu-id="0ce64-116">Payment schedule</span></span>

2. <span data-ttu-id="0ce64-117">Piegādātāja maksāšanas metode</span><span class="sxs-lookup"><span data-stu-id="0ce64-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="0ce64-118">Debitors (Organizācija)</span><span class="sxs-lookup"><span data-stu-id="0ce64-118">Customer (Organization)</span></span>

<span data-ttu-id="0ce64-119">Izpildes secība entītijai **Klients**:</span><span class="sxs-lookup"><span data-stu-id="0ce64-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="0ce64-120">Debitoru grupa</span><span class="sxs-lookup"><span data-stu-id="0ce64-120">Customer group</span></span>

    1. <span data-ttu-id="0ce64-121">Apmaksas nosacījumi</span><span class="sxs-lookup"><span data-stu-id="0ce64-121">Terms of payment</span></span>

        1. <span data-ttu-id="0ce64-122">Maksāšanas diena un rindas</span><span class="sxs-lookup"><span data-stu-id="0ce64-122">Payment day and lines</span></span>
        2. <span data-ttu-id="0ce64-123">Maksājums</span><span class="sxs-lookup"><span data-stu-id="0ce64-123">Payment</span></span> 

2. <span data-ttu-id="0ce64-124">Debitora maksāšanas metode</span><span class="sxs-lookup"><span data-stu-id="0ce64-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="0ce64-125">Kontaktpersona</span><span class="sxs-lookup"><span data-stu-id="0ce64-125">Contact (Person)</span></span>

<span data-ttu-id="0ce64-126">Izpildes secība entītijai **Kontaktpersona**:</span><span class="sxs-lookup"><span data-stu-id="0ce64-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="0ce64-127">Debitors</span><span class="sxs-lookup"><span data-stu-id="0ce64-127">Customer</span></span>
2. <span data-ttu-id="0ce64-128">Kreditors</span><span class="sxs-lookup"><span data-stu-id="0ce64-128">Vendor</span></span>
