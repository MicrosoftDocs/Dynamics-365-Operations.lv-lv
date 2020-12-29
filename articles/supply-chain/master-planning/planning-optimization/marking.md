---
title: Krājumu marķēšana, izmantojot plānošanas optimizāciju
description: Šajā tēmā sniegta informācija par opcijām, kas pieejamas krājumu marķēšanai apstiprinātos pasūtījumos, kad izmantojat plānošanas optimizāciju.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 99a52c03e519384955d68d7101a7b73b7e9a7af6
ms.sourcegitcommit: fe21a3a98dcf6fe4eb9351941493f2c0443d8696
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672197"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="0b5fa-103">Krājumu marķēšana, izmantojot plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="0b5fa-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b5fa-104">Šajā tēmā sniegta informācija par opcijām, kas pieejamas krājumu marķēšanai apstiprinātos pasūtījumos, kad izmantojat plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="0b5fa-105">*Marķēšana* tiek izmantota, lai saistītu piedāvājumu un pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="0b5fa-106">Tas līdzinās *piesaistei*, kas norāda, kā vispārējā plānošana paredz segt pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="0b5fa-107">No plānošanas viedokļa galvenā atšķirība ir tā, ka marķēšana ir daudz noturīgāka nekā piesaiste.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="0b5fa-108">Marķēšana tika ieviesta, lai atbalstītu īpašos izmaksu novērtēšanas scenārijus pirmais iekšā, pirmais ārā (FIFO) un pēdējais iekšā, pirmais ārā (LIFO) principiem.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="0b5fa-109">Tomēr tagad tas tiek izmantots arī dažiem bezizmaksu scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="0b5fa-110">Marķēšana starp piedāvājumu un pieprasījumu nav obligāta un ir gandrīz pastāvīga.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="0b5fa-111">Marķēšanu var manuāli noņemt lietotājs, vai to var noņemt, palaižot pārdošanas pasūtījuma rindas izvēršanu, kad tiek izvēlēta opcija **Noņemt marķējumu**.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="0b5fa-112">Piesaiste tiek kontrolēta, veicot vispārējo plānošanu nodrošinājuma periodā, lai saistītu pieprasījumu ar nepieciešamo piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="0b5fa-113">Piesaisti var atjaunināt katrai plānošanas izpildei, lai optimizētu nepieciešamo piedāvājumu, lai apmierinātu pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="0b5fa-114">Kad vispārējā plānošana atjaunina piesaistes informāciju, tā ievēro jebkuru esošo marķējumu.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="0b5fa-115">Piesaiste sākas ar atbilstošu marķēšanu, rīcībā esošām rezervācijām un pasūtījuma rezervācijām šādā secībā:</span><span class="sxs-lookup"><span data-stu-id="0b5fa-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="0b5fa-116">Marķēšana starp pieprasījumu un piedāvājumu</span><span class="sxs-lookup"><span data-stu-id="0b5fa-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="0b5fa-117">Rīcībā esošas rezervācijas</span><span class="sxs-lookup"><span data-stu-id="0b5fa-117">On-hand reservations</span></span>
1. <span data-ttu-id="0b5fa-118">Pasūtījuma rezervācijas</span><span class="sxs-lookup"><span data-stu-id="0b5fa-118">On-order reservations</span></span>

<span data-ttu-id="0b5fa-119">Apstiprinot plānoto pasūtījumu, **Apstiprināšanas** dialoglodziņš sniedz lauku **Atjaunot marķējumu**, ko lietojat, lai iestatītu marķēšanas opcijas pasūtījumiem, kas izveidoti apstiprināšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="0b5fa-120">Atlasiet vienu no šīm vērtībām:</span><span class="sxs-lookup"><span data-stu-id="0b5fa-120">Select one of the following values:</span></span>

- <span data-ttu-id="0b5fa-121">**Nē** – netiek lietota krājumu marķēšana.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="0b5fa-122">**Standarta** – krājumu marķēšana tiek atjaunināta atbilstoši piesaistei.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="0b5fa-123">Vajadzību pasūtījums (pieprasījums) ir marķēts pretēji izpildes pasūtījumam (piedāvājums).</span><span class="sxs-lookup"><span data-stu-id="0b5fa-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="0b5fa-124">Ja izpildes pasūtījumā tiek saglabāts kāds daudzums, tas netiek marķēts, un atsauces informācija tiek atstāta tukša.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="0b5fa-125">Piemēram, ja pārdošanas pasūtījums par 100 ea ir piesaistīts pirkšanas pasūtījumam 150 ea, atsauces informācija tiks piešķirta tikai pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="0b5fa-126">**Paplašināts** – gan vajadzību pasūtījums (pieprasījums), gan izpildes pasūtījums (piedāvājums) ir marķēts, neraugoties uz to, vai izpildes pasūtījumā paliek pāri kāds daudzums.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="0b5fa-127">Piemēram, ja pārdošanas pasūtījums par 100 ea ir piesaistīts pirkšanas pasūtījumam 150 ea, atsauces informācija tiks piešķirta tikai pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="0b5fa-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>
