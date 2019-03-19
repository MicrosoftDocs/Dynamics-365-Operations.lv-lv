---
title: Krājumu atgriešana vairākos debitoru pasūtījumos un rēķinos
description: Šajā tēmā ir aprakstīta funkcionalitāte, kas ļauj izmantot atgriešanu vairākos debitoru pasūtījumos un rēķinos programmā Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
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
ms.openlocfilehash: c201311028b11121d626e93859a2b98497c047d1
ms.sourcegitcommit: bacec397ee48ac583596be156c87ead474ee07df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/05/2019
ms.locfileid: "777230"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="97383-103">Krājumu atgriešana vairākos debitoru pasūtījumos un rēķinos</span><span class="sxs-lookup"><span data-stu-id="97383-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="97383-104">Dynamics 365 for Finance and Operations versijā 10.0 atgriešanu var veikt vairākos pasūtījumos un rēķinos, bet laidienos pirms versijas 10.0 atgriešanu vienlaikus varēja apstrādāt tikai vienam rēķinam.</span><span class="sxs-lookup"><span data-stu-id="97383-104">In Dynamics 365 for Finance and Operations version 10.0, returns can be made across multiple orders and invoices, whereas in releases prior to 10.0, returns could only be processed by a single invoice at a time.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="97383-105">Retail konfigurēšana, lai atbalstītu atgriešanu vairākos debitoru pasūtījumos un rēķinos</span><span class="sxs-lookup"><span data-stu-id="97383-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="97383-106">Dodieties uz **Retail parametri \> Debitoru pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="97383-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="97383-107">Ieslēdziet parametru **Iespējot atgriešanu vairākiem pasūtījumiem**.</span><span class="sxs-lookup"><span data-stu-id="97383-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="97383-108">Atgriešanu apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="97383-108">Process returns</span></span>

<span data-ttu-id="97383-109">Kad šis parametrs ir ieslēgts un izmaiņas ir sinhronizētas uz veikaliem, kasieris veikalā var atlasīt vairākus pārdošanas pasūtījumus vienam debitoram, lai tos atgrieztu.</span><span class="sxs-lookup"><span data-stu-id="97383-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="97383-110">Kad pasūtījumi ir atlasīti, tiek parādīts saraksts ar visām atgriežamajām precēm visos šo pasūtījumu rēķinos.</span><span class="sxs-lookup"><span data-stu-id="97383-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="97383-111">Pēc tam kasieris var atlasīt atgriežamās preces.</span><span class="sxs-lookup"><span data-stu-id="97383-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="97383-112">Visām atlasītajām precēm tiks izveidots viens atgriešanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="97383-112">A single return order will be created for all the selected products.</span></span>
