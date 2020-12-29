---
title: Krājumu aizstāšanas pasūtījuma izveidošana
description: Vienības maiņas pasūtījumi parasti tiek izveidoti pēc produkta atgriešanas pārbaudei.
author: josaw1
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e63c175d12cac91648cb57a3f41d1769e81d57af
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432970"
---
# <a name="create-an-item-replacement-order"></a><span data-ttu-id="89009-103">Krājumu aizstāšanas pasūtījuma izveidošana</span><span class="sxs-lookup"><span data-stu-id="89009-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="89009-104">Vienības maiņas pasūtījumi parasti tiek izveidoti pēc produkta atgriešanas pārbaudei.</span><span class="sxs-lookup"><span data-stu-id="89009-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="89009-105">Tomēr, ja vienības tiek apmainīta pirms atgriešanas, vai, ja oriģinālā vienība netiek atgriezta, varat izveidot vienības maiņas pasūtījumu tūlīt pēc atgriešanas pasūtījuma izveidošanas.</span><span class="sxs-lookup"><span data-stu-id="89009-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="89009-106">Aizstāšanas pasūtījuma izveidošana pēc atgriezta krājuma saņemšanas</span><span class="sxs-lookup"><span data-stu-id="89009-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="89009-107">Noklikšķiniet uz **Pārdošana un mārketings** \> **Vispārīgi** \> **Atdošanas pasūtījumi** \> **Visi atdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="89009-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="89009-108">Izveidojiet jaunu atgriešanas pasūtījumu vai atlasiet atgrieztu pasūtījumu sarakstā, lai atvērtu formu **Atgriešanas pasūtījums — AKA kods: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="89009-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="89009-109">Noklikšķiniet uz **Atgriešanas rinda** un pēc tam atlasiet **Krājuma aizstājējs**.</span><span class="sxs-lookup"><span data-stu-id="89009-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="89009-110">Atlasiet krājumu, ar kuru aizstāt atgriezto krājumu.</span><span class="sxs-lookup"><span data-stu-id="89009-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="89009-111">Ievadiet krājuma specifikācijas un pēc tam noklikšķiniet uz **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="89009-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="89009-112">Noklikšķiniet uz **Pavadzīme**, lai ģenerētu atgriešanas pasūtījuma pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="89009-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="89009-113">Atlasītajam aizvietošanas krājumam tiek ģenerēts pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="89009-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="89009-114">Pēc tam, kad krājuma aizstājējam ir izveidots pārdošanas pasūtījums, automātiski tiek meklēti pārdošanas līgumi, un, ja tiek atrasts piemērojams pārdošanas līgums, tas tiek izmantots pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="89009-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="89009-115">Aizstāšanas pasūtījuma izveidošana pirms atgriešanai paredzēta krājuma atgriešanas</span><span class="sxs-lookup"><span data-stu-id="89009-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="89009-116">Noklikšķiniet uz **Pārdošana un mārketings** \> **Vispārīgi** \> **Atdošanas pasūtījumi** \> **Visi atdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="89009-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="89009-117">Izveidojiet jaunu atgriešanas pasūtījumu vai atlasiet atgriešanas pasūtījumu sarakstā, lai atvērtu formu **Atgriešanas pasūtījums — AKA kods: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="89009-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="89009-118">Noklikšķiniet uz **Atrast pārdošanas pasūtījumu**, ja vēlaties identificēt atgrieztā krājuma pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="89009-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="89009-119">Aizpildiet formu **Atrast pārdošanas pasūtījumu** un pēc tam noklikšķiniet uz **Labi**, lai aizvērtu formu un atgrieztos formā **Atgriešanas pasūtījums — AKA kods: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="89009-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="89009-120">Atgriezto krājumu pārdošanas pasūtījuma rinda tiek kopēta atgriešanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="89009-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="89009-121">Lai atvērtu veidlapu **Pārdošanas pasūtījuma izveide**, noklikšķiniet uz **Aizstāšanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="89009-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="89009-122">Atzīmējiet izvēles rūtiņu **Kopēt atgriešanas pasūtījuma rindas**, lai uz šo pārdošanas pasūtījumu pasūtītu detalizētu informāciju no atgriešanas pasūtījuma, ko atlasījāt formā **Atgriešanas pasūtījums — AKA kods: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="89009-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="89009-123">Ja nepieciešams, ievadiet vai mainiet detaļas.</span><span class="sxs-lookup"><span data-stu-id="89009-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="89009-124">Ja 3. darbībā identificējāt pārdošanas pasūtījumu un ja pārdošanas pasūtījuma rinda atgrieztajam krājumam ir saistīta ar pārdošanas līgumu, piemērojamā pārdošanas līguma identifikators krājuma aizstāšanas pasūtījumam tiks automātiski rādīts laukā **Pārdošanas līguma ID**.</span><span class="sxs-lookup"><span data-stu-id="89009-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="89009-125">Noklikšķiniet uz **Labi**, lai aizvērtu veidlapu **Pārdošanas pasūtījuma izveide** un atvērtu veidlapu **Pārdošanas pasūtījums**, kur varat turpināt ievadīt informāciju par jauno pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="89009-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="89009-126">Visas piemērojamās atgriešanas pasūtījuma rindas tiks kopētas uz jauno pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="89009-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="89009-127">Ja pārdošanas līguma identifikators tiek automātiski rādīts laukā **Pārdošanas līguma ID**, pārdošanas līgums ir saistīts ar pārdošanas pasūtījuma virsrakstu krājumu aizstāšanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="89009-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="89009-128">Ja ir piemērojama saistība pārdošanas līgumā, kas vēl nav izpildīts, un pārdošanas pasūtījums tiek izveidots pirms pārdošanas līguma termiņa beigām, tiek izveidota saite starp pārdošanas līguma rindu un pārdošanas pasūtījuma rindu.</span><span class="sxs-lookup"><span data-stu-id="89009-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="89009-129">Tādēļ informācija no pārdošanas līguma, piemēram, preces cena, tiek kopēta jaunajā pārdošanas pasūtījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="89009-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  


