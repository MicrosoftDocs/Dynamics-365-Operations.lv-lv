---
title: Atgriezto krājumu pārbaudes veikšana
description: Veiciet atgriezto krājumu pārbaudi.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53cb727cc0f001a6ac344d37f25273999f992d8a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974089"
---
# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="299e2-103">Atgriezto krājumu pārbaudes veikšana</span><span class="sxs-lookup"><span data-stu-id="299e2-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="299e2-104">Noklikšķiniet uz **Krājumu pārvaldība** \> **Periodiskās darbības** \> **Kvalitātes pārvaldība** \> **Karantīnas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="299e2-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="299e2-105">Izvietojiet pasūtījuma rindu, kas atbilsts atgrieztajam krājumam, kurš tiek pārbaudīts.</span><span class="sxs-lookup"><span data-stu-id="299e2-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="299e2-106">Karantīnas pasūtījumu var saistīt tikai ar vienu krājuma numuru.</span><span class="sxs-lookup"><span data-stu-id="299e2-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="299e2-107">Ja 10 krājumi ar dažādiem krājumu numuriem tiek atgriezti vienā sūtījumā un nosūtīti uz karantīnu, tiek izveidoti 10 atsevišķi karantīnas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="299e2-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="299e2-108">Pēc krājuma pārbaudīšanas ir jāveic atzīme laukā **Atgriešanas metodes kods**, lai norādītu, kas ir jādara ar šo vienību un kā ir jāapstrādā saistītā finanšu transakcija.</span><span class="sxs-lookup"><span data-stu-id="299e2-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="299e2-109">Piemēri iekļauj vienības atgriešanu noliktavā un naudas atgriešanu klientam, vienības brāķēšanu un jaunas nosūtīšanu klientam vai arī vienības atgriešanu klientam bez jebkāda kredīta.</span><span class="sxs-lookup"><span data-stu-id="299e2-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="299e2-110">Ja vairākām atgrieztajām vienībām vienas vienības numura paketē nevar piešķirt to pašu atgriešanas metodes kodu, karantīnas pasūtījums ir jāsadala (<STRONG>Funkcijas</STRONG> &gt; <STRONG>Sadalīt</STRONG>), lai katrai apakšpaketei piešķirtu citu atgriešanas metodes kodu.</span><span class="sxs-lookup"><span data-stu-id="299e2-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="299e2-111">Kad pārbaude ir pabeigta, noklikšķiniet uz **Ziņot kā pabeigtu**, lai izlaistu atgrieztās vienības un izveidotu vienību saņemšanas žurnāla ierakstu.</span><span class="sxs-lookup"><span data-stu-id="299e2-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="299e2-112">Darbinieks vai nodaļa, kas saņēmusi krājumus, tad veic žurnāla apstrādi, lai atgrieztu krājumus inventārā.</span><span class="sxs-lookup"><span data-stu-id="299e2-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="299e2-113">–vai–</span><span class="sxs-lookup"><span data-stu-id="299e2-113">–or–</span></span>
    
    <span data-ttu-id="299e2-114">Pabeidziet karantīnas pasūtījumu un pārvietojiet vienības atpakaļ uz krājumiem tiešā veidā, izmantojot vienu no funkcijām **Krājumi**.</span><span class="sxs-lookup"><span data-stu-id="299e2-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="299e2-115">Aizveriet formu, lai saglabātu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="299e2-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="299e2-116">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="299e2-116">See also</span></span>

[<span data-ttu-id="299e2-117">Noteikšana, kā atbrīvoties no atgrieztiem krājumiem</span><span class="sxs-lookup"><span data-stu-id="299e2-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  


