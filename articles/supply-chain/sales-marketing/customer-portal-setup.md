---
title: Debitoru portāla instalēšana, iestatīšana un atjaunināšana
description: Šajā tēmā ir sniegta informācija par licencēšanu un iestatīšanas instrukcijas Debitoru portālam.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e61fc5f7151a0bb61d496d47f4ad4e727a2a1d65
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529534"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="469b4-103">Debitoru portāla instalēšana, iestatīšana un atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="469b4-103">Install, set up, and update the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a><span data-ttu-id="469b4-104">Licencēšanas prasības</span><span class="sxs-lookup"><span data-stu-id="469b4-104">Licensing requirements</span></span>

<span data-ttu-id="469b4-105">Lai ieviestu Debitoru portālu, ir jābūt tālāk minētajām licencēm.</span><span class="sxs-lookup"><span data-stu-id="469b4-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="469b4-106">**Power Apps portāli** — šī licence ir nepieciešama, lai viesotu Debitoru portālu.</span><span class="sxs-lookup"><span data-stu-id="469b4-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="469b4-107">Portāli tiek licencēti, pamatojoties uz lietojumu.</span><span class="sxs-lookup"><span data-stu-id="469b4-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="469b4-108">Plašāku informāciju skatiet [Power Apps portālu licencēšanas prasības](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span><span class="sxs-lookup"><span data-stu-id="469b4-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="469b4-109">**Duālais ieraksts** — jums ir jābūt nepieciešamajām licencēm, lai iespējotu duālo ierakstu Supply Chain Management entītijām.</span><span class="sxs-lookup"><span data-stu-id="469b4-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management entities.</span></span> <span data-ttu-id="469b4-110">Plašāku informāciju skatiet [duālā ieraksta sistēmas prasības](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span><span class="sxs-lookup"><span data-stu-id="469b4-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="469b4-111">Atkarības no duālā ieraksta un Power Apps portāli</span><span class="sxs-lookup"><span data-stu-id="469b4-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="469b4-112">Debitoru portāls ir atkarīgs no Power Apps portāliem un duālā ieraksta, kā parādīts attēlā zemāk.</span><span class="sxs-lookup"><span data-stu-id="469b4-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

<span data-ttu-id="469b4-113">![Debitoru portāla atkarības](media/customer-portal-elements.png "Debitoru portāla atkarības")</span><span class="sxs-lookup"><span data-stu-id="469b4-113">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="469b4-114">Atšķirībā no citiem Supply Chain Management līdzekļiem, Debitoru portāla veidne atrodas Power Apps portālos.</span><span class="sxs-lookup"><span data-stu-id="469b4-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="469b4-115">Tāpēc Debitoru portālu ierobežo funkcionalitāte un iespējas, ko sniedz Power Apps portāli un entītijas duālajā ierakstā.</span><span class="sxs-lookup"><span data-stu-id="469b4-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the entities in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="469b4-116">Nepieciešamais iestatījums Debitoru portāla iespējošanai</span><span class="sxs-lookup"><span data-stu-id="469b4-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="469b4-117">Kad esat pārliecinājies, ka jums ir nepieciešamās licences, varat iestatīt duālo ierakstu, kā aprakstīts [duālā ieraksta sākotnējās sinhronizācijas instrukcijas](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="469b4-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="469b4-118">Duālajā ierakstā noteikti iespējojiet tālāk minēto elementu kartējumus.</span><span class="sxs-lookup"><span data-stu-id="469b4-118">Be sure to enable the following entity mappings in dual-write:</span></span>

- <span data-ttu-id="469b4-119">Pārdošanas pasūtījuma virsraksts</span><span class="sxs-lookup"><span data-stu-id="469b4-119">Sales Order Header</span></span>
- <span data-ttu-id="469b4-120">Pārdošanas pasūtījumu informācija</span><span class="sxs-lookup"><span data-stu-id="469b4-120">Sales Order Details</span></span>
- <span data-ttu-id="469b4-121">Konti</span><span class="sxs-lookup"><span data-stu-id="469b4-121">Accounts</span></span>
- <span data-ttu-id="469b4-122">Kontaktpersonas</span><span class="sxs-lookup"><span data-stu-id="469b4-122">Contacts</span></span>
- <span data-ttu-id="469b4-123">Preces</span><span class="sxs-lookup"><span data-stu-id="469b4-123">Products</span></span>

