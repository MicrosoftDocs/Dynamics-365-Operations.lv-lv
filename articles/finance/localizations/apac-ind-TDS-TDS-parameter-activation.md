---
title: TDS parametru iestatīšana
description: Šajā tēmā skaidrots, kā iestatīt parametrus, lai aktivizētu No kopējo ienākumu summas atskaitītā nodokļa (TDS) funkcionalitāti norādītajos darījumos. Šis ir nepieciešams solis, lai izmantotu No kopējo ienākumu summas atskaitītā nodokļa funkciju.
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
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023416"
---
# <a name="set-the-tds-parameters"></a><span data-ttu-id="6dae7-104">TDS parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="6dae7-104">Set the TDS parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6dae7-105">Šajā tēmā skaidrots, kā iestatīt parametrus, lai aktivizētu No kopējo ienākumu summas atskaitītā nodokļa (TDS) funkcionalitāti norādītajos darījumos.</span><span class="sxs-lookup"><span data-stu-id="6dae7-105">This topic explains how to set parameters to activate Tax Deducted at Source (TDS) functionality in specified transactions.</span></span> <span data-ttu-id="6dae7-106">Šis ir nepieciešams solis, lai izmantotu No kopējo ienākumu summas atskaitītā nodokļa funkciju.</span><span class="sxs-lookup"><span data-stu-id="6dae7-106">This is a necessary step to use the Tax Deducted at Source TDS feature.</span></span>

1. <span data-ttu-id="6dae7-107">Dodieties uz **Virsgrāmata \> Virsgrāmatas iestatīšana \> Virsgrāmatas parametri**.</span><span class="sxs-lookup"><span data-stu-id="6dae7-107">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="6dae7-108">Cilnes **Tiešie nodokļi** sadaļā **No kopējo ienākumu summas atskaitītais nodoklis** iestatiet **Aktivizēt TDS** opciju uz **Jā**, lai aktivizētu TDS funkcionalitāti un tai izmantotās lapas un laukus.</span><span class="sxs-lookup"><span data-stu-id="6dae7-108">On the **Direct taxes** tab, in the **Tax Deducted at Source** section, set the **Activate TDS** option to **Yes** to activate the TDS functionality, and the pages and fields that are used for it.</span></span>
3. <span data-ttu-id="6dae7-109">Iestatiet opciju **Rēķins** uz **Jā**, lai aktivizētu laukus, kas tiek izmantoti, lai aprēķinātu un atskaitītu TDS rēķina līmenī.</span><span class="sxs-lookup"><span data-stu-id="6dae7-109">Set the **Invoice** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the invoice level.</span></span>
4. <span data-ttu-id="6dae7-110">Iestatiet opciju **Maksājums** uz **Jā**, lai aktivizētu laukus, kas tiek izmantoti, lai aprēķinātu un atskaitītu TDS maksājuma līmenī.</span><span class="sxs-lookup"><span data-stu-id="6dae7-110">Set the **Payment** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the payment level.</span></span>

    <span data-ttu-id="6dae7-111">[![Tiešie nodokļi cilne](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span><span class="sxs-lookup"><span data-stu-id="6dae7-111">[![Direct taxes tab](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span></span>

5. <span data-ttu-id="6dae7-112">Cilnē **Numuru sērijas** atrodiet rindu, kur **Atsauces** lauks ir iestatīts uz **Ieturētā nodokļa maksājumu**.</span><span class="sxs-lookup"><span data-stu-id="6dae7-112">On the **Number sequences** tab, find the row where the **Reference** field is set to **Withholding tax payment**.</span></span> <span data-ttu-id="6dae7-113">Rindas laukā **Numuru sērijas kods** atlasiet numuru sērijas kodu.</span><span class="sxs-lookup"><span data-stu-id="6dae7-113">In the **Number sequence code** field for the row, select the number sequence code.</span></span> <span data-ttu-id="6dae7-114">Numuru sērijas kods tiek lietots, lai ģenerētu dokumentu numurus periodiskā TDS norēķinu procesam.</span><span class="sxs-lookup"><span data-stu-id="6dae7-114">The number sequence code is used to generate voucher numbers for the periodic TDS settlement process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6dae7-115">Lai palaistu periodisko TDS norēķinu procesu, dodieties uz **Nodoklis \> Deklarācijas \> Ieturētais nodoklis \> Ieturētā nodokļa maksājums**.</span><span class="sxs-lookup"><span data-stu-id="6dae7-115">To run the periodic TDS settlement process, go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="6dae7-116">[![Cilne Numuru sērijas](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span><span class="sxs-lookup"><span data-stu-id="6dae7-116">[![Number sequences tab](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span></span>

6. <span data-ttu-id="6dae7-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6dae7-117">Close the page.</span></span>
