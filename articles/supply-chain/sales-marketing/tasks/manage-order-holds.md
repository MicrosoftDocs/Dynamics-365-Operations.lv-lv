---
title: Pasūtījumu aizturēšanas pārvaldība
description: Šajā procedūrā ir parādīts, kā aizturēt debitora pārdošanas pasūtījumus, kā strādāt ar pasūtījuma aizturēšanas izsniegšanām un kā noņemt pasūtījuma aizturēšanu.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27a5149812a8e478dae1d2385e6c139c9f635202
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010751"
---
# <a name="manage-order-holds"></a><span data-ttu-id="ad521-103">Pasūtījumu aizturēšanas pārvaldība</span><span class="sxs-lookup"><span data-stu-id="ad521-103">Manage order holds</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad521-104">Šajā procedūrā ir parādīts, kā aizturēt debitora pārdošanas pasūtījumus, kā strādāt ar pasūtījuma aizturēšanas izsniegšanām un kā noņemt pasūtījuma aizturēšanu.</span><span class="sxs-lookup"><span data-stu-id="ad521-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="ad521-105">Pasūtījums var tikt aizturēts dažādu iemeslu dēļ.</span><span class="sxs-lookup"><span data-stu-id="ad521-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="ad521-106">Piemēram, pasūtījumu var aizturēt līdz debitora adresi vai maksājuma metodi būs iespējams pārbaudīt vai līdz vadītājs varēs pārskatīt debitora kredīta limitu.</span><span class="sxs-lookup"><span data-stu-id="ad521-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer's credit limit.</span></span> <span data-ttu-id="ad521-107">Kamēr pasūtījums ir aizturēts, noliktava to nevar apstrādāt nosūtīšanai.</span><span class="sxs-lookup"><span data-stu-id="ad521-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="ad521-108">Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="ad521-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="ad521-109">Iestatīt pasūtījumu aizturēšanas</span><span class="sxs-lookup"><span data-stu-id="ad521-109">Set up order holds</span></span>
1. <span data-ttu-id="ad521-110">Dodieties uz **NNavigācijas rūts > Moduļi > Pārdošana un mārketings > Iestatīšana > Pārdošanas pasūtījumi > Pasūtījumu aizturēšanas kodi**.</span><span class="sxs-lookup"><span data-stu-id="ad521-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="ad521-111">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ad521-111">Click **New**.</span></span>
3. <span data-ttu-id="ad521-112">Ierakstiet kādu vērtību laukā **Aizturēšanas kods**.</span><span class="sxs-lookup"><span data-stu-id="ad521-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="ad521-113">Piemēram, ierakstiet 'Atzvanīt'.</span><span class="sxs-lookup"><span data-stu-id="ad521-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="ad521-114">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ad521-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="ad521-115">Piemēram, pasūtījums ir aizturēts, gaidot debitora atzvanīšanu.</span><span class="sxs-lookup"><span data-stu-id="ad521-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="ad521-116">Ja vēlaties, atzīmējiet izvēles rūtiņu **Noņemt rezervācijas**, lai pasūtījumam noņemtu visas fiziskās rezervācijas, kad tiek pievienots šis aizturēšanas kods.</span><span class="sxs-lookup"><span data-stu-id="ad521-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="ad521-117">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ad521-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="ad521-118">Aizturēt pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="ad521-118">Place order on hold</span></span>
1. <span data-ttu-id="ad521-119">Dodieties uz **Navigācijas rūts > Moduļi > Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="ad521-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="ad521-120">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ad521-120">Click **New**.</span></span>
3. <span data-ttu-id="ad521-121">Ievadiet vai atlasiet vērtību laukā **Klienta konts**.</span><span class="sxs-lookup"><span data-stu-id="ad521-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="ad521-122">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ad521-122">Click **OK**.</span></span>
5. <span data-ttu-id="ad521-123">Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="ad521-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="ad521-124">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="ad521-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="ad521-125">**Darbību rūtī** noklikšķiniet uz **Pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="ad521-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="ad521-126">Noklikšķiniet uz **Pasūtījumu aizturēšanas**.</span><span class="sxs-lookup"><span data-stu-id="ad521-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="ad521-127">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ad521-127">Click **New**.</span></span>
10. <span data-ttu-id="ad521-128">Laukā **Aizturēšanas kods** atlasiet kodu, kuru izveidojāt iepriekšējā apakšuzdevumā.</span><span class="sxs-lookup"><span data-stu-id="ad521-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="ad521-129">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ad521-129">Click **Save**.</span></span>
12. <span data-ttu-id="ad521-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ad521-130">Close the page.</span></span>
13. <span data-ttu-id="ad521-131">Pārejiet uz sadaļu **Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="ad521-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="ad521-132">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ad521-132">In the list, mark the selected row.</span></span> <span data-ttu-id="ad521-133">Pasūtījumiem, kas pašlaik ir aizturēti, ir atzīmēti lauki “Neapstrādāt” un “Aizturēts”.</span><span class="sxs-lookup"><span data-stu-id="ad521-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="ad521-134">Darbību rūtī noklikšķiniet uz **Izdot un iepakot**.</span><span class="sxs-lookup"><span data-stu-id="ad521-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="ad521-135">Pasūtījumu aizturēšanas pārvaldība</span><span class="sxs-lookup"><span data-stu-id="ad521-135">Manage order holds</span></span>
1. <span data-ttu-id="ad521-136">Dodieties uz **Pārdošana un mārketings > Pārdošanas pasūtījumi > Atvērtie pasūtījumi > Pasūtījumu aizturēšanas**.</span><span class="sxs-lookup"><span data-stu-id="ad521-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="ad521-137">Lapa **Pasūtījumu aizturēšanas** darbojas kā rīks, kurā varat gūt pārskatu par visām pašreizējām un apstrādātajām aizturēšanām, kā arī apstrādāt tās un saistītos pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="ad521-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="ad521-138">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="ad521-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="ad521-139">**Darbību rūtī** noklikšķiniet uz **Aizturēt izsniegšanu**.</span><span class="sxs-lookup"><span data-stu-id="ad521-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="ad521-140">Noklikšķiniet uz **Izsniegt**.</span><span class="sxs-lookup"><span data-stu-id="ad521-140">Click **Check out**.</span></span>
5. <span data-ttu-id="ad521-141">Sarakstā noņemiet atzīmi no atlasītās rindas.</span><span class="sxs-lookup"><span data-stu-id="ad521-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="ad521-142">Laukā **Izsniegt lietotājam** tagad ir redzams jūsu lietotāja ID.</span><span class="sxs-lookup"><span data-stu-id="ad521-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="ad521-143">Noklikšķiniet uz **Dzēst izsniegšanu**.</span><span class="sxs-lookup"><span data-stu-id="ad521-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="ad521-144">**Darbību rūtī** noklikšķiniet uz **Dzēst aizturēšanu**.</span><span class="sxs-lookup"><span data-stu-id="ad521-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="ad521-145">Kad esat gatavs noņemt aizturēšanu un ļaut, lai pasūtījums pāriet uz nākamo izpildes darbību, aizturēšana ir jānotīra.</span><span class="sxs-lookup"><span data-stu-id="ad521-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="ad521-146">Ja pasūtījumam nav jāveic nekādas izmaiņas, varat palaist darbību Notīrīt aizturēšanas.</span><span class="sxs-lookup"><span data-stu-id="ad521-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="ad521-147">Taču varat arī izmantot darbību Dzēst un mainīt, ja aizturēšanas dzēšanas laikā pasūtījums ir jāatjaunina.</span><span class="sxs-lookup"><span data-stu-id="ad521-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="ad521-148">Darbība **Notīrīt un iesniegt** ir spēkā tikai tad, ja izmantojat zvanu centra funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="ad521-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="ad521-149">Noklikšķiniet uz **Dzēst aizturēšanas**.</span><span class="sxs-lookup"><span data-stu-id="ad521-149">Click **Clear holds**.</span></span> <span data-ttu-id="ad521-150">Tagad aizturēšana ir dzēsta no pasūtījuma un noņemta no saraksta Aktīvās aizturēšanas.</span><span class="sxs-lookup"><span data-stu-id="ad521-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="ad521-151">Lai skatītu visas aizturēšanas vai to apakškopu pēc noteikta statusa, mainiet vērtību laukā Rādīt.</span><span class="sxs-lookup"><span data-stu-id="ad521-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

