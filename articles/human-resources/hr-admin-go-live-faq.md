---
title: Bieži uzdotie jautājumi par palaišanu
description: Šajā tēmā uzskaitīti bieži uzdotie jautājumi par to, kā sākt strādāt ar Dynamics 365 Human Resources ieviešanas projektu.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1b4b336953ef6bd74da009b3bb44fbcf2eab5a8
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892327"
---
# <a name="go-live-faq"></a><span data-ttu-id="08ad7-103">Bieži uzdotie jautājumi par palaišanu</span><span class="sxs-lookup"><span data-stu-id="08ad7-103">Go-live FAQ</span></span> 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="08ad7-104">Šajā tēmā uzskaitīti bieži uzdotie jautājumi par to, kā sākt strādāt ar Dynamics 365 Human Resources ieviešanas projektu.</span><span class="sxs-lookup"><span data-stu-id="08ad7-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="08ad7-105">Kad varu konfigurēt un pieprasīt savu ražošanas vidi?</span><span class="sxs-lookup"><span data-stu-id="08ad7-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="08ad7-106">Parasti ražošanas vide tiek izvietota, ja ir ievērota atbilstība tālāk minētajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="08ad7-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="08ad7-107">Visi pielāgojumi ir ar kodu pabeigti.</span><span class="sxs-lookup"><span data-stu-id="08ad7-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="08ad7-108">Lietotāju akceptēšanas testēšana (UAT) ir pabeigta.</span><span class="sxs-lookup"><span data-stu-id="08ad7-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="08ad7-109">Debitors ir parakstījis risinājumu.</span><span class="sxs-lookup"><span data-stu-id="08ad7-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="08ad7-110">Nav bloķējošu problēmu darba sākšanai.</span><span class="sxs-lookup"><span data-stu-id="08ad7-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="08ad7-111">Kad kvalificētie debitori ir šajā posmā, Microsoft FastTrack darba grupa strādās ar projekta grupu, lai veiktu darba sākšanas novērtējumu.</span><span class="sxs-lookup"><span data-stu-id="08ad7-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="08ad7-112">Kādi ir priekšnosacījumi ražošanas vides izvietošanai?</span><span class="sxs-lookup"><span data-stu-id="08ad7-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="08ad7-113">Priekšnosacījumu sarakstu skatiet tēmā [Sagatavošanās darba sākšanai](hr-admin-go-live-prepare.md).</span><span class="sxs-lookup"><span data-stu-id="08ad7-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="08ad7-114">Kas ir darba sākšanas novērtējums?</span><span class="sxs-lookup"><span data-stu-id="08ad7-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="08ad7-115">Darba sākšanas novērtējums ir daļa no [Microsoft FastTrack programmas](/dynamics365/fasttrack/).</span><span class="sxs-lookup"><span data-stu-id="08ad7-115">The go-live assessment is part of the [Microsoft FastTrack program](/dynamics365/fasttrack/).</span></span> <span data-ttu-id="08ad7-116">Šīs pārskatīšanas laikā risinājuma arhitekts izvērtē, vai ieviešanas projekts ir gatavs veiksmīgai pārslēgšanai un darba sākšanai.</span><span class="sxs-lookup"><span data-stu-id="08ad7-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="08ad7-117">Šī pārskatīšana ir obligāta katram ieviešanas projektam, pirms varat pieprasīt sākt darbu ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="08ad7-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="08ad7-118">Mūsu smilškastes vides ir izvietotas centrālajā ASV datu centrā.</span><span class="sxs-lookup"><span data-stu-id="08ad7-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="08ad7-119">Mēs vēlamies, lai mūsu ražošanas vides tiktu izvietotas ASV Rietumu datu centros.</span><span class="sxs-lookup"><span data-stu-id="08ad7-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="08ad7-120">Vai es varu atlasīt ASV Rietumus kā datu centru savā ražošanas konfigurācijā?</span><span class="sxs-lookup"><span data-stu-id="08ad7-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="08ad7-121">LCS neierobežo iespēju atlasīt citu datu centru, kad izvietojat Human Resources vidi, bet mēs stingri iesakām neizvēlēties citu datu centru.</span><span class="sxs-lookup"><span data-stu-id="08ad7-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="08ad7-122">Ja vēlaties, lai jūsu ražošanas vide būtu ASV Rietumu datu centrs, vispirms atkārtoti izvietojiet savas smilšu vides ASV Rietumu datu centrā, pārbaudiet tās un izrakstieties.</span><span class="sxs-lookup"><span data-stu-id="08ad7-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="08ad7-123">Informāciju par pareizā datu centra atlasīšanu skatiet tēmā [Tīkla prasības](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements).</span><span class="sxs-lookup"><span data-stu-id="08ad7-123">For information about selecting the correct datacenter, see [Network requirements](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="08ad7-124">Kāda līmeņa piekļuve man ir Azure resursiem manās Human Resources vidēs?</span><span class="sxs-lookup"><span data-stu-id="08ad7-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="08ad7-125">Piekļuve Human Resources vidēm ir ierobežota.</span><span class="sxs-lookup"><span data-stu-id="08ad7-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="08ad7-126">Jūs nevarat piekļūt virtuālajai mašīnai (VM) vai Microsoft interneta informācijas pakalpojumiem (IIS).</span><span class="sxs-lookup"><span data-stu-id="08ad7-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="08ad7-127">Jūs arī nevarat piekļūt datu bāzei, izmantojot Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="08ad7-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="08ad7-128">Lai gan nevarat piekļūt saviem Azure resursiem vai Dynamics 365 Human Resources videi tieši, ir papildu līdzekļi, ko varat izmantot, lai piekļūtu saviem datiem:</span><span class="sxs-lookup"><span data-stu-id="08ad7-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="08ad7-129">Azure SQL datu bāzi varat izvietot savā Azure nomniekā un izmantot līdzekli Savas datu bāzes izmantošana (BYOD), lai sinhronizētu datus.</span><span class="sxs-lookup"><span data-stu-id="08ad7-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="08ad7-130">Plašāku informāciju skatiet tēmā [Savas datu bāzes izmantošana (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span><span class="sxs-lookup"><span data-stu-id="08ad7-130">For more information, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span></span>

