---
title: Iestatiet TDS grupu, PAN un TAN informāciju debitoriem un kreditoriem
description: Šajā tēmā skaidrots, kā iestatīt informāciju par No kopējo ienākumu summas atskaitīto nodokli (TDS) grupā, pastāvīgu konta numuru (PAN) un nodokļu konta numuru (TAN) kreditoriem un debitoriem.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023419"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="43721-103">TDS grupas, PAN un TAN informācijas iestatīšana debitoriem un kreditoriem</span><span class="sxs-lookup"><span data-stu-id="43721-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43721-104">Šajā tēmā skaidrots, kā iestatīt informāciju par No kopējo ienākumu summas atskaitīto nodokli (TDS) grupā, pastāvīgu konta numuru (PAN) un nodokļu konta numuru (TAN) kreditoriem un debitoriem.</span><span class="sxs-lookup"><span data-stu-id="43721-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="43721-105">Dodieties uz **Kreditori \> Kreditori \> Visi kreditori** vai **Debitori \> Debitori \> Visi Debitori**.</span><span class="sxs-lookup"><span data-stu-id="43721-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="43721-106">[![Visu kreditoru lapa](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="43721-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="43721-107">Darbību rūtī atlasiet **Jauns**, lai izveidotu kreditoru vai debitoru, un ievadiet nepieciešamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="43721-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="43721-108">Vai arī atlasiet esošu kreditoru vai debitoru.</span><span class="sxs-lookup"><span data-stu-id="43721-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="43721-109">Kopsavilkuma cilnes **Rēķins un piegāde** sadaļā **Ieturētais nodoklis** iestatiet opciju **Aprēķināt ieturēto nodokli** uz **Jā**, lai aprēķinātu ieturēto nodokli, TDS vai TCS kreditoram vai debitoram.</span><span class="sxs-lookup"><span data-stu-id="43721-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="43721-110">TDS pirkšanas rēķinam tiek aprēķināts, balstoties uz noklusējuma TDS grupu, kas noteikta kreditoram vai debitoram.</span><span class="sxs-lookup"><span data-stu-id="43721-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="43721-111">Atlasiet noklusējuma TDS grupu laukā **TDS grupa**.</span><span class="sxs-lookup"><span data-stu-id="43721-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="43721-112">Kad atlasāt TDS grupu laukā **TDS grupa**, laukā **Ieturēto nodokļu grupa** un **TCS grupa** kļūst nepieejami.</span><span class="sxs-lookup"><span data-stu-id="43721-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="43721-113">Kopsavilkuma cilnes **Informācija par nodokļiem** sadaļā **PAN informācija**, laukā **Statuss** atlasiet kreditora vai debitora pastāvīgo konta numura statusu:</span><span class="sxs-lookup"><span data-stu-id="43721-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="43721-114">**Nav pieejams** – kreditoram vai debitoram nav PAN.</span><span class="sxs-lookup"><span data-stu-id="43721-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="43721-115">**Saņemts** – kreditoram vai debitoram ir PAN.</span><span class="sxs-lookup"><span data-stu-id="43721-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="43721-116">**Piemērots** – kreditors vai debitors ir pieteicies uz PAN.</span><span class="sxs-lookup"><span data-stu-id="43721-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="43721-117">**Nederīgs** - kreditoram vai debitoram ir PAN, bet tas nav derīgs.</span><span class="sxs-lookup"><span data-stu-id="43721-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="43721-118">Ja laukā **Statuss** atlasījāt **Saņemts**, lai norādītu, ka kreditoram vai debitoram ir PAN numurs, laukā **Numurs** ievadiet PAN.</span><span class="sxs-lookup"><span data-stu-id="43721-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="43721-119">PAN ir jāietver piecas alfabēta rakstzīmes, tad četras skaitliskas rakstzīmes un tad viena alfabēta rakstzīme.</span><span class="sxs-lookup"><span data-stu-id="43721-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="43721-120">Lūk, piemērs: **ABCDE1260A**.</span><span class="sxs-lookup"><span data-stu-id="43721-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="43721-121">Ja laukā **Statuss** atlasījāt **Piemērots**, lai norādītu, ka kreditoram vai debitoram ir piemērots PAN numuram, laukā **Atsauces numurs** ievadiet atsauces numuru.</span><span class="sxs-lookup"><span data-stu-id="43721-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="43721-122">Laukā **Vērtētāja raksturs** atlasiet vērtētāja rakstura kategoriju, kam pieder kreditors vai debitors:</span><span class="sxs-lookup"><span data-stu-id="43721-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="43721-123">Uzņēmums</span><span class="sxs-lookup"><span data-stu-id="43721-123">Company</span></span>
    - <span data-ttu-id="43721-124">HUF</span><span class="sxs-lookup"><span data-stu-id="43721-124">HUF</span></span>
    - <span data-ttu-id="43721-125">Apstiprināt</span><span class="sxs-lookup"><span data-stu-id="43721-125">Firm</span></span>
    - <span data-ttu-id="43721-126">Individuāls</span><span class="sxs-lookup"><span data-stu-id="43721-126">Individual</span></span>
    - <span data-ttu-id="43721-127">AOP</span><span class="sxs-lookup"><span data-stu-id="43721-127">AOP</span></span>
    - <span data-ttu-id="43721-128">BOI</span><span class="sxs-lookup"><span data-stu-id="43721-128">BOI</span></span>
    - <span data-ttu-id="43721-129">Vietējā pašvaldība</span><span class="sxs-lookup"><span data-stu-id="43721-129">Local authority</span></span>
    - <span data-ttu-id="43721-130">Citi</span><span class="sxs-lookup"><span data-stu-id="43721-130">Others</span></span>

    <span data-ttu-id="43721-131">[![Nodokļu informācijas kopsavilkuma cilne](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="43721-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="43721-132">Darbību rūtī cilnē **Kreditors**, grupā **Reģistrācija** atlasiet **Reģistrācijas ID**, lai atvērtu lapu **Pārvaldīt adreses**.</span><span class="sxs-lookup"><span data-stu-id="43721-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="43721-133">Lapas **Pārvaldīt adreses** kopsavilkuma cilnē **Informācija par nodokļiem** atlasiet **Pievienot** vai **Rediģēt** lai atvērtu lapu **Pārvaldīt nodokļu informāciju**, kur varat uzturēt nodokļu reģistrācijas ierakstu.</span><span class="sxs-lookup"><span data-stu-id="43721-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="43721-134">Lapas **Pārvaldīt nodokļu informāciju** kopsavilkuma cilnē **Ieturētais nodoklis**, laukā **Nodokļu konta numurs (TAN)** ievadiet TAN.</span><span class="sxs-lookup"><span data-stu-id="43721-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="43721-135">TAN ir jāietver četras alfabēta rakstzīmes, tad piecas skaitliskas rakstzīmes un tad viena alfabēta rakstzīme.</span><span class="sxs-lookup"><span data-stu-id="43721-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="43721-136">Lūk, piemērs: **AFGH54821T**.</span><span class="sxs-lookup"><span data-stu-id="43721-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="43721-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="43721-137">Close the page.</span></span>
