---
title: Krājumu atgriešana vairākos debitoru pasūtījumos un rēķinos
description: Šajā tēmā ir aprakstīta funkcionalitāte, kas ļauj izmantot atgriešanu vairākos debitoru pasūtījumos un rēķinos programmā Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: e95f06ffaaf2d250b02a8458faa2d9e0b5ef5631
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459459"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="f7e98-103">Krājumu atgriešana vairākos debitoru pasūtījumos un rēķinos</span><span class="sxs-lookup"><span data-stu-id="f7e98-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="f7e98-104">Šajā rakstā ir aprakstīti divi līdzekļi, kas optimizē debitora pasūtījumu atgriešanu vairākos rēķinos.</span><span class="sxs-lookup"><span data-stu-id="f7e98-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="f7e98-105">Iespējot atmaksas vairākos tvērumos</span><span class="sxs-lookup"><span data-stu-id="f7e98-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="f7e98-106">Šis līdzeklis aktivizē vairākas saistītās atmaksas vienā un tajā pašā debitora pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="f7e98-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="f7e98-107">Dodieties uz darbvietu **Līdzekļu pārvaldība** un meklējiet **Iespējot atmaksas vairākos tvērumos**.</span><span class="sxs-lookup"><span data-stu-id="f7e98-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="f7e98-108">Atlasiet **Iespējot atmaksas vairākos pasūtījumos** un pēc tam noklikšķiniet uz **Iespējot**.</span><span class="sxs-lookup"><span data-stu-id="f7e98-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="f7e98-109">Iespējot pareizu nodokļu aprēķināšanu daļējai atgriešanai</span><span class="sxs-lookup"><span data-stu-id="f7e98-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="f7e98-110">Šis līdzeklis nodrošina, ka gadījumā, ja pasūtījums tiek atgriezts vairākus rēķinos, nodokļi beigās būs vienādi ar sākotnēji iekasēto nodokļu summu.</span><span class="sxs-lookup"><span data-stu-id="f7e98-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="f7e98-111">Dodieties uz darbvietu **Līdzekļu pārvaldība** un meklējiet **Iespējot pareizu nodokļu aprēķināšanu daļējai atgriešanai**.</span><span class="sxs-lookup"><span data-stu-id="f7e98-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="f7e98-112">Atlasiet **Iespējot pareizu nodokļu aprēķināšanu daļējai atgriešanai** un pēc tam noklikšķiniet uz **Iespējot**.</span><span class="sxs-lookup"><span data-stu-id="f7e98-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="f7e98-113">Atgriešanu apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="f7e98-113">Process returns</span></span>

<span data-ttu-id="f7e98-114">Kad šie līdzekļi ir ieslēgti un izmaiņas ir sinhronizētas uz veikaliem, kasieris veikalā var atlasīt vairākus pārdošanas pasūtījumus vienam debitoram, lai tos atgrieztu.</span><span class="sxs-lookup"><span data-stu-id="f7e98-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="f7e98-115">Kad pasūtījumi ir atlasīti, tiek parādīts saraksts ar visām atgriežamajām precēm visos šo pasūtījumu rēķinos.</span><span class="sxs-lookup"><span data-stu-id="f7e98-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="f7e98-116">Pēc tam kasieris var atlasīt atgriežamās preces.</span><span class="sxs-lookup"><span data-stu-id="f7e98-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="f7e98-117">Visām atlasītajām precēm tiks izveidots viens atgriešanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="f7e98-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="f7e98-118">Ja pasūtījums tiek pilnībā atgriezts, debitoram atgriezto nodokļu summa būs vienāda ar sākotnēji iekasēto nodokļu summu.</span><span class="sxs-lookup"><span data-stu-id="f7e98-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>

