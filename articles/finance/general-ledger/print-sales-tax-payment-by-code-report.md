---
title: PVN maksājuma drukāšana pēc koda pārskata
description: Šī tēma sniedz informāciju par iestatījumiem un darbībām, kas nepieciešamas, lai drukātu PVN maksājumu pēc koda pārskata uzskaites vai nodokļu koda valūtā.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eb3ee4a12d2d29c2769f1ae22e11dc05608b47c1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815456"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="919ce-103">PVN maksājuma drukāšana pēc koda pārskata</span><span class="sxs-lookup"><span data-stu-id="919ce-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="919ce-104">Lai drukātu **PVN maksājumu pēc koda** pārskata, dodieties uz **Nodoklis** \> **Pieprasījumi un pārskati** \> **PVN pārskati** \> **PVN maksājumi pēc koda**.</span><span class="sxs-lookup"><span data-stu-id="919ce-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="919ce-105">Pēc noklusējuma pārskata summas tiek ģenerētas juridiskās personas uzskaites valūtā visiem pārskata kodiem, kas iestatīti **PVN pārskatu kodu** lapā.</span><span class="sxs-lookup"><span data-stu-id="919ce-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="919ce-106">Jūs varat arī ģenerēt šo pārskatu, lai tas parāda PVN maksājumu summas PVN kodu valūtās visiem pārskatu kodiem, kas piešķirti PVN kodiem **PVN kodu** lapā.</span><span class="sxs-lookup"><span data-stu-id="919ce-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="919ce-107">Līdzekļa ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="919ce-107">Turn on the feature</span></span>

<span data-ttu-id="919ce-108">**Līdzekļu pārvaldības** darbvietā ieslēdziet tālāk norādīto līdzekli: **Ģenerējiet PVN maksājumu pēc koda pārskata PVN koda valūtā**.</span><span class="sxs-lookup"><span data-stu-id="919ce-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="919ce-109">Palaist pārskatu</span><span class="sxs-lookup"><span data-stu-id="919ce-109">Run the report</span></span>

1. <span data-ttu-id="919ce-110">Dodieties uz sadaļu **Nodokļi** \> **Pieprasījumi un pārskati** \> **PVN pārskati** \> **PVN maksājums pēc koda**.</span><span class="sxs-lookup"><span data-stu-id="919ce-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="919ce-111">Laukā **Pārskata valūta** atlasiet vienu no šīm vērtībām:</span><span class="sxs-lookup"><span data-stu-id="919ce-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="919ce-112">**Uzskaites valūta** — drukāt pārskata summas uzskaites valūtā.</span><span class="sxs-lookup"><span data-stu-id="919ce-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="919ce-113">**PVN koda valūta** — drukāt pārskatu summas PVN kodu valūtās.</span><span class="sxs-lookup"><span data-stu-id="919ce-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![PVN maksājums pēc koda dialoglodziņš](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="919ce-115">Tālāk redzamajā attēlā ir parādīts ģenerēta pārskata piemērs.</span><span class="sxs-lookup"><span data-stu-id="919ce-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="919ce-116">Pārskats rāda, ka pārskata kodam **101** ir valūta **EUR**, ja **PVN valūtas** lauks ir iestatīts uz **EUR** PVN kodam, kuram ir piešķirts pārskata kods.</span><span class="sxs-lookup"><span data-stu-id="919ce-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![PVN maksājums pēc koda pārskata piemērs](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]