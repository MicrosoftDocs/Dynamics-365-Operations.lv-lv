---
title: Pamatlīdzekļu atjaunināšana masveidā
description: Ja lietojat grāmatas, varat mainīt vienā grāmatā ietverto līdzekļu grupu nolietojuma aprēķināšanas metodes.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 3521
ms.assetid: 50207ffb-6b89-4fb9-92e9-928bc0729489
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc2f311e2463d68b9a8f8edb3afb82bef0934540
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212449"
---
# <a name="fixed-asset-mass-update"></a><span data-ttu-id="0551f-103">Pamatlīdzekļu atjaunināšana masveidā</span><span class="sxs-lookup"><span data-stu-id="0551f-103">Fixed asset mass update</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0551f-104">Ja lietojat grāmatas, varat mainīt vienā grāmatā ietverto līdzekļu grupu nolietojuma aprēķināšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="0551f-104">If you use books, you can change the depreciation conventions for groups of assets that are part of the same book.</span></span>

<span data-ttu-id="0551f-105">Piemēram, ja atrodaties Amerikas Savienotajās Valstīs un gada ceturtā ceturkšņa laikā nododat lietošanā vairāk nekā 40 procentu savu līdzekļu, ceturkšņa vidū jums jāveic nolietojuma aprēķināšana.</span><span class="sxs-lookup"><span data-stu-id="0551f-105">For example, if you are in the United States, and you put more than 40 percent of your assets in service during the fourth quarter of the year, you must use the mid-quarter depreciation convention.</span></span> <span data-ttu-id="0551f-106">Jūs varat izmantot masveida atjaunināšanas procesu, lai izmainītu visus līdzekļus, kam jāveic nolietojuma aprēķināšana.</span><span class="sxs-lookup"><span data-stu-id="0551f-106">You can use the process for a mass update to change all assets that require the new depreciation convention.</span></span> 

<span data-ttu-id="0551f-107">Atjauninot līdzekļu nolietojuma aprēķinus, tiek dzēstas visas nolietojuma transakcijas, kas veiktas saistībā ar šiem līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="0551f-107">When you update the depreciation convention for assets, you delete all depreciation transactions that exist for those assets.</span></span> <span data-ttu-id="0551f-108">Tiek dzēstas arī visas ar šo līdzekļu nolietojuma korekcijām, papildnolietojumu un ārkārtas nolietojumu saistītās transakcijas.</span><span class="sxs-lookup"><span data-stu-id="0551f-108">You also delete all transactions for depreciation adjustments, transactions for bonus depreciation, and transactions for extraordinary depreciation for those assets.</span></span> 

<span data-ttu-id="0551f-109">Lai atjauninātu norakstīto līdzekļu nolietojuma aprēķinus, vispirms ir jāizdzēš esošās norakstīšanas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="0551f-109">To update the depreciation convention for assets that have already been disposed of, you must first delete the existing disposal transactions.</span></span> <span data-ttu-id="0551f-110">Jādzēš arī visas transakcijas, kas tika ģenerētas saistībā ar norakstīšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="0551f-110">You must also delete all transactions that were generated because of the disposal process.</span></span> 

<span data-ttu-id="0551f-111">Kad līdzekļu nolietojuma aprēķināšana ir atjaunināta, var izpildīt katra līdzekļa nolietojuma un ārkārtas nolietojuma aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="0551f-111">After you update the depreciation convention for assets, you can process depreciation and extraordinary depreciation for each asset.</span></span> <span data-ttu-id="0551f-112">Nepieciešamības gadījumā var veikt arī manuālas nolietojuma korekcijas.</span><span class="sxs-lookup"><span data-stu-id="0551f-112">You can also make manual depreciation adjustments, if any adjustments are required.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]