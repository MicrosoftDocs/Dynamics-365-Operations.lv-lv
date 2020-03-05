---
title: Opcijas, kas neļauj lietot atlaides mazumtirdzniecības precēm
description: Ir dažādi iemesli, kāpēc mazumtirgotāji varētu vēlēties nepieļaut atlaižu piemērošanu dažiem produktiem veicināšanas pasākumu vai pārdošanas ietvaros POS terminālī.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 822bd39bca3a95f073bacea90a8ee58eada50ae2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023336"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="a2ac9-103">Opcijas, kas neļauj lietot atlaides mazumtirdzniecības precēm</span><span class="sxs-lookup"><span data-stu-id="a2ac9-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a2ac9-104">Ir dažādi iemesli, kāpēc mazumtirgotāji varētu vēlēties nepieļaut atlaižu piemērošanu dažiem produktiem veicināšanas pasākumu vai pārdošanas ietvaros POS terminālī.</span><span class="sxs-lookup"><span data-stu-id="a2ac9-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="a2ac9-105">Tālāk norādītas izlaisto preču cilnē **Komercija** pieejamās opcijas preces konfigurēšanai tā, lai nepieļautu nekādas vai manuālas atlaides.</span><span class="sxs-lookup"><span data-stu-id="a2ac9-105">The following options, which can be found on the **Commerce** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="a2ac9-106">Iestatījumus var norādīt mazumtirdzniecības kategoriju hierarhijas kategoriju līmenī.</span><span class="sxs-lookup"><span data-stu-id="a2ac9-106">The settings can also be specified at the category level from the retail category hierarchy.</span></span>

- <span data-ttu-id="a2ac9-107">**Nepieļaut nekādas atlaides** — atlasiet šo opciju, lai nepieļautu nekādu veidu atlaides šai precei.</span><span class="sxs-lookup"><span data-stu-id="a2ac9-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="a2ac9-108">Tas ietver veicināšanas pasākumus, piemēram, komplektu piedāvājumus, daudzuma un sliekšņvērtību atlaides, kā arī manuālas rindu un transakciju atlaides, ko tirdzniecības laikā piemēro POS lietotājs.</span><span class="sxs-lookup"><span data-stu-id="a2ac9-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="a2ac9-109">**Nepieļaut manuālas atlaides** — atlasiet šo opciju, lai nepieļautu tikai manuālas rindu vai transakciju atlaides, ko tirdzniecības laikā piemēro POS lietotājs.</span><span class="sxs-lookup"><span data-stu-id="a2ac9-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="a2ac9-110">Precēm, kurām ir atlasīta šī opcija, joprojām var piemērot veicināšanas pasākumus, piemēram, komplekta atlaides un daudzuma un sliekšņvērtības atlaides.</span><span class="sxs-lookup"><span data-stu-id="a2ac9-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="a2ac9-111">Šie iestatījumi neierobežo cenas pārrakstīšanas darbību, jo tās gaitā tiek iestatīta pamatcena, kas netiek uzskatīta par atlaidi.</span><span class="sxs-lookup"><span data-stu-id="a2ac9-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="a2ac9-112">[![Lauks Nepieļaut atlaides](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="a2ac9-112">[![Prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>