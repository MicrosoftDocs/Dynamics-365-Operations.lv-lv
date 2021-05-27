---
title: Mazumtirdzniecības darījumu finanšu dimensiju rediģēšana
description: Šajā tēmā ir aprakstīts, kā rediģēt mazumtirdzniecības darījumu finanšu dimensijas programmā Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 381d8bb0939f6c4c163477990e49382201487375
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019911"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="d26e2-103">Mazumtirdzniecības darījumu finanšu dimensiju rediģēšana</span><span class="sxs-lookup"><span data-stu-id="d26e2-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d26e2-104">Šajā tēmā ir aprakstīts, kā rediģēt mazumtirdzniecības darījumu finanšu dimensijas programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d26e2-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="d26e2-105">Finanšu dimensiju rediģēšana</span><span class="sxs-lookup"><span data-stu-id="d26e2-105">Edit financial dimensions</span></span>

<span data-ttu-id="d26e2-106">Lai rediģētu mazumtirdzniecības darījumu finanšu dimensijas komponentā Commerce Headquarters, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="d26e2-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d26e2-107">Atveriet lapu **Finanšu dimensiju konfigurēšana programmu integrēšanai**.</span><span class="sxs-lookup"><span data-stu-id="d26e2-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="d26e2-108">Atlasiet aktīvo ierakstu **Noklusējuma dimensiju integrācija**.</span><span class="sxs-lookup"><span data-stu-id="d26e2-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="d26e2-109">Kopsavilkuma cilnē **Finanšu dimensijas** pārliecinieties, vai sarakstā **Atlasīts** ir visas dimensijas, kuras vēlaties rediģēt Excel darblapā.</span><span class="sxs-lookup"><span data-stu-id="d26e2-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="d26e2-110">Plašāku informāciju skatiet sadaļā [Datu elementi](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).</span><span class="sxs-lookup"><span data-stu-id="d26e2-110">For more information, see [Data entities](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).</span></span>
1. <span data-ttu-id="d26e2-111">Lejupielādējiet un atveriet Excel failu lapā **Pārskati**, lapā **Mazumtirdzniecības darījumi** vai elementā **Darījumu validācijas kļūmes** darbvietā **Veikala finanses**.</span><span class="sxs-lookup"><span data-stu-id="d26e2-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="d26e2-112">Lai mainītu darījuma finanšu dimensiju, atlasiet **Noformējums** un pēc tam atlasiet zīmuļa simbolu blakus rindai **Darījums (auditējams)**.</span><span class="sxs-lookup"><span data-stu-id="d26e2-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="d26e2-113">Atrodiet un atlasiet lauku **FinancialDimensionDisplayValue**, atlasiet šūnu Excel darblapas galvenes daļā un pēc tam atlasiet **Pievienot etiķeti**.</span><span class="sxs-lookup"><span data-stu-id="d26e2-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="d26e2-114">Atlasiet šūnu zem iepriekšējā darbībā atlasītās šūnas, atlasiet **Pievienot vērtību** un pēc tam atlasiet **Atsvaidzināt**.</span><span class="sxs-lookup"><span data-stu-id="d26e2-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="d26e2-115">Finanšu dimensijas ir pievienotas Excel darblapai, un pēc tam tās var rediģēt un publicēt.</span><span class="sxs-lookup"><span data-stu-id="d26e2-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="d26e2-116">Lai mainītu dimensijas darījumu rindās, atlasiet rindu **Pārdošanas darījumi (auditējami)**, atlasiet zīmuļa simbolu un pēc tam atkārtojiet 6. un 7. darbību.</span><span class="sxs-lookup"><span data-stu-id="d26e2-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="d26e2-117">Lai mainītu dimensijas maksājumu rindās, atlasiet rindu **Maksājumu darījumi (auditējami)**, atlasiet zīmuļa simbolu un pēc tam atkārtojiet 6. un 7. darbību.</span><span class="sxs-lookup"><span data-stu-id="d26e2-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d26e2-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d26e2-118">Additional resources</span></span>

[<span data-ttu-id="d26e2-119">Darījumu, kas saistīti ar pārdošanu skaidrā naudā bez piegādes, un skaidras naudas pārvaldības darījumu rediģēšana un auditēšana</span><span class="sxs-lookup"><span data-stu-id="d26e2-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="d26e2-120">Tiešsaistes pasūtījumu un asinhrono debitoru pasūtījumu darījumu rediģēšana un auditēšana</span><span class="sxs-lookup"><span data-stu-id="d26e2-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="d26e2-121">Excel darbgrāmatas izveide, lai rediģētu mazumtirdzniecības darījumus</span><span class="sxs-lookup"><span data-stu-id="d26e2-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="d26e2-122">Lauku pievienošana Excel darbgrāmatai, lai rediģētu mazumtirdzniecības darījumus</span><span class="sxs-lookup"><span data-stu-id="d26e2-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]