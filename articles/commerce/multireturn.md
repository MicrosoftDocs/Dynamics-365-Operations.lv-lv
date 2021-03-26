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
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4d1be6606793d498d01be91de6205e3a45c6dfdf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251263"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="b5f44-103">Krājumu atgriešana vairākos debitoru pasūtījumos un rēķinos</span><span class="sxs-lookup"><span data-stu-id="b5f44-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="b5f44-104">Šajā rakstā ir aprakstīti divi līdzekļi, kas optimizē debitora pasūtījumu atgriešanu vairākos rēķinos.</span><span class="sxs-lookup"><span data-stu-id="b5f44-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="b5f44-105">Iespējot atmaksas vairākos tvērumos</span><span class="sxs-lookup"><span data-stu-id="b5f44-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="b5f44-106">Šis līdzeklis aktivizē vairākas saistītās atmaksas vienā un tajā pašā debitora pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="b5f44-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="b5f44-107">Dodieties uz darbvietu **Līdzekļu pārvaldība** un meklējiet **Iespējot atmaksas vairākos tvērumos**.</span><span class="sxs-lookup"><span data-stu-id="b5f44-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="b5f44-108">Atlasiet **Iespējot atmaksas vairākos pasūtījumos** un pēc tam noklikšķiniet uz **Iespējot**.</span><span class="sxs-lookup"><span data-stu-id="b5f44-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="b5f44-109">Iespējot pareizu nodokļu aprēķināšanu daļējai atgriešanai</span><span class="sxs-lookup"><span data-stu-id="b5f44-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="b5f44-110">Šis līdzeklis nodrošina, ka gadījumā, ja pasūtījums tiek atgriezts vairākus rēķinos, nodokļi beigās būs vienādi ar sākotnēji iekasēto nodokļu summu.</span><span class="sxs-lookup"><span data-stu-id="b5f44-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="b5f44-111">Dodieties uz darbvietu **Līdzekļu pārvaldība** un meklējiet **Iespējot pareizu nodokļu aprēķināšanu daļējai atgriešanai**.</span><span class="sxs-lookup"><span data-stu-id="b5f44-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="b5f44-112">Atlasiet **Iespējot pareizu nodokļu aprēķināšanu daļējai atgriešanai** un pēc tam noklikšķiniet uz **Iespējot**.</span><span class="sxs-lookup"><span data-stu-id="b5f44-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="b5f44-113">Atgriešanu apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="b5f44-113">Process returns</span></span>

<span data-ttu-id="b5f44-114">Kad šie līdzekļi ir ieslēgti un izmaiņas ir sinhronizētas uz veikaliem, kasieris veikalā var atlasīt vairākus pārdošanas pasūtījumus vienam debitoram, lai tos atgrieztu.</span><span class="sxs-lookup"><span data-stu-id="b5f44-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="b5f44-115">Kad pasūtījumi ir atlasīti, tiek parādīts saraksts ar visām atgriežamajām precēm visos šo pasūtījumu rēķinos.</span><span class="sxs-lookup"><span data-stu-id="b5f44-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="b5f44-116">Pēc tam kasieris var atlasīt atgriežamās preces.</span><span class="sxs-lookup"><span data-stu-id="b5f44-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="b5f44-117">Visām atlasītajām precēm tiks izveidots viens atgriešanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="b5f44-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="b5f44-118">Ja pasūtījums tiek pilnībā atgriezts, debitoram atgriezto nodokļu summa būs vienāda ar sākotnēji iekasēto nodokļu summu.</span><span class="sxs-lookup"><span data-stu-id="b5f44-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]