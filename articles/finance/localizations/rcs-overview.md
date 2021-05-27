---
title: Regulatory Configuration Service
description: Šajā tēmā sniegts pārskats par Regulatory Configuration Service (RCS) iespējām un skaidrots, kā piekļūt šim pakalpojumam.
author: JaneA07
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1eeac7217290e0583fcecdf5b4b5b9153d266240
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019398"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="86e7a-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="86e7a-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86e7a-104">Regulatory Configuration Service (RCS) ir savrups veidotājs un dzīves cikla pārvaldības pakalpojums bezkoda/zema koda globalizācijas funkcionalitātei.</span><span class="sxs-lookup"><span data-stu-id="86e7a-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="86e7a-105">RCS ļauj globalizācijas ieinteresētajām personām paplašināt un pielāgot galvenās globalizācijas jomas, proti, nodokļu, e-rēķinu, regulatīvo ziņojumu, banku un uzņēmējdarbības dokumentus, nepiesaistot izstrādātājus.</span><span class="sxs-lookup"><span data-stu-id="86e7a-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="86e7a-106">Šī bezkoda/zema koda globalizācijas pieeja padara globalizāciju vieglāku, ātrāku un izmaksu ziņā efektīvāku, lai to izveidotu vai paplašinātu.</span><span class="sxs-lookup"><span data-stu-id="86e7a-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="86e7a-107">RCS nodrošina šādas iespējas:</span><span class="sxs-lookup"><span data-stu-id="86e7a-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="86e7a-108">Atbalsts visai funkcionalitātei, ko nodrošina elektronisko pārskatu izrakstīšana (ER).</span><span class="sxs-lookup"><span data-stu-id="86e7a-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="86e7a-109">Jaunu globalizācijas mikropakalnu konfigurēšanas priekšnosacījums.</span><span class="sxs-lookup"><span data-stu-id="86e7a-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="86e7a-110">Atbalsts elektroniskajai rēķinu izrakstīšanai.</span><span class="sxs-lookup"><span data-stu-id="86e7a-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="86e7a-111">Plašāku informāciju skatiet [Elektronisko rēķinu izrakstīšana](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="86e7a-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="86e7a-112">Atbalsts nodokļu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="86e7a-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="86e7a-113">Papildinformāciju skatiet sadaļā [Nodokļu pakalpojums](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="86e7a-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="86e7a-114">Atbalsts jaunajai globalizācijas līdzekļa funkcionalitātei, kas vienkāršo vairāku komponentu līdzekļu dzīves cikla pārvaldību un nodrošina papildu spēju konfigurēt darbības un iestatīt funkcionalitātes parametrus.</span><span class="sxs-lookup"><span data-stu-id="86e7a-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="86e7a-115">Plašāku informāciju skatiet [Regulatory Configuration Service - vienkāršota globalizācijas līdzekļu pārvaldība globalizācijas pakalpojumiem](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="86e7a-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="86e7a-116">Atbalsts pielāgotu konfigurāciju centralizētai publicēšanai, uzglabāšanai un koplietošanai globālajā repozitorijā, lai atvieglotu konfigurācijas pārvaldību, neprasot Microsoft Dynamics Lifecycle Services (LCS) lietošanu.</span><span class="sxs-lookup"><span data-stu-id="86e7a-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="86e7a-117">Piekļuve RCS</span><span class="sxs-lookup"><span data-stu-id="86e7a-117">Access RCS</span></span>

<span data-ttu-id="86e7a-118">Varat pierakstīties uz RCS vai pieteikties RCS no [Regulatory Configuration Service lapas](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="86e7a-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![Pierakstīties/pieteikties RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="86e7a-120">Lapā **Regulatory Configuration Service** pārskatiet un akceptējiet pakalpojuma papildu noteikumus un nosacījumus un pēc tam atlasiet vienu no šīm pogām:</span><span class="sxs-lookup"><span data-stu-id="86e7a-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="86e7a-121">**Pierakstīties**, ja esat pakalpojuma pirmreizējs lietotājs un izmantojat uzņēmuma e-pasta adresi, lai nodrošinātu uzņēmumam pakalpojumu vidi</span><span class="sxs-lookup"><span data-stu-id="86e7a-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="86e7a-122">**Pieteikties**, ja iepriekš esat pierakstījies pakalpojumam un vēlaties piekļūt savas organizācijas videi</span><span class="sxs-lookup"><span data-stu-id="86e7a-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="86e7a-123">Reģionālā pieejamība</span><span class="sxs-lookup"><span data-stu-id="86e7a-123">Regional availability</span></span>

<span data-ttu-id="86e7a-124">RCS ir pieejams šādos reģionos:</span><span class="sxs-lookup"><span data-stu-id="86e7a-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="86e7a-125">ASV</span><span class="sxs-lookup"><span data-stu-id="86e7a-125">United States</span></span>
- <span data-ttu-id="86e7a-126">Indija</span><span class="sxs-lookup"><span data-stu-id="86e7a-126">India</span></span>
- <span data-ttu-id="86e7a-127">Francija</span><span class="sxs-lookup"><span data-stu-id="86e7a-127">France</span></span>
- <span data-ttu-id="86e7a-128">Eiropa</span><span class="sxs-lookup"><span data-stu-id="86e7a-128">Europe</span></span>

<span data-ttu-id="86e7a-129">Pilnīgu reģionu sarakstu skatiet [Dynamics 365 un Power Platform: pieejamība, datu atrašanās vieta, valoda un lokalizācija](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="86e7a-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="86e7a-130">Saistītā RCS dokumentācija</span><span class="sxs-lookup"><span data-stu-id="86e7a-130">Related RCS documentation</span></span>

<span data-ttu-id="86e7a-131">Papildinformāciju par saistītiem komponentiem skatiet tālāk minētajā dokumentācijā.</span><span class="sxs-lookup"><span data-stu-id="86e7a-131">For more information about related components, see the following documentation:</span></span>

- <span data-ttu-id="86e7a-132">**Globālais repozitorijs:**</span><span class="sxs-lookup"><span data-stu-id="86e7a-132">**Global repository:**</span></span>

    - [<span data-ttu-id="86e7a-133">Izveidot ER konfigurāciju & augšupielādēt globālajā repozitorijā</span><span class="sxs-lookup"><span data-stu-id="86e7a-133">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="86e7a-134">Kopīgot konfigurāciju globālajā repozitorijā</span><span class="sxs-lookup"><span data-stu-id="86e7a-134">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="86e7a-135">Uzlabota filtrēšana globālajā repozitorijā</span><span class="sxs-lookup"><span data-stu-id="86e7a-135">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="86e7a-136">Elektronisko pārskatu konfigurāciju lejupielāde no globālā repozitorija</span><span class="sxs-lookup"><span data-stu-id="86e7a-136">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="86e7a-137">Pārtraukt konfigurācijas globālajā repozitorijā</span><span class="sxs-lookup"><span data-stu-id="86e7a-137">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)

- <span data-ttu-id="86e7a-138">**Globalizācijas līdzeklis:**</span><span class="sxs-lookup"><span data-stu-id="86e7a-138">**Globalization feature:**</span></span>

    - [<span data-ttu-id="86e7a-139">Regulatory Configuration Service (RCS) — globalizācijas līdzeklis</span><span class="sxs-lookup"><span data-stu-id="86e7a-139">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)