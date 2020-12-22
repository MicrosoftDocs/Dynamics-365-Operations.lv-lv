---
title: Rēķinu apmaksas scenāriju iestatīšana
description: Šajā tēmā ir aprakstīts, kā konfigurēt programmu Dynamics 365 Commerce, lai atbalstītu dažādus scenārijus saistībā ar rēķinu maksājumiem.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9fe8fde32549568812a724311781d3515ef7036c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459500"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="0337b-103">Rēķinu apmaksas scenāriju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="0337b-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0337b-104">Rēķinu apmaksāšanas funkcionalitāte programmā Dynamics 365 Commerce ir paplašināta, lai atbalstītu tālāk minētos elementus.</span><span class="sxs-lookup"><span data-stu-id="0337b-104">The Pay invoice functionality in Dynamics 365 Commerce has been expanded to support:</span></span>

- <span data-ttu-id="0337b-105">Vairāku pārdošanas pasūtījumu rēķinu apmaksa vienā POS transakcijā.</span><span class="sxs-lookup"><span data-stu-id="0337b-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="0337b-106">Dažādu debitora rēķinu veidu, tostarp brīva teksta rēķinu, projekta rēķinu un kredīta notu, apmaksa.</span><span class="sxs-lookup"><span data-stu-id="0337b-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="0337b-107">Lai iespējotu šos scenārijus, funkcionalitātes profils veikaliem jākonfigurē, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="0337b-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="0337b-108">Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Kanāla iestatīšana \> POS iestatījumi \> POS profili \> Funkcionalitātes profili** un izvēlieties profilu, kas ir piesaistīts veikaliem, kuriem vēlaties veikt izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="0337b-108">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="0337b-109">Cilnē **Funkcijas** pēc nepieciešamības konfigurējiet tālāk norādītos parametrus.</span><span class="sxs-lookup"><span data-stu-id="0337b-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="0337b-110">**Pārdošanas pasūtījuma rēķins** — atlasiet **Jā**, lai atļautu lietotājiem apmaksāt vienu vai vairākus pārdošanas pasūtījuma rēķinus vienā POS transakcijā.</span><span class="sxs-lookup"><span data-stu-id="0337b-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="0337b-111">**Brīva teksta rēķins** — atlasiet **Jā**, lai atļautu lietotājiem apmaksāt vienu vai vairākus brīva teksta rēķinus vienā POS transakcijā.</span><span class="sxs-lookup"><span data-stu-id="0337b-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="0337b-112">**Projekta rēķins** — atlasiet **Jā**, lai atļautu lietotājiem apmaksāt vienu vai vairākus projekta rēķinus vienā POS transakcijā.</span><span class="sxs-lookup"><span data-stu-id="0337b-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="0337b-113">**Pārdošanas pasūtījuma kredīta nota** — atlasiet **Jā**, lai atļautu lietotājiem nosegt vairākas pārdošanas pasūtījumu kredīta notas ar atvērtiem rēķiniem vai apstrādāt atmaksu debitoram par atvērtu kredīta notu.</span><span class="sxs-lookup"><span data-stu-id="0337b-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="0337b-114">Daļēju summu maksājums vai segšana vēl netiek atbalstīta.</span><span class="sxs-lookup"><span data-stu-id="0337b-114">Payment or settlement of partial amounts is not yet supported.</span></span>
