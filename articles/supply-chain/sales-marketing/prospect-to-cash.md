---
title: "No potenciālā klienta līdz skaidrai naudai"
description: "Šajā tēmā ir sniegts apskats par risinājumu No potenciālā klienta līdz skaidrai naudai programmās Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, un Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 02/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: 62f328c5a6bf5343c97de0b7d907bbcfe2fcde4d
ms.contentlocale: lv-lv
ms.lasthandoff: 02/23/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="473bd-103">No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="473bd-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="473bd-104">Risinājums “No potenciālā klienta līdz skaidrai naudai” nodrošina tiešu sinhronizēšanu starp programmu Dynamics 365 for Finance and Operations, Enterprise Edition, un programmu Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="473bd-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, Enterprise edition, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="473bd-105">Risinājuma No potenciālā klienta līdz skaidrai naudai veidnes, kas ir pieejamas ar līdzekli Datu integrācija, nodrošina ar kontiem, kontaktpersonām, precēm, pārdošanas piedāvājumiem, pārdošanas pasūtījumiem un pārdošanas rēķiniem saistīto datu plūsmu starp programmām Finance and Operations un Sales.</span><span class="sxs-lookup"><span data-stu-id="473bd-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="473bd-106">Kamēr notiek datu plūsma starp Finance and Operations un Sales, programmā Sales varat veikt pārdošanas un mārketinga aktivitātes, un varat tikt galā ar pasūtījuma izpildi, izmantojot krājumu vadību programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="473bd-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="473bd-107">Lai iegūtu papildinformāciju par integrāciju No potenciālā klienta līdz skaidrai naudai, noskatieties īso YouTube video:</span><span class="sxs-lookup"><span data-stu-id="473bd-107">For more information about the Prospect to cash integration, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

