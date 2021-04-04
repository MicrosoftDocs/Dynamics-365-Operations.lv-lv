---
title: Elektroniskās rēķinu izrakstīšanas pievienojumprogrammas administrēšanas komponenti
description: Šajā tēmā sniegta informācija par komponentiem, kas ir saistīti ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammas administrēšanu.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592578"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="17264-103">Elektroniskās rēķinu izrakstīšanas pievienojumprogrammas administrēšanas komponenti</span><span class="sxs-lookup"><span data-stu-id="17264-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="17264-104">Šajā tēmā sniegta informācija par komponentiem, kas ir saistīti ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammas administrēšanu.</span><span class="sxs-lookup"><span data-stu-id="17264-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="17264-105">Tā sniedz arī informāciju par elektronisko rēķinu izrakstīšanas pievienojumprogrammas pakalpojuma konfigurēšanu.</span><span class="sxs-lookup"><span data-stu-id="17264-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="17264-106">Azure</span><span class="sxs-lookup"><span data-stu-id="17264-106">Azure</span></span>

<span data-ttu-id="17264-107">Izmantojiet Microsoft Azure, lai izveidotu noslēpumus atslēgai, kas atrodas krātuves kontā.</span><span class="sxs-lookup"><span data-stu-id="17264-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="17264-108">Tad izmantojiet Elektronisko rēķinu izrakstīšanas pievienojumprogrammas konfigurācijas noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="17264-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="17264-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="17264-109">Lifecycle Services</span></span>

