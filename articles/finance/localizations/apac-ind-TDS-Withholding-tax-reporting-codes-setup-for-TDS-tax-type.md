---
title: ieturētā nodokļa kodu pārskatu iestatīšana TDS nodokļu tipam
description: Ieturētā nodokļa pārskatu kodi tiek izmantoti, lai ģenerētu formas 26Q un formas 27Q pārskatus par No kopējo ienākumu summas atskaitīto nodokli (TDS). Šajā tēmā skaidrots, kā iestatīt ieturētā nodokļa pārskatu kodu darbības, lai varētu iestatīt TDS pārskatu kodus.
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
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023428"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a><span data-ttu-id="6e2e4-104">ieturētā nodokļa kodu pārskatu iestatīšana TDS nodokļu tipam</span><span class="sxs-lookup"><span data-stu-id="6e2e4-104">Set up withholding tax reporting codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e2e4-105">Ieturētā nodokļa pārskatu kodi tiek izmantoti, lai ģenerētu formas 26Q un formas 27Q pārskatus par No kopējo ienākumu summas atskaitīto nodokli (TDS).</span><span class="sxs-lookup"><span data-stu-id="6e2e4-105">Withholding tax reporting codes are used to generate Form 26Q and Form 27Q statements for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="6e2e4-106">Šajā tēmā skaidrots, kā iestatīt ieturētā nodokļa pārskatu kodu darbības, lai varētu iestatīt TDS pārskatu kodus.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-106">This topic explains how to set up withholding tax reporting codes steps so that you can set up TDS reporting codes.</span></span>

1. <span data-ttu-id="6e2e4-107">Atveriet **Nodoklis \> Iestatīšana \> Ieturētais nodoklis \> ieturētā nodokļa pārskatu kodi**.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-107">Go to **Tax \> Setup \> Withholding tax \> Withholding tax reporting codes**.</span></span>

    <span data-ttu-id="6e2e4-108">[![Ieturēto nodokļu pārskatu kodi lapa](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span><span class="sxs-lookup"><span data-stu-id="6e2e4-108">[![Withholding tax reporting codes page](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span></span>

2. <span data-ttu-id="6e2e4-109">Laukā **Nodokļu tips** atlasiet **TDS**, lai definētu ieturētā nodokļa pārskatu kodus TDS nodokļa tipam.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-109">In the **Tax type** field, select **TDS** to define withholding tax reporting codes for the TDS tax type.</span></span>
3. <span data-ttu-id="6e2e4-110">Laukā **Ieturama nodokļa komponents** atlasiet TDS komponentu, kam definē ieturētā nodokļa pārskata kodu.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-110">In the **Withholding tax component** field, select the TDS component to that you're defining the withholding tax reporting code for.</span></span> <span data-ttu-id="6e2e4-111">**Ieturētā nodokļa komponentu grupas** lauks rāda TDS komponentu grupu, kas tika definēta jūsu definētajam TDS komponentam.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-111">The **Withholding tax component group** field shows the TDS component group that was defined for the TDS component that you're defining.</span></span>

    <span data-ttu-id="6e2e4-112">Lauks **Sadaļas kods** kopsavilkuma cilnē **Vispārīgi** rāda sadaļas kodu, kas ir piesaistīts TDS komponentu grupai.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-112">The **Section code** field on the **General** FastTab shows the section code that is attached to the TDS component group.</span></span>

4. <span data-ttu-id="6e2e4-113">Kopsavilkuma cilnē **Vispārīgi** laukā **Pārskatu kods** atlasiet TDS pārskata kodu:</span><span class="sxs-lookup"><span data-stu-id="6e2e4-113">On the **General** FastTab, in the **Reporting code** field, select the TDS reporting code:</span></span>

    - <span data-ttu-id="6e2e4-114">TDS</span><span class="sxs-lookup"><span data-stu-id="6e2e4-114">TDS</span></span>
    - <span data-ttu-id="6e2e4-115">TCS</span><span class="sxs-lookup"><span data-stu-id="6e2e4-115">TCS</span></span>
    - <span data-ttu-id="6e2e4-116">Piemaksa</span><span class="sxs-lookup"><span data-stu-id="6e2e4-116">Surcharge</span></span>
    - <span data-ttu-id="6e2e4-117">PE\_Cess</span><span class="sxs-lookup"><span data-stu-id="6e2e4-117">PE\_Cess</span></span>
    - <span data-ttu-id="6e2e4-118">SHE\_Cess</span><span class="sxs-lookup"><span data-stu-id="6e2e4-118">SHE\_Cess</span></span>

5. <span data-ttu-id="6e2e4-119">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-119">Close the page.</span></span>
