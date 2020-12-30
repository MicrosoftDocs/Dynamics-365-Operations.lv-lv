---
title: Debitoru rēķini un atgriešanas pārdošanas pasūtījumi Austrumeiropas valstīs
description: Šajā tēmā ir aprakstīts, kā iestatīt informāciju debitoru rēķiniem un pārdoto krājumu atgriešanas pasūtījumiem Austrumeiropas valstīs.
author: epopov
manager: annbe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a00a960142b0e3955c80d75f7963f4827209bf75
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408267"
---
# <a name="customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a><span data-ttu-id="926be-103">Debitoru rēķini un atgriešanas pārdošanas pasūtījumi Austrumeiropas valstīs</span><span class="sxs-lookup"><span data-stu-id="926be-103">Customer invoices and return sales orders in Eastern European countries</span></span>


[!include [banner](../../includes/banner.md)]

<span data-ttu-id="926be-104">Šajā tēmā ir aprakstīts, kā iestatīt informāciju debitoru rēķiniem un pārdoto krājumu atgriešanas pasūtījumiem Austrumeiropas valstīs.</span><span class="sxs-lookup"><span data-stu-id="926be-104">This topic describes how to set up information for customer invoices and return sales orders in Eastern European countries.</span></span>

<span data-ttu-id="926be-105">Par debitoru rēķiniem un pārdoto krājumu atgriešanas pasūtījumiem, kas tiek ģenerēti programmā Retail point of sale (POS), varat iestatīt tālāk aprakstīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="926be-105">You can set up the following information for customer invoices and return sales orders that are generated in Retail point of sale (POS).</span></span>

- <span data-ttu-id="926be-106">Varat izmantot PVN grupas, lai apstrādātu atgrieztos krājumus, izmantojot pārdoto krājumu atgriešanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="926be-106">You can use sales tax groups to process returns by using return sales orders.</span></span> <span data-ttu-id="926be-107">Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri \> Komercijas parametri**.</span><span class="sxs-lookup"><span data-stu-id="926be-107">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="926be-108">Atveriet cilni **Grāmatošana \> Rēķins** un iestatiet vienumu **Izmantot PVN grupu atgrieztajiem krājumiem** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="926be-108">Open the **Posting \> Invoice** tab, and then set **Use sales tax group for returns** to **Yes**.</span></span>

    * <span data-ttu-id="926be-109">Lai norādītu PVN grupu debitoru atgrieztajiem krājumiem, lapas **Debitori** kopsavilkuma cilnē **Komercija**, laukā **PVN grupa atgrieztajiem krājumiem** atlasiet kādu PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="926be-109">To specify the sales tax group for returns that are made by a customer, on the **Customers** page, on the **Commerce** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="926be-110">Kad kādam debitoram grāmatojat pārdoto krājumu atgriešanas pasūtījumu, pārdoto krājumu atgriešanas pasūtījuma rinda tiek atjaunināta ar formā **Debitori** krājumu atgriešanai norādīto PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="926be-110">When you post a return sales order for a customer, the return sales order line is updated with the sales tax group for returns that is specified in the **Customers** form.</span></span>
    * <span data-ttu-id="926be-111">Lai norādītu PVN grupu atgrieztajiem krājumiem, ko debitors veic pārdošanas punktā Retail POS, lapā **Veikali**, kopsavilkuma cilnē **Vispārīgi**, laukā **PVN grupa atgrieztajiem krājumiem** atlasiet kādu PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="926be-111">To specify a sales tax group for returns that are made at a retail POS by a customer, on the **Stores** page, on the **General** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="926be-112">Kad grāmatojat pārdoto krājumu atgriešanas pasūtījumu kādam veikala debitoram, pārdoto krājumu atgriešanas pasūtījuma rinda tiek atjaunināta ar lapā **Veikali** norādīto PVN grupu atgrieztajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="926be-112">When you post a return sales order for a customer of a  store, the return sales order line is updated with the sales tax group for returns that are specified on the **Stores** page.</span></span>

- <span data-ttu-id="926be-113">Ja rēķinam vai krājumu atgriešanai nav noklusējuma pārdošanas datuma, kā rēķina vai atgriešanas pārdošanas datumu varat izmantot debitora rēķina grāmatošanas datumu vai pārdoto krājumu atgriešanas pasūtījuma datumu.</span><span class="sxs-lookup"><span data-stu-id="926be-113">You can use the posting date of a customer invoice or a return sales order as the sales date of the invoice or return if the invoice or return does not have a default sales date.</span></span> <span data-ttu-id="926be-114">Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri \> Komercijas parametri**.</span><span class="sxs-lookup"><span data-stu-id="926be-114">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="926be-115">Atveriet cilni **Grāmatošana \> Rēķins** un iestatiet vienumu **Izmantot grāmatošanas datumu kā pārdošanas datumu** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="926be-115">Open the **Posting \> Invoice** tab, and then set **Use posting date as sales date** to **Yes**.</span></span>
- <span data-ttu-id="926be-116">Lai numurētu Latvijas un Lietuvas debitoru rēķinus un pārdoto krājumu atgriešanas pasūtījumus, varat izmantot numuru diapazonu, ko nodrošina nodokļu iestādes.</span><span class="sxs-lookup"><span data-stu-id="926be-116">You can use the number range that is provided by the tax authorities to number Latvian and Lithuanian customer invoices and return sales orders.</span></span>

    * <span data-ttu-id="926be-117">Dodieties uz **Organizācijas administrēšana \> Numuru sērijas \> Skaitītāju pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="926be-117">Go to **Organization administration \> Number sequences \> Counters management**.</span></span> <span data-ttu-id="926be-118">Tur vajadzētu būt ierakstam, kur **Modulis** = **Pārdošana** un **Tips** = **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="926be-118">There should be a record where **Module** = **Sales** and **Type** = **Invoice**.</span></span>
    * <span data-ttu-id="926be-119">Dodieties uz **Organizācijas administrēšana \> Numuru sērijas \> Rēķinu numerācijas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="926be-119">Go to **Organization administration \> Number sequences \> Invoice numbering setup**.</span></span> <span data-ttu-id="926be-120">Atlasiet izvēles rūtiņu **Komercija** tai numuru sērijas rindai, kas tiek izmantota, lai numurētu debitoru rēķinus.</span><span class="sxs-lookup"><span data-stu-id="926be-120">Select the **Commerce** check box for the number sequence line that is used to number the customer invoices.</span></span>
