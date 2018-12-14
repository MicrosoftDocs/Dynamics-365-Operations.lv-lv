---
title: "Retail debitoru rēķini un atgriešanas pārdošanas pasūtījumi Austrumeiropas valstīs"
description: "Šajā tēmā ir aprakstīts, kā iestatīt informāciju debitoru rēķiniem un pārdoto krājumu atgriešanas pasūtījumiem Austrumeiropas valstīs."
author: epopov
manager: annbe
ms.date: 10/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 01239f0eff3e59f62188fca64f99e93be843d2e2
ms.openlocfilehash: 20ae19fb03acb075b6553b95808779c905bcd31b
ms.contentlocale: lv-lv
ms.lasthandoff: 10/24/2018

---

# <a name="retail-customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a><span data-ttu-id="e3e6d-103">Retail debitoru rēķini un atgriešanas pārdošanas pasūtījumi Austrumeiropas valstīs</span><span class="sxs-lookup"><span data-stu-id="e3e6d-103">Retail customer invoices and return sales orders in Eastern European countries</span></span>


[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3e6d-104">Šajā tēmā ir aprakstīts, kā iestatīt informāciju debitoru rēķiniem un pārdoto krājumu atgriešanas pasūtījumiem Austrumeiropas valstīs.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-104">This topic describes how to set up information for customer invoices and return sales orders in Eastern European countries.</span></span>

<span data-ttu-id="e3e6d-105">Par debitoru rēķiniem un pārdoto krājumu atgriešanas pasūtījumiem, kas tiek ģenerēti programmā Retail point of sale (POS), varat iestatīt tālāk aprakstīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-105">You can set up the following information for customer invoices and return sales orders that are generated in Retail point of sale (POS).</span></span>

- <span data-ttu-id="e3e6d-106">Varat izmantot PVN grupas, lai apstrādātu atgrieztos krājumus, izmantojot pārdoto krājumu atgriešanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-106">You can use sales tax groups to process returns by using return sales orders.</span></span> <span data-ttu-id="e3e6d-107">Dodieties uz **Retail > Headquarters iestatīšana > Parametri > Mazumtirdzniecības parametri**.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-107">Go to **Retail > Headquarters setup > Parameters > Retail parameters**.</span></span> <span data-ttu-id="e3e6d-108">Atveriet cilni **Grāmatošana > Rēķins** un vienumu **Izmantot PVN grupu atgrieztajiem krājumiem** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-108">Open the **Posting > Invoice** tab, and then set **Use sales tax group for returns** to **Yes**.</span></span> 

  * <span data-ttu-id="e3e6d-109">Lai norādītu PVN grupu debitoru atgrieztajiem krājumiem, lapas **Debitori** kopsavilkuma cilnē **Mazumtirdzniecība**, laukā **PVN grupa atgrieztajiem krājumiem** atlasiet kādu PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-109">To specify the sales tax group for returns that are made by a customer, on the **Customers** page, on the **Retail** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="e3e6d-110">Kad kādam debitoram grāmatojat pārdoto krājumu atgriešanas pasūtījumu, pārdoto krājumu atgriešanas pasūtījuma rinda tiek atjaunināta ar formā **Debitori** krājumu atgriešanai norādīto PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-110">When you post a return sales order for a customer, the return sales order line is updated with the sales tax group for returns that is specified in the **Customers** form.</span></span>
  
  * <span data-ttu-id="e3e6d-111">Lai norādītu PVN grupu atgrieztajiem krājumiem, ko debitors veic pārdošanas punktā Retail POS, lapā **Veikali**, kopsavilkuma cilnē **Vispārīgi**, laukā **PVN grupa atgrieztajiem krājumiem** atlasiet kādu PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-111">To specify a sales tax group for returns that are made at a retail POS by a customer, on the **Stores** page, on the **General** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="e3e6d-112">Kad grāmatojat pārdoto krājumu atgriešanas pasūtījumu kādam mazumtirdzniecības veikala debitoram, pārdoto krājumu atgriešanas pasūtījuma rinda tiek atjaunināta ar lapā **Veikali** norādīto PVN grupu atgrieztajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-112">When you post a return sales order for a customer of a retail store, the return sales order line is updated with the sales tax group for returns that are specified on the **Stores** page.</span></span>

- <span data-ttu-id="e3e6d-113">Ja rēķinam vai krājumu atgriešanai nav noklusējuma pārdošanas datuma, kā rēķina vai atgriešanas pārdošanas datumu varat izmantot mazumtirdzniecības debitora rēķina grāmatošanas datumu vai pārdoto krājumu atgriešanas pasūtījuma datumu.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-113">You can use the posting date of a retail customer invoice or a return sales order as the sales date of the invoice or return if the invoice or return does not have a default sales date.</span></span> <span data-ttu-id="e3e6d-114">Dodieties uz **Retail > Headquarters iestatīšana > Parametri > Mazumtirdzniecības parametri**.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-114">Go to **Retail > Headquarters setup > Parameters > Retail parameters**.</span></span> <span data-ttu-id="e3e6d-115">Atveriet cilni **Grāmatošana > Rēķins** un vienumu **Izmantot grāmatošanas datumu kā pārdošanas datumu** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-115">Open the **Posting > Invoice** tab, and then set **Use posting date as sales date** to **Yes**.</span></span>

- <span data-ttu-id="e3e6d-116">Lai numurētu Latvijas un Lietuvas debitoru rēķinus un pārdoto krājumu atgriešanas pasūtījumus, varat izmantot numuru diapazonu, ko nodrošina nodokļu iestādes.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-116">You can use the number range that is provided by the tax authorities to number Latvian and Lithuanian customer invoices and return sales orders.</span></span> 

  * <span data-ttu-id="e3e6d-117">Dodieties uz **Organizācijas administrēšana > Numuru sērijas > Skaitītāju pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-117">Go to **Organization administration > Number sequences > Counters management**.</span></span> <span data-ttu-id="e3e6d-118">Tur vajadzētu būt ierakstam, kur **Modulis** = **Pārdošana** un **Tips** = **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-118">There should be a record where **Module** = **Sales** and **Type** = **Invoice**.</span></span>

  * <span data-ttu-id="e3e6d-119">Dodieties uz **Organizācijas administrēšana > Numuru sērijas > Rēķinu numerācijas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-119">Go to **Organization administration > Number sequences > Invoice numbering setup**.</span></span> <span data-ttu-id="e3e6d-120">Atlasiet izvēles rūtiņu **Mazumtirdzniecība** tai numuru sērijas rindai, kas tiek izmantota, lai numurētu debitoru rēķinus.</span><span class="sxs-lookup"><span data-stu-id="e3e6d-120">Select the **Retail** check box for the number sequence line that is used to number the customer invoices.</span></span>