<span data-ttu-id="17264-110">Izmantojiet Microsoft Dynamics Lifecycle Services (LCS), lai iespējotu pievienojumprogrammu mikropakalpojumiem jūsu LCS izvietošanas projektam.</span><span class="sxs-lookup"><span data-stu-id="17264-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="17264-111">Mikropakalpojuma pievienojumprogrammas LCS instalācijai ir nepieciešama vismaz 2. pakāpes virtuālā mašīna.</span><span class="sxs-lookup"><span data-stu-id="17264-111">The installation of the microservice add-on in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="17264-112">Lai iegūtu vairāk informācijas par vides plānošanu, skatiet [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="17264-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="17264-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="17264-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="17264-114">Dynamics 365 Regulatory Configuration Services (RCS) ir interfeiss, ko izmanto, lai konfigurētu elektronisko rēķinu izrakstīšanas pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="17264-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="17264-115">Resursi, piemēram, vides un elektronisko rēķinu izrakstīšanas līdzekļi, tiek izveidoti, uzturēti un viesoti pakalpojumā RCS.</span><span class="sxs-lookup"><span data-stu-id="17264-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="17264-116">Kad resursi ir gatavi, tie tiek publicēti Elektronisko rēķinu izrakstīšanas pievienojumprogrammas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="17264-116">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="17264-117">Informāciju par RCS pierakstīšanos skatiet sadaļā [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="17264-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="17264-118">Papildinformāciju par RCS skatiet sadaļā [Regulatory Configuration Services (RCS) — Globalizācijas līdzekļi](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="17264-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="17264-119">Integrēšana ar elektroniskās rēķinu izveides pievienojumprogrammu</span><span class="sxs-lookup"><span data-stu-id="17264-119">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="17264-120">Pirms RCS izmantošanas Elektronisko rēķinu konfigurēšanai, jums jākonfigurē RCS, lai ļautu sazināties ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="17264-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="17264-121">Šī konfigurācija tiek pabeigta **Elektronisko pārskatu parametru** lapas **Elektronisko rēķinu izrakstīšanas pievienojumprogrammas** cilnē.</span><span class="sxs-lookup"><span data-stu-id="17264-121">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="17264-122">Pakalpojuma galapunkts</span><span class="sxs-lookup"><span data-stu-id="17264-122">Service endpoint</span></span>

<span data-ttu-id="17264-123">Elektronisko rēķinu izrakstīšanas pievienojumprogramma ir pieejama vairākās Azure datucentru ģeogrāfijās.</span><span class="sxs-lookup"><span data-stu-id="17264-123">The Electronic invoicing add-on is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="17264-124">Tabulā zemāk ir uzskaitīti pieejamības dati par reģionu.</span><span class="sxs-lookup"><span data-stu-id="17264-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="17264-125">Azure datacenter ģeogrāfija</span><span class="sxs-lookup"><span data-stu-id="17264-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="17264-126">ASV austrumi</span><span class="sxs-lookup"><span data-stu-id="17264-126">East US</span></span>                    |
| <span data-ttu-id="17264-127">ASV rietumi</span><span class="sxs-lookup"><span data-stu-id="17264-127">West US</span></span>                    |
| <span data-ttu-id="17264-128">Ziemeļeiropa</span><span class="sxs-lookup"><span data-stu-id="17264-128">North EU</span></span>                   |
| <span data-ttu-id="17264-129">Rietumeiropa</span><span class="sxs-lookup"><span data-stu-id="17264-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="17264-130">Pakalpojumu vides</span><span class="sxs-lookup"><span data-stu-id="17264-130">Service environments</span></span>

<span data-ttu-id="17264-131">Pakalpojumu vides ir loģiskie nodalījumi, kas izveidoti elektronisko rēķinu izrakstīšanas funkciju izpildes atbalstam Elektronisko rēķinu izrakstīšanas pievienojumprogrammai.</span><span class="sxs-lookup"><span data-stu-id="17264-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="17264-132">Drošības noslēpumi un digitālie sertifikāti, un vadība (tas ir, piekļuves atļaujas) ir jākonfigurē pakalpojuma vides līmenī.</span><span class="sxs-lookup"><span data-stu-id="17264-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="17264-133">Klienti var izveidot tik daudz pakalpojumu vides, cik nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="17264-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="17264-134">Visas klientu izveidojušās pakalpojumu vides ir neatkarīgas viena no otras.</span><span class="sxs-lookup"><span data-stu-id="17264-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="17264-135">Pakalpojuma vides ir jāizveido un jāuztur pakalpojumā RCS.</span><span class="sxs-lookup"><span data-stu-id="17264-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="17264-136">Kad pakalpojumu vides ir gatavas, tām jābūt publicētām Elektronisko rēķinu izrakstīšanas pievienojumprogrammā.</span><span class="sxs-lookup"><span data-stu-id="17264-136">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="17264-137">Vides statusa pakalpojums</span><span class="sxs-lookup"><span data-stu-id="17264-137">Service environment status</span></span>

<span data-ttu-id="17264-138">Pakalpojuma vides var pārvaldīt ar statusu.</span><span class="sxs-lookup"><span data-stu-id="17264-138">Service environments can be managed through status.</span></span> <span data-ttu-id="17264-139">Iespējamās opcijas ir šādas:</span><span class="sxs-lookup"><span data-stu-id="17264-139">The possible options are:</span></span>

- <span data-ttu-id="17264-140">**Nav publicēts** – vide ir izveidota, bet vēl nav publicēta.</span><span class="sxs-lookup"><span data-stu-id="17264-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="17264-141">**Publicēts** – vide ir publicēta Elektronisko rēķinu izrakstīšanas pievienojumprogrammā.</span><span class="sxs-lookup"><span data-stu-id="17264-141">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="17264-142">**Mainīts** – publicētās vides atribūti ir izmainīti, bet izmaiņas vēl nav publicētas.</span><span class="sxs-lookup"><span data-stu-id="17264-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="17264-143">Klienta noslēpumi</span><span class="sxs-lookup"><span data-stu-id="17264-143">Customer secrets</span></span>

<span data-ttu-id="17264-144">Elektronisko rēķinu izrakstīšanas pievienojumprogramma ir atbildīga par visu jūsu uzņēmuma datu glabāšanu Azure resursos, kas pieder jūsu uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="17264-144">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="17264-145">Lai nodrošinātu, ka pakalpojums darbojas pareizi un ka visiem biznesa datiem, kas ir nepieciešami un ko ģenerē Elektronisko rēķinu izrakstīšanas pievienojumprogramma, ir piekļuve tikai pievienojumprogrammai, ir jāizveido divi galvenie Azure resursi:</span><span class="sxs-lookup"><span data-stu-id="17264-145">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="17264-146">Azure krātuves konts (BLOB krātuve), kas glabās elektroniskos rēķinus</span><span class="sxs-lookup"><span data-stu-id="17264-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="17264-147">Azure atslēgu glabātuve, kur tiks glabāti sertifikāti un krātuves konta vienoto resursu identifikatoru (URI)</span><span class="sxs-lookup"><span data-stu-id="17264-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="17264-148">Īpašam galvenās akreditācijas datu glabātuvei un debitora krātuves kontam ir jābūt piešķirtiem tieši lietošanai ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="17264-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="17264-149">Papildinformāciju skatiet šeit: [Azure krātuves konta un galvenās glabātavas izveide](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="17264-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="17264-150">Lietotāji</span><span class="sxs-lookup"><span data-stu-id="17264-150">Users</span></span>

<span data-ttu-id="17264-151">Katrai pakalpojumu videi ir jāsaraksta tās lietotājam, kas var pievienoties no Dynamics 365 Finance un Dynamics 365 Supply Chain Management Elektronisko rēķinu izrakstīšanas pievienojumprogrammā.</span><span class="sxs-lookup"><span data-stu-id="17264-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="17264-152">Publicēšana</span><span class="sxs-lookup"><span data-stu-id="17264-152">Publication</span></span>

<span data-ttu-id="17264-153">Pakalpojumu vidēm ir jābūt publicētām Elektronisko rēķinu izrakstīšanas pievienojumprogrammā pirms to izmantošanas.</span><span class="sxs-lookup"><span data-stu-id="17264-153">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="17264-154">Finance un Supply Chain Management var piekļūt tikai publicētām vidēm.</span><span class="sxs-lookup"><span data-stu-id="17264-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="17264-155">Turklāt pakalpojumu vide ir jāpublicē pirms jebkādu tās atribūtu atjauninājumiem, kas stājas spēkā elektronisko rēķinu izrakstīšanas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="17264-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="17264-156">Savienotās programmas</span><span class="sxs-lookup"><span data-stu-id="17264-156">Connected applications</span></span>

<span data-ttu-id="17264-157">Saistītās programmas ir Finance un Supply Chain Management instances, kuras, iespējams, vēlēsities sasniegt, izmantojot RCS.</span><span class="sxs-lookup"><span data-stu-id="17264-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="17264-158">Papildus programmas URL un tās nomniekam savienotā programma ietver akreditācijas datus, kas ļauj RCS izveidot savienojumu ar vidi.</span><span class="sxs-lookup"><span data-stu-id="17264-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="17264-159">Izmantojot savienotās programmas, varat konfigurēt daļu no elektronisko rēķinu izrakstīšanas funkcijas Finance un Supply Chain Management, lai izveidotu visu elektronisko rēķinu izrakstīšanas funkcijas darbu.</span><span class="sxs-lookup"><span data-stu-id="17264-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="17264-160">Finance un Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="17264-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="17264-161">Integrēšana ar elektroniskās rēķinu izveides pievienojumprogrammu</span><span class="sxs-lookup"><span data-stu-id="17264-161">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="17264-162">Pirms Finance un Supply Chain Management izmantošanas, lai izsniegtu elektroniskos rēķinus ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammas palīdzību, pievienojumprogramma ir jākonfigurē, lai ļautu sazināties ar pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="17264-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="17264-163">Elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšanas līdzeklis</span><span class="sxs-lookup"><span data-stu-id="17264-163">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="17264-164">Lai iespējotu komunikāciju starp Finance un Supply Chain Management, un elektronisko rēķinu izrakstīšanas pievienojumprogrammu, jums jāieslēdz **Elektronisko rēķinu izrakstīšanas pievienojumprogrammas integrēšanas** līdzeklis **Līdzekļa pārvaldības** darbvietā.</span><span class="sxs-lookup"><span data-stu-id="17264-164">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="17264-165">Pakalpojuma galapunkts</span><span class="sxs-lookup"><span data-stu-id="17264-165">Service endpoint</span></span>

<span data-ttu-id="17264-166">Pakalpojuma galapunkts ir URL, kur atrodas Elektronisko rēķinu izrakstīšanas pievienojumprogramma.</span><span class="sxs-lookup"><span data-stu-id="17264-166">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="17264-167">Pirms var tikt izdoti elektroniskie rēķini, pakalpojuma galapunktam jābūt konfigurētam pakalpojumos Finance un Supply Chain Management, lai ļautu sazināties ar pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="17264-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="17264-168">Lai konfigurētu pakalpojuma galapunktu, dodieties uz **Organizācijas administrēšana \> Iestatīšana \> Elektronisko dokumentu parametrs** un pēc tam cilnes **Iesniegšanas pakalpojumi** laukā **Elektronisko rēķinu izrakstīšanas pievienojumprogrammas URL** ievadiet URL kā aprakstīts sadaļas **Pakalpojuma galapunkts** tabulā.</span><span class="sxs-lookup"><span data-stu-id="17264-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="17264-169">Vides</span><span class="sxs-lookup"><span data-stu-id="17264-169">Environments</span></span>

<span data-ttu-id="17264-170">Vides nosaukums, kas ir ievadīts pakalpojumos Finance un Supply Chain Management, attiecas uz vides nosaukumu, kas ir izveidots pakalpojumā RCS un publicēts Elektronisko rēķinu izrakstīšanas pievienojumprogrammā.</span><span class="sxs-lookup"><span data-stu-id="17264-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="17264-171">Vide ir jākonfigurē **Iesniegšanas pakalpojumi** cilnes **Elektronisko dokumentu parametra** lapā, lai katrā elektronisko rēķinu izsniegšanas pieprasījumā būtu vide, kur elektronisko rēķinu izrakstīšanas pievienojumprogramma var noteikt, kurai elektronisko rēķinu izrakstīšanas funkcijai ir jāapstrādā pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="17264-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17264-172">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="17264-172">Additional resources</span></span>

- [<span data-ttu-id="17264-173">Konfigurēt elektroniskos rēķinus pakalpojumā RCS</span><span class="sxs-lookup"><span data-stu-id="17264-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="17264-174">Elektronisko rēķinu izdošana programmās Finance un Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="17264-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
