---
title: Piegādātāju katalogu importēšana
description: Šajā tēmā ir aprakstīts piegādātāju katalogu datu importēšanas process.
author: mkirknel
manager: tfehr
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 7ed2c50b28fdbd1baf4caa0a8a7f2f05d6a53fd6
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018587"
---
# <a name="import-vendor-catalogs"></a><span data-ttu-id="3b896-103">Importēt piegādātāju katalogus</span><span class="sxs-lookup"><span data-stu-id="3b896-103">Import vendor catalogs</span></span>

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="3b896-104">Piegādātāju katalogu importēšana</span><span class="sxs-lookup"><span data-stu-id="3b896-104">Vendor catalogs import</span></span>

<span data-ttu-id="3b896-105">Programmā Dynamics 365 Supply Chain Management iepirkumu speciālisti var izveidot un uzturēt katalogus, ko uzņēmuma darbinieki var izmantot, pasūtot krājumus un pakalpojumus iekšējai lietošanai.</span><span class="sxs-lookup"><span data-stu-id="3b896-105">In Dynamics 365 Supply Chain Management, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="3b896-106">Lai izveidotu sagādes katalogu, varat pievienot krājumus un pakalpojumus, kurus vēlaties padarīt pieejamus darbiniekiem, Tas ir izdarāms, vai nu importējot preču kataloga datus, vai manuāli pievienojot preču kataloga datus preces šablonam.</span><span class="sxs-lookup"><span data-stu-id="3b896-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="3b896-107">Kreditora iesniegtos kataloga datus varat augšupielādēt Microsoft Dynamics 365 klientā.</span><span class="sxs-lookup"><span data-stu-id="3b896-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="3b896-108">Preces datiem, ko piegādātājs jums iesniedz kataloga uzturēšanas pieprasījuma (Catalog Maintenance Request — CMR) faila formā, ir jābūt XML faila formātā.</span><span class="sxs-lookup"><span data-stu-id="3b896-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="3b896-109">CMR failā ir jābūt informācijai par precēm, ko šis piegādātājs piegādā jūsu uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="3b896-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>

## <a name="import-vendor-catalog-data"></a><span data-ttu-id="3b896-110">Piegādātāja kataloga datu importēšana</span><span class="sxs-lookup"><span data-stu-id="3b896-110">Import vendor catalog data</span></span>

<span data-ttu-id="3b896-111">Lai importētu piegādātāja kataloga datus, jums ir jāizpilda tālāk minētie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="3b896-111">To import vendor catalog data, you must complete the following tasks:</span></span>

1. <span data-ttu-id="3b896-112">Iestatiet projektu tajā datu pārvaldības darbvietā, kur ir definētas jūsu datu kartēšanas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="3b896-112">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="3b896-113">Atlasiet **Datu pārvaldība** un pēc tam atlasiet **Iestatīt lomas datu projektiem**.</span><span class="sxs-lookup"><span data-stu-id="3b896-113">Select **Data management** and then select **Set up roles for data projects**.</span></span>

