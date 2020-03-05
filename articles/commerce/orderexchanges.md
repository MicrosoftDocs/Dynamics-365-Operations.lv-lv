---
title: Atgriešanas pasūtījumu apmaiņu konfigurēšana un apstrādāšana
description: Šajā tēmā ir paskaidrots, kā konfigurēt atgriešanas apmaiņu programmā Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
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
ms.openlocfilehash: a6d7688e78a375bc262b1156c5439c0fff7cd1f0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004439"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="8a98f-103">Atgriešanas pasūtījumu apmaiņu konfigurēšana un apstrādāšana</span><span class="sxs-lookup"><span data-stu-id="8a98f-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8a98f-104">Iepriekšējās Dynamics 365 Commerce versijās atgriešana pret klientu pasūtījumiem tika apstrādāta, izmantojot atgriešanas pasūtījuma dokumentu komponentā Headquarters.</span><span class="sxs-lookup"><span data-stu-id="8a98f-104">In previous versions of Dynamics 365 Commerce, returns against customer orders were processed by using the return order document in Headquarters.</span></span> <span data-ttu-id="8a98f-105">Tomēr atgriešanas pasūtījuma dokumentu var izmantot, lai apstrādātu tikai preces, kas tiek atgrieztas.</span><span class="sxs-lookup"><span data-stu-id="8a98f-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="8a98f-106">Atgrieztās preces tiek norādītas ar negatīvu daudzumu atgriešanas pasūtījuma rindās.</span><span class="sxs-lookup"><span data-stu-id="8a98f-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="8a98f-107">Turpretim pārdošanu norāda ar pozitīvu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="8a98f-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="8a98f-108">Tomēr atgriešanas pasūtījuma dokuments neatbalsta pozitīvas daudzuma vērtības.</span><span class="sxs-lookup"><span data-stu-id="8a98f-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="8a98f-109">Šī ierobežojuma dēļ iepriekšējās programmas versijas neatbalstīja scenārijus, kuru ietvaros preču apmaiņa tika veikta, izmantojot atgriešanas pasūtījuma dokumentu.</span><span class="sxs-lookup"><span data-stu-id="8a98f-109">Because of this limitation, previous versions of the app didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="8a98f-110">Tomēr ir pievienota funkcionalitāte, lai nodrošinātu atbalstu scenārijiem, kuru ietvaros tiek veikta apmaiņa atgriešanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="8a98f-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="8a98f-111">Tagad programmā Commerce atgriešanas pasūtījuma dokumenta vietā tiek izmantots pārdošanas pasūtījuma dokuments, lai apstrādātu šādas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="8a98f-111">Commerce now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a><span data-ttu-id="8a98f-112">Commerce konfigurēšana, lai atbalstītu apmaiņu atgriešanas pasūtījumos</span><span class="sxs-lookup"><span data-stu-id="8a98f-112">Configure Commerce to support exchanges on return orders</span></span>

<span data-ttu-id="8a98f-113">Izpildiet šīs darbības, lai konfigurētu sistēmu, lai tā atbalstītu apmaiņu atgriešanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="8a98f-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="8a98f-114">Dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Tirdzniecības parametri**.</span><span class="sxs-lookup"><span data-stu-id="8a98f-114">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="8a98f-115">Kopsavilkuma cilnē **Debitoru pasūtījumi** opcijai **Apstrādāt atgriešanas pasūtījumus kā pārdošanas pasūtījumus** atlasiet iestatījumu **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8a98f-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="8a98f-116">Palaidiet darbu **Globālās konfigurācijas sadales grafiks** (**1110**).</span><span class="sxs-lookup"><span data-stu-id="8a98f-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="8a98f-117">Apmaiņas veikšana</span><span class="sxs-lookup"><span data-stu-id="8a98f-117">Make an exchange</span></span>

<span data-ttu-id="8a98f-118">Pēc tam, kad sistēma ir konfigurēta, kā aprakstīts iepriekšējā sadaļā, pārdošanas punkta (POS) lietotājs joprojām atlasa pārdošanas pasūtījumu vai pārdošanas rēķinu, lai apstrādātu atgriešanu kā iepriekšējās programmas versijās.</span><span class="sxs-lookup"><span data-stu-id="8a98f-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of the app.</span></span> <span data-ttu-id="8a98f-119">Tomēr pēc atgriezto krājumu pievienošanas grozam lietotājs varēs pievienot grozam jaunas pārdošanas rindas.</span><span class="sxs-lookup"><span data-stu-id="8a98f-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="8a98f-120">Šīm jaunajām pārdošanas rindām lietotājam ir jādefinē visi atribūti, kas vajadzīgi, lai apstrādātu debitora pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="8a98f-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="8a98f-121">Šie atribūti ietver piegādes veidu un izpildes vietu.</span><span class="sxs-lookup"><span data-stu-id="8a98f-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="8a98f-122">Par transakciju paredzētais maksājums ir atgriešanas pasūtījuma rindu un pārdošanas pasūtījuma rindu neto vērtība.</span><span class="sxs-lookup"><span data-stu-id="8a98f-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="8a98f-123">Kad darījumam atbilstošais maksājums tiks samaksāts, atgriešanas pasūtījums tiks grāmatots kā pārdošanas pasūtījuma dokuments programmā Headquarters un sistēma nekavējoties iekļaus rēķinā atgriešanas rindas.</span><span class="sxs-lookup"><span data-stu-id="8a98f-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="8a98f-124">Lai nodrošinātu labāku piekļuvi dažādām groza summām, grozā ir pievienoti trīs jauni summu lauki.</span><span class="sxs-lookup"><span data-stu-id="8a98f-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="8a98f-125">Var izmantot ekrāna veidotāju, lai nodrošinātu šo lauku pieejamību POS lietotāja interfeisā (UI).</span><span class="sxs-lookup"><span data-stu-id="8a98f-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="8a98f-126">**Piemērotais depozīts** — depozīta summa, kuru attiecina uz transakciju, kad lietotājs veic debitora pasūtījuma savākšanu.</span><span class="sxs-lookup"><span data-stu-id="8a98f-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="8a98f-127">Ja nav veikta depozīta ignorēšana un ir konfigurēts 10 procentu depozīts, šajā laukā norādītā summa ir 90 procenti no kopējās debitora pasūtījuma summas.</span><span class="sxs-lookup"><span data-stu-id="8a98f-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="8a98f-128">**Iznesto preču summa** — kopējā tādu rindu summa, kurām piegādes veids tika iestatīts kā **Iznest**, izveidojot vai rediģējot debitora pasūtījumu vai debitoru pasūtījuma apmaiņas laikā.</span><span class="sxs-lookup"><span data-stu-id="8a98f-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="8a98f-129">Šajā laukā norādītajā summā ir iekļauti nodokļi un papildmaksas.</span><span class="sxs-lookup"><span data-stu-id="8a98f-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="8a98f-130">**Atgriešanas summa** — kopējā tādu rindu summa, kurās ir negatīvas summas debitora pasūtījuma apmaiņas laikā.</span><span class="sxs-lookup"><span data-stu-id="8a98f-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="8a98f-131">Šajā laukā norādītajā summā ir iekļauti nodokļi un papildmaksas.</span><span class="sxs-lookup"><span data-stu-id="8a98f-131">The amount in this field includes taxes and charges.</span></span>