- <span data-ttu-id="08ad7-131">Varat izmantot Dataverse integrāciju, lai sinhronizētu atlases elementus Dataverse datu bāzē.</span><span class="sxs-lookup"><span data-stu-id="08ad7-131">You can use Dataverse integration to synchronize select entities into the Dataverse database.</span></span> <span data-ttu-id="08ad7-132">Papildinformāciju skatiet šeit: [Dataverse tabulas](hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="08ad7-132">For more information, see [Dataverse tables](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="08ad7-133">Cik bieži mana ražošanas datu bāze tiek dublēta?</span><span class="sxs-lookup"><span data-stu-id="08ad7-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="08ad7-134">Datu bāzes tiek aizsargātas ar automātisko dublēšanu šādā biežumā:</span><span class="sxs-lookup"><span data-stu-id="08ad7-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="08ad7-135">Dublējuma veids</span><span class="sxs-lookup"><span data-stu-id="08ad7-135">Type of backup</span></span> | <span data-ttu-id="08ad7-136">Biežums</span><span class="sxs-lookup"><span data-stu-id="08ad7-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="08ad7-137">Pilna datu bāzes dublēšana</span><span class="sxs-lookup"><span data-stu-id="08ad7-137">Full database backup</span></span> | <span data-ttu-id="08ad7-138">Reizi nedēļā</span><span class="sxs-lookup"><span data-stu-id="08ad7-138">Weekly</span></span> |
| <span data-ttu-id="08ad7-139">Diferenciālā datu bāzes dublēšana</span><span class="sxs-lookup"><span data-stu-id="08ad7-139">Differential database backup</span></span> | <span data-ttu-id="08ad7-140">Ik pēc 12-24 stundām</span><span class="sxs-lookup"><span data-stu-id="08ad7-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="08ad7-141">Darījumu žurnāla dublēšana</span><span class="sxs-lookup"><span data-stu-id="08ad7-141">Transaction log backup</span></span> | <span data-ttu-id="08ad7-142">Ik pēc 5–10 minūtēm</span><span class="sxs-lookup"><span data-stu-id="08ad7-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="08ad7-143">Microsoft saglabā pietiekamu dublēšanu, lai nodrošinātu punkta laikā atjaunošanu (PITR) pēdējo 14 dienu laikā.</span><span class="sxs-lookup"><span data-stu-id="08ad7-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last 14 days.</span></span> 

<span data-ttu-id="08ad7-144">Plašāku informāciju skatiet [Uzzināt par automātisko SQL datu bāzu dublēšanu](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span><span class="sxs-lookup"><span data-stu-id="08ad7-144">For more information, see [Learn about automatic SQL Database backups](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="08ad7-145">Vai varu pieprasīt manas ražošanas datu bāzes dublējuma kopiju?</span><span class="sxs-lookup"><span data-stu-id="08ad7-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="08ad7-146">Nr.p.k.</span><span class="sxs-lookup"><span data-stu-id="08ad7-146">No.</span></span> <span data-ttu-id="08ad7-147">Tomēr varat iesniegt datu bāzes atsvaidzināšanas pakalpojuma pieprasījumu, lai iekopētu ražošanas vidi savā smilškastes vidē.</span><span class="sxs-lookup"><span data-stu-id="08ad7-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="08ad7-148">Azure SQL datu bāzi varat izvietot savā Azure nomniekā un izmantot līdzekli BYOD, lai sinhronizētu datus no savas ražošanas vides.</span><span class="sxs-lookup"><span data-stu-id="08ad7-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="08ad7-149">Plašāku informāciju skatiet tēmā [Savas datu bāzes izmantošana (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span><span class="sxs-lookup"><span data-stu-id="08ad7-149">For more information, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="08ad7-150">Kā es varu pārvietot savu smilškastes vidi uz ražošanu darba sākšanai?</span><span class="sxs-lookup"><span data-stu-id="08ad7-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="08ad7-151">Tā kā kopēšanas līdzeklis nav pieejams, lai pārvietotu vidi no smilškastes uz ražošanas vidi, jums jāizmanto datu pakotnes, lai pārvietotu datus uz ražošanas vidi.</span><span class="sxs-lookup"><span data-stu-id="08ad7-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="08ad7-152">Mēs iesakām uzturēt skaidru to elementu sarakstu, kas konfigurēti jūsu smilškastē, visa projekta gaitā.</span><span class="sxs-lookup"><span data-stu-id="08ad7-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="08ad7-153">Pēc tam testējiet pārslēgšanas un migrācijas procesu visām datu pakotnēm, kas nepieciešamas jūsu darba sākšanai.</span><span class="sxs-lookup"><span data-stu-id="08ad7-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="08ad7-154">Jums ir manuāli jāpārvieto visas datu pakotnes ražošanas vidē, kad esat gatavs sākt darbu.</span><span class="sxs-lookup"><span data-stu-id="08ad7-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="08ad7-155">Ko darīt, ja mana ražošanas vide nedarbojas?</span><span class="sxs-lookup"><span data-stu-id="08ad7-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="08ad7-156">Lai ziņotu par ražošanas pārtraukumu, izpildiet procesu, kas aprakstīts tēmā [Ziņošana par ražošanas pārtraukumu](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md).</span><span class="sxs-lookup"><span data-stu-id="08ad7-156">To report a Production outage, follow the process described in [Report a production outage](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="08ad7-157">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="08ad7-157">See also</span></span>

 [<span data-ttu-id="08ad7-158">Sagatavošana publicēšanai</span><span class="sxs-lookup"><span data-stu-id="08ad7-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]