<span data-ttu-id="469b4-124">Kad iestatīšana ir pabeigta, varat nodrošināt Debitoru portāla veidni.</span><span class="sxs-lookup"><span data-stu-id="469b4-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="469b4-125">Debitoru portāla nodrošinājums</span><span class="sxs-lookup"><span data-stu-id="469b4-125">Provision the Customer portal</span></span>

<span data-ttu-id="469b4-126">Pirms sākat, pārliecinieties, ka esat jau pabeidzis [nepieciešamo iestatīšanu](#required-setup).</span><span class="sxs-lookup"><span data-stu-id="469b4-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="469b4-127">Pēc tam veiciet tālāk minētās darbības, lai nodrošinātu Debitoru portālu.</span><span class="sxs-lookup"><span data-stu-id="469b4-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="469b4-128">Dodieties uz [make.powerapps.com](https://make.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="469b4-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="469b4-129">Pārliecinieties, ka izmantojat vidi, kurā iespējojāt duālo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="469b4-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="469b4-130">Cilnē **Izveidot** ritiniet uz leju līdz sadaļai **Sākt no veidnes** un atlasiet veidni ar nosaukumu **Debitoru portāls**.</span><span class="sxs-lookup"><span data-stu-id="469b4-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Customer Portal**.</span></span>
4. <span data-ttu-id="469b4-131">Izpildiet ekrānā redzamos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="469b4-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="469b4-132">Kad nodrošinājums ir pabeigts, varat piekļūt Debitoru portālam lapas **Sākums** sadaļā **Jūsu programmas**.</span><span class="sxs-lookup"><span data-stu-id="469b4-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="469b4-133">Ja duālā ieraksta risinājums nav instalēts vidē, kurā strādājat, tiks parādīts kļūdas ziņojums, un Debitoru portāls netiks nodrošināts.</span><span class="sxs-lookup"><span data-stu-id="469b4-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="469b4-134">Debitoru portāla atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="469b4-134">Update the Customer portal</span></span>

<span data-ttu-id="469b4-135">Papildu funkcionalitāti Debitoru portālam var pievienot vēlāk.</span><span class="sxs-lookup"><span data-stu-id="469b4-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="469b4-136">Visas izmaiņas, ko korporācija Microsoft veic pamata risinājuma komponentiem, automātiski parādīsies jūsu vidē.</span><span class="sxs-lookup"><span data-stu-id="469b4-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="469b4-137">Tomēr tīmekļa vietne, kas tiek nodrošināta jūsu vidē, automātiski neatspoguļos izmaiņas, kas veiktas konfigurācijas datos.</span><span class="sxs-lookup"><span data-stu-id="469b4-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="469b4-138">Jums būs manuāli jāpiemēro šīs izmaiņas, iegūstot kodu no jaunās veidnes un apvienojot to ar nodrošināto tīmekļa vietni.</span><span class="sxs-lookup"><span data-stu-id="469b4-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="469b4-139">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="469b4-139">Additional resources</span></span>

<span data-ttu-id="469b4-140">Lai uzzinātu, kā var iestatīt un pielāgot Debitoru portālu, jāsāk ar sekojošās pamattehnoloģiju dokumentācijas pārskatīšanu.</span><span class="sxs-lookup"><span data-stu-id="469b4-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="469b4-141">Power Apps portālu dokumentācija</span><span class="sxs-lookup"><span data-stu-id="469b4-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="469b4-142">Duālā ieraksta dokumentācija</span><span class="sxs-lookup"><span data-stu-id="469b4-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="469b4-143">Lai efektīvi pārvaldītu portālus, ir jāizprot Power Apps portāli un Common Data Service dzīves cikls.</span><span class="sxs-lookup"><span data-stu-id="469b4-143">To effectively manage your portals, you must understand the Power Apps portals and Common Data Service lifecycle.</span></span> <span data-ttu-id="469b4-144">Papildinformāciju skatiet tālāk norādītajos resursos.</span><span class="sxs-lookup"><span data-stu-id="469b4-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="469b4-145">Par portāla dzīves ciklu</span><span class="sxs-lookup"><span data-stu-id="469b4-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="469b4-146">Portāla jaunināšana</span><span class="sxs-lookup"><span data-stu-id="469b4-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="469b4-147">Portāla konfigurācijas migrācija</span><span class="sxs-lookup"><span data-stu-id="469b4-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="469b4-148">Risinājuma dzīves cikla pārvaldība: programma Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="469b4-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)
