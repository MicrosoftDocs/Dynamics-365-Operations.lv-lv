---
title: Regulatory Configuration Service
description: Šajā tēmā sniegts pārskats par Regulatory Configuration Service (RCS) iespējām un skaidrots, kā piekļūt šim pakalpojumam.
author: JaneA07
ms.date: 06/04/2021
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
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216566"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="4a949-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="4a949-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a949-104">Regulatory Configuration Service (RCS) ir savrups veidotājs un dzīves cikla pārvaldības pakalpojums bezkoda/zema koda globalizācijas funkcionalitātei.</span><span class="sxs-lookup"><span data-stu-id="4a949-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="4a949-105">RCS ļauj globalizācijas ieinteresētajām personām paplašināt un pielāgot galvenās globalizācijas jomas, proti, nodokļu, e-rēķinu, regulatīvo ziņojumu, banku un uzņēmējdarbības dokumentus, nepiesaistot izstrādātājus.</span><span class="sxs-lookup"><span data-stu-id="4a949-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="4a949-106">Šī bezkoda/zema koda globalizācijas pieeja padara globalizāciju vieglāku, ātrāku un izmaksu ziņā efektīvāku, lai to izveidotu vai paplašinātu.</span><span class="sxs-lookup"><span data-stu-id="4a949-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="4a949-107">RCS nodrošina šādas iespējas:</span><span class="sxs-lookup"><span data-stu-id="4a949-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="4a949-108">Atbalsts visai funkcionalitātei, ko nodrošina elektronisko pārskatu izrakstīšana (ER).</span><span class="sxs-lookup"><span data-stu-id="4a949-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="4a949-109">Jaunu globalizācijas mikropakalnu konfigurēšanas priekšnosacījums.</span><span class="sxs-lookup"><span data-stu-id="4a949-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="4a949-110">Atbalsts elektroniskajai rēķinu izrakstīšanai.</span><span class="sxs-lookup"><span data-stu-id="4a949-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="4a949-111">Plašāku informāciju skatiet [Elektronisko rēķinu izrakstīšana](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="4a949-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="4a949-112">Atbalsts nodokļu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="4a949-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="4a949-113">Papildinformāciju skatiet sadaļā [Nodokļu pakalpojums](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="4a949-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="4a949-114">Atbalsts jaunajai globalizācijas līdzekļa funkcionalitātei, kas vienkāršo vairāku komponentu līdzekļu dzīves cikla pārvaldību un nodrošina papildu spēju konfigurēt darbības un iestatīt funkcionalitātes parametrus.</span><span class="sxs-lookup"><span data-stu-id="4a949-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="4a949-115">Plašāku informāciju skatiet [Regulatory Configuration Service - vienkāršota globalizācijas līdzekļu pārvaldība globalizācijas pakalpojumiem](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="4a949-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="4a949-116">Atbalsts pielāgotu konfigurāciju centralizētai publicēšanai, uzglabāšanai un koplietošanai globālajā repozitorijā, lai atvieglotu konfigurācijas pārvaldību, neprasot Microsoft Dynamics Lifecycle Services (LCS) lietošanu.</span><span class="sxs-lookup"><span data-stu-id="4a949-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="4a949-117">Piekļuve RCS</span><span class="sxs-lookup"><span data-stu-id="4a949-117">Access RCS</span></span>

