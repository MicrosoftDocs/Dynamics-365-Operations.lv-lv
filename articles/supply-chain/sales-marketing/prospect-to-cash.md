---
title: "No potenciālā klienta līdz skaidrai naudai"
description: "Šajā tēmā ir sniegts apskats par risinājumu No potenciālā klienta līdz skaidrai naudai programmās Dynamics 365 for Finance and Operations, Enterprise Edition un Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="62eec-103">No potenciālā klienta līdz skaidrai naudai</span><span class="sxs-lookup"><span data-stu-id="62eec-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="62eec-104">Risinājumā No potenciālā klienta līdz skaidrai naudai tiek izmantota [Datu integrācija](/common-data-service/entity-reference/dynamics-365-integration), lai sinhronizētu datus starp Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition un Dynamics 365 for Sales instancēm, izmantojot Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="62eec-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="62eec-105">Līdzeklī Datu integrācija pieejamās risinājuma No potenciālā klienta līdz skaidrai naudai veidnes ļauj izmantot kontu, kontaktpersonu, preču, pārdošanas piedāvājumu, pārdošanas pasūtījumu un pārdošanas rēķinu datu plūsmu starp Finance and Operations un Sales.</span><span class="sxs-lookup"><span data-stu-id="62eec-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="62eec-106">Kamēr notiek datu plūsma starp Finance and Operations un Sales, programmā Sales varat veikt pārdošanas un mārketinga aktivitātes, savukārt programmā Finance and Operations varat veikt pasūtījuma izpildi ar krājumu vadību.</span><span class="sxs-lookup"><span data-stu-id="62eec-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="62eec-107">Šis risinājums nodrošina integrāciju tālāk norādītajās jomās.</span><span class="sxs-lookup"><span data-stu-id="62eec-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="62eec-108">Kontu uzturēšana programmā Sales un to sinhronizēšana ar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="62eec-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="62eec-109">Kontaktpersonu uzturēšana programmā Sales un to sinhronizēšana ar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="62eec-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="62eec-110">Preču uzturēšana programmā Finance and Operations un to sinhronizēšana ar Sales</span><span class="sxs-lookup"><span data-stu-id="62eec-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="62eec-111">Pārdošanas piedāvājumu izveidošana programmā Sales un to sinhronizēšana ar Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="62eec-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="62eec-112">Pārdošanas pasūtījumu izveidošana programmā Finance and Operations un to sinhronizēšana ar Sales</span><span class="sxs-lookup"><span data-stu-id="62eec-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="62eec-113">Pārdošanas rēķinu izveidošana programmā Finance and Operations un to sinhronizēšana ar Sales</span><span class="sxs-lookup"><span data-stu-id="62eec-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="62eec-114">Sistēmas prasības programmai Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="62eec-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="62eec-115">Lai izmantotu risinājumu No potenciālā klienta līdz skaidrai naudai, ir nepieciešams instalēt tālāk uzskaitītos elementus.</span><span class="sxs-lookup"><span data-stu-id="62eec-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="62eec-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (2017. jūlijs) ar platformas 8. atjauninājumu (programma 7.2.11792.56024 ar platformu 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="62eec-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="62eec-117">Divi labojumfaili programmatūrai Dynamics 365 for Finance and Operations, Enterprise Edition (2017. gada jūlijs).</span><span class="sxs-lookup"><span data-stu-id="62eec-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="62eec-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) — šis labojumfails ļauj veikt pārdošanas pasūtījuma rindas sinhronizēšanu ar līdzekli Datu integrācija no programmas Finance and Operations uz programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="62eec-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="62eec-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) — šis labojumfails ļauj veikt pārdošanas pasūtījuma sinhronizēšanu ar līdzekli Datu integrācija no programmas Finance and Operations uz programmu Sales.</span><span class="sxs-lookup"><span data-stu-id="62eec-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="62eec-120">**Piezīme**. Labojumfails KB4036524 ir jāinstalē tikai tāpēc, ka instalācijā ir ietvertas izmaiņas no KB4036461.</span><span class="sxs-lookup"><span data-stu-id="62eec-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="62eec-121">Sistēmas prasības programmai Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="62eec-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="62eec-122">Lai izmantotu risinājumu No potenciālā klienta līdz skaidrai naudai, ir nepieciešams instalēt tālāk uzskaitītos elementus.</span><span class="sxs-lookup"><span data-stu-id="62eec-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="62eec-123">Dynamics 365 for Sales versija 1612 (8.2.1.207) (DB 8.2.1.207) tiešsaistes versija vai jaunāka.</span><span class="sxs-lookup"><span data-stu-id="62eec-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="62eec-124">Risinājums No potenciālā klienta līdz skaidrai naudai programmai Dynamics 365 for Sales, versija 1.14.0.0 (v14) vai jaunāka.</span><span class="sxs-lookup"><span data-stu-id="62eec-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="62eec-125">Instalēt risinājumu No potenciālā klienta līdz skaidrai naudai programmai Sales</span><span class="sxs-lookup"><span data-stu-id="62eec-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="62eec-126">Lejupielādējiet [Risinājuma No potenciālā klienta līdz skaidrai naudai programmai Dynamics 365 for Sales pakotnes zip failu](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) vietnē CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="62eec-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="62eec-127">Pārliecinieties, vai zip fails ir atbloķēts, lai risinājuma pakotnes instalēšanas laikā jums nerādītu kļūdas ziņojumu “Importēšanas pakotnes nav atrastas”.</span><span class="sxs-lookup"><span data-stu-id="62eec-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="62eec-128">Lai failu atbloķētu, izpildiet tālāk aprakstītos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="62eec-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="62eec-129">Noklikšķiniet uz zip faila ar peles labo pogu.</span><span class="sxs-lookup"><span data-stu-id="62eec-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="62eec-130">Atlasiet **Rekvizīti** un pēc tam atlasiet **Atbloķēt**.</span><span class="sxs-lookup"><span data-stu-id="62eec-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="62eec-131">Izgūstiet no ZIP arhīva un palaidiet failu PackageDeployer.exe.</span><span class="sxs-lookup"><span data-stu-id="62eec-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="62eec-132">Instalējiet risinājumu No potenciālā klienta līdz skaidrai naudai savai Sales instancei.</span><span class="sxs-lookup"><span data-stu-id="62eec-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="62eec-133">Atlasiet izvietošanas tipu **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="62eec-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="62eec-134">Atlasiet **Rādīt papildu**.</span><span class="sxs-lookup"><span data-stu-id="62eec-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="62eec-135">Lai veiktu ātru instalēšanu, atlasiet kādu vērtību vienumam **Reģions**.</span><span class="sxs-lookup"><span data-stu-id="62eec-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="62eec-136">Ja atlasāt **Nezinu**, tad sistēma meklē visus reģionus un instalēšanai var būt nepieciešams ilgāks laiks.</span><span class="sxs-lookup"><span data-stu-id="62eec-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="62eec-137">Ievadiet vērtības laukiem **Lietotājvārds** un **Parole** lietotājam–administratoram, kuram ir lietotāja tiesības veikt instalēšanu.</span><span class="sxs-lookup"><span data-stu-id="62eec-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

