---
title: Iestatīt ieturētā nodokļa iestādes TDS nodokļu tipam
description: Šajā tēmā skaidrots, kā iestatīt No kopējās ienākumu summas atskaitītā nodokļa (TDS) iestādes.
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
ms.openlocfilehash: 5375363a9b1383a83e80fc3c4b841780adab4172
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023410"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a><span data-ttu-id="81baa-103">Iestatīt ieturētā nodokļa iestādes TDS nodokļu tipam</span><span class="sxs-lookup"><span data-stu-id="81baa-103">Set up withholding tax authorities for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81baa-104">Šajā tēmā skaidrots, kā iestatīt No kopējās ienākumu summas atskaitītā nodokļa (TDS) iestādes.</span><span class="sxs-lookup"><span data-stu-id="81baa-104">This topic explains how to set up Tax Deducted at Source (TDS) authorities.</span></span>

1. <span data-ttu-id="81baa-105">Dodieties uz **Nodoklis \> Netiešie nodokļi \> ieturētā nodokļa iestādes**.</span><span class="sxs-lookup"><span data-stu-id="81baa-105">Go to **Tax \> Indirect taxes \> Withholding tax authorities**.</span></span>

    <span data-ttu-id="81baa-106">[![ieturētā nodokļa iestāžu lapa](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span><span class="sxs-lookup"><span data-stu-id="81baa-106">[![Withholding tax authorities page](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span></span>

2. <span data-ttu-id="81baa-107">Laukā **Nodokļu tips** atlasiet **TDS**, lai iestatītu ieturētā nodokļa iestādes TDS nodokļa tipam.</span><span class="sxs-lookup"><span data-stu-id="81baa-107">In the **Tax type** field, select **TDS** to set up withholding tax authorities for the TDS tax type.</span></span>
3. <span data-ttu-id="81baa-108">Lai izveidotu rindu, darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="81baa-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="81baa-109">Laukā **ieturētā nodokļa iestāde** ievadiet TDS iestādes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="81baa-109">In the **Withholding tax authority** field, enter a name for the TDS authority.</span></span>
5. <span data-ttu-id="81baa-110">Ievadiet aprakstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="81baa-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="81baa-111">Kopsavilkuma cilnes **Vispārīgi** laukā **Kreditora konts** atlasiet kreditora kontu TDS iestādei.</span><span class="sxs-lookup"><span data-stu-id="81baa-111">On the **General** FastTab, in the **Vendor account** field, select the vendor account for the TDS authority.</span></span>

    > [!NOTE]
    > <span data-ttu-id="81baa-112">Ir jādefinē bankas nosaukums, kurā tiks noguldīti līdzekļi, kas ir parādā TDS iestādes kreditoram.</span><span class="sxs-lookup"><span data-stu-id="81baa-112">You must define the name of the bank where funds that are owed to the TDS authority vendor will be deposited.</span></span> <span data-ttu-id="81baa-113">Bankas nosaukums ir definēts lapā **Bankas konts** (**Kreditori \> Visi kreditori \> Kreditors \> Iestatīt \> Bankas konti**).</span><span class="sxs-lookup"><span data-stu-id="81baa-113">The bank's name is defined on the **Bank accounts** page (**Accounts payable \> All vendors \> Vendor \> Set up \> Bank accounts**).</span></span>

7. <span data-ttu-id="81baa-114">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="81baa-114">Close the page.</span></span>
