---
title: Mainīt piegādes veidu punktā POS
description: Šajā tēmā ir aprakstīts, kā konfigurēt un izmantot piegādes veida izmaiņu režīmu punktā POS.
author: hhainesms
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: a88ca9cc8fc8cde6d738dbc4fcf474f1e27e05dd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796394"
---
# <a name="change-mode-of-delivery-in-pos"></a><span data-ttu-id="2f68d-103">Mainīt piegādes veidu punktā POS</span><span class="sxs-lookup"><span data-stu-id="2f68d-103">Change mode of delivery in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2f68d-104">Šajā tēmā ir aprakstīts, kā iestatīt un izmantot funkciju "piegādes režīma maiņa" jūsu pārdošanas punktā (POS) vidē.</span><span class="sxs-lookup"><span data-stu-id="2f68d-104">This topic describes how to set up and use the "change mode of delivery" functionality in your point of sale (POS) environment.</span></span> 

<span data-ttu-id="2f68d-105">Dynamics 365 Commerce versijās 10.0.10 un jaunākās versijās **Mainīt piegādes veidu** operācijas (647) ir pieejamas pievienošanai jūsu POS ekrāna izkārtojumiem.</span><span class="sxs-lookup"><span data-stu-id="2f68d-105">In Dynamics 365 Commerce versions 10.0.10 and later, the **Change mode of delivery** operation (647) is available to add to your POS screen layouts.</span></span>

<span data-ttu-id="2f68d-106">Piegādes līdzekļa maiņas veids sniedz iespēju mainīt piegādes veidu vienai vai vairākām pārdošanas rindām, kas konfigurētas POS darbībā.</span><span class="sxs-lookup"><span data-stu-id="2f68d-106">The change mode of delivery feature provides you with the option to change the mode of delivery for one or more shipment-configured sales lines on the POS transaction.</span></span> <span data-ttu-id="2f68d-107">Iepriekšējās Commerce versijas jums bija jāiziet cauri pilnām **Nosūtīt visus** vai **Nosūtīt atlasītās** konfigurācijas plūsmām, ja vēlējāties mainīt piegādes veidu esošajā rindā, kas tika konfigurēta nosūtīšanai.</span><span class="sxs-lookup"><span data-stu-id="2f68d-107">In previous versions of Commerce, you had to go through the full **Ship all** or **Ship selected** configuration flows if you wanted to change the mode of delivery on an existing line that was configured for shipment.</span></span> <span data-ttu-id="2f68d-108">Šis process bija laikietilpīgs, un tas varēja izraisīt nejaušas izmaiņas šīs rindas piegādājamo preču izcelsmes vai saņemšanas datumā.</span><span class="sxs-lookup"><span data-stu-id="2f68d-108">This process was time consuming and could result in accidental changes to the delivery origin or delivery dates for the line.</span></span> <span data-ttu-id="2f68d-109">Jaunā funkcionalitāte sniedz alternatīvu metodi, kā efektīvi atjaunināt piegādes veidu šajās pārdošanas rindās.</span><span class="sxs-lookup"><span data-stu-id="2f68d-109">The new functionality provides an alternative method for efficiently updating the mode of delivery on these sales lines.</span></span>

