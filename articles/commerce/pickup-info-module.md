---
title: Saņemšanas informācijas modulis
description: Šajā tēmā tiek stāstīts par saņemšanas informācijas moduli un aprakstīts, kā to pievienot izrakstīšanās lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d04e2650f9c601d008ebf19080059b70416d7917
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000613"
---
# <a name="pickup-information-module"></a><span data-ttu-id="82b3c-103">Saņemšanas informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="82b3c-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="82b3c-104">Šajā tēmā tiek stāstīts par saņemšanas informācijas moduli un aprakstīts, kā to pievienot izrakstīšanās lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="82b3c-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="82b3c-105">Saņemšanas informācijas moduli var izmantot izrakstīšanās modulī, lai parādītu pasūtījuma saņemšanas informāciju.</span><span class="sxs-lookup"><span data-stu-id="82b3c-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="82b3c-106">Klienti var skatīt pieejamos saņemšanas datumus un laika nišas un pēc tam izvēlēties piemērotāko laiku, lai paņemtu pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="82b3c-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="82b3c-107">Piemēram, klients var izvēlēties saņemt pasūtījumu 21. martā plkst. 15.00 no Sanfrancisko veikala.</span><span class="sxs-lookup"><span data-stu-id="82b3c-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="82b3c-108">Commerce Headquarters ir jākonfigurē atbilstošajiem veikaliem paredzētās izdošanas laika nišas.</span><span class="sxs-lookup"><span data-stu-id="82b3c-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="82b3c-109">Papildinformāciju skatiet šeit: [Izveidot un atjaunināt laika nišas klientu preču saņemšanai](dev-itpro/pickup-timeslots.md).</span><span class="sxs-lookup"><span data-stu-id="82b3c-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="82b3c-110">Ja saņemšanas informācijas modulis ir izveidots izrakstīšanās lapā, bet veikalam, kas atlasīts saņemšanai, nav definētas laika nišas, modulis parādīs informāciju, bet lietotājs nevarēs atlasīt laika nišas.</span><span class="sxs-lookup"><span data-stu-id="82b3c-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="82b3c-111">Laika nišas nav obligātas un nav nepieciešams veikt pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="82b3c-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="82b3c-112">Ja ir atlasīti vairāki krājumi vairākiem veikaliem, saņemšanas informācijas modulis ļaus lietotājam izvēlēties laika nišu katram veikalam ar nosacījumu, ka laika nišas ir pieejamas.</span><span class="sxs-lookup"><span data-stu-id="82b3c-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="82b3c-113">Atbalsts laika nišām un izrakstīšanās saņemšanas informācijas modulim ir pieejams Dynamics 365 Commerce versijā 10.0.15 un jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="82b3c-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="82b3c-114">Sekojošajā attēlā ir parādīts laika nišas atlases piemērs, izmantojot saņemšanas informācijas moduli, kas atrodas izrakstīšanās lapā.</span><span class="sxs-lookup"><span data-stu-id="82b3c-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![Saņemšanas informācijas moduļa piemērs norēķināšanās lapā](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="82b3c-116">Moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="82b3c-116">Module properties</span></span>

- <span data-ttu-id="82b3c-117">**Virsraksts** - ievadiet virsrakstu modulim.</span><span class="sxs-lookup"><span data-stu-id="82b3c-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="82b3c-118">Rādīt laika nišu informāciju pēc tam, kad pasūtījums ir izveidots</span><span class="sxs-lookup"><span data-stu-id="82b3c-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="82b3c-119">Pēc tam, kad pasūtījums ir izveidots, informāciju par atlasīto laika nišu var apskatīt [pasūtījuma apstiprināšanas modulī](order-confirmation-module.md) un [pasūtījuma detalizētas informācijas modulī](account-management.md#order-details-page).</span><span class="sxs-lookup"><span data-stu-id="82b3c-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="82b3c-120">Abiem šiem moduļiem ir rekvizīts **Parādīt laika nišu informāciju**.</span><span class="sxs-lookup"><span data-stu-id="82b3c-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="82b3c-121">Pirms tiek parādīts atlasītais laika periods pasūtījuma procesa laikā, šis rekvizīts ir jāiestata uz **Patiess**.</span><span class="sxs-lookup"><span data-stu-id="82b3c-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="82b3c-122">Pievienot izrakstīšanās saņemšanas informācijas moduli lapā</span><span class="sxs-lookup"><span data-stu-id="82b3c-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="82b3c-123">Instrukcijas par to, kā pievienot saņemšanas informācijas moduli izrakstīšanās lapai un iestatīt pieprasītos rekvizītus, skatiet sadaļu [Izrakstīšanās modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="82b3c-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="82b3c-124">Sekojošajā attēlā parādīts e-tirdzniecības norēķinu lapas piemērs, kurā ir ietvertas saņemšanas rindu krājumu laika nišas.</span><span class="sxs-lookup"><span data-stu-id="82b3c-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![E-tirdzniecības norēķinu lapas piemērs, kurā ir ietvertas saņemšanas rindu krājumu laika nišas](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="82b3c-126">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="82b3c-126">Additional resources</span></span>

[<span data-ttu-id="82b3c-127">Izveidot un atjaunināt laika nišas klientu preču saņemšanai</span><span class="sxs-lookup"><span data-stu-id="82b3c-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="82b3c-128">Norēķināšanās modulis</span><span class="sxs-lookup"><span data-stu-id="82b3c-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="82b3c-129">Pasūtījuma apstiprinājuma modulis</span><span class="sxs-lookup"><span data-stu-id="82b3c-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="82b3c-130">Pasūtījumu informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="82b3c-130">Order details module</span></span>](account-management.md)
