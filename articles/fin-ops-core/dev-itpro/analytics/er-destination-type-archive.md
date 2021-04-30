---
title: Arhīva ER adresāta tips
description: Šajā tēmā sniegta informācija par to, kā konfigurēt arhīva mērķi katrai MAPEI vai FAILA komponentam elektronisko pārskatu (ER) formātā.
author: NickSelin
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 079eda04fcc41fc637419a83452db10b89ed1ab9
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894032"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="7a56c-103">Arhīva ER adresāta tips</span><span class="sxs-lookup"><span data-stu-id="7a56c-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a56c-104">Varat konfigurēt arhīva adresātu katram **Mapes** vai **Faila** komponentam elektroniskās ziņošanas (ER) formātā, kas ir konfigurēts izejošo dokumentu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="7a56c-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="7a56c-105">Pamatojoties uz adresāta iestatījumu, ģenerētais dokuments tiek saglabāts kā ER darbu saraksta ieraksta pielikums.</span><span class="sxs-lookup"><span data-stu-id="7a56c-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="7a56c-106">Lai skatītu rezultātus, atveriet sadaļu **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Elektronisko pārskatu darbi**.</span><span class="sxs-lookup"><span data-stu-id="7a56c-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="7a56c-107">Varat izmantot šo opciju, lai nosūtītu -ģenerēto dokumentu uz Microsoft SharePoint mapi vai Microsoft Azure krātuvi.</span><span class="sxs-lookup"><span data-stu-id="7a56c-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="7a56c-108">Opciju **Iespējots** iestatiet uz **Jā**, lai izvadi sūtītu uz galamērķi, kas ir definēts ar atlasīto dokumentu tipu.</span><span class="sxs-lookup"><span data-stu-id="7a56c-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="7a56c-109">Atlasei ir pieejami tikai tie dokumentu tipi, kur grupa ir iestatīta uz **Fails**.</span><span class="sxs-lookup"><span data-stu-id="7a56c-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="7a56c-110">Dokuments jādefinē sadaļā [tipi](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) at **Organizācijas administrēšana** \> **Dokumentu pārvaldība** \> **Dokumentu tipi**.</span><span class="sxs-lookup"><span data-stu-id="7a56c-110">You define document [types](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="7a56c-111">Konfigurēšana ER galamērķiem ir tāda pati kā konfigurēšana dokumentu pārvaldības sistēmai.</span><span class="sxs-lookup"><span data-stu-id="7a56c-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="7a56c-112">[![Lapa Dokumentu tipi](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="7a56c-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="7a56c-113">Atrašanās vieta nosaka, kur fails tiek saglabāts.</span><span class="sxs-lookup"><span data-stu-id="7a56c-113">The location determines where the file is saved.</span></span> <span data-ttu-id="7a56c-114">Kad ir iespējots galamērķis **Arhīvs**, rezultātus var saglabāt darbu arhīvā.</span><span class="sxs-lookup"><span data-stu-id="7a56c-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="7a56c-115">Rezultātus varat skatīt sadaļā **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Elektronisko pārskatu arhivētie darbi**.</span><span class="sxs-lookup"><span data-stu-id="7a56c-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="7a56c-116">Atlasiet darbu arhīva dokumenta veidu, pārejot uz sadaļu **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana** \> **Elektronisko pārskatu parametri**.</span><span class="sxs-lookup"><span data-stu-id="7a56c-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="7a56c-117">Papildinformāciju skatiet tēmā [Elektronisko pārskatu (EP) veidošanas struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="7a56c-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="7a56c-118">SharePoint</span><span class="sxs-lookup"><span data-stu-id="7a56c-118">SharePoint</span></span>

<span data-ttu-id="7a56c-119">Varat saglabāt failu norādītajā SharePoint mapē.</span><span class="sxs-lookup"><span data-stu-id="7a56c-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="7a56c-120">Lai definētu noklusējuma serveri SharePoint, pārejiet uz **Organizācijas administrēšana** \> **Dokumentu pārvaldība** \> **Dokumentu pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="7a56c-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="7a56c-121">Cilnē **SharePoint** konfigurējiet mapi SharePoint.</span><span class="sxs-lookup"><span data-stu-id="7a56c-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="7a56c-122">Pēc tam varat atlasīt to kā mapi, kurā tiks saglabāta ER izvade.</span><span class="sxs-lookup"><span data-stu-id="7a56c-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="7a56c-123">Šajā dokumentu tipā jaatlasa atrašanās vieta **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="7a56c-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="7a56c-124">[![Risinājuma SharePoint mapes atlase](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="7a56c-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="7a56c-125">Azure krātuve</span><span class="sxs-lookup"><span data-stu-id="7a56c-125">Azure Storage</span></span>

<span data-ttu-id="7a56c-126">Kad dokumentu tipa atrašanās vieta ir iestatīta uz **Azure krātuve**, varat failu saglabāt Azure krātuvē.</span><span class="sxs-lookup"><span data-stu-id="7a56c-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="7a56c-127">ER struktūra pastāvīgi glabā failus Azure Blob krātuvē atšķirībā no datu pārvaldības struktūras, kas piemēro septiņu dienu saglabāšanas politiku dokumentiem, kas ir jāapstrādā.</span><span class="sxs-lookup"><span data-stu-id="7a56c-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="7a56c-128">Papildinformāciju skatiet šeit: [API ziņojuma statusa iegūšanai](../data-entities/recurring-integrations.md#api-for-getting-message-status) un [Stāvokļa pārbaudes API](../data-entities/data-management-api.md#status-check-api).</span><span class="sxs-lookup"><span data-stu-id="7a56c-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="7a56c-129">Ar ER saistītie faili tiks glabāti Azure Blob krātuvē kā pielikumi programmas tabulas ierakstiem tik ilgi, cik nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="7a56c-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="7a56c-130">Viens fails tiks dzēsts no Azure Blob krātuves kopā ar programmas tabulas ierakstu, kuram šis fails tika pievienots.</span><span class="sxs-lookup"><span data-stu-id="7a56c-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a56c-131">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="7a56c-131">Additional resources</span></span>

- [<span data-ttu-id="7a56c-132">Elektronisko pārskatu veidošanas (ER) apskats</span><span class="sxs-lookup"><span data-stu-id="7a56c-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="7a56c-133">Elektroniskās pārskatu veidošanas (ER) adresāti</span><span class="sxs-lookup"><span data-stu-id="7a56c-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="7a56c-134">Dokumentu pārvaldības konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="7a56c-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]