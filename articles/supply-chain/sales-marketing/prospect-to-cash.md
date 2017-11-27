---
title: "No potenciālā klienta līdz skaidrai naudai"
description: "Šajā tēmā ir sniegts apskats par risinājumu No potenciālā klienta līdz skaidrai naudai programmās Dynamics 365 for Finance and Operations, Enterprise Edition un Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: lv-lv
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="27ac1-103">No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="27ac1-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="27ac1-104">Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantota [Datu integrācija](/common-data-service/entity-reference/dynamics-365-integration), lai sinhronizētu datus starp Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition un Dynamics 365 for Sales instancēm, izmantojot Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="27ac1-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="27ac1-105">Līdzeklī Datu integrācija pieejamās risinājuma No potenciālā klienta līdz skaidrai naudai veidnes ļauj izmantot kontu, kontaktpersonu, preču, pārdošanas piedāvājumu, pārdošanas pasūtījumu un pārdošanas rēķinu datu plūsmu starp Finance and Operations un Sales.</span><span class="sxs-lookup"><span data-stu-id="27ac1-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="27ac1-106">Kamēr notiek datu plūsma starp Finance and Operations un Sales, programmā Sales varat veikt pārdošanas un mārketinga aktivitātes, savukārt programmā Finance and Operations varat veikt pasūtījuma izpildi ar krājumu vadību.</span><span class="sxs-lookup"><span data-stu-id="27ac1-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="27ac1-107">Šis risinājums nodrošina integrāciju tālāk norādītajās jomās.</span><span class="sxs-lookup"><span data-stu-id="27ac1-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="27ac1-108">Kontu uzturēšana programmā Sales un to sinhronizēšana ar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27ac1-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="27ac1-109">Kontaktpersonu uzturēšana programmā Sales un to sinhronizēšana ar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27ac1-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="27ac1-110">Preču uzturēšana programmā Finance and Operations un to sinhronizēšana ar Sales</span><span class="sxs-lookup"><span data-stu-id="27ac1-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="27ac1-111">Pārdošanas piedāvājumu izveidošana programmā Sales un to sinhronizēšana ar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27ac1-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="27ac1-112">Pārdošanas pasūtījumu izveidošana programmā Finance and Operations un to sinhronizēšana ar Sales</span><span class="sxs-lookup"><span data-stu-id="27ac1-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="27ac1-113">Pārdošanas rēķinu izveidošana programmā Finance and Operations un to sinhronizēšana ar Sales</span><span class="sxs-lookup"><span data-stu-id="27ac1-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

<span data-ttu-id="27ac1-114">Šis risinājums nodrošina tiešu sinhronizēšanu tālāk norādītajos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="27ac1-114">This solution provides direct synchronization in the following areas:</span></span>

