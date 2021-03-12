---
title: Pavadzīmju atjauninājumi atgrieztajiem krājumiem
description: Pirms atgriezto krājumu saņemšanas noliktavā, tiem piederošā pasūtījuma pavadzīme ir jāatjaunina.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c82e43beddb8bae0a56b0894ce484ca7605b42e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006720"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="df72d-103">Pavadzīmju atjauninājumi atgrieztajiem krājumiem</span><span class="sxs-lookup"><span data-stu-id="df72d-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="df72d-104">Pirms atgriezto krājumu saņemšanas noliktavā, tiem piederošā pasūtījuma pavadzīme ir jāatjaunina.</span><span class="sxs-lookup"><span data-stu-id="df72d-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="df72d-105">Tāpat kā rēķinu atjaunināšanas process ir atjaunināšana uz finanšu darījumu, pavadzīmju atjaunināšanas process ir fiziska krājumu ierakstu atjaunināšana. Tas nozīmē, ka tiek veiktas izmaiņas krājumos.</span><span class="sxs-lookup"><span data-stu-id="df72d-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="df72d-106">Atgriešanas gadījumā darbības, kas ir piešķirtas atgriešanas metodes darbībai, tiek ieviestas pavadzīmes atjaunināšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="df72d-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="df72d-107">Pavadzīmju atjaunināšanu ir iespējams apstrādāt krājumu saņemšanas žurnālā vai atgriešanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="df72d-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="df72d-108">Kā daļa no pavadzīmju iegrāmatošanas procesa pavadzīmju atsauces numurs no klienta piegādes dokumentiem var tikt saistīts ar pasūtījuma rindām.</span><span class="sxs-lookup"><span data-stu-id="df72d-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="df72d-109">Šī saistīšana nav obligāta un tiek izmantota tikai kā atsauce.</span><span class="sxs-lookup"><span data-stu-id="df72d-109">This association is optional and for reference only.</span></span> <span data-ttu-id="df72d-110">Tā neizraisa nekādus transakcijas atjauninājumus.</span><span class="sxs-lookup"><span data-stu-id="df72d-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="df72d-111">Ja nav tikuši saņemti visi paredzētie atgrieztie krājumi, pavadzīmes atjaunināšanā jāiekļauj tikai tas daudzums, kas ticis saņemts.</span><span class="sxs-lookup"><span data-stu-id="df72d-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="df72d-112">Atlikušie krājumi jāatstāj pasūtījumā, līdz tiek saņemta pārējā kravas daļa.</span><span class="sxs-lookup"><span data-stu-id="df72d-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="df72d-113">Ja krājums ticis atsūtīts atpakaļ no karantīnas uz Nosūtīšanas un Saņemšanas nodaļu, piemēram, kad karantīnas inspektors nezina, kur noliktavā uzglabāt šo krājumu, attiecīgā pavadzīme ir jāatjaunina, lai pareizi reģistrētu un rīkotos pēc izvietojuma koda, kas ir noteikts kā karantīnas rezultāts.</span><span class="sxs-lookup"><span data-stu-id="df72d-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="df72d-114">Atjauninot pavadzīmi atgrieztajam krājumam, kas ir no pārdošanas līguma, attiecīgā krājuma pārdošanas līguma saistības tiek automātiski atjauninātas, lai atspoguļotu daudzuma vai summas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="df72d-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="df72d-115">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="df72d-115">See also</span></span>

[<span data-ttu-id="df72d-116">Rēķinu atjauninājumu veikšana atgrieztajiem krājumiem</span><span class="sxs-lookup"><span data-stu-id="df72d-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  


