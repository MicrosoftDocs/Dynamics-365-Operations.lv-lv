---
title: Elektroniskās rēķinu izveides administrēšanas komponenti
description: Šajā tēmā sniegta informācija par komponentiem, kas ir saistīti ar Elektronisko rēķinu izrakstīšanas administrēšanu.
author: gionoder
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 081d23c85d3555210b54597920a49e800ffe284b
ms.sourcegitcommit: 35fdcc6501e099c54a58583b1e3aba16f02a5ccc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2021
ms.locfileid: "5980928"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="cafd1-103">Elektroniskās rēķinu izveides administrēšanas komponenti</span><span class="sxs-lookup"><span data-stu-id="cafd1-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="cafd1-104">Šajā tēmā sniegta informācija par komponentiem, kas ir saistīti ar Elektronisko rēķinu izrakstīšanas administrēšanu.</span><span class="sxs-lookup"><span data-stu-id="cafd1-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="cafd1-105">Tā sniedz arī informāciju par elektronisko rēķinu izrakstīšanas pakalpojuma konfigurēšanu.</span><span class="sxs-lookup"><span data-stu-id="cafd1-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="cafd1-106">Azure</span><span class="sxs-lookup"><span data-stu-id="cafd1-106">Azure</span></span>

<span data-ttu-id="cafd1-107">Izmantojiet Microsoft Azure, lai izveidotu noslēpumus Key Vault un krātuves kontam.</span><span class="sxs-lookup"><span data-stu-id="cafd1-107">Use Microsoft Azure to create the secrets for the Key Vault and storage account.</span></span> <span data-ttu-id="cafd1-108">Tad izmantojiet Elektronisko rēķinu izrakstīšanas konfigurācijas noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="cafd1-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="cafd1-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="cafd1-109">Lifecycle Services</span></span>

