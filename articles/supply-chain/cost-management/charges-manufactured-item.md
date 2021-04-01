---
title: Saražoto krājumu maksu parādīšana
description: Ražota krājuma konstantas izmaksas atspoguļo operāciju iestatījumu laikus un komponentus ar konstantu daudzumu vai konstantu brāķa apjomu.
author: AndersGirke
manager: tfehr
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: f8d7fd7488630d9d24d5d7dc31ea39a10385a290
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235512"
---
# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="3050d-103">Saražoto krājumu maksu parādīšana</span><span class="sxs-lookup"><span data-stu-id="3050d-103">Display charges for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3050d-104">Ražota krājuma konstantas izmaksas atspoguļo operāciju iestatījumu laikus un komponentus ar konstantu daudzumu vai konstantu brāķa apjomu.</span><span class="sxs-lookup"><span data-stu-id="3050d-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="3050d-105">Krājuma maksu aprēķināto summu var parādīt ar krājumu vienības izmaksām.</span><span class="sxs-lookup"><span data-stu-id="3050d-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="3050d-106">Tomēr dažreiz maksas tiek attēlotas kā atsevišķi lauki un tās netiek iekļautas krājumu vienības izmaksās.</span><span class="sxs-lookup"><span data-stu-id="3050d-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="3050d-107">Ja maksas tiek attēlotas atsevišķos laukos, tad vienā laukā tiek attēlota kopējā maksu summa un otrā laukā tiek attēlots uzskaites laidiena apjoms, kas izmantots summas amortizācijā.</span><span class="sxs-lookup"><span data-stu-id="3050d-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="3050d-108">Piemēram, lapā Krājumu cena maksas ir parādītas divos atsevišķos laukos.</span><span class="sxs-lookup"><span data-stu-id="3050d-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="3050d-109">Tomēr lapā Pabeigt ir parādītas krājumu vienības kopējās izmaksas, un amortizētās izmaksas ir iekļautas vienības izmaksās.</span><span class="sxs-lookup"><span data-stu-id="3050d-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>

<span data-ttu-id="3050d-110">Maksas saražotajiem krājumiem vienmēr tiek iekļautas krājumu vienības izmaksās standarta izmaksu mērķiem.</span><span class="sxs-lookup"><span data-stu-id="3050d-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="3050d-111">Tās pēc izvēles ir iespējams plānoto izmaksu nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="3050d-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="3050d-112">Izmaksu novērtēšanas versijas politika pastiprina maksu iekļaušanu ražoto krājumu izmaksās.</span><span class="sxs-lookup"><span data-stu-id="3050d-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="3050d-113">Aktivizējot krājumu izmaksu ierakstu, tiek atjauninātas maksas krājumu pamata izmaksu informācijai, kas tiek parādīta lapā Krājumu cena.</span><span class="sxs-lookup"><span data-stu-id="3050d-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="3050d-114">Dažreiz maksas tiek attēlotas kā divi atsevišķi lauki un tās netiek iekļautas krājumu vienības izmaksās.</span><span class="sxs-lookup"><span data-stu-id="3050d-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="3050d-115">Katra aktivizācija atjaunina krājumu pamata izmaksu informāciju, pat ja aktivizācija atspoguļo dažādas vietas.</span><span class="sxs-lookup"><span data-stu-id="3050d-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="3050d-116">Tādēļ pamata izmaksu informācija būtu jāizmanto kā atsauces informācija.</span><span class="sxs-lookup"><span data-stu-id="3050d-116">Therefore, you should view the base cost information as reference information.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]