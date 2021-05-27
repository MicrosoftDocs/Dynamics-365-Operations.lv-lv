---
title: Virsgrāmatas konta TDS iestatīšana
description: Šajā tēmā skaidrots, kā iestatīt virsgrāmatas kontu No kopējo ienākumu summas atskaitītā nodokļa (TDS) funkcijai.
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
ms.openlocfilehash: 93d4cb54488ec0eeee40ca56f3e46f30012f54f5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023417"
---
# <a name="set-up-tds-ledger-accounts"></a><span data-ttu-id="f686c-103">Virsgrāmatas konta TDS iestatīšana</span><span class="sxs-lookup"><span data-stu-id="f686c-103">Set up TDS ledger accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f686c-104">Šajā tēmā skaidrots, kā iestatīt virsgrāmatas kontu No kopējo ienākumu summas atskaitītā nodokļa (TDS) funkcijai.</span><span class="sxs-lookup"><span data-stu-id="f686c-104">This topic explains how to set up ledger accounts for the Tax Deducted at Source (TDS) feature.</span></span> <span data-ttu-id="f686c-105">Jūs izmantojat lapu **Kontu plāns**, lai iestatītu virsgrāmatas kontus TDS.</span><span class="sxs-lookup"><span data-stu-id="f686c-105">You use the **Chart of accounts** page to set up ledger accounts for TDS.</span></span>

1. <span data-ttu-id="f686c-106">Dodieties uz **Virsgrāmata \> Kontu plāns \> Konti \> Galvenie konti**.</span><span class="sxs-lookup"><span data-stu-id="f686c-106">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**.</span></span>
2. <span data-ttu-id="f686c-107">Cilnē **Pārskats** atlasiet **Alt+N**, lai izveidotu TDS virsgrāmatas kontu, un ievadiet nepieciešamo informāciju.</span><span class="sxs-lookup"><span data-stu-id="f686c-107">On the **Overview** tab, select **Alt+N** to create a TDS ledger account, and enter the required details.</span></span>
3. <span data-ttu-id="f686c-108">Cilnes **Iestatījumi** laukā **Grāmatošanas tips** atlasiet **Ieturētais nodoklis**.</span><span class="sxs-lookup"><span data-stu-id="f686c-108">On the **Setup** tab, in the **Posting type** field, select **Withholding tax**.</span></span>     

    > [!NOTE]
    > <span data-ttu-id="f686c-109">Virsgrāmatas kontus, kuru grāmatošanas tips ir **Ieturētais nodoklis** var definēt tikai kā debitoru kontus, kas tiek izmantoti TDS ieņēmumu summas grāmatošanai TDS nodokļa kodam.</span><span class="sxs-lookup"><span data-stu-id="f686c-109">Ledger accounts that have a posting type of **Withholding tax** can be defined only as receivable accounts that are used to post the TDS receivable amount for a TDS tax code.</span></span>

4. <span data-ttu-id="f686c-110">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f686c-110">Close the page.</span></span>