<span data-ttu-id="cafd1-110">Izmantojiet Microsoft Dynamics Lifecycle Services (LCS), lai iespējotu mikropakalpojumus jūsu LCS izvietošanas projektam.</span><span class="sxs-lookup"><span data-stu-id="cafd1-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="cafd1-111">Mikropakalpojuma LCS instalācijai ir nepieciešama vismaz 2. pakāpes virtuālā mašīna.</span><span class="sxs-lookup"><span data-stu-id="cafd1-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="cafd1-112">Lai iegūtu vairāk informācijas par vides plānošanu, skatiet [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="cafd1-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="cafd1-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="cafd1-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="cafd1-114">Dynamics 365 Regulatory Configuration Services (RCS) ir interfeiss, ko izmanto, lai konfigurētu elektronisko rēķinu izrakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="cafd1-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="cafd1-115">Resursi, piemēram, vides un elektronisko rēķinu izrakstīšanas līdzekļi, tiek izveidoti, uzturēti un viesoti pakalpojumā RCS.</span><span class="sxs-lookup"><span data-stu-id="cafd1-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="cafd1-116">Kad resursi ir gatavi, tie tiek publicēti Elektronisko rēķinu izrakstīšanas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="cafd1-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="cafd1-117">Informāciju par RCS pierakstīšanos skatiet sadaļā [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="cafd1-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="cafd1-118">Papildinformāciju par RCS skatiet sadaļā [Regulatory Configuration Services (RCS) — Globalizācijas līdzekļi](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="cafd1-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="cafd1-119">Integrēšana ar elektroniskās rēķinu izrakstīšanu</span><span class="sxs-lookup"><span data-stu-id="cafd1-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="cafd1-120">Pirms RCS izmantošanas Elektronisko rēķinu konfigurēšanai, jums jākonfigurē RCS, lai ļautu sazināties ar Elektronisko rēķinu izrakstīšanu.</span><span class="sxs-lookup"><span data-stu-id="cafd1-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="cafd1-121">Šī konfigurācija tiek pabeigta **Elektronisko pārskatu parametru** lapas **Elektronisko rēķinu izrakstīšanas** cilnē.</span><span class="sxs-lookup"><span data-stu-id="cafd1-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="cafd1-122">Pakalpojuma galapunkts</span><span class="sxs-lookup"><span data-stu-id="cafd1-122">Service endpoint</span></span>

<span data-ttu-id="cafd1-123">Elektronisko rēķinu izrakstīšana ir pieejama vairākās Azure datucentru ģeogrāfijās.</span><span class="sxs-lookup"><span data-stu-id="cafd1-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="cafd1-124">Tabulā zemāk ir uzskaitīti pieejamības dati par reģionu.</span><span class="sxs-lookup"><span data-stu-id="cafd1-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="cafd1-125">Azure datacenter ģeogrāfija</span><span class="sxs-lookup"><span data-stu-id="cafd1-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="cafd1-126">ASV</span><span class="sxs-lookup"><span data-stu-id="cafd1-126">United States</span></span>              |
| <span data-ttu-id="cafd1-127">Eiropa</span><span class="sxs-lookup"><span data-stu-id="cafd1-127">Europe</span></span>                     |
| <span data-ttu-id="cafd1-128">Apvienotā Karaliste</span><span class="sxs-lookup"><span data-stu-id="cafd1-128">United Kingdom</span></span>             |
| <span data-ttu-id="cafd1-129">Āzija</span><span class="sxs-lookup"><span data-stu-id="cafd1-129">Asia</span></span>                       |

### <a name="service-environments"></a><span data-ttu-id="cafd1-130">Pakalpojumu vides</span><span class="sxs-lookup"><span data-stu-id="cafd1-130">Service environments</span></span>

<span data-ttu-id="cafd1-131">Pakalpojumu vides ir loģiskie nodalījumi, kas izveidoti elektronisko rēķinu izrakstīšanas funkciju izpildes atbalstam Elektronisko rēķinu izrakstīšanai.</span><span class="sxs-lookup"><span data-stu-id="cafd1-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="cafd1-132">Drošības noslēpumi un digitālie sertifikāti, un vadība (tas ir, piekļuves atļaujas) ir jākonfigurē pakalpojuma vides līmenī.</span><span class="sxs-lookup"><span data-stu-id="cafd1-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="cafd1-133">Klienti var izveidot tik daudz pakalpojumu vides, cik nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="cafd1-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="cafd1-134">Visas klientu izveidojušās pakalpojumu vides ir neatkarīgas viena no otras.</span><span class="sxs-lookup"><span data-stu-id="cafd1-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="cafd1-135">Pakalpojuma vides ir jāizveido un jāuztur pakalpojumā RCS.</span><span class="sxs-lookup"><span data-stu-id="cafd1-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="cafd1-136">Kad pakalpojumu vides ir gatavas, tām jābūt publicētām Elektronisko rēķinu izrakstīšanā.</span><span class="sxs-lookup"><span data-stu-id="cafd1-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="cafd1-137">Vides statusa pakalpojums</span><span class="sxs-lookup"><span data-stu-id="cafd1-137">Service environment status</span></span>

<span data-ttu-id="cafd1-138">Pakalpojuma vides var pārvaldīt ar statusu.</span><span class="sxs-lookup"><span data-stu-id="cafd1-138">Service environments can be managed through status.</span></span> <span data-ttu-id="cafd1-139">Iespējamās opcijas ir šādas:</span><span class="sxs-lookup"><span data-stu-id="cafd1-139">The possible options are:</span></span>

- <span data-ttu-id="cafd1-140">**Nav publicēts** – vide ir izveidota, bet vēl nav publicēta.</span><span class="sxs-lookup"><span data-stu-id="cafd1-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="cafd1-141">**Publicēts** – vide ir publicēta Elektronisko rēķinu izrakstīšanā .</span><span class="sxs-lookup"><span data-stu-id="cafd1-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="cafd1-142">**Mainīts** – publicētās vides atribūti ir izmainīti, bet izmaiņas vēl nav publicētas.</span><span class="sxs-lookup"><span data-stu-id="cafd1-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="cafd1-143">Klienta noslēpumi</span><span class="sxs-lookup"><span data-stu-id="cafd1-143">Customer secrets</span></span>

<span data-ttu-id="cafd1-144">Elektronisko rēķinu izrakstīšana ir atbildīga par visu jūsu uzņēmuma datu glabāšanu Azure resursos, kas pieder jūsu uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="cafd1-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="cafd1-145">Lai nodrošinātu, ka pakalpojums darbojas pareizi un ka visiem biznesa datiem, kas ir nepieciešami un ko ģenerē Elektronisko rēķinu izrakstīšana, ir atbilstoši pieejami, ir jāizveido divi galvenie Azure resursi:</span><span class="sxs-lookup"><span data-stu-id="cafd1-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="cafd1-146">Azure krātuves konts (BLOB krātuve), kas glabās elektroniskos rēķinus</span><span class="sxs-lookup"><span data-stu-id="cafd1-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="cafd1-147">Azure Key Vault, kur tiks glabāti sertifikāti un krātuves konta vienoto resursu identifikatoru (URI)</span><span class="sxs-lookup"><span data-stu-id="cafd1-147">An Azure Key Vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>


<span data-ttu-id="cafd1-148">Īpašam Key Vault un debitora krātuves kontam ir jābūt piešķirtiem tieši lietošanai ar Elektronisko rēķinu izrakstīšanu .</span><span class="sxs-lookup"><span data-stu-id="cafd1-148">A dedicated Key Vault and customer storage account must be allocated specifically for use with Electronic Invoicing.</span></span> <span data-ttu-id="cafd1-149">Papildinformāciju skatiet šeit: [Azure krātuves konta un Key Vault izveide](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="cafd1-149">For more information, see [Create an Azure storage account and a Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

<span data-ttu-id="cafd1-150">Lai pārraudzītu savas Key Vault darbspēju un saņemtu brīdinājumus, konfigurējiet Azure Monitor pakalpojumam Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cafd1-150">To monitor the health of your Key Vault and receive alerts, configure the Azure Monitor for key Vault.</span></span> <span data-ttu-id="cafd1-151">Aktivizējot Key Vault reģistrāciju, var pārraudzīt, kad un kam ir piekļuve Key Vault.</span><span class="sxs-lookup"><span data-stu-id="cafd1-151">By enabling Key Vault logging, you can monitor how, when, and by whom your Key Vaults are accessed.</span></span> <span data-ttu-id="cafd1-152">Papildinformāciju skatiet [Azure Key Vault uzraudzība un brīdināšana](/azure/key-vault/general/alert) un [Kā iespējot Key Vault reģistrāciju](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span><span class="sxs-lookup"><span data-stu-id="cafd1-152">For more information, see [Monitoring and alerting for Azure Key Vault](/azure/key-vault/general/alert) and [How to enable Key Vault logging](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span></span>

<span data-ttu-id="cafd1-153">Kā labākā prakse - periodiski pagriezt noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="cafd1-153">As a best practice, periodically rotate the secrets.</span></span> <span data-ttu-id="cafd1-154">Papildinformāciju skatiet [Noslēpumu dokumentācijā](/azure/key-vault/secrets/).</span><span class="sxs-lookup"><span data-stu-id="cafd1-154">For more information, see [Secrets documentation](/azure/key-vault/secrets/).</span></span>

#### <a name="users"></a><span data-ttu-id="cafd1-155">Lietotāji</span><span class="sxs-lookup"><span data-stu-id="cafd1-155">Users</span></span>

<span data-ttu-id="cafd1-156">Katrai pakalpojumu videi ir jāsaraksta tās lietotājam, kas var pievienoties no Dynamics 365 Finance un Dynamics 365 Supply Chain Management Elektronisko rēķinu izrakstīšanā.</span><span class="sxs-lookup"><span data-stu-id="cafd1-156">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="cafd1-157">Publicēšana</span><span class="sxs-lookup"><span data-stu-id="cafd1-157">Publication</span></span>

<span data-ttu-id="cafd1-158">Pakalpojumu vidēm ir jābūt publicētām Elektronisko rēķinu izrakstīšanā pirms to izmantošanas.</span><span class="sxs-lookup"><span data-stu-id="cafd1-158">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="cafd1-159">Finance un Supply Chain Management var piekļūt tikai publicētām vidēm.</span><span class="sxs-lookup"><span data-stu-id="cafd1-159">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="cafd1-160">Turklāt pakalpojumu vide ir jāpublicē pirms jebkādu tās atribūtu atjauninājumiem, kas stājas spēkā elektronisko rēķinu izrakstīšanas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="cafd1-160">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="cafd1-161">Savienotās programmas</span><span class="sxs-lookup"><span data-stu-id="cafd1-161">Connected applications</span></span>

<span data-ttu-id="cafd1-162">Saistītās programmas ir Finance un Supply Chain Management instances, kuras, iespējams, vēlēsities sasniegt, izmantojot RCS.</span><span class="sxs-lookup"><span data-stu-id="cafd1-162">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="cafd1-163">Papildus programmas URL un tās nomniekam savienotā programma ietver akreditācijas datus, kas ļauj RCS izveidot savienojumu ar vidi.</span><span class="sxs-lookup"><span data-stu-id="cafd1-163">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="cafd1-164">Izmantojot savienotās programmas, varat konfigurēt daļu no elektronisko rēķinu izrakstīšanas funkcijas Finance un Supply Chain Management, lai izveidotu visu elektronisko rēķinu izrakstīšanas funkcijas darbu.</span><span class="sxs-lookup"><span data-stu-id="cafd1-164">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="cafd1-165">Finance un Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cafd1-165">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="cafd1-166">Integrēšana ar elektroniskās rēķinu izrakstīšanu</span><span class="sxs-lookup"><span data-stu-id="cafd1-166">Integration with Electronic invoicing</span></span>

<span data-ttu-id="cafd1-167">Pirms Finance un Supply Chain Management izmantošanas, lai izsniegtu elektroniskos rēķinus ar Elektronisko rēķinu izrakstīšanas palīdzību, tas ir jākonfigurē, lai ļautu sazināties ar pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="cafd1-167">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="cafd1-168">Elektronisko rēķinu izrakstīšanas integrēšanas līdzeklis</span><span class="sxs-lookup"><span data-stu-id="cafd1-168">Electronic invoicing integration feature</span></span>

<span data-ttu-id="cafd1-169">Lai iespējotu komunikāciju starp Finance un Supply Chain Management, un elektronisko rēķinu izrakstīšanu, jums jāieslēdz **Elektronisko rēķinu izrakstīšanas integrēšanas** līdzeklis **Līdzekļa pārvaldības** darbvietā.</span><span class="sxs-lookup"><span data-stu-id="cafd1-169">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="cafd1-170">Pakalpojuma galapunkts</span><span class="sxs-lookup"><span data-stu-id="cafd1-170">Service endpoint</span></span>

<span data-ttu-id="cafd1-171">Pakalpojuma galapunkts ir URL, kur atrodas Elektronisko rēķinu izrakstīšana.</span><span class="sxs-lookup"><span data-stu-id="cafd1-171">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="cafd1-172">Pirms var tikt izdoti elektroniskie rēķini, pakalpojuma galapunktam jābūt konfigurētam pakalpojumos Finance un Supply Chain Management, lai ļautu sazināties ar pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="cafd1-172">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="cafd1-173">Lai konfigurētu pakalpojuma galapunktu, dodieties uz **Organizācijas administrēšana \> Iestatīšana \> Elektronisko dokumentu parametrs** un pēc tam cilnes **Iesniegšanas pakalpojumi** laukā **Elektronisko rēķinu izrakstīšanas URL** ievadiet URL kā aprakstīts sadaļas **Pakalpojuma galapunkts** tabulā.</span><span class="sxs-lookup"><span data-stu-id="cafd1-173">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="cafd1-174">Vides</span><span class="sxs-lookup"><span data-stu-id="cafd1-174">Environments</span></span>

<span data-ttu-id="cafd1-175">Vides nosaukums, kas ir ievadīts pakalpojumos Finance un Supply Chain Management, attiecas uz vides nosaukumu, kas ir izveidots pakalpojumā RCS un publicēts Elektronisko rēķinu izrakstīšanā.</span><span class="sxs-lookup"><span data-stu-id="cafd1-175">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="cafd1-176">Vide ir jākonfigurē **Iesniegšanas pakalpojumi** cilnes **Elektronisko dokumentu parametra** lapā, lai katrā elektronisko rēķinu izsniegšanas pieprasījumā būtu vide, kur elektronisko rēķinu izrakstīšana var noteikt, kurai elektronisko rēķinu izrakstīšanas funkcijai ir jāapstrādā pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="cafd1-176">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cafd1-177">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="cafd1-177">Additional resources</span></span>

- [<span data-ttu-id="cafd1-178">Konfigurēt elektroniskos rēķinus pakalpojumā RCS</span><span class="sxs-lookup"><span data-stu-id="cafd1-178">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="cafd1-179">Elektronisko rēķinu izdošana programmās Finance un Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cafd1-179">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
