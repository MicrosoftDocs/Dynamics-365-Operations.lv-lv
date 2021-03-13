---
title: Atgriezto krājumu daļēju piegāžu saņemšana
description: Daļējas piegādes tiek definētas atgriešanas pasūtījuma rindās, nevis atgriešanas pasūtījuma sūtījumā.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31db10ad820bf049192ba0446b59da16cab3c553
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010601"
---
# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="6a0c0-103">Atgriezto krājumu daļēju piegāžu saņemšana</span><span class="sxs-lookup"><span data-stu-id="6a0c0-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6a0c0-104">Daļējas piegādes tiek definētas atgriešanas pasūtījuma rindās, nevis atgriešanas pasūtījuma sūtījumā.</span><span class="sxs-lookup"><span data-stu-id="6a0c0-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="6a0c0-105">Tas nozīmē, ka gadījumā, ja saņemat visu daudzumu, kas ir norādīts atgriešanas pasūtījuma rindā, bet nesaņemat neko no atgriešanas pasūtījuma citām rindām, piegāde nav daļēja piegāde.</span><span class="sxs-lookup"><span data-stu-id="6a0c0-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="6a0c0-106">Tomēr, ja atgriešanas pasūtījuma rindās norādītas attiecīgās atgriežamās preces 10 vienības, bet jūs saņemat tikai 4, tā ir daļēja piegāde.</span><span class="sxs-lookup"><span data-stu-id="6a0c0-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="6a0c0-107">Ja atgrieztajā sūtījumā ir mazāk nekā pilns daudzums no atgriešanas pasūtījuma rindas, jūs varat sūtījumu rezervēt un nogaidīt, līdz tiek saņemts pārējais daudzums vai arī varat reģistrēt un grāmatot daļēju daudzumu.</span><span class="sxs-lookup"><span data-stu-id="6a0c0-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="6a0c0-108">Reģistrēt un grāmatot daļēju daudzumu</span><span class="sxs-lookup"><span data-stu-id="6a0c0-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="6a0c0-109">Kad ir atlasīts atgriešanas pasūtījums saņemšanai, formā **Saņemšanas darbību apskats — noliktava: %1, doks: %2, žurnāla nosaukums: %3** noklikšķiniet uz **Sākt saņemšanu**, lai izveidotu saņemšanas žurnālu, un pēc tam noklikšķiniet uz vienuma **Žurnāli** \> **Rādīt saņemšanas no ieejas plūsmām**, lai atvērtu formu **Novietojumu žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="6a0c0-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="6a0c0-110">Atlasiet žurnāla rindu, ar kuru vēlaties strādāt, un pēc tam noklikšķiniet uz **Rindas**, lai atvērtu veidlapu **Žurnāla rindas, novietojumi**.</span><span class="sxs-lookup"><span data-stu-id="6a0c0-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="6a0c0-111">Atlasiet krājuma koda rindu, kurai ir saņemts tikai daļējs daudzums un tad noklikšķiniet uz **Funkcijas** \> **Sadale**, lai atvērtu veidlapu **Sadale**.</span><span class="sxs-lookup"><span data-stu-id="6a0c0-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="6a0c0-112">Laukā **Atdalīt daudzumu** ierakstiet kopējo saņemto krājumu daudzumu un pēc tam noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6a0c0-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="6a0c0-113">Veidlapā **Žurnāla rindas, novietojumi** atlasiet saņemto krājumu daudzuma rindu un pēc tam noklikšķiniet uz **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="6a0c0-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="6a0c0-114">Jūs varat grāmatot papildu daudzuma rindu pēc tam, kad krājumi tiek saņemti.</span><span class="sxs-lookup"><span data-stu-id="6a0c0-114">You can post the line for the additional quantity after the items have arrived.</span></span>




