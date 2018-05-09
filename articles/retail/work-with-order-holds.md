---
title: "Pasūtījumu aizturēšana"
description: "Šajā tēmā ir aprakstīts, kā aizturēt pasūtījumus, izmantojot Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 106ce40f93704e67e53db2e62ae481d271aed755
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="order-holds"></a><span data-ttu-id="00f14-103">Pasūtījumu aizturēšana</span><span class="sxs-lookup"><span data-stu-id="00f14-103">Order holds</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="00f14-104">Šajā tēmā ir aprakstīts, kā aizturēt pasūtījumus, izmantojot Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="00f14-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="00f14-105">Pasūtījumu var aizturēt dažādu iemeslu dēļ.</span><span class="sxs-lookup"><span data-stu-id="00f14-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="00f14-106">Piemēram, pasūtījumu var aizturēt līdz debitora adresi vai maksājuma metodi būs iespējams pārbaudīt vai līdz vadītājs varēs pārskatīt debitora kredīta limitu.</span><span class="sxs-lookup"><span data-stu-id="00f14-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="00f14-107">Gadās, ka pārdošanas procesa laikā pārdošanas pasūtījumi ir jāaiztur.</span><span class="sxs-lookup"><span data-stu-id="00f14-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="00f14-108">Piemēram, pārdošanas pasūtījums varētu tikt aizturēts, ja radušās problēmas ar debitora maksājumu sakarā ar aizdomām par pārkāpumu, vai tāpēc, ka vadītājam jāpārskata pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="00f14-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="00f14-109">Kad pārdošanas pasūtījums ir aizturēts, pārdošanas pasūtījumam tiek piešķirts pasūtījuma aizturēšanas kods, ar kuru norāda aizturēšanas iemeslu.</span><span class="sxs-lookup"><span data-stu-id="00f14-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="00f14-110">Pārdošanas pasūtījuma aizturēšanas kodus var konfigurēt sadaļā **Pārdošana un mārketings** &gt; **Iestatījumi** &gt; **Pārdošanas pasūtījumi** &gt; **Pasūtījumu aizturēšanas kodi**.</span><span class="sxs-lookup"><span data-stu-id="00f14-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="00f14-111">Aizturēt pārdošanas pasūtījumu var manuāli pasūtījuma izveides brīdī vai vēlāk.</span><span class="sxs-lookup"><span data-stu-id="00f14-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="00f14-112">Turklāt var pasūtījumu aizturēt automātiski, pamatojoties uz pārkāpumu kārtulām.</span><span class="sxs-lookup"><span data-stu-id="00f14-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="00f14-113">Kamēr pārdošanas pasūtījums ir aizturēts, iespējams, vajadzēs tam pievienot papildu informāciju.</span><span class="sxs-lookup"><span data-stu-id="00f14-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="00f14-114">Vai arī varat izrakstīt pārdošanas pasūtījumu, turpinot strādāt pie tā.</span><span class="sxs-lookup"><span data-stu-id="00f14-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="00f14-115">Varat izrakstīt pārdošanas pasūtījumu, to atkal ierakstīt vai pat ignorēt cita lietotāja veiktu izrakstīšanu, izmantojot pasūtījumu aizturēšanas rīku (**Mazumtirdzniecība** &gt; **Debitori** &gt; **Pasūtījumu aizturēšana**).</span><span class="sxs-lookup"><span data-stu-id="00f14-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="00f14-116">Ja pasūtījums ir gatavs pabeigšanai, aizturēšana ir jānoņem pirms pasūtījuma procesa pabeigšanas.</span><span class="sxs-lookup"><span data-stu-id="00f14-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>




