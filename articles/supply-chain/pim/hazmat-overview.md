---
title: Bīstamo materiālu pārskats
description: Šī tēma sniedz apskatu par līdzekļiem, kas ir saistīti ar bīstamu materiālu apstrādi un dokumentēšanu preču informācijas pārvaldības un noliktavu pārvaldības laikā.
author: dasani-madipalli
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 15edf61cba03a57b9b4d2c939228fd064b797942
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829382"
---
# <a name="hazardous-materials-overview"></a><span data-ttu-id="85887-103">Bīstamo materiālu pārskats</span><span class="sxs-lookup"><span data-stu-id="85887-103">Hazardous materials overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85887-104">Lai saglabātu atbilstību kuģošanas un pārvadāšanas noteikumiem, organizācijām, kas piegādā materiālus, kas klasificēti kā bīstamas preces, ir jāiekļauj papildu dokumenti ar to sūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="85887-104">To remain compliant with shipping and transport regulations, organizations that ship materials that are classified as dangerous goods must include additional paperwork with their shipments.</span></span> <span data-ttu-id="85887-105">Bīstamo materiālu līdzeklis ļauj klientiem glabāt informāciju, kas saistīta ar izlaistajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="85887-105">The hazardous materials feature lets customers store information that is related to released items.</span></span> <span data-ttu-id="85887-106">Šo informāciju var izmantot, lai palīdzētu sagatavot nosūtīšanas dokumentus.</span><span class="sxs-lookup"><span data-stu-id="85887-106">This information can then be used to help prepare shipping documentation.</span></span> <span data-ttu-id="85887-107">Organizācijai, kas piegādā bīstamas kravas, ir pašai savi procesi un procedūras, lai pārvaldītu nosūtīšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="85887-107">An organization that ships dangerous goods must have its own processes and procedures for managing the shipping process.</span></span> <span data-ttu-id="85887-108">Microsoft Dynamics 365 Supply Chain Management ir tikai rīks, kas var palīdzēt ģenerēt pieprasītos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="85887-108">Microsoft Dynamics 365 Supply Chain Management is just a tool that can help generate the required documents.</span></span>

<span data-ttu-id="85887-109">Sekojošajā diagrammā ir attēlotas darbības, kas jāveic, lai iestatītu un lietotu bīstamo materiālu līdzekli.</span><span class="sxs-lookup"><span data-stu-id="85887-109">The following diagram illustrates the steps needed to set up and use the hazardous materials feature.</span></span>

<span data-ttu-id="85887-110">![Bīstamo materiālu iestatīšana un izmantošanas līdzeklis](media/hazmat-overview.png "Bīstamo materiālu iestatīšana un izmantošanas līdzeklis")</span><span class="sxs-lookup"><span data-stu-id="85887-110">![Setup and use of the hazardous materials feature](media/hazmat-overview.png "Setup and use of the hazardous materials feature")</span></span>

<span data-ttu-id="85887-111">Bīstamo materiālu līdzeklis ir iestatīts Preču informācijas pārvaldībā un nodrošina dokumentus, kurus var izdrukāt ar noliktavas pārvaldības starpniecību.</span><span class="sxs-lookup"><span data-stu-id="85887-111">The hazardous materials feature is set up in Product information management and provides documents that can be printed through Warehouse management.</span></span> <span data-ttu-id="85887-112">Tāpēc vispārīgi runājot, šīs jomas ir divas galvenās jomas, kurās jūs pārskatīsiet, iestatīsit un izmantosiet šī līdzekļa funkcionalitāti:</span><span class="sxs-lookup"><span data-stu-id="85887-112">Therefore, broadly speaking, those areas are the two main areas where you will review, set up, and use this feature's functionality:</span></span>

- <span data-ttu-id="85887-113">**Preču informācijas pārvaldība** - iestatiet kodus, kuri tiks lietoti izlaistajai precei.</span><span class="sxs-lookup"><span data-stu-id="85887-113">**Product information management** – Set up the codes that will be applied to a released product.</span></span>
- <span data-ttu-id="85887-114">**Noliktavas pārvaldība** – strādājiet ar papildu piegādes dokumentiem, kas tiks drukāti kravām.</span><span class="sxs-lookup"><span data-stu-id="85887-114">**Warehouse management** – Work with additional shipping documents that will be printed for shipments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85887-115">Supply Chain Management norādītie bīstamie materiālu līdzekļi sniedz noderīgus preces informācijas laukus un saistīto funkcionalitāti, kas var palīdzēt reģistrēt un saistīt informāciju, kas saistīta ar jūsu bīstamajām precēm.</span><span class="sxs-lookup"><span data-stu-id="85887-115">The hazardous materials features in Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="85887-116">Šos līdzekļus var arī izmantot, lai izstrādātu un izdrukātu nosūtīšanas dokumentus, kas ietver daļu no tās pašas informācijas par visiem bīstamajiem materiāliem, ko sūtāt.</span><span class="sxs-lookup"><span data-stu-id="85887-116">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="85887-117">Tomēr sistēma automātiski neliks jums ievērot visus piemērojamos noteikumus jūsu valstī vai reģionā.</span><span class="sxs-lookup"><span data-stu-id="85887-117">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="85887-118">Lai gan šie rīki ir paredzēti, lai palīdzētu jums ievērot kopīgos noteikumus, tie nav ne pietiekami, ne arī garantē to.</span><span class="sxs-lookup"><span data-stu-id="85887-118">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="85887-119">Jūsu organizācija ir atbildīga par visu piemērojamo noteikumu pārzināšanu un visu nepieciešamo darbību veikšanu, lai tās izpildītu.</span><span class="sxs-lookup"><span data-stu-id="85887-119">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="85887-120">Preču informācijas pārvaldība</span><span class="sxs-lookup"><span data-stu-id="85887-120">Product information management</span></span>

