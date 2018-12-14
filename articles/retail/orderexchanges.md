---
title: "Konfigurēt un apstrādāt apmaiņu atgriešanas pasūtījumos"
description: "Šajā tēmā ir paskaidrots, kā konfigurēt atgriešanas apmaiņu programmā Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3331b984693c58c6ee8c49b98ed7d3a8df5b79ff
ms.openlocfilehash: 45b628376a483d3d639e5c018dd93570ed8ce7af
ms.contentlocale: lv-lv
ms.lasthandoff: 12/04/2018

---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="ddc5b-103">Konfigurēt un apstrādāt apmaiņu atgriešanas pasūtījumos</span><span class="sxs-lookup"><span data-stu-id="ddc5b-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ddc5b-104">Microsoft Dynamics 365 for Retail iepriekšējās versijās klientu pasūtījumu atgriešana tika apstrādāta, izmantojot atgriešanas pasūtījuma dokumentu, kas pieejams Retail Headquarters.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-104">In previous versions of Microsoft Dynamics 365 for Retail, returns against customer orders were processed by using the return order document in Retail headquarters.</span></span> <span data-ttu-id="ddc5b-105">Tomēr atgriešanas pasūtījuma dokumentu var izmantot, lai apstrādātu tikai preces, kas tiek atgrieztas.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="ddc5b-106">Atgrieztās preces tiek norādītas ar negatīvu daudzumu atgriešanas pasūtījuma rindās.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="ddc5b-107">Turpretim pārdošanu norāda ar pozitīvu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="ddc5b-108">Tomēr atgriešanas pasūtījuma dokuments neatbalsta pozitīvas daudzuma vērtības.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="ddc5b-109">Šī ierobežojuma dēļ iepriekšējās Retail versijas neatbalstīja scenārijus, kuru ietvaros preču apmaiņa tika veikta, izmantojot atgriešanas pasūtījuma dokumentu.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-109">Because of this limitation, previous versions of Retail didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="ddc5b-110">Tomēr ir pievienota funkcionalitāte, lai nodrošinātu atbalstu scenārijiem, kuru ietvaros tiek veikta apmaiņa atgriešanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="ddc5b-111">Tagad programmā Retail atgriešanas pasūtījuma dokumenta vietā tiek izmantots pārdošanas pasūtījuma dokuments, lai apstrādātu šādas transakcijas.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-111">Retail now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a><span data-ttu-id="ddc5b-112">Retail konfigurēšana, lai atbalstītu apmaiņu atgriešanas pasūtījumos</span><span class="sxs-lookup"><span data-stu-id="ddc5b-112">Configure Retail to support exchanges on return orders</span></span>

<span data-ttu-id="ddc5b-113">Izpildiet šīs darbības, lai konfigurētu sistēmu, lai tā atbalstītu apmaiņu atgriešanas pasūtījumos.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="ddc5b-114">Dodieties uz **Mazumtirdzniecība \> Headquarters iestatīšana \> Parametri \> Mazumtirdzniecības parametri**.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-114">Go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="ddc5b-115">Kopsavilkuma cilnē **Debitoru pasūtījumi** opcijai **Apstrādāt atgriešanas pasūtījumus kā pārdošanas pasūtījumus** atlasiet iestatījumu **Jā**.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="ddc5b-116">Palaidiet darbu **Globālās konfigurācijas sadales grafiks** (**1110**).</span><span class="sxs-lookup"><span data-stu-id="ddc5b-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="ddc5b-117">Apmaiņas veikšana</span><span class="sxs-lookup"><span data-stu-id="ddc5b-117">Make an exchange</span></span>

<span data-ttu-id="ddc5b-118">Pēc tam, kad sistēma ir konfigurēta, kā aprakstīts iepriekšējā sadaļā, pārdošanas punkta (POS) lietotājs joprojām atlasa pārdošanas pasūtījumu vai pārdošanas rēķinu, lai apstrādātu atgriešanu kā iepriekšējās Retail versijās.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of Retail.</span></span> <span data-ttu-id="ddc5b-119">Tomēr pēc atgriezto krājumu pievienošanas grozam lietotājs varēs pievienot grozam jaunas pārdošanas rindas.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="ddc5b-120">Šīm jaunajām pārdošanas rindām lietotājam ir jādefinē visi atribūti, kas vajadzīgi, lai apstrādātu debitora pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="ddc5b-121">Šie atribūti ietver piegādes veidu un izpildes vietu.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="ddc5b-122">Par transakciju paredzētais maksājums ir atgriešanas pasūtījuma rindu un pārdošanas pasūtījuma rindu neto vērtība.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="ddc5b-123">Ja maksājums par transakciju ir samaksāts, atgriešanas pasūtījums tiks grāmatots kā pārdošanas pasūtījuma dokuments programmā Retail Headquarters un sistēma nekavējoties iekļaus rēķinā atgriešanas rindas.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Retail headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="ddc5b-124">Lai nodrošinātu labāku piekļuvi dažādām groza summām, grozā ir pievienoti trīs jauni summu lauki.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="ddc5b-125">Var izmantot ekrāna veidotāju, lai nodrošinātu šo lauku pieejamību POS lietotāja interfeisā (UI).</span><span class="sxs-lookup"><span data-stu-id="ddc5b-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="ddc5b-126">**Piemērotais depozīts** — depozīta summa, kuru attiecina uz transakciju, kad lietotājs veic debitora pasūtījuma savākšanu.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="ddc5b-127">Ja nav veikta depozīta ignorēšana un ir konfigurēts 10 procentu depozīts, šajā laukā norādītā summa ir 90 procenti no kopējās debitora pasūtījuma summas.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="ddc5b-128">**Iznesto preču summa** — kopējā tādu rindu summa, kurām piegādes veids tika iestatīts kā **Iznest**, izveidojot vai rediģējot debitora pasūtījumu vai debitoru pasūtījuma apmaiņas laikā.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="ddc5b-129">Šajā laukā norādītajā summā ir iekļauti nodokļi un papildmaksas.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="ddc5b-130">**Atgriešanas summa** — kopējā tādu rindu summa, kurās ir negatīvas summas debitora pasūtījuma apmaiņas laikā.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="ddc5b-131">Šajā laukā norādītajā summā ir iekļauti nodokļi un papildmaksas.</span><span class="sxs-lookup"><span data-stu-id="ddc5b-131">The amount in this field includes taxes and charges.</span></span>