-   [<span data-ttu-id="27ac1-115">Kontu uzturēšana programmā Sales un to tieša sinhronizēšana ar programmu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27ac1-115">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
-   [<span data-ttu-id="27ac1-116">Preču uzturēšana programmā Finance and Operations un to tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="27ac1-116">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
-   [<span data-ttu-id="27ac1-117">Kontaktpersonu uzturēšana programmā Sales un to tieša sinhronizēšana ar kontaktpersonām vai debitoriem programmā Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27ac1-117">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
-   [<span data-ttu-id="27ac1-118">Programmā Sales ietverto pārdošanas piedāvājumu galveņu un rindu tieša sinhronizēšana ar programmu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27ac1-118">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
-   [<span data-ttu-id="27ac1-119">Pārdošanas pasūtījumu izveide programmā Finance and Operations un to tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="27ac1-119">Create sales orders in Finance and Operations and sync them directly to Sales</span></span>](sales-order-template-mapping-direct.md)
-  [<span data-ttu-id="27ac1-120">Pārdošanas pasūtījumu galveņu un rindu tieša sinhronizēšana programmās Sales un Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27ac1-120">Synchronize sales order headers and lines directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-between-sales-fin.md)
-   [<span data-ttu-id="27ac1-121">Pārdošanas pasūtījumu tieša sinhronizēšana programmās Sales un Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="27ac1-121">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
-   [<span data-ttu-id="27ac1-122">Pārdošanas rēķinu izveide programmā Finance and Operations un to tieša sinhronizēšana ar programmu Sales</span><span class="sxs-lookup"><span data-stu-id="27ac1-122">Create sales invoices in Finance and Operations and sync them directly to Sales</span></span>](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="27ac1-123">Sistēmas prasības programmai Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="27ac1-123">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="27ac1-124">Lai izmantotu risinājumu No potenciālā klienta līdz skaidrai naudai, ir nepieciešams instalēt tālāk uzskaitītos elementus.</span><span class="sxs-lookup"><span data-stu-id="27ac1-124">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="27ac1-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (2017. jūlijs) ar platformas 8. atjauninājumu (programma 7.2.11792.56024 ar platformu 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="27ac1-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="27ac1-126">Dynamics 365 for Finance and Operations Enterprise Edition labojumfaili (2017. gada jūlijs).</span><span class="sxs-lookup"><span data-stu-id="27ac1-126">Hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>
        
    -  <span data-ttu-id="27ac1-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) — šis labojumfails nodrošina atbalstu programmā Sales ietverto pārdošanas pasūtījumu sinhronizēšanai ar programmu Finance and Operations, izmantojot līdzekli Datu integrācija, kā arī vairākus citus uzlabojumus.</span><span class="sxs-lookup"><span data-stu-id="27ac1-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - This hotfix enabels support for sales order synchronization with the Data Integration feature from Sales to Finance and Operations, along with a number of other enhancements.</span></span>

    -  <span data-ttu-id="27ac1-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) — šis labojumfails ļauj veikt pārdošanas pasūtījuma rindas sinhronizēšanu ar līdzekli Datu integrācija no programmas Finance and Operations uz programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="27ac1-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="27ac1-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) — šis labojumfails ļauj veikt pārdošanas pasūtījuma sinhronizēšanu ar līdzekli Datu integrācija no programmas Finance and Operations uz programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="27ac1-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>

<span data-ttu-id="27ac1-130">**Piezīme**. Ir jāinstalē tikai labojumfails KB4045570, jo instalācijā ir ietvertas citos labojumfailos iekļautās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="27ac1-130">**Note**: You only need to install KB4045570 because the installation includes the changes from the other KB's.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="27ac1-131">Sistēmas prasības programmai Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="27ac1-131">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="27ac1-132">Lai izmantotu risinājumu No potenciālā klienta līdz skaidrai naudai, ir nepieciešams instalēt tālāk uzskaitītos elementus.</span><span class="sxs-lookup"><span data-stu-id="27ac1-132">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="27ac1-133">Dynamics 365 for Sales tiešsaistes versija 1612 (8.2.1.207) (DB 8.2.1.207).</span><span class="sxs-lookup"><span data-stu-id="27ac1-133">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online.</span></span>
- <span data-ttu-id="27ac1-134">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Dynamics 365 for Sales, versija 1.14.0.0 (v14) vai jaunāka.</span><span class="sxs-lookup"><span data-stu-id="27ac1-134">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="27ac1-135">Instalēt risinājumu No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="27ac1-135">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="27ac1-136">Lejupielādējiet [Risinājuma No potenciālā klienta līdz skaidrai naudai programmai Dynamics 365 for Sales pakotnes zip failu](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) vietnē CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="27ac1-136">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="27ac1-137">Pārliecinieties, vai zip fails ir atbloķēts, lai risinājuma pakotnes instalēšanas laikā jums nerādītu kļūdas ziņojumu “Importēšanas pakotnes nav atrastas”.</span><span class="sxs-lookup"><span data-stu-id="27ac1-137">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="27ac1-138">Lai failu atbloķētu, izpildiet tālāk aprakstītos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="27ac1-138">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="27ac1-139">Noklikšķiniet uz zip faila ar peles labo pogu.</span><span class="sxs-lookup"><span data-stu-id="27ac1-139">Right-click the zip file.</span></span>
    -  <span data-ttu-id="27ac1-140">Atlasiet **Rekvizīti** un pēc tam atlasiet **Atbloķēt**.</span><span class="sxs-lookup"><span data-stu-id="27ac1-140">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="27ac1-141">Izgūstiet no ZIP arhīva un palaidiet failu PackageDeployer.exe.</span><span class="sxs-lookup"><span data-stu-id="27ac1-141">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="27ac1-142">Instalējiet risinājumu No potenciālā klienta līdz skaidrai naudai savai Sales instancei.</span><span class="sxs-lookup"><span data-stu-id="27ac1-142">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="27ac1-143">Atlasiet izvietošanas tipu **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="27ac1-143">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="27ac1-144">Atlasiet **Rādīt papildu**.</span><span class="sxs-lookup"><span data-stu-id="27ac1-144">Select **Show advanced**.</span></span>
    - <span data-ttu-id="27ac1-145">Lai veiktu ātru instalēšanu, atlasiet kādu vērtību vienumam **Reģions**.</span><span class="sxs-lookup"><span data-stu-id="27ac1-145">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="27ac1-146">Ja atlasāt **Nezinu**, tad sistēma meklē visus reģionus un instalēšanai var būt nepieciešams ilgāks laiks.</span><span class="sxs-lookup"><span data-stu-id="27ac1-146">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="27ac1-147">Ievadiet vērtības laukiem **Lietotājvārds** un **Parole** lietotājam–administratoram, kuram ir lietotāja tiesības veikt instalēšanu.</span><span class="sxs-lookup"><span data-stu-id="27ac1-147">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

