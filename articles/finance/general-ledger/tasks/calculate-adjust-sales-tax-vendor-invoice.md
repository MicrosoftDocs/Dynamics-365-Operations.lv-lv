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
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03313d875d23489b3293376dd94f808c73a4bd15
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983553"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="c03cd-103">PVN aprēķināšana un koriģēšana kreditora rēķinā</span><span class="sxs-lookup"><span data-stu-id="c03cd-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c03cd-104">Šajā tēmā paskaidrots, kā pielāgot PVN kreditora rēķinam .</span><span class="sxs-lookup"><span data-stu-id="c03cd-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="c03cd-105">Ja sākotnējā pirmdokumentā ir parādīta atšķirīga nodokļu summa, nekā aprēķināts, pirms grāmatošanas šīs summas varat pielāgot.</span><span class="sxs-lookup"><span data-stu-id="c03cd-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="c03cd-106">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums DEMF.</span><span class="sxs-lookup"><span data-stu-id="c03cd-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="c03cd-107">Navigācijas rūtī atveriet **Moduļi > Kreditori > Rēķini > Rēķinu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="c03cd-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="c03cd-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="c03cd-108">Select **New**.</span></span>
3. <span data-ttu-id="c03cd-109">Jaunās rindas laukā **Nosaukums** atlasiet opciju nolaižamajā izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="c03cd-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="c03cd-110">Darbību rūtī atlasiet **Rindiņas**.</span><span class="sxs-lookup"><span data-stu-id="c03cd-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="c03cd-111">Laukā **Konts** norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="c03cd-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="c03cd-112">Laukā **Rēķins** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c03cd-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="c03cd-113">Laukā **Kredīts** ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="c03cd-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="c03cd-114">Laukā **Korespondējošais konts** norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="c03cd-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="c03cd-115">Atlasiet **PVN**.</span><span class="sxs-lookup"><span data-stu-id="c03cd-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="c03cd-116">Ievadiet skaitli laukā **Reālā PVN kopsumma**.</span><span class="sxs-lookup"><span data-stu-id="c03cd-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="c03cd-117">PVN summas katram PVN kodam iespējams koriģēt cilnē **Korekcija**.</span><span class="sxs-lookup"><span data-stu-id="c03cd-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="c03cd-118">Atlasiet **Atiestatīt faktiskās izmaksas no aprēķinātās summas**.</span><span class="sxs-lookup"><span data-stu-id="c03cd-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="c03cd-119">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c03cd-119">Select **OK**.</span></span>
14. <span data-ttu-id="c03cd-120">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c03cd-120">Select **Save**.</span></span>