<span data-ttu-id="473bd-108">Pašreizējā versijā risinājums No potenciālā klienta līdz skaidrai naudai nodrošina tālāk aprakstītos tiešās sinhronizācijas tipus.</span><span class="sxs-lookup"><span data-stu-id="473bd-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="473bd-109">Kontu uzturēšana programmā Sales un to tieša sinhronizēšana ar programmu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="473bd-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="473bd-110">Preču uzturēšana programmā Finance and Operations un to tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="473bd-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="473bd-111">Kontaktpersonu uzturēšana programmā Sales un to tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="473bd-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="473bd-112">Programmā Sales ietverto pārdošanas piedāvājumu tieša sinhronizēšana ar programmu Finance and Operations (veidne, kas gaida izlaišanu)</span><span class="sxs-lookup"><span data-stu-id="473bd-112">Synchronize sales quotation directly from Sales to Finance and Operations (template pending release)</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="473bd-113">Pārdošanas pasūtījumu tieša sinhronizēšana no programmas Finance and Operations uz programmu Sales</span><span class="sxs-lookup"><span data-stu-id="473bd-113">Synchronize sales orders directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)
- [<span data-ttu-id="473bd-114">Pārdošanas pasūtījumu tieša sinhronizēšana no programmas Sales uz programmu Finance and Operations un otrādi (veidne, kas gaida izlaišanu)</span><span class="sxs-lookup"><span data-stu-id="473bd-114">Synchronize sales orders directly between Sales and Finance and Operations (template pending release)</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="473bd-115">Pārdošanas rēķina tieša sinhronizēšana no programmas Finance and Operations uz programmu Sales</span><span class="sxs-lookup"><span data-stu-id="473bd-115">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="473bd-116">Sistēmas prasības programmai Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="473bd-116">System requirements for Finance and Operations</span></span>

<span data-ttu-id="473bd-117">Integrācija No potenciālā klienta līdz skaidrai naudai tiek atbalstīta tālāk norādītajās versijās.</span><span class="sxs-lookup"><span data-stu-id="473bd-117">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="473bd-118">Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 (2017. gada decembris)</span><span class="sxs-lookup"><span data-stu-id="473bd-118">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="473bd-119">Dynamics 365 for Finance and Operations Enterprise Edition (2017. gada decembris) — programmas būvējums 7.3.11971.56116 ar 12. platformas atjauninājumu (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="473bd-119">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="473bd-120">Dynamics 365 for Finance and Operations, Enterprise Edition (2017. gada jūlijs)</span><span class="sxs-lookup"><span data-stu-id="473bd-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="473bd-121">Dynamics 365 for Finance and Operations Enterprise Edition (2017. jūlijs) — ar 8. platformas atjauninājumu (programmas būvējums 7.2.11792.56024 ar platformas būvējumu 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="473bd-121">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="473bd-122">Ir nepieciešami tālāk minētie labojumfaili.</span><span class="sxs-lookup"><span data-stu-id="473bd-122">The following hotfixes are required:</span></span>

    - <span data-ttu-id="473bd-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** — šis labojumfails ļauj veikt pārdošanas pasūtījumu sinhronizēšanu no Sales uz Finance and Operations, izmantojot līdzekli Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="473bd-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="473bd-124">Tas nodrošina arī vairākus citus uzlabojumus.</span><span class="sxs-lookup"><span data-stu-id="473bd-124">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="473bd-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** — šis labojumfails ļauj veikt pārdošanas pasūtījumu rindu sinhronizēšanu no Finance and Operations uz Sales, izmantojot līdzekli Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="473bd-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="473bd-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** — šis labojumfails ļauj veikt pārdošanas pasūtījumu sinhronizēšanu no Finance and Operations uz Sales, izmantojot līdzekli Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="473bd-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="473bd-127">Ir nepieciešams instalēt tikai labojumfailu KB4045570, jo tā instalācijā ir ietvertas citos labojumfailos ietvertās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="473bd-127">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="473bd-128">Dynamics 365 for Finance and Operations, versija 1611 (2016. gada novembris)</span><span class="sxs-lookup"><span data-stu-id="473bd-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="473bd-129">Dynamics 365 for Finance and Operations, versija 1611 (2016. gada novembris) ar platformas 8. atjauninājumu vai jaunāku</span><span class="sxs-lookup"><span data-stu-id="473bd-129">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="473bd-130">Ir nepieciešami tālāk minētie labojumfaili.</span><span class="sxs-lookup"><span data-stu-id="473bd-130">The following hotfixes are required:</span></span>

    - <span data-ttu-id="473bd-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** — ļauj veikt pārdošanas pasūtījumu sinhronizēšanu programmā Finance and Operations un programmā Sales, izmantojot datu integrētāju.</span><span class="sxs-lookup"><span data-stu-id="473bd-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
    - <span data-ttu-id="473bd-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** — ļauj veikt pārdošanas pasūtījumu virsrakstu un rindu sinhronizēšanu programmā Finance and Operations un programmā Sales, izmantojot datu integrētāju.</span><span class="sxs-lookup"><span data-stu-id="473bd-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
    - <span data-ttu-id="473bd-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** — ir nepieciešams atbalsts risinājuma “No potenciālā klienta līdz skaidrai naudai” integrēšanai datu elementos.</span><span class="sxs-lookup"><span data-stu-id="473bd-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="473bd-134">Pēc labojumfailu instalēšanas jums ir nepieciešams aktivizēt tālāk norādīto pakešuzdevumu no formas **SalesPopulateProspectToCash**.</span><span class="sxs-lookup"><span data-stu-id="473bd-134">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="473bd-135">Šī forma ir slēpta, jo jums tā ir nepieciešama tikai vienreiz.</span><span class="sxs-lookup"><span data-stu-id="473bd-135">This form is hidden because you only need it once.</span></span> <span data-ttu-id="473bd-136">Lai piekļūtu šai formai, piesakieties vidē un savā pārlūkprogrammas adresē pievienojiet šādu vietrādi URL: &mi=action:SalesPopulateProspectToCash, piemēram, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="473bd-136">To access the form, log in to the environment and add the following to the URL in your browser address: &mi=action:SalesPopulateProspectToCash, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="473bd-137">Kad forma tiek atvērta, noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="473bd-137">When the form opens, click OK.</span></span> <span data-ttu-id="473bd-138">Šādi tiek aizpildīts jauns lauks **LineCreationSequnceNumber** tabulās **SalesLine**, **SalesQuotationLine** un **CustInvoiceTrans**, izmantojot unikālas vērtības, un tiek atsvaidzināts preču saraksts.</span><span class="sxs-lookup"><span data-stu-id="473bd-138">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="473bd-139">Lai darbotos risinājuma “No potenciālā klienta līdz skaidrai naudai” integrēšana, šī procedūra ir jāizpilda obligāti.</span><span class="sxs-lookup"><span data-stu-id="473bd-139">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="473bd-140">Sistēmas prasības programmai Sales</span><span class="sxs-lookup"><span data-stu-id="473bd-140">System requirements for Sales</span></span>

<span data-ttu-id="473bd-141">Lai lietotu risinājumu No potenciālā klienta līdz skaidrai naudai, ir jābūt instalētiem tālāk uzskaitītajiem komponentiem.</span><span class="sxs-lookup"><span data-stu-id="473bd-141">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="473bd-142">Dynamics 365 for Sales versija 1612 (8.2.1.207) (DB 8.2.1.207), tiešsaistes versija</span><span class="sxs-lookup"><span data-stu-id="473bd-142">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online</span></span>
- <span data-ttu-id="473bd-143">Risinājums “No potenciālā klienta līdz skaidrai naudai” programmai Dynamics 365 for Sales, versija 1.15.0.0 (v15)</span><span class="sxs-lookup"><span data-stu-id="473bd-143">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="473bd-144">Instalēt risinājumu No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="473bd-144">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="473bd-145">Lejupielādējiet [Risinājuma No potenciālā klienta līdz skaidrai naudai programmai Dynamics 365 for Sales pakotnes zip failu](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) no vietnes CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="473bd-145">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="473bd-146">Pārliecinieties, vai .zip fails ir atbloķēts.</span><span class="sxs-lookup"><span data-stu-id="473bd-146">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="473bd-147">Pretējā gadījumā, kad mēģināt instalēt risinājuma pakotni, var tikt parādīts šāds kļūdas ziņojums: “Importēšanas pakotnes nav atrastas.”</span><span class="sxs-lookup"><span data-stu-id="473bd-147">Otherwise, when you try to install the solution package, you may receive the following error message, "No import packages were found."</span></span> <span data-ttu-id="473bd-148">Lai atbloķētu zip failu, noklikšķiniet uz tā ar peles labo pogu un atlasiet **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="473bd-148">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="473bd-149">Atlasiet **Atbloķēt**.</span><span class="sxs-lookup"><span data-stu-id="473bd-149">Select **Unblock**.</span></span>
3. <span data-ttu-id="473bd-150">Izgūstiet no zip arhīva un palaidiet failu **PackageDeployer.exe**.</span><span class="sxs-lookup"><span data-stu-id="473bd-150">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="473bd-151">Tālāk aprakstītajā veidā instalējiet risinājumu No potenciālā klienta līdz skaidrai naudai savā Sales instancē.</span><span class="sxs-lookup"><span data-stu-id="473bd-151">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="473bd-152">Kā izvietojuma tipu atlasiet **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="473bd-152">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="473bd-153">Atlasiet **Rādīt papildu**.</span><span class="sxs-lookup"><span data-stu-id="473bd-153">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="473bd-154">Lai veiktu ātru instalēšanu, atlasiet kādu reģionu.</span><span class="sxs-lookup"><span data-stu-id="473bd-154">For a quick installation, select a region.</span></span> <span data-ttu-id="473bd-155">Ja atlasāt **Nezinu**, sistēma meklē visus reģionus un instalēšana aizņem vairāk laika.</span><span class="sxs-lookup"><span data-stu-id="473bd-155">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="473bd-156">Ievadiet lietotājvārdu un paroli lietotājam ar administratora tiesībām, kuram ir tiesības veikt instalēšanu.</span><span class="sxs-lookup"><span data-stu-id="473bd-156">Enter the user name and password of an admin user who has installation rights.</span></span>



