---
title: PVN aprēķināšana un koriģēšana kreditora rēķinā
description: Šajā tēmā paskaidrots, kā pielāgot PVN kreditora rēķinam Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a68e0df78516875168d977f78adf023887b2362d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186283"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="03fb1-103">PVN aprēķināšana un koriģēšana kreditora rēķinā</span><span class="sxs-lookup"><span data-stu-id="03fb1-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="03fb1-104">Šajā tēmā paskaidrots, kā pielāgot PVN kreditora rēķinam .</span><span class="sxs-lookup"><span data-stu-id="03fb1-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="03fb1-105">Ja sākotnējā pirmdokumentā ir parādīta atšķirīga nodokļu summa, nekā aprēķināts, pirms grāmatošanas šīs summas varat pielāgot.</span><span class="sxs-lookup"><span data-stu-id="03fb1-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="03fb1-106">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums DEMF.</span><span class="sxs-lookup"><span data-stu-id="03fb1-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="03fb1-107">Navigācijas rūtī atveriet **Moduļi > Kreditori > Rēķini > Rēķinu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="03fb1-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="03fb1-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="03fb1-108">Select **New**.</span></span>
3. <span data-ttu-id="03fb1-109">Jaunās rindas laukā **Nosaukums** atlasiet opciju nolaižamajā izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="03fb1-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="03fb1-110">Darbību rūtī atlasiet **Rindiņas**.</span><span class="sxs-lookup"><span data-stu-id="03fb1-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="03fb1-111">Laukā **Konts** norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="03fb1-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="03fb1-112">Laukā **Rēķins** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="03fb1-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="03fb1-113">Laukā **Kredīts** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="03fb1-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="03fb1-114">Laukā **Korespondējošais konts** norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="03fb1-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="03fb1-115">Atlasiet **PVN**.</span><span class="sxs-lookup"><span data-stu-id="03fb1-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="03fb1-116">Ievadiet skaitli laukā **Reālā PVN kopsumma**.</span><span class="sxs-lookup"><span data-stu-id="03fb1-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="03fb1-117">PVN summas katram PVN kodam iespējams koriģēt cilnē **Korekcija**.</span><span class="sxs-lookup"><span data-stu-id="03fb1-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="03fb1-118">Atlasiet **Atiestatīt faktiskās izmaksas no aprēķinātās summas**.</span><span class="sxs-lookup"><span data-stu-id="03fb1-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="03fb1-119">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="03fb1-119">Select **OK**.</span></span>
14. <span data-ttu-id="03fb1-120">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="03fb1-120">Select **Save**.</span></span>

