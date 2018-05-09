--- 
title: "Attiecināmo cenu un atlaižu pārlūkošana"
description: "Šajā procedūrā parādīts, kā atrast cenu un/vai atlaidi precei, kas pašlaik derīga noteiktam debitoram, neizveidojot pārdošanas pasūtījumu."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ba95e651898da0e0fbd1221f61436ffac59db09e
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="54eeb-103">Attiecināmo cenu un atlaižu pārlūkošana</span><span class="sxs-lookup"><span data-stu-id="54eeb-103">Look up applicable prices and discounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54eeb-104">Šajā procedūrā parādīts, kā atrast cenu un/vai atlaidi precei, kas pašlaik derīga noteiktam debitoram, neizveidojot pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="54eeb-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="54eeb-105">Procedūra palīdz veikt konkrētu piemēru, un, lai atlasītu nepieciešamās vērtības, ir nepieciešams sekot piemēram, izmantojot USMF demonstrācijas uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="54eeb-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="54eeb-106">Piemērojamās cenas atrašana</span><span class="sxs-lookup"><span data-stu-id="54eeb-106">Find the applicable price</span></span>
1. <span data-ttu-id="54eeb-107">Dodieties uz sadaļu Pārdošana un mārketings > Cenas un atlaides > Atrast cenas.</span><span class="sxs-lookup"><span data-stu-id="54eeb-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="54eeb-108">Laukā Debitora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="54eeb-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="54eeb-109">Sarakstā atrodiet un atlasiet debitoru US-001.</span><span class="sxs-lookup"><span data-stu-id="54eeb-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="54eeb-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="54eeb-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="54eeb-111">Laukā Krājuma kods ierakstiet T0004.</span><span class="sxs-lookup"><span data-stu-id="54eeb-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="54eeb-112">Pēc noklusējuma lauka Daudzums vērtības iestatījums ir 1.</span><span class="sxs-lookup"><span data-stu-id="54eeb-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="54eeb-113">Tomēr, ja zināt konkrētas preces pasūtījuma apjomu, ko veiks debitors, tad ievadiet tā vērtību.</span><span class="sxs-lookup"><span data-stu-id="54eeb-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="54eeb-114">Šī informācija ir būtiska, ja tirdzniecības līgumos ar debitoru pastāv daudzumu pārtraukumi, t.i., preces cena ir atkarīga no minimālā iepirktā daudzuma.</span><span class="sxs-lookup"><span data-stu-id="54eeb-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="54eeb-115">Laukā Datums ievadiet datumu, kad debitors plāno veikt pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="54eeb-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="54eeb-116">Datums var būt šodienas datums vai jebkurš datums nākotnē.</span><span class="sxs-lookup"><span data-stu-id="54eeb-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="54eeb-117">Sistēma tagad atgriež cenu, kura atbilst atlasītajai precei, kad atlasītais debitors to pērk atlasītajā datumā un norādītajā daudzumā.</span><span class="sxs-lookup"><span data-stu-id="54eeb-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="54eeb-118">Šajā piemērā, ja debitors US-001 pērk 1 preces T0004 vienību šodien, tam būs jāmaksā 350 CAD par vienību.</span><span class="sxs-lookup"><span data-stu-id="54eeb-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="54eeb-119">Šī cena tiek ņemta no esošā un aktīvā tirdzniecības līguma ar debitoru.</span><span class="sxs-lookup"><span data-stu-id="54eeb-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="54eeb-120">Citi lauki lapā sniedz papildinformāciju par preces cenu un preces izmaksām (ja iestatīts preču šablonā), un aprēķināto ienesīgumu.</span><span class="sxs-lookup"><span data-stu-id="54eeb-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="54eeb-121">Ja ir atlasīta opcija Rādīt saistītās preces variantus, tas nozīmē, ka ir papildu tirdzniecības līgumi preces variantiem.</span><span class="sxs-lookup"><span data-stu-id="54eeb-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="54eeb-122">Atzīmējiet izvēles rūtiņu Rādīt saistītos preces variantus.</span><span class="sxs-lookup"><span data-stu-id="54eeb-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="54eeb-123">Preču variantu saraksts tiek parādīts kopā ar informāciju par to dimensijām.</span><span class="sxs-lookup"><span data-stu-id="54eeb-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="54eeb-124">Sarakstā iezīmējiet Baltās krāsas rindu.</span><span class="sxs-lookup"><span data-stu-id="54eeb-124">In the list, mark the line representing color White.</span></span>
    * <span data-ttu-id="54eeb-125">Ņemiet vērā, ka preces cena tagad atšķiras no iepriekš parādītās, kad dimensijas nebija norādītas.</span><span class="sxs-lookup"><span data-stu-id="54eeb-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="54eeb-126">Noklikšķiniet uz Skatīt pārdošanas cenas.</span><span class="sxs-lookup"><span data-stu-id="54eeb-126">Click View sales prices.</span></span>
    * <span data-ttu-id="54eeb-127">Lapā Cena (pārdošana) tiek parādīti visi tirdzniecības līgumi, kas attiecas uz preci, tostarp tās variantiem.</span><span class="sxs-lookup"><span data-stu-id="54eeb-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="54eeb-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="54eeb-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="54eeb-129">Piemērojamās atlaides atrašana</span><span class="sxs-lookup"><span data-stu-id="54eeb-129">Find the applicable discount</span></span>
    * <span data-ttu-id="54eeb-130">Pārliecinieties, ka laukā Debitora konts ir norādīts klienta numurs US-001 </span><span class="sxs-lookup"><span data-stu-id="54eeb-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="54eeb-131">Laukā Krājuma kods ierakstiet T0012.</span><span class="sxs-lookup"><span data-stu-id="54eeb-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="54eeb-132">Pārliecinieties, ka laukā Daudzums vērtība ir iestatīta uz 1.</span><span class="sxs-lookup"><span data-stu-id="54eeb-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="54eeb-133">Parādītās papildinformācijas par cenu noteikšanu precei T0012 dati nāk no viena vai vairākiem tirdzniecības līgumiem: vienības cena ir 1000 CAD un atlaides procents ir 5.</span><span class="sxs-lookup"><span data-stu-id="54eeb-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="54eeb-134">Daudzuma laukā iestatiet vērtību 20.</span><span class="sxs-lookup"><span data-stu-id="54eeb-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="54eeb-135">Palielināts pasūtījuma daudzums nodrošinās, ka rindas atlaide, kas tiks piedāvāta debitoram, manīsies no 5 uz 7 procentiem.</span><span class="sxs-lookup"><span data-stu-id="54eeb-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="54eeb-136">Neto summa tiek aprēķināta, pamatojoties uz vienības cenu, atlaidi un kopējo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="54eeb-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="54eeb-137">Noklikšķiniet uz Skatīt rindas atlaidi.</span><span class="sxs-lookup"><span data-stu-id="54eeb-137">Click View line discount.</span></span>
    * <span data-ttu-id="54eeb-138">Precei T0012 ir divi rindas atlaides līgumi, kuros 5 procentu atlaide norādīta pasūtījuma rindas daudzumam no 1 līdz 10 un 7 procentu atlaide pasūtījuma daudzumam virs 10.</span><span class="sxs-lookup"><span data-stu-id="54eeb-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="54eeb-139">Ievērojiet, ka atlaides tiek lietots preču grupai, šajā piemērā, Grupas kodam 01, kura daļa ir prece T0012.</span><span class="sxs-lookup"><span data-stu-id="54eeb-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="54eeb-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="54eeb-140">Close the page.</span></span>


