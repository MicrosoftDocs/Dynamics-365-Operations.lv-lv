---
title: Iestatīt maksājumu grafikus ar TDS sadalījumu
description: Šajā tēmā skaidrots, kā iestatīt maksājumu grafikus ar No kopējo ienākumu summas atskaitītā nodokļa (TDS) sadalījumu.
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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023426"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="a50f9-103">Iestatīt maksājumu grafikus ar TDS sadalījumu</span><span class="sxs-lookup"><span data-stu-id="a50f9-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a50f9-104">Šajā tēmā skaidrots, kā iestatīt maksājumu grafikus ar No kopējo ienākumu summas atskaitītā nodokļa (TDS) sadalījumu.</span><span class="sxs-lookup"><span data-stu-id="a50f9-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="a50f9-105">Dodieties uz **Kreditori \> Maksājuma iestatījumi \> Maksājuma grafiki**.</span><span class="sxs-lookup"><span data-stu-id="a50f9-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="a50f9-106">[![Maksājumu grafiku lapa](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="a50f9-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="a50f9-107">Darbību rūtī atlasiet **Jauns**, lai izveidotu maksājuma grafiku, un ievadiet nepieciešamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="a50f9-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="a50f9-108">Laukā **Sadalījums** atlasiet metodi, ko izmantot maksājuma grafika sadalīšanai:</span><span class="sxs-lookup"><span data-stu-id="a50f9-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="a50f9-109">Summa</span><span class="sxs-lookup"><span data-stu-id="a50f9-109">Total</span></span>
    - <span data-ttu-id="a50f9-110">Fiksēta summa</span><span class="sxs-lookup"><span data-stu-id="a50f9-110">Fixed amount</span></span>
    - <span data-ttu-id="a50f9-111">Fiksēts skaits</span><span class="sxs-lookup"><span data-stu-id="a50f9-111">Fixed quantity</span></span>
    - <span data-ttu-id="a50f9-112">Cenu kalkulācija</span><span class="sxs-lookup"><span data-stu-id="a50f9-112">Specified</span></span>

    <span data-ttu-id="a50f9-113">**Ieturētā nodokļa sadalījuma** lauks rāda TDS sadalījuma metodi maksājumu grafikam.</span><span class="sxs-lookup"><span data-stu-id="a50f9-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="a50f9-114">Ja laukā **Sadalījums** atlasāt **Kopsumma**, lauks **Ieturētā nodokļa sadalījums** automātiski tiek iestatīts uz **Kopsumma**.</span><span class="sxs-lookup"><span data-stu-id="a50f9-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="a50f9-115">Ja atlasāt **Fiksēta summa**, **Fiksēts daudzums** vai **Norādīts** laukā **Sadalījums**, lauks **Ieturētā nodokļa sadalījums** tiek automātiski iestatīts uz **Proporcionāls**.</span><span class="sxs-lookup"><span data-stu-id="a50f9-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a50f9-116">Ja lauks **Ieturētā nodokļa sadalījums** ir iestatīts uz **Kopsumma**, maksājumi tiek aprēķināti, pamatojoties uz bruto summu, kas ietver TDS summu.</span><span class="sxs-lookup"><span data-stu-id="a50f9-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="a50f9-117">Ja lauks **Ieturētā nodokļa sadalījums** ir iestatīts uz **Proporcionāls**, maksājumi tiek aprēķināti, pamatojoties uz neto rēķina summu pēc TDS summas atskaitīšanas.</span><span class="sxs-lookup"><span data-stu-id="a50f9-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="a50f9-118">Ievadiet pārējo nepieciešamo informāciju un aizveriet lapu.</span><span class="sxs-lookup"><span data-stu-id="a50f9-118">Enter the other required details, and then close the page.</span></span>
