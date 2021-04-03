---
title: Mazumtirdzniecības darījumu finanšu dimensiju rediģēšana
description: Šajā tēmā ir aprakstīts, kā rediģēt mazumtirdzniecības darījumu finanšu dimensijas programmā Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 4d4b7e383ca2089ee98e70d23ccd890d0e6a86c5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221802"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="a72c7-103">Mazumtirdzniecības darījumu finanšu dimensiju rediģēšana</span><span class="sxs-lookup"><span data-stu-id="a72c7-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a72c7-104">Šajā tēmā ir aprakstīts, kā rediģēt mazumtirdzniecības darījumu finanšu dimensijas programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a72c7-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="a72c7-105">Finanšu dimensiju rediģēšana</span><span class="sxs-lookup"><span data-stu-id="a72c7-105">Edit financial dimensions</span></span>

<span data-ttu-id="a72c7-106">Lai rediģētu mazumtirdzniecības darījumu finanšu dimensijas komponentā Commerce Headquarters, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="a72c7-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a72c7-107">Atveriet lapu **Finanšu dimensiju konfigurēšana programmu integrēšanai**.</span><span class="sxs-lookup"><span data-stu-id="a72c7-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="a72c7-108">Atlasiet aktīvo ierakstu **Noklusējuma dimensiju integrācija**.</span><span class="sxs-lookup"><span data-stu-id="a72c7-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="a72c7-109">Kopsavilkuma cilnē **Finanšu dimensijas** pārliecinieties, vai sarakstā **Atlasīts** ir visas dimensijas, kuras vēlaties rediģēt Excel darblapā.</span><span class="sxs-lookup"><span data-stu-id="a72c7-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="a72c7-110">Plašāku informāciju skatiet sadaļā [Datu elementi](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span><span class="sxs-lookup"><span data-stu-id="a72c7-110">For more information, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span></span>
1. <span data-ttu-id="a72c7-111">Lejupielādējiet un atveriet Excel failu lapā **Pārskati**, lapā **Mazumtirdzniecības darījumi** vai elementā **Darījumu validācijas kļūmes** darbvietā **Veikala finanses**.</span><span class="sxs-lookup"><span data-stu-id="a72c7-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="a72c7-112">Lai mainītu darījuma finanšu dimensiju, atlasiet **Noformējums** un pēc tam atlasiet zīmuļa simbolu blakus rindai **Darījums (auditējams)**.</span><span class="sxs-lookup"><span data-stu-id="a72c7-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="a72c7-113">Atrodiet un atlasiet lauku **FinancialDimensionDisplayValue**, atlasiet šūnu Excel darblapas galvenes daļā un pēc tam atlasiet **Pievienot etiķeti**.</span><span class="sxs-lookup"><span data-stu-id="a72c7-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="a72c7-114">Atlasiet šūnu zem iepriekšējā darbībā atlasītās šūnas, atlasiet **Pievienot vērtību** un pēc tam atlasiet **Atsvaidzināt**.</span><span class="sxs-lookup"><span data-stu-id="a72c7-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="a72c7-115">Finanšu dimensijas ir pievienotas Excel darblapai, un pēc tam tās var rediģēt un publicēt.</span><span class="sxs-lookup"><span data-stu-id="a72c7-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="a72c7-116">Lai mainītu dimensijas darījumu rindās, atlasiet rindu **Pārdošanas darījumi (auditējami)**, atlasiet zīmuļa simbolu un pēc tam atkārtojiet 6. un 7. darbību.</span><span class="sxs-lookup"><span data-stu-id="a72c7-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="a72c7-117">Lai mainītu dimensijas maksājumu rindās, atlasiet rindu **Maksājumu darījumi (auditējami)**, atlasiet zīmuļa simbolu un pēc tam atkārtojiet 6. un 7. darbību.</span><span class="sxs-lookup"><span data-stu-id="a72c7-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a72c7-118">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a72c7-118">Additional resources</span></span>

[<span data-ttu-id="a72c7-119">Darījumu, kas saistīti ar pārdošanu skaidrā naudā bez piegādes, un skaidras naudas pārvaldības darījumu rediģēšana un auditēšana</span><span class="sxs-lookup"><span data-stu-id="a72c7-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="a72c7-120">Tiešsaistes pasūtījumu un asinhrono debitoru pasūtījumu darījumu rediģēšana un auditēšana</span><span class="sxs-lookup"><span data-stu-id="a72c7-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="a72c7-121">Excel darbgrāmatas izveide, lai rediģētu mazumtirdzniecības darījumus</span><span class="sxs-lookup"><span data-stu-id="a72c7-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="a72c7-122">Lauku pievienošana Excel darbgrāmatai, lai rediģētu mazumtirdzniecības darījumus</span><span class="sxs-lookup"><span data-stu-id="a72c7-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]