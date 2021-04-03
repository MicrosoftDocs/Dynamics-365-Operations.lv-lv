---
title: Virsgrāmatas noklusētie apraksti
description: Noklusētos aprakstus var izmantot, lai atjauninātu lauka Apraksts dokumentu grāmatojumus Virsgrāmatā.
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 47c5c9e71dba7a0cb7c798c167208faebeb5af6c
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500384"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="226e5-103">Virsgrāmatas noklusētie apraksti</span><span class="sxs-lookup"><span data-stu-id="226e5-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="226e5-104">Noklusētos aprakstus var izmantot, lai atjauninātu lauka **Apraksts** dokumentu grāmatojumus Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="226e5-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="226e5-105">Šī funkcionalitāte ir uzlabota darbam ar Kopīgajām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="226e5-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="226e5-106">Lai iestatītu noklusējuma aprakstus virsgrāmatas grāmatojumi, dodieties uz sadaļu **Organizācijas administrēšana \> Iestatījumi \> Noklusētie apraksti**.</span><span class="sxs-lookup"><span data-stu-id="226e5-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="226e5-107">Šajā tabulā uzskaitītas jaunās vērtības, kas ir pievienotas laukam **Apraksts** lapā **Noklusējuma apraksti**, lai atbalstītu Kopīgās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="226e5-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="226e5-108">Apraksta veids</span><span class="sxs-lookup"><span data-stu-id="226e5-108">Description type</span></span> | <span data-ttu-id="226e5-109">Piezīmes</span><span class="sxs-lookup"><span data-stu-id="226e5-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="226e5-110">Importa izmaksu aprēķināšana - izmaksu uzkrājums</span><span class="sxs-lookup"><span data-stu-id="226e5-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="226e5-111">Kad pirkšanas pasūtījuma rēķins tiek grāmatots, izmaksu uzkrājums tiek apstrādāts prognozētajām reisa izmaksām.</span><span class="sxs-lookup"><span data-stu-id="226e5-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="226e5-112">Var norādīt noklusējuma aprakstus, lai aprakstam pievienotu reisa numuru.</span><span class="sxs-lookup"><span data-stu-id="226e5-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="226e5-113">Sūtīšanas numuram izmantojiet *%4*.</span><span class="sxs-lookup"><span data-stu-id="226e5-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="226e5-114">Importa izmaksu aprēķināšana - tranzītpreču pasūtījums</span><span class="sxs-lookup"><span data-stu-id="226e5-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="226e5-115">Ja izmantojat tranzīta apstrādi, pirkšanas pasūtījuma rēķins tiek grāmatots un preces tiek grāmatotas tranzītkontā.</span><span class="sxs-lookup"><span data-stu-id="226e5-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="226e5-116">Var norādīt noklusējuma aprakstus, lai aprakstam pievienotu reisa numuru.</span><span class="sxs-lookup"><span data-stu-id="226e5-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="226e5-117">Lietojiet *%4* tranzīta pasūtījuma numuram.</span><span class="sxs-lookup"><span data-stu-id="226e5-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="226e5-118">Krājumi - Slēgšana - Korekcija</span><span class="sxs-lookup"><span data-stu-id="226e5-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="226e5-119">Ja kreditoru (AP) rēķins tiek apstrādāts reisa izmaksām, krājuma korekcija tiek apstrādāta, lai novērtētu reisa izmaksas.</span><span class="sxs-lookup"><span data-stu-id="226e5-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="226e5-120">Var norādīt noklusējuma aprakstus, lai aprakstam pievienotu reisa numuru.</span><span class="sxs-lookup"><span data-stu-id="226e5-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="226e5-121">Sūtīšanas numuram izmantojiet *%4*.</span><span class="sxs-lookup"><span data-stu-id="226e5-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="226e5-122">Papildinformāciju par to, kā strādāt ar lapu **Noklusējuma apraksti**, skatiet sadaļā [Automātiskās grāmatošanas noklusēto aprakstu iestatīšana](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span><span class="sxs-lookup"><span data-stu-id="226e5-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>
