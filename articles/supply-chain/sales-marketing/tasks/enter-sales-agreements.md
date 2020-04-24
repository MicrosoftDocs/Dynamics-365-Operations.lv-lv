---
title: Pārdošanas līgumu ievade
description: Šajā tēmā ir aprakstīts, kā izveidot pārdošanas līgumu, kas i vienu no jūsu klientiem nopirkt preci par noteiktu summu laika gaitā apmaiņā par īpašām atlaidēm.
author: omulvad
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 723621f61a237d4b390271e65bce204c44ee4fc2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204336"
---
# <a name="enter-sales-agreements"></a><span data-ttu-id="e70ea-103">Pārdošanas līgumu ievade</span><span class="sxs-lookup"><span data-stu-id="e70ea-103">Enter sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e70ea-104">Šajā tēmā ir aprakstīts, kā izveidot pārdošanas līgumu, kas i vienu no jūsu klientiem nopirkt preci par noteiktu summu laika gaitā apmaiņā par īpašām atlaidēm.</span><span class="sxs-lookup"><span data-stu-id="e70ea-104">This topic explains how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="e70ea-105">Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="e70ea-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="e70ea-106">Pārdošanas līguma virsraksta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e70ea-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="e70ea-107">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Pārdošana un mārketings > Pārdošanas līgumi > Pārdošanas līgumi**.</span><span class="sxs-lookup"><span data-stu-id="e70ea-107">In the navigation pane, go to **Modules > Sales and marketing > Sales agreements > Sales agreements**.</span></span>
2. <span data-ttu-id="e70ea-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e70ea-108">Select **New**.</span></span>
3. <span data-ttu-id="e70ea-109">Laukā **Debitora konts** nolaižamajā izvēlnē atlasiet vēlamo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e70ea-109">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="e70ea-110">Laukā **Pārdošanas līguma klasifikācijā** atlasiet vēlamo ierakstu nolaižamajā izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="e70ea-110">In the **Sales agreement classification** field, select the desired record from the drop-down menu.</span></span>
5. <span data-ttu-id="e70ea-111">Izvērsiet sadaļu **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="e70ea-111">Expand the **General** section.</span></span>
6. <span data-ttu-id="e70ea-112">Laukā **Noklusējuma saistības** atlasiet **Preces vērtības saistības**.</span><span class="sxs-lookup"><span data-stu-id="e70ea-112">In the **Default commitment** field, select **Product value commitment**.</span></span> <span data-ttu-id="e70ea-113">Saistību veids ir obligāts kritērijs, kas ir jāpiešķir līgumam, lai definētu, kā līgums tiks izpildīts.</span><span class="sxs-lookup"><span data-stu-id="e70ea-113">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="e70ea-114">Izmantojot četrus iepriekš definētus veidus, var iestatīt klienta saistību mērķi, kas tiek izteikts kā daudzums vai vērtība.</span><span class="sxs-lookup"><span data-stu-id="e70ea-114">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="e70ea-115">Daudzuma saistību veidu var lietot tikai noteiktām precēm, bet vērtību veidus var lietot konkrētu vai vispārīga veida preču pārdošanā.</span><span class="sxs-lookup"><span data-stu-id="e70ea-115">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
7. <span data-ttu-id="e70ea-116">Laukā **Beigu datums** iestatiet datumu un nākotnes vēlamo līguma izbeigšanas datumu.</span><span class="sxs-lookup"><span data-stu-id="e70ea-116">In the **Expiration date** field, set the date to a future date when you want the agreement to expire.</span></span>
8. <span data-ttu-id="e70ea-117">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e70ea-117">Select **OK**.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="e70ea-118">Uz preču vērtību attiecināmo saistību rindu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="e70ea-118">Set up product value commitment lines</span></span>
1. <span data-ttu-id="e70ea-119">Atlasiet **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="e70ea-119">Select **Add line**.</span></span>
2. <span data-ttu-id="e70ea-120">Laukā **Vienuma numurs** atlasiet vēlamo ierakstu nolaižamajā izvēlnē.</span><span class="sxs-lookup"><span data-stu-id="e70ea-120">In the **Item number** field, select the desired record from the drop-down menu.</span></span> <span data-ttu-id="e70ea-121">Līgumam izvēlēto saistību veids ietekmē to, kāda veida informāciju var ievadīt līguma rindās.</span><span class="sxs-lookup"><span data-stu-id="e70ea-121">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="e70ea-122">Piemēram, vērtību līgumam ir jānorāda kopējā neto summa (saskaņotajā valūtā), par kuru debitors apņēmās nopirkt no jums preces.</span><span class="sxs-lookup"><span data-stu-id="e70ea-122">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="e70ea-123">Šajā piemērā lauki **Daudzums** un **Vienība** rindā nav pieejami, jo jūs veidojat līgumu, lai klients iegādātos noteiktu preces vērtību.</span><span class="sxs-lookup"><span data-stu-id="e70ea-123">In this example the **Quantity** and **Unit** fields on the line are unavailable because you're creating an agreement for the customer to buy a specific value of a product.</span></span>   
3. <span data-ttu-id="e70ea-124">Laukā **Neto summa** ievadiet naudas summu, ko klients ir iesniedzis pirkumam.</span><span class="sxs-lookup"><span data-stu-id="e70ea-124">In the **Net amount** field, enter the monetary amount that the customer has committed to buying.</span></span>
4. <span data-ttu-id="e70ea-125">Laukā **Atlaides procents** ievadiet procentuālo vērtību, kas tiks piemērota klienta pārdošanas pasūtījuma rindām, kas saistītas ar šo līgumu.</span><span class="sxs-lookup"><span data-stu-id="e70ea-125">In the **Discount percent** field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
5. <span data-ttu-id="e70ea-126">Izvērsiet sadaļu **Detalizēta informācija par rindu**.</span><span class="sxs-lookup"><span data-stu-id="e70ea-126">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="e70ea-127">Atlasiet **Jā** laukā **Sasniegts maksimums**.</span><span class="sxs-lookup"><span data-stu-id="e70ea-127">Select **Yes** in the **Max is enforced** field.</span></span>
    - <span data-ttu-id="e70ea-128">Atlasot **Sasniegts maksimums** nozīmē, ka kopējais pārdošanas pasūtījuma rindu skaits, kas izmanto apņemšanās īpašās cenas, atlaides un/vai maksājuma nosacījumus, nedrīkst pārsniegt apņemšanās norādīto summu.</span><span class="sxs-lookup"><span data-stu-id="e70ea-128">Selecting **Max is enforced** means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    - <span data-ttu-id="e70ea-129">Minimālā un maksimālā izlaišanas summa norāda to vērtību diapazonu, kas ir jāpārdod katrā pārdošanas pasūtījumā, kas izmanto atlasīto līgumu.</span><span class="sxs-lookup"><span data-stu-id="e70ea-129">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
