---
title: Sērijveida kontrolētu preču atgriešana POS
description: Šajā tēmā aprakstītas serializētu krājumu validēšanas iespējas kā daļa no atgriešanas procesa Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) programmā.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129819"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a><span data-ttu-id="507d2-103">Sērijveida kontrolētu preču atgriešana POS</span><span class="sxs-lookup"><span data-stu-id="507d2-103">Return serial number–controlled products in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="507d2-104">Šajā tēmā aprakstītas serializētu krājumu validēšanas iespējas kā daļa no atgriešanas procesa Microsoft Dynamics 365 Commerce pārdošanas punkta (POS) programmā.</span><span class="sxs-lookup"><span data-stu-id="507d2-104">This topic describes the capabilities for validating serialized items as part of the return process in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

> [!NOTE]
> <span data-ttu-id="507d2-105">Commerce 10.0.20 un jaunākās versijās ir pieejams jauns līdzeklis ar nosaukumu **Vienotā atpakaļ atdošanas apstrādes pieredze programmā POS**.</span><span class="sxs-lookup"><span data-stu-id="507d2-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="507d2-106">Lai izmantotu sērijas numura validāciju atgriezto pasūtījumu apstrādes laikā programmā POS, šis līdzeklis ir jāieslēdz.</span><span class="sxs-lookup"><span data-stu-id="507d2-106">To use serial number validation during return order processing in POS, you must turn on this feature.</span></span> <span data-ttu-id="507d2-107">Informāciju par citām iespējām, ko šis līdzeklis nodrošina, kad tas ir ieslēgts, skatiet sadaļā [Atgriešanas izveide programmā POS](POS-returns.md).</span><span class="sxs-lookup"><span data-stu-id="507d2-107">For information about others capabilities that this feature provides when it's turned on, see [Create returns in POS)](POS-returns.md).</span></span>
>
> <span data-ttu-id="507d2-108">Kad līdzeklis ir ieslēgts, to nevar izslēgt.</span><span class="sxs-lookup"><span data-stu-id="507d2-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="options-for-validating-serialized-returns"></a><span data-ttu-id="507d2-109">Serializēto atgriešanu validēšanas opcijas</span><span class="sxs-lookup"><span data-stu-id="507d2-109">Options for validating serialized returns</span></span>

<span data-ttu-id="507d2-110">Ja ir ieslēgts līdzeklis **Vienotā atgriešanas apstrādes pieredze programmā POS**, organizācijas var veikt atgriešanas validāciju sērijveida kontrolētiem krājumiem, izmantojot POS.</span><span class="sxs-lookup"><span data-stu-id="507d2-110">When the **Unified return processing experience in POS** feature is turned on, organizations can perform a validation on returns of serial number–controlled items through POS.</span></span> <span data-ttu-id="507d2-111">Šī iespēja var brīdināt lietotājus, ja atgrieztais sērijas numurs atšķiras no sākotnējā pārdotā sērijas numura.</span><span class="sxs-lookup"><span data-stu-id="507d2-111">This capability can warn users if the serial number that is being returned differs from the original serial number that was sold.</span></span> <span data-ttu-id="507d2-112">Commerce 10.0.20 un jaunākās versijās šis ziņojums, ko lietotāji saņem, ir tikai brīdinājuma ziņojums.</span><span class="sxs-lookup"><span data-stu-id="507d2-112">In the Commerce version 10.0.20 release and later, the message that users receive is only a warning message.</span></span> <span data-ttu-id="507d2-113">Lietotāji var turpināt apstrādāt atgriešanu sērijas numuram, kas atšķiras no sērijas numura, kas sākotnēji tika pārdots.</span><span class="sxs-lookup"><span data-stu-id="507d2-113">Users can continue to process a return against a serial number that differs from the serial number that was originally sold.</span></span>

<span data-ttu-id="507d2-114">Lai konfigurētu sērijas numura validāciju organizācijai pēc tam, kad ir ieslēgts līdzeklis **Vienotā atgriešanas apstrādes pieredze programmā POS**, dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Commerce parametri**, kas atrodami Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="507d2-114">To configure serial number validation for an organization after the **Unified return processing experience in POS** feature is turned on, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters** in Commerce headquarters.</span></span> <span data-ttu-id="507d2-115">Cilnes **Krājumi** kopsavilkuma cilnē **Veikala krājumu operācijas** iestatiet opciju **Iespējot sērijas numuru validāciju atgriešanai POS** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="507d2-115">On the **Inventory** tab, on the **Store inventory operations** FastTab, set the **Enable validation of serial numbers on POS returns** option to **Yes**.</span></span>

## <a name="process-returns-for-serialized-items-in-pos"></a><span data-ttu-id="507d2-116">Serializēto krājumu atgriešanas apstrāde programmā POS</span><span class="sxs-lookup"><span data-stu-id="507d2-116">Process returns for serialized items in POS</span></span>

<span data-ttu-id="507d2-117">Ja opcija **Iespējot sērijas numuru validāciju atgriešanai POS** ir iestatīta uz **Jā**, kad sērijveida kontrolēts krājums tiek atgriezts, izmantojot POS, lietotājs var ievadīt sērijas numuru atgriešanas rindai informācijas rūtī, kas atrodas lapā **Atgriežamās preces**.</span><span class="sxs-lookup"><span data-stu-id="507d2-117">If the **Enable validation of serial numbers on POS returns** option has been set to **Yes**, when a serial number–controlled item is returned through POS, the user can enter the serial number for the return line in the details pane on the **Returnable products** page.</span></span> <span data-ttu-id="507d2-118">Ja ievadītais sērijas numurs neatbilst sākotnējam sērijas numuram, kas tika pārdots pārdošanas darbībā, lietotājs saņem brīdinājuma ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="507d2-118">If the serial number that is entered doesn't match the original serial number that was sold for the sales transaction, the user receives a warning message.</span></span> <span data-ttu-id="507d2-119">Tomēr programma neliedz lietotājam turpināt iegrāmatot atgriešanu.</span><span class="sxs-lookup"><span data-stu-id="507d2-119">However, the application doesn't prevent the user from continuing to post the return.</span></span>

> [!NOTE]
> <span data-ttu-id="507d2-120">Pašlaik POS atbalsta sērijas numuru validāciju tikai atgriešanas rindām, kurās oriģinālais pasūtītais daudzums nav lielāks par vienu.</span><span class="sxs-lookup"><span data-stu-id="507d2-120">Currently, POS supports validation of serial numbers only on return lines where the original ordered quantity is no more than one.</span></span> <span data-ttu-id="507d2-121">Ja sākotnējā pārdošanas pasūtījuma rinda tika izveidota kanālā, kas nav POS, un daudzums, kas tika pasūtīts serializētajam krājumam konkrētajā pārdošanas rindā, ir vairāk nekā viens, tad krājumu nevar pareizi atgriezt, izmantojot POS.</span><span class="sxs-lookup"><span data-stu-id="507d2-121">If the original sales order line was created in a non-POS channel, and if the quantity that was ordered for the serialized item on a given sales line is more than one, the item can't be correctly returned through POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="507d2-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="507d2-122">Additional resources</span></span>

[<span data-ttu-id="507d2-123">Atgriešanas izveide programmā POS</span><span class="sxs-lookup"><span data-stu-id="507d2-123">Create returns in POS</span></span>](POS-returns.md)