<span data-ttu-id="85887-121">Preču informācijas pārvaldība nodrošina virkni uzstādījumu tabulu, kurās varat ievadīt atsauces informāciju dažādu bīstamo kravu sarakstiem, kas paredzētas ceļu, gaisa un jūras kravām.</span><span class="sxs-lookup"><span data-stu-id="85887-121">Product information management provides a range of setup tables where you can enter reference information for the various dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="85887-122">Kad šī funkcionalitāte tika izstrādāta, tika minētas šādas kopējas regulas:</span><span class="sxs-lookup"><span data-stu-id="85887-122">The following common regulations were referenced when this functionality was developed:</span></span>

- <span data-ttu-id="85887-123">**ADR** – regulas, kas saistītas ar starptautiskajiem bīstamo kravu autopārvadājumiem</span><span class="sxs-lookup"><span data-stu-id="85887-123">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="85887-124">**KM 49** – Amerikas Savienoto Valstu preču pārvadāšanas noteikumi bīstamo kravu pārvadāšanai</span><span class="sxs-lookup"><span data-stu-id="85887-124">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="85887-125">**IMDG** – SStarptautisko jūras bīstamo kravu kodekss (IMDG) kodekss</span><span class="sxs-lookup"><span data-stu-id="85887-125">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="85887-126">**IATA** – Starptautiskās gaisa transporta asociācijas (IATA) noteikumi par bīstamajām kravām</span><span class="sxs-lookup"><span data-stu-id="85887-126">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="85887-127">Katra regulu kopa sniedz standartizētus bīstamo preču un atsauču kodu sarakstus.</span><span class="sxs-lookup"><span data-stu-id="85887-127">Each set of regulations provides standardized lists of dangerous goods and reference codes.</span></span> <span data-ttu-id="85887-128">Tādēļ Supply Chain Management sniedz atsauču tabulu kopīgos kodus šajos sarakstos.</span><span class="sxs-lookup"><span data-stu-id="85887-128">Therefore, Supply Chain Management provides a reference table for the common codes on those lists.</span></span> <span data-ttu-id="85887-129">Katram sarakstam ir arī daži unikāli kodi, kurus varat definēt.</span><span class="sxs-lookup"><span data-stu-id="85887-129">Each list also has some unique codes that you can define.</span></span>

<span data-ttu-id="85887-130">Lai iegūtu vairāk informācijas par to, kā iestatīt noteikumus un vērtības bīstamiem materiāliem un kā piešķirt vērtības attiecīgajām precēm, skatiet sekojošās tēmas:</span><span class="sxs-lookup"><span data-stu-id="85887-130">For more information about how to set up regulations and values for hazardous materials, and how to assign the values to relevant products, see the following topics:</span></span>

- [<span data-ttu-id="85887-131">Bīstamo materiālu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="85887-131">Set up hazardous materials</span></span>](hazmat-setup.md)
- [<span data-ttu-id="85887-132">Bīstamie materiāli precēs, pasūtījumos, sūtījumos un kravās</span><span class="sxs-lookup"><span data-stu-id="85887-132">Hazardous materials in products, orders, shipments, and loads</span></span>](hazmat-items.md)

## <a name="warehouse-management"></a><span data-ttu-id="85887-133">Noliktavas vadība</span><span class="sxs-lookup"><span data-stu-id="85887-133">Warehouse management</span></span>

<span data-ttu-id="85887-134">Sagatavojot sūtījumu Noliktavas pārvaldībā, varēsit drukāt vairākus jaunus pārskatus, kas izmanto informāciju, kas iestatīta preču informācijas pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="85887-134">When you prepare a shipment in Warehouse management, you will be able to print several new reports that use the information that you set up in Product information management.</span></span> <span data-ttu-id="85887-135">Plašāku informāciju par pieejamiem pārskatiem un to lietošanu skatiet šeit: [Bīstamo materiālu pieprasījumi un pārskati](hazmat-reports.md).</span><span class="sxs-lookup"><span data-stu-id="85887-135">For more information about the available reports and how to use them, see [Hazardous materials inquiries and reports](hazmat-reports.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]