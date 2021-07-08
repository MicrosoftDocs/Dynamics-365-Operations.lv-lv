---
title: Atvaļinājuma iegāde un pārdošana
description: Programmā Dynamics 365 Human Resources varat iesniegt pieprasījumus pirkt un pārdot atvaļinājumu, pamatojoties uz pirkšanas un pārdošanas atvaļinājumu politikām, ko iestatījis uzņēmums.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271493"
---
# <a name="buy-and-sell-leave"></a><span data-ttu-id="011cc-103">Atvaļinājuma iegāde un pārdošana</span><span class="sxs-lookup"><span data-stu-id="011cc-103">Buy and sell leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="011cc-104">Programmā Dynamics 365 Human Resources varat iesniegt pieprasījumus pirkt un pārdot atvaļinājumu, pamatojoties uz pirkšanas un pārdošanas atvaļinājumu politikām, ko iestatījis uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="011cc-104">In Dynamics 365 Human Resources, you can submit requests to buy and sell leave based on the buy and sell leave policies set up by your company.</span></span>  

## <a name="request-to-buy-leave"></a><span data-ttu-id="011cc-105">Pieprasījums pirkt atvaļinājumu</span><span class="sxs-lookup"><span data-stu-id="011cc-105">Request to buy leave</span></span>

1. <span data-ttu-id="011cc-106">Darbvietā **Darbinieku patstāvīgi izmantotie pakalpojumi** atlasiet opciju **Atvaļinājuma pirkšanas pieprasījums** rūtī **Brīvā laika bilances**.</span><span class="sxs-lookup"><span data-stu-id="011cc-106">In the **Employee self service** workspace, select **Buy leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="011cc-107">Pievienojiet **Atvaļinājuma veids** un ievadiet **Summu** summu par atvaļinājumu, kuru vēlaties pirkt.</span><span class="sxs-lookup"><span data-stu-id="011cc-107">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to buy.</span></span> 

3. <span data-ttu-id="011cc-108">Atlasiet **Iesniegt**, kad esat gatavs iesniegt savu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="011cc-108">Select **Submit** when you're ready to submit your request.</span></span> 

<span data-ttu-id="011cc-109">Jūsu atlikumi tiks automātiski atjaunināti vai pirms atjaunināšanas tiks veikti apstiprināšanas procesi.</span><span class="sxs-lookup"><span data-stu-id="011cc-109">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="011cc-110">Tas ir atkarīgs no tā, kā pirkšanas politika ir konfigurēta.</span><span class="sxs-lookup"><span data-stu-id="011cc-110">This depends on how the buy policy has been configured.</span></span>

## <a name="request-to-sell-leave"></a><span data-ttu-id="011cc-111">Pieprasījums pārdot atvaļinājumu</span><span class="sxs-lookup"><span data-stu-id="011cc-111">Request to sell leave</span></span>

1. <span data-ttu-id="011cc-112">Darbvietā **Darbinieku patstāvīgi izmantotie pakalpojumi** atlasiet opciju **Atvaļinājuma pārdošanas pieprasījums** rūtī **Brīvā laika bilances**.</span><span class="sxs-lookup"><span data-stu-id="011cc-112">In the **Employee self service** workspace, select **Sell leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="011cc-113">Pievienojiet **Atvaļinājuma veids** un ievadiet **Summu** summu par atvaļinājumu, kuru vēlaties pārdot.</span><span class="sxs-lookup"><span data-stu-id="011cc-113">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to sell.</span></span> 

3. <span data-ttu-id="011cc-114">Atlasiet **Iesniegt**, kad esat gatavs iesniegt savu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="011cc-114">Select **Submit** when you're ready to submit your request.</span></span>

<span data-ttu-id="011cc-115">Jūsu atlikumi tiks automātiski atjaunināti vai pirms atjaunināšanas tiks veikti apstiprināšanas procesi.</span><span class="sxs-lookup"><span data-stu-id="011cc-115">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="011cc-116">Tas ir atkarīgs no tā, kā pirkšanas politika ir konfigurēta.</span><span class="sxs-lookup"><span data-stu-id="011cc-116">This depends on how the buy policy has been configured.</span></span>


## <a name="troubleshooting"></a><span data-ttu-id="011cc-117">Problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="011cc-117">Troubleshooting</span></span> 

<span data-ttu-id="011cc-118">Ja pirkšanas vai pārdošanas atvaļinājumu pieprasījuma darbplūsma neizdodas, lietotāji, kuriem ir privilēģija **EssLeaveBuySellRequestApprover**, var pārskatīt ziņojumu žurnālu par visiem atvaļinājumu pirkšanas un pārdošanas pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="011cc-118">If a buy or sell leave request workflow fails, users with the **EssLeaveBuySellRequestApprover** privilege can review the message log for all leave buy and sell requests.</span></span> <span data-ttu-id="011cc-119">Lai to izdarītu, dodieties uz **Atvaļinājums un prombūtne > Saite > Pirkšanas vai pārdošanas atvaļinājumu pieprasījumi > Ziņojumu žurnāls** (augšējā kreisajā pusē).</span><span class="sxs-lookup"><span data-stu-id="011cc-119">To do this, go to **Leave and absence > Link > Buy and sell leave requests > Message log** (on the upper left).</span></span> <span data-ttu-id="011cc-120">Sadaļa **Ziņojumu žurnāls** parāda lietotājiem to, kā darbības ir apstrādātas, un saistīto darbplūsmas vēsturi.</span><span class="sxs-lookup"><span data-stu-id="011cc-120">The **Message log** shows users how the transactions were processed and the associated workflow history.</span></span>


## <a name="see-also"></a><span data-ttu-id="011cc-121">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="011cc-121">See also</span></span>

[<span data-ttu-id="011cc-122">Atvaļinājumu un kavējumu apskats</span><span class="sxs-lookup"><span data-stu-id="011cc-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="011cc-123">Atvaļinājuma iegādes un pārdošanas politiku pārvaldība</span><span class="sxs-lookup"><span data-stu-id="011cc-123">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
