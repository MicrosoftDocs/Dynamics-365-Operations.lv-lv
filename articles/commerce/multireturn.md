---
title: Krājumu atgriešana vairākos debitoru pasūtījumos un rēķinos
description: Šajā tēmā ir aprakstīta funkcionalitāte, kas ļauj izmantot atgriešanu vairākos debitoru pasūtījumos un rēķinos programmā Dynamics 365 Commerce.
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
ms.openlocfilehash: c5f17424f0837344030f9ce2d2d037cde08c4e49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004462"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="64570-103">Krājumu atgriešana vairākos debitoru pasūtījumos un rēķinos</span><span class="sxs-lookup"><span data-stu-id="64570-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="64570-104">Atgriešanu var veikt vairākos pasūtījumos un rēķinos.</span><span class="sxs-lookup"><span data-stu-id="64570-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="64570-105">Commerce konfigurēšana, lai atbalstītu atgriešanu vairākos debitoru pasūtījumos un rēķinos</span><span class="sxs-lookup"><span data-stu-id="64570-105">Configure Commerce to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="64570-106">Dodieties uz **Commerce parametri \> Debitoru pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="64570-106">Go to **Commerce parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="64570-107">Ieslēdziet parametru **Iespējot atgriešanu vairākiem pasūtījumiem**.</span><span class="sxs-lookup"><span data-stu-id="64570-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="64570-108">Atgriešanu apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="64570-108">Process returns</span></span>

<span data-ttu-id="64570-109">Kad šis parametrs ir ieslēgts un izmaiņas ir sinhronizētas uz veikaliem, kasieris veikalā var atlasīt vairākus pārdošanas pasūtījumus vienam debitoram, lai tos atgrieztu.</span><span class="sxs-lookup"><span data-stu-id="64570-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="64570-110">Kad pasūtījumi ir atlasīti, tiek parādīts saraksts ar visām atgriežamajām precēm visos šo pasūtījumu rēķinos.</span><span class="sxs-lookup"><span data-stu-id="64570-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="64570-111">Pēc tam kasieris var atlasīt atgriežamās preces.</span><span class="sxs-lookup"><span data-stu-id="64570-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="64570-112">Visām atlasītajām precēm tiks izveidots viens atgriešanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="64570-112">A single return order will be created for all the selected products.</span></span>