<span data-ttu-id="2f68d-110">Lai iegūtu vairāk informācijas par to, kā pievienot operāciju pogai, kas atrodas POS pogu režģī, skatiet [Pārdošanas punkta ekrāna izkārtojumus](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span><span class="sxs-lookup"><span data-stu-id="2f68d-110">For more information about how to add an operation to a button on your POS button grid, see [Screen layouts for the point of sale](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span></span>

<span data-ttu-id="2f68d-111">Pēc tam, kad šī funkcija ir konfigurēta POS, kad atlasāt **Mainīt piegādes veidu**, jums tiks parādīta saraksta lapa, kas ļaus izvēlēties darbības rindas, kurām vēlaties mainīt piegādes veidu.</span><span class="sxs-lookup"><span data-stu-id="2f68d-111">After this feature is configured in POS, when you select **Change mode of delivery**, you will be presented with a list page that allows you to choose the lines of the transaction that you want to change the mode of delivery for.</span></span> <span data-ttu-id="2f68d-112">Varat izvēlēties dažas vai visas rindas vai iziet, neveicot nekādas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="2f68d-112">You can choose some or all of the lines, or exit without making any changes.</span></span> <span data-ttu-id="2f68d-113">Pārdošanas rindas, kas iepriekš konfigurētas sūtījumam, ir vienīgās rindas sarakstā, ko varat mainīt.</span><span class="sxs-lookup"><span data-stu-id="2f68d-113">The sales lines that were previously configured for shipment are the only lines in the list that you can change.</span></span> <span data-ttu-id="2f68d-114">Ja vēlaties mainīt rindu, kas paredzēta izsniegšanai vai uzkrājuma sūtīšanai, ir jāizmanto **Nosūtīt visas** vai **Nosūtīt atlasītās** darbības.</span><span class="sxs-lookup"><span data-stu-id="2f68d-114">If you want to change a line designated for pickup or carryout to ship, you must use the **Ship all** or **Ship selected** operations.</span></span> <span data-ttu-id="2f68d-115">Pretējā gadījumā, ja vēlaties mainīt rindu, kas norādīta kā sūtījums uz saņemšanu vai realizēšanu, ir jāizmanto visas darbības **Saņemt visas**, **Saņemt atlasītās**, **Realizēt visas** vai **Realizēt atlasītās**.</span><span class="sxs-lookup"><span data-stu-id="2f68d-115">Conversely, if you want to change a line designated as a shipment to a pickup or carryout, you must use the  **Pickup all**, **Pickup selected**, **Carryout all**, or **Carryout selected** operations.</span></span>

<span data-ttu-id="2f68d-116">Pēc tam, kad atlasāt rindas, kuras vēlaties mainīt, noklikšķiniet uz **Mainīt piegādes veidu**, lai tiktu piedāvāts izvēlēties piegādes veida opcijas.</span><span class="sxs-lookup"><span data-stu-id="2f68d-116">After you select the lines that you want to change, click **Change mode of delivery** to be prompted to select the delivery mode options.</span></span> <span data-ttu-id="2f68d-117">Ja atlasījāt vairākas rindas, ko mainīt, punktā POS tiek rādīti tikai piegādes veidi, kas ir konfigurēti kā atļaujami visām atlasītajām precēm.</span><span class="sxs-lookup"><span data-stu-id="2f68d-117">If you selected multiple lines to change, POS will only display modes of delivery that have been configured as allowable for all of the selected products.</span></span> <span data-ttu-id="2f68d-118">Piegādes veidus var konfigurēt, lai atbalstītu noteiktas preces un piegādes adreses.</span><span class="sxs-lookup"><span data-stu-id="2f68d-118">Modes of delivery can be configured to support specific products and delivery addresses.</span></span> <span data-ttu-id="2f68d-119">Ja ir piegādes veids, kas ir pieņemams vienai precei un adreses kombinācijai, bet nav pieņemams citai izvēlētai preces un adreses kombinācijai, piegādes veids nav pieejams.</span><span class="sxs-lookup"><span data-stu-id="2f68d-119">If there is a mode of delivery that is acceptable for one product and address combination but is not acceptable for another selected product and address combination, the mode of delivery is not available.</span></span> <span data-ttu-id="2f68d-120">Pastāv iespēja, ka rindas jāizvēlas pa vienai, un katrai rindai jāmaina piegādes veids, ja vēlaties atlasīt piegādes veidu vienai precei, ko neatbalsta cita prece.</span><span class="sxs-lookup"><span data-stu-id="2f68d-120">You may need to select lines one by one and change the mode of delivery for each line separately if you want to select a mode of delivery for one product that is not supported by another product.</span></span>  

<span data-ttu-id="2f68d-121">Pēc jauna piegādes veida atlases tiek parādīta transakciju lapa.</span><span class="sxs-lookup"><span data-stu-id="2f68d-121">After you select the new mode of delivery, the transaction page is displayed.</span></span> <span data-ttu-id="2f68d-122">Lai pārskatītu jaunās piegādes veida atlases, atlasiet cilni **Piegāde** transakciju sarakstā.</span><span class="sxs-lookup"><span data-stu-id="2f68d-122">To review your new delivery mode selections, select the **Delivery** tab on the transaction list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f68d-123">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2f68d-123">Additional resources</span></span>

[<span data-ttu-id="2f68d-124">Zvanu centra pasūtījumu izveide</span><span class="sxs-lookup"><span data-stu-id="2f68d-124">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="2f68d-125">Darījumu e-pasta ziņojumu pielāgošana pēc piegādes veida</span><span class="sxs-lookup"><span data-stu-id="2f68d-125">Customize transactional emails by mode of delivery</span></span>](customize-email-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]