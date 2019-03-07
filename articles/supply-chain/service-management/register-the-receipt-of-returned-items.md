---
title: Atgrieztu krājumu saņemšanas reģistrēšana
description: Atgrieztu krājumu saņemšanu varat reģistrēt, izmantojot veidlapu Saņemšanas apskats vai veidlapu Reģistrācija.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2be628d312e623e8ea6d92eb5edce12334190d9e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "328083"
---
# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="ba286-103">Atgrieztu krājumu saņemšanas reģistrēšana</span><span class="sxs-lookup"><span data-stu-id="ba286-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ba286-104">Pastāv divas metodes atgriezto krājumu saņemšanas reģistrācijai.</span><span class="sxs-lookup"><span data-stu-id="ba286-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="ba286-105">Pirmā metode ir noliktavas saņemšanas process, kas izmanto veidlapu **Saņemšanas apskats**.</span><span class="sxs-lookup"><span data-stu-id="ba286-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="ba286-106">Otrā metode paredz veidlapas **Reģistrācija** izmantošanu.</span><span class="sxs-lookup"><span data-stu-id="ba286-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="ba286-107">Atgriezto krājumu saņemšanas reģistrēšana formā Saņemšanas transakciju apskats</span><span class="sxs-lookup"><span data-stu-id="ba286-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="ba286-108">Varat izmantot veidlapu **Saņemšanas apskats**, lai atgriešanas sūtījumu identificētu pēc tā atgrieztā krājuma autorizācijas (AKA) koda.</span><span class="sxs-lookup"><span data-stu-id="ba286-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="ba286-109">Ja ir definēts žurnāla nosaukums cilnē **Iestatījumi** un ir žurnāla rindas, kas atbilst veidlapā **Saņemšanas apskats** atlasītajām rindām, tiek izveidots jauns žurnāla virsraksts, kad noklikšķināt uz **Sākt saņemšanu**.</span><span class="sxs-lookup"><span data-stu-id="ba286-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="ba286-110">Noklikšķiniet uz **Krājumu pārvaldība** \> **Periodiskās darbības** \> **Saņemšanas pārskats**.</span><span class="sxs-lookup"><span data-stu-id="ba286-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="ba286-111">Laukā **Iestatījumu nosaukums** atlasiet **Atgriešanas pasūtījums** un pēc tam noklikšķiniet uz **Atjaunināt**.</span><span class="sxs-lookup"><span data-stu-id="ba286-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="ba286-112">Varat izmantot laukus <STRONG>Diapazons</STRONG>, lai sašaurinātu meklēšanas rezultātus.</span><span class="sxs-lookup"><span data-stu-id="ba286-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="ba286-113">Varat ierakstīt izvēlētos AKA kodu laukā <STRONG>AKA kods</STRONG>, lai iegūtu precīzu rezultātu.</span><span class="sxs-lookup"><span data-stu-id="ba286-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="ba286-114">Lai noteiktu un saglabātu filtru kopu, kas ierobežo to, kuras ienākošās saņemšanas tiek parādītas, noklikšķiniet uz cilnes <STRONG>Iestatījumi</STRONG>. Pieejamo filtru klāstā ietilpst tipi, noliktavas un doki.</span><span class="sxs-lookup"><span data-stu-id="ba286-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="ba286-115">Atgrieztos pasūtījumus nedrīkst jaukt ar citiem saņemšanas tipiem veidlapā <STRONG>Saņemšanas apskats</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ba286-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="ba286-116">Tāpēc atsauce vienmēr būs pārdošanas pasūtījums, bet iztrūkstošs pārdošanas pasūtījuma ID tiks norādīts žurnāla virsrakstā.</span><span class="sxs-lookup"><span data-stu-id="ba286-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="ba286-117">Režģī **Ieejas plūsmas** atrodiet rindu, kas atbilst atgrieztajam krājumam, un pēc tam atzīmējiet izvēles rūtiņu kolonnā **Atlasīt saņemšanai**.</span><span class="sxs-lookup"><span data-stu-id="ba286-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="ba286-118">Lai izņemtu noteiktas rindas no atgriezto preču saņemšanas pavadzīmes, piemēram, krājumus no oriģinālā pasūtījuma, kas nebija iekļauti atgrieztajā sūtījumā, noņemiet atzīmes no saistītām izvēles rūtiņām **Atlasīt saņemšanai** tabulā **Rindas** veidlapas apakšdaļā.</span><span class="sxs-lookup"><span data-stu-id="ba286-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="ba286-119">Noklikšķiniet uz pogas **Sākt saņemšanu**, lai izveidotu saņemšanas žurnālu.</span><span class="sxs-lookup"><span data-stu-id="ba286-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="ba286-120">Varat izvēlēties vairākus atgriešanas pasūtījumus un iekļaut tos vienā saņemšanas procesā.</span><span class="sxs-lookup"><span data-stu-id="ba286-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="ba286-121">Katra atgriešanas pasūtījuma rinda tiks pārkopēta uz atbilstošu vienības pienākšanas žurnāla rindā.</span><span class="sxs-lookup"><span data-stu-id="ba286-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="ba286-122">Saņemšanas žurnālu varat veidot arī manuāli, izmantojot veidlapu <STRONG>Krājumu saņemšana</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ba286-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="ba286-123">Noklikšķiniet uz **Krājumu vadība** \> **Žurnāli** \> **Krājumu saņemšana** \> **Krājumu saņemšana**.</span><span class="sxs-lookup"><span data-stu-id="ba286-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="ba286-124">Atlasiet tikko izveidoto saņemšanas žurnālu un pēc tam noklikšķiniet uz **Rindas**, lai atvērtu veidlapu **Žurnāla rindas, vietas**.</span><span class="sxs-lookup"><span data-stu-id="ba286-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="ba286-125">Cilnē **Vispārīgi** pielāgojiet skaitli laukā **Daudzums**, ja nepieciešams, un pēc tam piešķiriet atgriešanas metodes kodu laukā **Atgriešanas metodes kods**.</span><span class="sxs-lookup"><span data-stu-id="ba286-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="ba286-126">Varat arī atzīmēt izvēles rūtiņu **Karantīnas pārraudzība**, lai atgrieztie krājumi tiktu nosūtīti caur pārbaudes procesu karantīnas pasūtījuma kontekstā.</span><span class="sxs-lookup"><span data-stu-id="ba286-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="ba286-127">Ja atgrieztos krājumus sūtāt caur karantīnu, atgriešanas metodes kodu nevar norādīt.</span><span class="sxs-lookup"><span data-stu-id="ba286-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="ba286-128">Noklikšķiniet uz pogas **Validēt**.</span><span class="sxs-lookup"><span data-stu-id="ba286-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="ba286-129">Ja apstiprināšanas procesā nav kļūdu, noklikšķiniet uz **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="ba286-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="ba286-130">Atgriezto krājumu saņemšanas reģistrēšana formā Reģistrācija</span><span class="sxs-lookup"><span data-stu-id="ba286-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="ba286-131">Kā alternatīvu veidlapas **Saņemšanas apskats** izmantošanai varat izmantot veidlapu **Reģistrācija**, lai reģistrētu atgriezto krājumu saņemšanu.</span><span class="sxs-lookup"><span data-stu-id="ba286-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="ba286-132">Noklikšķiniet uz **Pārdošana un mārketings** \> **Vispārīgi** \> **Atdošanas pasūtījumi** \> **Visi atdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="ba286-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="ba286-133">Izveidojiet jaunu atgriešanas pasūtījumu vai atveriet atgriešanas pasūtījumu no saraksta.</span><span class="sxs-lookup"><span data-stu-id="ba286-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="ba286-134">Kopsavilkuma cilnē **Rindas** atlasiet atgriešanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="ba286-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="ba286-135">Noklikšķiniet uz **Atjaunināt rindu** un pēc tam noklikšķiniet uz **Reģistrācija**.</span><span class="sxs-lookup"><span data-stu-id="ba286-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="ba286-136">Piešķiriet atgriešanas metodes kodu laukā **Atgriešanas metodes kods** un tad noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ba286-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="ba286-137">Izmantojot veidlapu <STRONG>Reģistrācija</STRONG>, krājumu nav iespējams nosūtīt pārbaudei kā karantīnas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="ba286-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="ba286-138">Režģī **Darbības** atlasiet reģistrējamo darījumu.</span><span class="sxs-lookup"><span data-stu-id="ba286-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="ba286-139">Režģī **Reģistrēt tagad** noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="ba286-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="ba286-140">Atkārtojiet iepriekšējās divas darbības, līdz visi atgrieztie krājumi ir redzami režģī **Reģistrēt tagad**.</span><span class="sxs-lookup"><span data-stu-id="ba286-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="ba286-141">Noklikšķiniet uz **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="ba286-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba286-142">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="ba286-142">See also</span></span>

<span data-ttu-id="ba286-143">[Ieņēmumu apskats (forma)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="ba286-143">[Arrival overview (form)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span></span>

  


