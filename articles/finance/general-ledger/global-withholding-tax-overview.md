---
title: Globālais ieturētais nodoklis
description: Šajā tēmā ir sniegta informācija par globālā ieturētā nodokļa funkcionalitāti un tās iestatīšanu. Globālā ieturētā nodokļa funkcionalitāte ir uzlabota kreditoru un debitoru transakcijām, tādējādi ieturētais nodoklis tiek aprēķināts krājumu līmenī.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 17ed1dcae97f6cd28175c483be5ca3ce96d59e05
ms.sourcegitcommit: 053f4cda6862fbcd9e3aa6e9cb009e7de833beac
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/28/2021
ms.locfileid: "5075742"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="4d1ba-104">Globālais ieturētais nodoklis</span><span class="sxs-lookup"><span data-stu-id="4d1ba-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d1ba-105">Šajā tēmā ir sniegta informācija par globālā ieturētā nodokļa funkcionalitāti un paskaidrota tās iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="4d1ba-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="4d1ba-106">Jaunā funkcionalitāte ir pieejama versijā 10.0.17 un jaunākās.</span><span class="sxs-lookup"><span data-stu-id="4d1ba-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="4d1ba-107">Globālā ieturētā nodokļa funkcionalitāte ir uzlabota kreditoru un debitoru transakcijām, tādējādi ieturētais nodoklis tiek aprēķināts krājumu līmenī.</span><span class="sxs-lookup"><span data-stu-id="4d1ba-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="4d1ba-108">Ieturamā nodokļa konta bilanci no pirkšanas transakcijām var segt, izpildot ieturamā nodokļa maksājuma uzdevumu ieturamā nodokļa norēķinu kontā.</span><span class="sxs-lookup"><span data-stu-id="4d1ba-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="4d1ba-109">Globālais ieturētais nodoklis neatbalsta funkciju **Uzturēt maksas** pirkšanas pasūtījuma, kreditora rēķina un pārdošanas pasūtījuma lapās.</span><span class="sxs-lookup"><span data-stu-id="4d1ba-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="4d1ba-110">Globālā ieturētā nodokļa iespējošana</span><span class="sxs-lookup"><span data-stu-id="4d1ba-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="4d1ba-111">Darbvietā **Līdzekļu pārvaldība** atlasiet **Globālais ieturētais nodoklis** un pēc tam atlasiet **Iespējot tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="4d1ba-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="4d1ba-112">Dodieties uz **Nodokļi \> Iestatīšana \> Parametri \> Virsgrāmatas parametri** un pēc tam cilnē **Ieturētais nodoklis** iestatiet opciju **Iespējot globālo ieturēto nodokli** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="4d1ba-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="4d1ba-113">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="4d1ba-113">Select **Save**.</span></span>
4. <span data-ttu-id="4d1ba-114">Atsvaidziniet lapu savā tīmekļa pārlūkprogrammā.</span><span class="sxs-lookup"><span data-stu-id="4d1ba-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="4d1ba-115">Globālo ieturētā nodokļa funkcionalitāti nevar iespējot tām valstīm/reģioniem, kur lokalizēti ieturētā nodokļa risinājumi jau pastāv.</span><span class="sxs-lookup"><span data-stu-id="4d1ba-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="4d1ba-116">Šīs teritorijas ietver Indiju, Brazīliju, Taizemi, Saūda Arābiju, Īriju, Lielbritāniju un Amerikas Savienotās Valstis, bet ne tikai.</span><span class="sxs-lookup"><span data-stu-id="4d1ba-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>
