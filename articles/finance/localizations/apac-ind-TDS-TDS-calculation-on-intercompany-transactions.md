---
title: TDS aprēķins starpuzņēmumu darījumiem
description: Šajā tēmā aprakstīts process, kas tiek izmantots, lai aprēķinātu No kopējo ienākumu summas atskaitīto nodokli (TDS) starpuzņēmumu darījumos fāzēs.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023421"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="5d94b-103">TDS aprēķins starpuzņēmumu darījumiem</span><span class="sxs-lookup"><span data-stu-id="5d94b-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d94b-104">Šajā tēmā aprakstīts process, kas tiek izmantots, lai aprēķinātu No kopējo ienākumu summas atskaitīto nodokli (TDS) starpuzņēmumu darījumos fāzēs.</span><span class="sxs-lookup"><span data-stu-id="5d94b-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="5d94b-105">Kad starpuzņēmuma pirkšanas pasūtījums vai pārdošanas pasūtījums ir izveidots, TDS noklusējuma grupa, kas noteikta debitoram vai kreditoram, tiek izmantota TDS summas aprēķinam.</span><span class="sxs-lookup"><span data-stu-id="5d94b-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="5d94b-106">TDS summa tiek grāmatota atgūstamajiem vai maksājamajiem kontiem pēc rēķina iegrāmatošanas.</span><span class="sxs-lookup"><span data-stu-id="5d94b-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="5d94b-107">Oriģinālajam pirkšanas pasūtījumam vai pārdošanas pasūtījumam automātiski tiek izveidots starpuzņēmumu pārdošanas pasūtījums vai pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="5d94b-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="5d94b-108">Noklusējuma TDS grupa tiek parādīta starpuzņēmumu pasūtījumā, lai var aprēķināt TDS.</span><span class="sxs-lookup"><span data-stu-id="5d94b-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="5d94b-109">Jūs varat izmainīt TDS grupu.</span><span class="sxs-lookup"><span data-stu-id="5d94b-109">You can change the TDS group.</span></span> <span data-ttu-id="5d94b-110">Rēķinu var grāmatot tikai tad, ja rēķina neto summa starpuzņēmumu pasūtījumā, kas tiek automātiski izveidots, atbilst rēķina neto summai oriģinālajā pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="5d94b-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="5d94b-111">(Neto summa ir rēķina summa pēc TDS atskaitījuma.)</span><span class="sxs-lookup"><span data-stu-id="5d94b-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="5d94b-112">Piemēram, pārdošanas rēķins ir izveidots 50 000 un tam ir pievienota **10%** TDS grupa.</span><span class="sxs-lookup"><span data-stu-id="5d94b-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="5d94b-113">Grāmatotā rēķina summa ir 45 000, un iegrāmatotā TDS summa pārdošanas rēķinam ir 5000.</span><span class="sxs-lookup"><span data-stu-id="5d94b-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="5d94b-114">Pirkšanas pasūtījums tiek automātiski izveidots starpuzņēmumu pārdošanas pasūtījumam un tam tiek pievienota **10%** TDS grupa.</span><span class="sxs-lookup"><span data-stu-id="5d94b-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="5d94b-115">Ja maināt TDS grupu uz **15%**, rēķinu nevar grāmatot, jo automātiski izveidotā starpuzņēmumu pārdošanas pasūtījuma rēķina neto summa neatbilst sākotnējā pārdošanas pasūtījuma neto rēķina summai.</span><span class="sxs-lookup"><span data-stu-id="5d94b-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="5d94b-116">Maksājumu žurnāls, kas izveidots starpuzņēmumu rēķinam, tiek grāmatots automātiski.</span><span class="sxs-lookup"><span data-stu-id="5d94b-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="5d94b-117">Šo maksājumu žurnālu var grāmatot tikai tad, ja tā neto maksājuma summa atbilst neto maksājuma summai oriģinālajā maksājumu žurnālā.</span><span class="sxs-lookup"><span data-stu-id="5d94b-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>