7. <span data-ttu-id="e70ea-130">Izvērtiet sadaļu **Pārdošanas līguma virsraksts**.</span><span class="sxs-lookup"><span data-stu-id="e70ea-130">Expand the **Sales agreement header** section.</span></span> <span data-ttu-id="e70ea-131">Ja vien līguma statuss nav iestatīts uz **Spēkā**, pārdošanas pasūtījumus nevar saistīt ar līgumu un tādēļ nevar ietekmēt šāda līguma izpildi.</span><span class="sxs-lookup"><span data-stu-id="e70ea-131">Unless the status of the agreement is set to **Effective**, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="e70ea-132">Šajā posmā statusu var mainīt manuāli.</span><span class="sxs-lookup"><span data-stu-id="e70ea-132">You can change the status manually at this stage.</span></span> <span data-ttu-id="e70ea-133">Tomēr statuss parasti ir jāmaina tad, kad apstiprināt debitora līgumu.</span><span class="sxs-lookup"><span data-stu-id="e70ea-133">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
8. <span data-ttu-id="e70ea-134">Darbību rūtī atlasiet **Pārdošanas līgums**.</span><span class="sxs-lookup"><span data-stu-id="e70ea-134">On the Action Pane, select **Sales agreement**.</span></span>
9. <span data-ttu-id="e70ea-135">Atlasiet **Apstiprināšana**.</span><span class="sxs-lookup"><span data-stu-id="e70ea-135">Select **Confirmation**.</span></span> <span data-ttu-id="e70ea-136">Pārliecinieties, ka opcija **Atzīmēt līgumu kā spēkā esošu** ir iestatīta uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="e70ea-136">Make sure that the **Mark agreement as effective** option is set to **Yes**.</span></span>  
10. <span data-ttu-id="e70ea-137">Laukā **Drukāt pārskatu** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="e70ea-137">Select **Yes** in the **Print report** field.</span></span>
11. <span data-ttu-id="e70ea-138">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e70ea-138">Select **OK**.</span></span>
12. <span data-ttu-id="e70ea-139">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e70ea-139">Close the page.</span></span> <span data-ttu-id="e70ea-140">Līgums tagad ir spēkā.</span><span class="sxs-lookup"><span data-stu-id="e70ea-140">The agreement is now effective.</span></span> <span data-ttu-id="e70ea-141">Varat sākt saistīt klienta pasūtījumus ar līgumu, lai to ieskaitītu noteiktajā mērķī.</span><span class="sxs-lookup"><span data-stu-id="e70ea-141">You can start linking the customer's orders to the agreement to offset against the committed target.</span></span>  