<span data-ttu-id="4a949-118">Varat pierakstīties uz RCS vai pieteikties RCS no [Regulatory Configuration Service lapas](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="4a949-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![Pierakstīties/pieteikties RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="4a949-120">Lapā **Regulatory Configuration Service** pārskatiet un akceptējiet pakalpojuma papildu noteikumus un nosacījumus un pēc tam atlasiet vienu no šīm pogām:</span><span class="sxs-lookup"><span data-stu-id="4a949-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="4a949-121">**Pierakstīties**, ja esat pakalpojuma pirmreizējs lietotājs un izmantojat uzņēmuma e-pasta adresi, lai nodrošinātu uzņēmumam pakalpojumu vidi</span><span class="sxs-lookup"><span data-stu-id="4a949-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="4a949-122">**Pieteikties**, ja iepriekš esat pierakstījies pakalpojumam un vēlaties piekļūt savas organizācijas videi</span><span class="sxs-lookup"><span data-stu-id="4a949-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="4a949-123">Reģionālā pieejamība</span><span class="sxs-lookup"><span data-stu-id="4a949-123">Regional availability</span></span>

<span data-ttu-id="4a949-124">RCS ir pieejams šādos reģionos:</span><span class="sxs-lookup"><span data-stu-id="4a949-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="4a949-125">ASV</span><span class="sxs-lookup"><span data-stu-id="4a949-125">United States</span></span>
- <span data-ttu-id="4a949-126">Indija</span><span class="sxs-lookup"><span data-stu-id="4a949-126">India</span></span>
- <span data-ttu-id="4a949-127">Francija</span><span class="sxs-lookup"><span data-stu-id="4a949-127">France</span></span>
- <span data-ttu-id="4a949-128">Eiropa</span><span class="sxs-lookup"><span data-stu-id="4a949-128">Europe</span></span>

<span data-ttu-id="4a949-129">Pilnīgu reģionu sarakstu skatiet [Dynamics 365 un Power Platform: pieejamība, datu atrašanās vieta, valoda un lokalizācija](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="4a949-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="rcs-default-company"></a><span data-ttu-id="4a949-130">RCS noklusējuma uzņēmums</span><span class="sxs-lookup"><span data-stu-id="4a949-130">RCS default company</span></span>

<span data-ttu-id="4a949-131">Noformēšanas laika funkcionalitāte, kas tiek izmantota RCS, tiek koplietota visos uzņēmumos.</span><span class="sxs-lookup"><span data-stu-id="4a949-131">Design time functionality that is used in RCS is shared across all companies.</span></span> <span data-ttu-id="4a949-132">Nav uzņēmumam raksturīgu funkcionalitāšu.</span><span class="sxs-lookup"><span data-stu-id="4a949-132">There is no company-specific functionality.</span></span> <span data-ttu-id="4a949-133">Tāpēc ieteicams izmantot vienu uzņēmumu, **DAT** ar savu RCS vidi.</span><span class="sxs-lookup"><span data-stu-id="4a949-133">Therefore, we recommend that you use one company, **DAT**, with your RCS environment.</span></span>

<span data-ttu-id="4a949-134">Tomēr dažos scenārijos, iespējams, vēlēsities izveidot ER formātus, izmantojot parametrus, kas saistīti ar noteiktu juridisku personu.</span><span class="sxs-lookup"><span data-stu-id="4a949-134">However, in some scenarios, you might want to make ER formats use parameters that are related to a specific legal entity.</span></span> <span data-ttu-id="4a949-135">Tikai šajos scenārijos ir jāizmanto noklusējuma uzņēmuma pārslēdzējs.</span><span class="sxs-lookup"><span data-stu-id="4a949-135">In these scenarios only, you should use the default company switcher.</span></span> <span data-ttu-id="4a949-136">Piemēru skatiet sadaļā [Elektronisko pārskatu formātu konfigurēšana, lai izmantotu parametrus, kas norādīti juridiskajai personai](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="4a949-136">For an example, see [Configure ER format to use parameters that are specified per legal entity](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="4a949-137">Saistītā RCS dokumentācija</span><span class="sxs-lookup"><span data-stu-id="4a949-137">Related RCS documentation</span></span>

<span data-ttu-id="4a949-138">Papildinformāciju par saistītiem komponentiem skatiet tālāk norādītajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="4a949-138">For more information about related components, see the following topics:</span></span>

- <span data-ttu-id="4a949-139">**RCS:**</span><span class="sxs-lookup"><span data-stu-id="4a949-139">**RCS:**</span></span>

    - [<span data-ttu-id="4a949-140">Elektronisko pārskatu konfigurāciju izveide pakalpojumā RCS un to augšupielāde globālajā repozitorijā</span><span class="sxs-lookup"><span data-stu-id="4a949-140">Create ER configurations in RCS and upload them to the Global repository</span></span>](rcs-global-repo-upload.md)

- <span data-ttu-id="4a949-141">**Globālais repozitorijs:**</span><span class="sxs-lookup"><span data-stu-id="4a949-141">**Global repository:**</span></span>

    - [<span data-ttu-id="4a949-142">Izveidot ER konfigurāciju & augšupielādēt globālajā repozitorijā</span><span class="sxs-lookup"><span data-stu-id="4a949-142">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="4a949-143">Kopīgot konfigurāciju globālajā repozitorijā</span><span class="sxs-lookup"><span data-stu-id="4a949-143">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="4a949-144">Uzlabota filtrēšana globālajā repozitorijā</span><span class="sxs-lookup"><span data-stu-id="4a949-144">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="4a949-145">Elektronisko pārskatu konfigurāciju lejupielāde no globālā repozitorija</span><span class="sxs-lookup"><span data-stu-id="4a949-145">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="4a949-146">Pārtraukt konfigurācijas globālajā repozitorijā</span><span class="sxs-lookup"><span data-stu-id="4a949-146">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)
    - [<span data-ttu-id="4a949-147">Regulatory Configuration Service (RCS) — Lifecycle Services (LCS) krātuves nolietojums</span><span class="sxs-lookup"><span data-stu-id="4a949-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation</span></span>](rcs-lcs-repo-dep-faq.md)

- <span data-ttu-id="4a949-148">**Globalizācijas līdzeklis:**</span><span class="sxs-lookup"><span data-stu-id="4a949-148">**Globalization feature:**</span></span>

    - [<span data-ttu-id="4a949-149">Regulatory Configuration Service (RCS) — globalizācijas līdzeklis</span><span class="sxs-lookup"><span data-stu-id="4a949-149">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a><span data-ttu-id="4a949-150">RCS reģistrēšanās problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="4a949-150">Troubleshooting RCS sign-up</span></span>

<span data-ttu-id="4a949-151">Pierakstoties RCS no pakalpojuma lapas, varat saskarties ar problēmu, kas ir saistīta ar Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="4a949-151">When you sign up for RCS from the service page, you might encounter an issue that is related to Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="4a949-152">Saņemtais kļūdas ziņojums norāda, ka pierakstīšanās RCS pašlaik ir izslēgta un tā ir jāieslēdz pirms pierakstīšanās procesa pabeigšanas.</span><span class="sxs-lookup"><span data-stu-id="4a949-152">The error message that you receive indicates that sign-up for RCS is currently turned off and must be turned on before you can complete the sign-up process.</span></span>

![RCS pierakstīšanās procesa kļūdas ziņojums](media/01_RCSSignUpError.jpg)

<span data-ttu-id="4a949-154">Problēma rodas, jo esat bloķēts pierakstīties ekspromta abonementiem, un šim `AllowAdHocSubscriptions` rekvizītam ir jābūt iespējotam nomniekā.</span><span class="sxs-lookup"><span data-stu-id="4a949-154">The issue occurs because you're blocked from signing up for ad-hoc subscriptions, and the `AllowAdHocSubscriptions` property must be enabled in your tenant.</span></span> 

- <span data-ttu-id="4a949-155">Ja IT nodaļa pārvalda jūsu organizācijas Azure nomniekus, sazinieties ar šo nodaļu, lai ziņotu par problēmu.</span><span class="sxs-lookup"><span data-stu-id="4a949-155">If your IT department manages your organization's Azure tenants, contact that department to report the issue.</span></span>
- <span data-ttu-id="4a949-156">Ja pats esat atbildīgs par Azure nomnieku pārvaldību, tad varat novērst problēmas, izpildot darbības, kas norādītas sadaļā [Kas ir patstāvīgi izmantojama pierakstīšanās Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span><span class="sxs-lookup"><span data-stu-id="4a949-156">If you're responsible for managing your Azure tenants, you can fix the issues by following the steps in [What is self-service sign-up for Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span></span>
