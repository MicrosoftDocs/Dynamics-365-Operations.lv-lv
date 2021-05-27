---
title: ieturētā nodokļa norēķinu periodu iestatīšana TDS nodokļu tipam
description: Šajā tēmā skaidrots, kā iestatīt No kopējo ienākumu summas atskaitītā nodokļa (TDS) norēķinu periodus.
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
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023405"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="30d8c-103">ieturētā nodokļa norēķinu periodu iestatīšana TDS nodokļu tipam</span><span class="sxs-lookup"><span data-stu-id="30d8c-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30d8c-104">Šajā tēmā skaidrots, kā iestatīt No kopējo ienākumu summas atskaitītā nodokļa (TDS) norēķinu periodus.</span><span class="sxs-lookup"><span data-stu-id="30d8c-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="30d8c-105">Pārejiet uz sadaļu **Nodokļi \> Netiešie nodokļi \> Ieturētais nodoklis \> ieturētā nodokļa norēķinu periodi**.</span><span class="sxs-lookup"><span data-stu-id="30d8c-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="30d8c-106">[![ieturētā nodokļa samaksas periodu lapa](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="30d8c-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="30d8c-107">Laukā **Nodokļu tips** atlasiet **TDS**, lai iestatītu ieturētā nodokļa norēķinu periodus TDS nodokļa tipam.</span><span class="sxs-lookup"><span data-stu-id="30d8c-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="30d8c-108">Atlasiet **Jauns**, lai izveidotu rindu.</span><span class="sxs-lookup"><span data-stu-id="30d8c-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="30d8c-109">Laukā **Norēķinu periods** ievadiet TDS apmaksas perioda nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="30d8c-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="30d8c-110">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="30d8c-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="30d8c-111">Laukā **ieturētā nodokļa iestāde** atlasiet TDS iestādi, kam nosakāt TDS norēķinu periodu.</span><span class="sxs-lookup"><span data-stu-id="30d8c-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="30d8c-112">Kopsavilkuma cilnes **Vispārīgi** laukā **Periodu intervāls** atlasiet perioda intervāla tipu TDS norēķinu periodam.</span><span class="sxs-lookup"><span data-stu-id="30d8c-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="30d8c-113">Laukā **Vienību skaits** norādiet vienību skaitu perioda intervāla tipam.</span><span class="sxs-lookup"><span data-stu-id="30d8c-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="30d8c-114">Kopsavilkuma cilnes **Periodi** laukā **Sākuma datums** atlasiet TDS apmaksas perioda sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="30d8c-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="30d8c-115">Laukā **Beigu datums** atlasiet beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="30d8c-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="30d8c-116">Lai veidotu sekojošu TDS norēķinu periodu esošam periodam, pamatojoties uz perioda intervālu un perioda vienībām, atlasiet **Jauns periods**.</span><span class="sxs-lookup"><span data-stu-id="30d8c-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="30d8c-117">Lai skatītu informāciju par periodisko TDS norēķinu, kas tiek izpildīts noteiktam apmaksas periodam, atlasiet **ieturētā nodokļa maksājumi**, lai atvērtu **ieturētā nodokļa maksājuma** lapu.</span><span class="sxs-lookup"><span data-stu-id="30d8c-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="30d8c-118">Lai palaistu periodisko TDS norēķinu procesu, dodieties uz **Virsgrāmata \> Periodiski \> Ieturētais nodoklis \> ieturētā nodokļa maksājums**.</span><span class="sxs-lookup"><span data-stu-id="30d8c-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="30d8c-119">[![ieturētā nodokļa maksājuma lapa](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="30d8c-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="30d8c-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="30d8c-120">Close the page.</span></span>
