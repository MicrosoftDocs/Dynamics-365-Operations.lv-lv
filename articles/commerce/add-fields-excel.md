---
title: Lauku pievienošana Excel darbgrāmatai, lai rediģētu mazumtirdzniecības darījumus
description: Šajā tēmā ir aprakstīts, kā pievienot laukus Microsoft Excel darbgrāmatai, lai programmā Microsoft Dynamics 365 Commerce varat rediģēt mazumtirdzniecības darījumus.
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
ms.openlocfilehash: fb0435a617585689a87caa76f80e9774182576cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206323"
---
# <a name="add-fields-to-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="6cb7a-103">Lauku pievienošana Excel darbgrāmatai, lai rediģētu mazumtirdzniecības darījumus</span><span class="sxs-lookup"><span data-stu-id="6cb7a-103">Add fields to an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6cb7a-104">Šajā tēmā ir aprakstīts, kā pievienot laukus Microsoft Excel darbgrāmatai, lai programmā Microsoft Dynamics 365 Commerce varat rediģēt mazumtirdzniecības darījumus.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-104">This topic describes how to add fields to a Microsoft Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6cb7a-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="6cb7a-105">Overview</span></span>

<span data-ttu-id="6cb7a-106">Ģenerējot Excel failu, lai varētu rediģēt mazumtirdzniecības darījumus, fails tiek aizpildīts ar dažiem noklusējuma laukiem.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-106">When you generate an Excel file so that you can edit retail transactions, the file is filled with some default fields.</span></span> <span data-ttu-id="6cb7a-107">Ja atjaunināmais lauks ģenerētajā Excel failā nav redzams pēc noklusējuma, varat to pievienot.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-107">If a field that must be updated isn't visible by default in the generated Excel file, you can add it.</span></span>

## <a name="add-fields-to-a-worksheet-in-an-excel-workbook"></a><span data-ttu-id="6cb7a-108">Lauku pievienošana darblapai Excel darbgrāmatā</span><span class="sxs-lookup"><span data-stu-id="6cb7a-108">Add fields to a worksheet in an Excel workbook</span></span>

<span data-ttu-id="6cb7a-109">Lai pievienotu laukus Excel darbgrāmatai un varētu rediģēt mazumtirdzniecības darījumus, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-109">To add fields to an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="6cb7a-110">Lejupielādējiet un atveriet Excel failu lapā **Pārskati**, lapā **Mazumtirdzniecības darījumi** vai elementā **Darījumu validācijas kļūmes** darbvietā **Veikala finanses**.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-110">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="6cb7a-111">Atlasiet **Dizains**.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-111">Select **Design**.</span></span>
1. <span data-ttu-id="6cb7a-112">Atlasiet vajadzīgās tabulas zīmuļa simbolu un pēc tam pieejamo lauku sarakstā atrodiet un atlasiet pievienojamo lauku.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-112">Select the pencil symbol for the desired table, and then, in the list of available fields, find and select the field that you want to add.</span></span>
1. <span data-ttu-id="6cb7a-113">Atlasiet **Pievienot** un pēc tam atlasiet **Atjaunināt**.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-113">Select **Add**, and then select **Update**.</span></span> <span data-ttu-id="6cb7a-114">Laukus varat pārkārtot.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-114">You can reorder fields.</span></span>
1. <span data-ttu-id="6cb7a-115">Kad atjaunināšana ir pabeigta, atlasiet **Atsvaidzināt**, lai ienestu datus jaunajā kolonnā.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-115">After the update is completed, select **Refresh** to fetch the data for the new column.</span></span>

<span data-ttu-id="6cb7a-116">Jaunajam laukam un tā datiem tagad ir jābūt pieejamiem rediģēšanai programmā Excel.</span><span class="sxs-lookup"><span data-stu-id="6cb7a-116">The new field and data for it should now be available for editing in Excel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6cb7a-117">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="6cb7a-117">Additional resources</span></span>

[<span data-ttu-id="6cb7a-118">Darījumu, kas saistīti ar pārdošanu skaidrā naudā bez piegādes, un skaidras naudas pārvaldības darījumu rediģēšana un auditēšana</span><span class="sxs-lookup"><span data-stu-id="6cb7a-118">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="6cb7a-119">Tiešsaistes pasūtījumu un asinhrono debitoru pasūtījumu darījumu rediģēšana un auditēšana</span><span class="sxs-lookup"><span data-stu-id="6cb7a-119">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="6cb7a-120">Mazumtirdzniecības darījumu finanšu dimensiju rediģēšana</span><span class="sxs-lookup"><span data-stu-id="6cb7a-120">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="6cb7a-121">Excel darbgrāmatas izveide, lai rediģētu mazumtirdzniecības darījumus</span><span class="sxs-lookup"><span data-stu-id="6cb7a-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]