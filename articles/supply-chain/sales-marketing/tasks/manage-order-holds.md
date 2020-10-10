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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: edb3c6941af132f9ea1bf9f52f94cd6acc008d6c
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830060"
---
# <a name="manage-order-holds"></a><span data-ttu-id="51516-103">Pasūtījumu aizturēšanas pārvaldība</span><span class="sxs-lookup"><span data-stu-id="51516-103">Manage order holds</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51516-104">Šajā procedūrā ir parādīts, kā aizturēt debitora pārdošanas pasūtījumus, kā strādāt ar pasūtījuma aizturēšanas izsniegšanām un kā noņemt pasūtījuma aizturēšanu.</span><span class="sxs-lookup"><span data-stu-id="51516-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="51516-105">Pasūtījums var tikt aizturēts dažādu iemeslu dēļ.</span><span class="sxs-lookup"><span data-stu-id="51516-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="51516-106">Piemēram, pasūtījumu var aizturēt līdz debitora adresi vai maksājuma metodi būs iespējams pārbaudīt vai līdz vadītājs varēs pārskatīt debitora kredīta limitu.</span><span class="sxs-lookup"><span data-stu-id="51516-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer's credit limit.</span></span> <span data-ttu-id="51516-107">Kamēr pasūtījums ir aizturēts, noliktava to nevar apstrādāt nosūtīšanai.</span><span class="sxs-lookup"><span data-stu-id="51516-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="51516-108">Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="51516-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="51516-109">Iestatīt pasūtījumu aizturēšanas</span><span class="sxs-lookup"><span data-stu-id="51516-109">Set up order holds</span></span>
1. <span data-ttu-id="51516-110">Dodieties uz **NNavigācijas rūts > Moduļi > Pārdošana un mārketings > Iestatīšana > Pārdošanas pasūtījumi > Pasūtījumu aizturēšanas kodi**.</span><span class="sxs-lookup"><span data-stu-id="51516-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="51516-111">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="51516-111">Click **New**.</span></span>
3. <span data-ttu-id="51516-112">Ierakstiet kādu vērtību laukā **Aizturēšanas kods**.</span><span class="sxs-lookup"><span data-stu-id="51516-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="51516-113">Piemēram, ierakstiet 'Atzvanīt'.</span><span class="sxs-lookup"><span data-stu-id="51516-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="51516-114">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="51516-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="51516-115">Piemēram, pasūtījums ir aizturēts, gaidot debitora atzvanīšanu.</span><span class="sxs-lookup"><span data-stu-id="51516-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="51516-116">Ja vēlaties, atzīmējiet izvēles rūtiņu **Noņemt rezervācijas**, lai pasūtījumam noņemtu visas fiziskās rezervācijas, kad tiek pievienots šis aizturēšanas kods.</span><span class="sxs-lookup"><span data-stu-id="51516-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="51516-117">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="51516-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="51516-118">Aizturēt pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="51516-118">Place order on hold</span></span>
1. <span data-ttu-id="51516-119">Dodieties uz **Navigācijas rūts > Moduļi > Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="51516-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="51516-120">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="51516-120">Click **New**.</span></span>
3. <span data-ttu-id="51516-121">Ievadiet vai atlasiet vērtību laukā **Klienta konts**.</span><span class="sxs-lookup"><span data-stu-id="51516-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="51516-122">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="51516-122">Click **OK**.</span></span>
5. <span data-ttu-id="51516-123">Laukā **Krājuma kods** ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="51516-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="51516-124">Laukā **Daudzums** ierakstiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="51516-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="51516-125">**Darbību rūtī** noklikšķiniet uz **Pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="51516-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="51516-126">Noklikšķiniet uz **Pasūtījumu aizturēšanas**.</span><span class="sxs-lookup"><span data-stu-id="51516-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="51516-127">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="51516-127">Click **New**.</span></span>
10. <span data-ttu-id="51516-128">Laukā **Aizturēšanas kods** atlasiet kodu, kuru izveidojāt iepriekšējā apakšuzdevumā.</span><span class="sxs-lookup"><span data-stu-id="51516-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="51516-129">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="51516-129">Click **Save**.</span></span>
12. <span data-ttu-id="51516-130">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="51516-130">Close the page.</span></span>
13. <span data-ttu-id="51516-131">Pārejiet uz sadaļu **Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="51516-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="51516-132">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="51516-132">In the list, mark the selected row.</span></span> <span data-ttu-id="51516-133">Pasūtījumiem, kas pašlaik ir aizturēti, ir atzīmēti lauki “Neapstrādāt” un “Aizturēts”.</span><span class="sxs-lookup"><span data-stu-id="51516-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="51516-134">Darbību rūtī noklikšķiniet uz **Izdot un iepakot**.</span><span class="sxs-lookup"><span data-stu-id="51516-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="51516-135">Pasūtījumu aizturēšanas pārvaldība</span><span class="sxs-lookup"><span data-stu-id="51516-135">Manage order holds</span></span>
1. <span data-ttu-id="51516-136">Dodieties uz **Pārdošana un mārketings > Pārdošanas pasūtījumi > Atvērtie pasūtījumi > Pasūtījumu aizturēšanas**.</span><span class="sxs-lookup"><span data-stu-id="51516-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="51516-137">Lapa **Pasūtījumu aizturēšanas** darbojas kā rīks, kurā varat gūt pārskatu par visām pašreizējām un apstrādātajām aizturēšanām, kā arī apstrādāt tās un saistītos pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="51516-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="51516-138">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="51516-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="51516-139">**Darbību rūtī** noklikšķiniet uz **Aizturēt izsniegšanu**.</span><span class="sxs-lookup"><span data-stu-id="51516-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="51516-140">Noklikšķiniet uz **Izsniegt**.</span><span class="sxs-lookup"><span data-stu-id="51516-140">Click **Check out**.</span></span>
5. <span data-ttu-id="51516-141">Sarakstā noņemiet atzīmi no atlasītās rindas.</span><span class="sxs-lookup"><span data-stu-id="51516-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="51516-142">Laukā **Izsniegt lietotājam** tagad ir redzams jūsu lietotāja ID.</span><span class="sxs-lookup"><span data-stu-id="51516-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="51516-143">Noklikšķiniet uz **Dzēst izsniegšanu**.</span><span class="sxs-lookup"><span data-stu-id="51516-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="51516-144">**Darbību rūtī** noklikšķiniet uz **Dzēst aizturēšanu**.</span><span class="sxs-lookup"><span data-stu-id="51516-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="51516-145">Kad esat gatavs noņemt aizturēšanu un ļaut, lai pasūtījums pāriet uz nākamo izpildes darbību, aizturēšana ir jānotīra.</span><span class="sxs-lookup"><span data-stu-id="51516-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="51516-146">Ja pasūtījumam nav jāveic nekādas izmaiņas, varat palaist darbību Notīrīt aizturēšanas.</span><span class="sxs-lookup"><span data-stu-id="51516-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="51516-147">Taču varat arī izmantot darbību Dzēst un mainīt, ja aizturēšanas dzēšanas laikā pasūtījums ir jāatjaunina.</span><span class="sxs-lookup"><span data-stu-id="51516-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="51516-148">Darbība **Notīrīt un iesniegt** ir spēkā tikai tad, ja izmantojat zvanu centra funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="51516-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="51516-149">Noklikšķiniet uz **Dzēst aizturēšanas**.</span><span class="sxs-lookup"><span data-stu-id="51516-149">Click **Clear holds**.</span></span> <span data-ttu-id="51516-150">Tagad aizturēšana ir dzēsta no pasūtījuma un noņemta no saraksta Aktīvās aizturēšanas.</span><span class="sxs-lookup"><span data-stu-id="51516-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="51516-151">Lai skatītu visas aizturēšanas vai to apakškopu pēc noteikta statusa, mainiet vērtību laukā Rādīt.</span><span class="sxs-lookup"><span data-stu-id="51516-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

