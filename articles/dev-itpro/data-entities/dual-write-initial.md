---
title: Izpildes rīkojums Finance and Operations un Common Data Service sākotnējai sinhronizācijai
description: Šajā tēmā ir norādīta sinhronizācijas secība, kas jāizpilda, lai izveidotu sākotnējos datus.
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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797302"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="29428-103">Izpildes rīkojums Finance and Operations un Common Data Service sākotnējai sinhronizācijai</span><span class="sxs-lookup"><span data-stu-id="29428-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="29428-104">Pirms datu integrācijas izmantošanas ir jāizveido sākotnējie dati, kas nepieciešami debitoriem, kreditoriem un kontaktpersonām.</span><span class="sxs-lookup"><span data-stu-id="29428-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="29428-105">Piemēram, ja vēlaties izveidot jaunu vienumu **Kreditoru grupa** un iestatīt tās **Maksāšanas nosacījumus** kā **Net30**, tad, pirms mēģināt izveidot vienumu **Kreditoru grupa**, pārliecinieties, vai **Net30** pastāv gan Finance and Operations, gan Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="29428-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="29428-106">(Turpmāk mēs izlaidīsim duāla ieraksta platformas funkcionalitāti, ko sauc par **Sākotnējo sinhronizāciju.** Tā vienu reizi veiks datu sinhronizāciju starp Finance and Operations un Common Data Service kā daļu no duālā ieraksta iestatīšanas.)</span><span class="sxs-lookup"><span data-stu-id="29428-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="29428-107">Padomi: mēs izlaižam duālā ieraksta karti visiem atsauces datiem, tostarp **Maksāšanas nosacījumiem** (Samaksas noteikumi).</span><span class="sxs-lookup"><span data-stu-id="29428-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="29428-108">Ja jums jau ir sākotnējie dati vienā sistēmā, neliela atjaunināšanas operācija ierakstā var izraisīt duālu ierakstu par šo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="29428-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="29428-109">Jums jāievēro šāda prioritārā secība un jāpārliecinās, ka sākotnējie dati ir pieejami gan programmā Finance and Operations, gan Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="29428-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="29428-110">Kreditors</span><span class="sxs-lookup"><span data-stu-id="29428-110">Vendor</span></span>

<span data-ttu-id="29428-111">Izpildes secība kreditoram ir šāda:</span><span class="sxs-lookup"><span data-stu-id="29428-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="29428-112">Debitors (Organizācija)</span><span class="sxs-lookup"><span data-stu-id="29428-112">Customer (Organization)</span></span>

<span data-ttu-id="29428-113">Izpildes secība debitoram ir šāda:</span><span class="sxs-lookup"><span data-stu-id="29428-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="29428-114">Kontaktpersona</span><span class="sxs-lookup"><span data-stu-id="29428-114">Contact (Person)</span></span>

<span data-ttu-id="29428-115">Izpildes secība kontaktpersonai ir šāda:</span><span class="sxs-lookup"><span data-stu-id="29428-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```
