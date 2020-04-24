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
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5006f06d90ddcc314a51878e9e21337de7d493e7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208469"
---
# <a name="hazardous-materials"></a><span data-ttu-id="019a1-103">Bīstamie materiāli</span><span class="sxs-lookup"><span data-stu-id="019a1-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="019a1-104">Informācija par bīstamiem materiāliem ir iestatīta modulī Preču informācijas pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="019a1-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="019a1-105">Šis modulis nodrošina arī dokumentus, ko var izdrukāt ar noliktavas vadības starpniecību.</span><span class="sxs-lookup"><span data-stu-id="019a1-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="019a1-106">Kad nosūtāt materiālus, kas klasificēti kā bīstamas preces, sūtījumam jāpievieno papildu dokumenti.</span><span class="sxs-lookup"><span data-stu-id="019a1-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="019a1-107">Bīstamo materiālu funkcionalitāte ļauj klientiem uzglabāt klasifikācijas informāciju un saistīt to ar izlaistajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="019a1-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="019a1-108">Šo informāciju var izmantot, lai palīdzētu sagatavot nosūtīšanas dokumentus.</span><span class="sxs-lookup"><span data-stu-id="019a1-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="019a1-109">Lai palīdzētu pārvaldīt bīstamu preču sūtījumus, Microsoft Dynamics 365 Supply Chain Management ļauj iestatīt papildu atsauces informāciju, kas ir saistīta ar precēm.</span><span class="sxs-lookup"><span data-stu-id="019a1-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="019a1-110">Varat arī iestatīt papildu nosūtīšanas dokumentus.</span><span class="sxs-lookup"><span data-stu-id="019a1-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="019a1-111">Tomēr, sistēma nav automātiski atbilstoša jūsu valsts vai reģiona noteikumiem.</span><span class="sxs-lookup"><span data-stu-id="019a1-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="019a1-112">Tā ir rīks, kas var palīdzēt vispārējai programmai.</span><span class="sxs-lookup"><span data-stu-id="019a1-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="019a1-113">Lai varētu lietot šo funkcionalitāti, nepieciešams tālak norādītais iestatījums.</span><span class="sxs-lookup"><span data-stu-id="019a1-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="019a1-114">**Preču informācijas pārvaldība:** iestatiet kodus, kurus var lietot izlaistām precēm.</span><span class="sxs-lookup"><span data-stu-id="019a1-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="019a1-115">**Noliktavas vadība:** lietojiet papildu nosūtīšanas dokumentus, lai drukātu piegādes informāciju.</span><span class="sxs-lookup"><span data-stu-id="019a1-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="019a1-116">Preču informācijas pārvaldība</span><span class="sxs-lookup"><span data-stu-id="019a1-116">Product information management</span></span>

<span data-ttu-id="019a1-117">Produktu informācijas pārvaldībā ir iekļauta virkne uzstādījumu tabulu, kurās varat pievienot atsauces informāciju, kas tiek sniegta bīstamo kravu sarakstos, kas paredzētas ceļu, gaisa un jūras kravām.</span><span class="sxs-lookup"><span data-stu-id="019a1-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="019a1-118">Lūk, daži no noteikumiem, uz kuriem bieži atsaucas.</span><span class="sxs-lookup"><span data-stu-id="019a1-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="019a1-119">**ADR** – regulas, kas saistītas ar starptautiskajiem bīstamo kravu autopārvadājumiem</span><span class="sxs-lookup"><span data-stu-id="019a1-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="019a1-120">**KM 49** – Amerikas Savienoto Valstu preču pārvadāšanas noteikumi bīstamo kravu pārvadāšanai</span><span class="sxs-lookup"><span data-stu-id="019a1-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="019a1-121">**IMDG** – SStarptautisko jūras bīstamo kravu kodekss (IMDG) kodekss</span><span class="sxs-lookup"><span data-stu-id="019a1-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="019a1-122">**IATA** – Starptautiskās gaisa transporta asociācijas (IATA) noteikumi par bīstamajām kravām</span><span class="sxs-lookup"><span data-stu-id="019a1-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="019a1-123">Katrai no šīm regulām ir bīstamo preču saraksts, kurā ietilpst atsauču kodi.</span><span class="sxs-lookup"><span data-stu-id="019a1-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="019a1-124">Saraksti, kas paredzēti katram transporta veidam, tiek apvienoti ar kopīgām starptautiskām klasifikācijām.</span><span class="sxs-lookup"><span data-stu-id="019a1-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="019a1-125">Piegādes ķēžu pārvaldība sniedz atsauču tabulu kopīgos kodus šajos sarakstos.</span><span class="sxs-lookup"><span data-stu-id="019a1-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="019a1-126">Katram sarakstam ir arī daži unikāli kodi, kurus var definēt.</span><span class="sxs-lookup"><span data-stu-id="019a1-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="019a1-127">Lai sāktu konfigurēt šo informāciju, izveidojiet noteikumu, ko varat izmantot, lai konfigurētu sākotnējos parametrus.</span><span class="sxs-lookup"><span data-stu-id="019a1-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="019a1-128">Noliktavas vadība</span><span class="sxs-lookup"><span data-stu-id="019a1-128">Warehouse management</span></span>

<span data-ttu-id="019a1-129">Kad krava ir sagatavota, var izdrukāt vairākus jaunus pārskatus.</span><span class="sxs-lookup"><span data-stu-id="019a1-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="019a1-130">Šajos pārskatos izmanto informāciju, kas iestatīta preču informācijas pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="019a1-130">These reports use the information that you set up in Product information management.</span></span>
