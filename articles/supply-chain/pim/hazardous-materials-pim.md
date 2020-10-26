---
title: Bīstamie materiāli
description: Šajā tēmā ir sniegta informācija par bīstamiem materiālu dokumentiem un informāciju, kas glabājas jūsu vidē.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: feee6b348ac1870295a894ad988278b23a3f30a3
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979044"
---
# <a name="hazardous-materials"></a><span data-ttu-id="a1d1d-103">Bīstamie materiāli</span><span class="sxs-lookup"><span data-stu-id="a1d1d-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a1d1d-104">Informācija par bīstamiem materiāliem ir iestatīta modulī Preču informācijas pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="a1d1d-105">Šis modulis nodrošina arī dokumentus, ko var izdrukāt ar noliktavas vadības starpniecību.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="a1d1d-106">Kad nosūtāt materiālus, kas klasificēti kā bīstamas preces, sūtījumam jāpievieno papildu dokumenti.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="a1d1d-107">Bīstamo materiālu funkcionalitāte ļauj klientiem uzglabāt klasifikācijas informāciju un saistīt to ar izlaistajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="a1d1d-108">Šo informāciju var izmantot, lai palīdzētu sagatavot nosūtīšanas dokumentus.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1d1d-109">Microsoft Dynamics 365 Supply Chain Management norādītie bīstamie materiālu līdzekļi sniedz noderīgus preces informācijas laukus un saistīto funkcionalitāti, kas var palīdzēt reģistrēt un saistīt informāciju, kas saistīta ar jūsu bīstamajām precēm.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="a1d1d-110">Šos līdzekļus var arī izmantot, lai izstrādātu un izdrukātu nosūtīšanas dokumentus, kas ietver daļu no tās pašas informācijas par visiem bīstamajiem materiāliem, ko sūtāt.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="a1d1d-111">Tomēr sistēma automātiski neliks jums ievērot visus piemērojamos noteikumus jūsu valstī vai reģionā.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="a1d1d-112">Lai gan šie rīki ir paredzēti, lai palīdzētu jums ievērot kopīgos noteikumus, tie nav ne pietiekami, ne arī garantē to.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="a1d1d-113">Jūsu organizācija ir atbildīga par visu piemērojamo noteikumu pārzināšanu un visu nepieciešamo darbību veikšanu, lai tās izpildītu.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="a1d1d-114">Lai varētu lietot šo funkcionalitāti, nepieciešams tālak norādītais iestatījums.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="a1d1d-115">**Preču informācijas pārvaldība:** iestatiet kodus, kurus var lietot izlaistām precēm.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="a1d1d-116">**Noliktavas vadība:** lietojiet papildu nosūtīšanas dokumentus, lai drukātu piegādes informāciju.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="a1d1d-117">Preču informācijas pārvaldība</span><span class="sxs-lookup"><span data-stu-id="a1d1d-117">Product information management</span></span>

<span data-ttu-id="a1d1d-118">Produktu informācijas pārvaldībā ir iekļauta virkne uzstādījumu tabulu, kurās varat pievienot atsauces informāciju, kas tiek sniegta bīstamo kravu sarakstos, kas paredzētas ceļu, gaisa un jūras kravām.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="a1d1d-119">Lūk, daži no noteikumiem, uz kuriem bieži atsaucas.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="a1d1d-120">**ADR** – regulas, kas saistītas ar starptautiskajiem bīstamo kravu autopārvadājumiem</span><span class="sxs-lookup"><span data-stu-id="a1d1d-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="a1d1d-121">**KM 49** – Amerikas Savienoto Valstu preču pārvadāšanas noteikumi bīstamo kravu pārvadāšanai</span><span class="sxs-lookup"><span data-stu-id="a1d1d-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="a1d1d-122">**IMDG** – SStarptautisko jūras bīstamo kravu kodekss (IMDG) kodekss</span><span class="sxs-lookup"><span data-stu-id="a1d1d-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="a1d1d-123">**IATA** – Starptautiskās gaisa transporta asociācijas (IATA) noteikumi par bīstamajām kravām</span><span class="sxs-lookup"><span data-stu-id="a1d1d-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="a1d1d-124">Katrai no šīm regulām ir bīstamo preču saraksts, kurā ietilpst atsauču kodi.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="a1d1d-125">Saraksti, kas paredzēti katram transporta veidam, tiek apvienoti ar kopīgām starptautiskām klasifikācijām.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="a1d1d-126">Piegādes ķēžu pārvaldība sniedz atsauču tabulu kopīgos kodus šajos sarakstos.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="a1d1d-127">Katram sarakstam ir arī daži unikāli kodi, kurus var definēt.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="a1d1d-128">Lai sāktu konfigurēt šo informāciju, izveidojiet noteikumu, ko varat izmantot, lai konfigurētu sākotnējos parametrus.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="a1d1d-129">Noliktavas vadība</span><span class="sxs-lookup"><span data-stu-id="a1d1d-129">Warehouse management</span></span>

<span data-ttu-id="a1d1d-130">Kad krava ir sagatavota, var izdrukāt vairākus jaunus pārskatus.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="a1d1d-131">Šajos pārskatos izmanto informāciju, kas iestatīta preču informācijas pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-131">These reports use the information that you set up in Product information management.</span></span>
