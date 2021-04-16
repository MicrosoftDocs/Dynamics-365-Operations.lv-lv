---
title: Līdzekļu un līdzekļu veidu garantijas
description: Šajā tēmā ir paskaidrots, kā iestatīt līdzekļu un līdzekļu veidu garantijas līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f05f5af76aeb037d606d38a368a49d011f0d2bd6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825570"
---
# <a name="warranties-on-assets-and-asset-types"></a><span data-ttu-id="ba5bd-103">Līdzekļu un līdzekļu veidu garantijas</span><span class="sxs-lookup"><span data-stu-id="ba5bd-103">Warranties on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="ba5bd-104">Šajā tēmā ir paskaidrots, kā iestatīt līdzekļu un līdzekļu veidu garantijas līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="ba5bd-105">Garantijas iestatīšana līdzekļa veidam</span><span class="sxs-lookup"><span data-stu-id="ba5bd-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="ba5bd-106">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļa veidi** \> **Līdzekļa veidi**.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="ba5bd-107">Kreisajā rūtī atlasiet līdzekļa veidu, kam pievienot kreditora garantijas līgumu, un pēc tam atlasiet **Līdzekļu veidu noklusējumi**.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="ba5bd-108">Kopsavilkuma cilnes **Vispārīgi** laukā **Kreditora garantija** atlasiet līgumu.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="ba5bd-109">Garantijas iestatīšana līdzeklim</span><span class="sxs-lookup"><span data-stu-id="ba5bd-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="ba5bd-110">Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="ba5bd-111">Atlasiet līdzekli un pēc tam atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="ba5bd-112">Kopsavilkuma cilnes **Kreditors** sadaļā **Kreditora garantija** ir lauks **Garantija**, kurā jums ir jāatlasa garantijas līgums.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="ba5bd-113">Laukos **Garantijas sākums** un **Garantijas beigas** atlasiet sākuma un beigu datumus.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="ba5bd-114">Ja darba pasūtījuma laukā **Garantijas sākums** ir atlasīts datums, garantija ir derīga darba pasūtījumam šajā datumā.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="ba5bd-115">Veidojot darba pasūtījumu, lauks **Garantijas sākums** automātiski tiek iestatīts uz izveides datumu.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="ba5bd-116">Tomēr varat mainīt datumu tā, lai tas atbilstu, piemēram, garantijas līguma sākuma datumam.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![Darba pasūtījumu lapa](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="ba5bd-118">Kad izveidojat darba pasūtījumu līdzeklim, ko sedz kreditora garantija, ja darba pasūtījumam garantijas periodā ir paredzamais sākuma datums, jūs saņemat paziņojumu par garantijas līgumu.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="ba5bd-119">Pēc tam varat atcelt darba pasūtījumu, kā nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="ba5bd-119">You can then cancel the work order, as you require.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]