2. <span data-ttu-id="3b896-114">Iestatiet sagādes kategoriju hierarhiju un savus piegādātājus piešķirt sagādes kategorijām.</span><span class="sxs-lookup"><span data-stu-id="3b896-114">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="3b896-115">Ja izmantojat preču kodus, šie preču kodi ir jāpievieno sagādes kategorijām.</span><span class="sxs-lookup"><span data-stu-id="3b896-115">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="3b896-116">Informāciju par sagādes kategoriju hierarhijas iestatīšanu skatiet rakstā [Sagādes kategoriju hierarhijas iestatīšana](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="3b896-116">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>

3. <span data-ttu-id="3b896-117">Konfigurējiet piegādātāju kataloga importēšanai.</span><span class="sxs-lookup"><span data-stu-id="3b896-117">Configure the vendor for catalog import.</span></span> <span data-ttu-id="3b896-118">Atlasiet piegādātāju un pēc tam atlasiet **Sagāde** > **Iestatīt** > **Konfigurēt piegādātāju kataloga importēšanai**.</span><span class="sxs-lookup"><span data-stu-id="3b896-118">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>

4. <span data-ttu-id="3b896-119">Konfigurējiet darbplūsmu katalogu importēšanai.</span><span class="sxs-lookup"><span data-stu-id="3b896-119">Configure workflow for catalog import.</span></span> <span data-ttu-id="3b896-120">Izveidojiet CMR faila veidni un kopīgojiet to ar piegādāju.</span><span class="sxs-lookup"><span data-stu-id="3b896-120">Create a CMR file template and share this with your vendor.</span></span>

5. <span data-ttu-id="3b896-121">Lai izveidotu piegādātāja katalogu, atlasiet **Sagāde un avoti** \> **Vispārīgi** \> **Katalogi** \> **Piegādātāju katalogi**.</span><span class="sxs-lookup"><span data-stu-id="3b896-121">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="3b896-122">Šajā katalogā tiek grupēti kataloga uzturēšanas pieprasījuma (CMR) faili, ko saņemat no sava piegādātāja.</span><span class="sxs-lookup"><span data-stu-id="3b896-122">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6. <span data-ttu-id="3b896-123">Augšupielādējiet CMR failu.</span><span class="sxs-lookup"><span data-stu-id="3b896-123">Upload the CMR file.</span></span>

7. <span data-ttu-id="3b896-124">Pārskatiet, apstipriniet vai noraidiet preces šajā piegādātāju katalogā.</span><span class="sxs-lookup"><span data-stu-id="3b896-124">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="3b896-125">Preces tiek automātiski kartētas uz sagādes kategorijām.</span><span class="sxs-lookup"><span data-stu-id="3b896-125">The products are automatically mapped to the procurement categories.</span></span> 

<span data-ttu-id="3b896-126">Apstiprinātās preces tiek pievienotas preces šablonam un izlaistas atlasītajām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="3b896-126">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="3b896-127">Sagādes katalogam var pievienot tikai apstiprinātās preces.</span><span class="sxs-lookup"><span data-stu-id="3b896-127">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="3b896-128">Kataloga importēšanas faila veidnes ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="3b896-128">Generate a catalog import file template</span></span>

<span data-ttu-id="3b896-129">Kataloga importēšanas faila veidne ir XSD fails, ko izmanto, lai izveidotu CMR failu piegādātāja precēm.</span><span class="sxs-lookup"><span data-stu-id="3b896-129">The catalog import file template is an XSD file that you use to create a CMR file for a vendor's products.</span></span> <span data-ttu-id="3b896-130">Varat izmantot CMR failu, lai izveidotu jaunu katalogu, aizstātu esošu katalogu vai modificētu esošu katalogu.</span><span class="sxs-lookup"><span data-stu-id="3b896-130">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1. <span data-ttu-id="3b896-131">Atlasiet **Sagāde un avoti** \> **Katalogi** \> **Piegādātāju katalogi** un veiciet dubultklikšķi uz kataloga, ar kuru vēlaties strādāt.</span><span class="sxs-lookup"><span data-stu-id="3b896-131">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor  catalogs** and double-click the catalog that you want  to work with.</span></span>

2. <span data-ttu-id="3b896-132">Lejupielādējiet pašreizēju kataloga importēšanas veidni (XSD fails).</span><span class="sxs-lookup"><span data-stu-id="3b896-132">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="3b896-133">Lapā **Atjaunināt katalogu** , loga **Darbību rūts** cilnē **Katalogi** , grupā **Saistītā informācija** noklikšķiniet uz **Ģenerēt kataloga veidni** un atlasiet **Sagādes kategorija**.</span><span class="sxs-lookup"><span data-stu-id="3b896-133">On the **Update catalog** page, on the **Action Pane** , on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    - <span data-ttu-id="3b896-134">Izmantojot opciju **Sagādes kategorija** , varat ģenerēt kataloga veidni, kur ir sagādes kategorijas, kurās piegādātājs ir autorizēts nodrošināt preces.</span><span class="sxs-lookup"><span data-stu-id="3b896-134">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="3b896-135">Dialoglodziņā **Saglabāt kā** atlasiet atrašanās vietu, kur vēlaties saglabāt kataloga faila veidni, un saglabājiet failu.</span><span class="sxs-lookup"><span data-stu-id="3b896-135">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="3b896-136">Papildinformāciju un piemērus skatiet šajā emuāra ierakstā: [Piegādātāju katalogi sistēmā Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span><span class="sxs-lookup"><span data-stu-id="3b896-136">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>
