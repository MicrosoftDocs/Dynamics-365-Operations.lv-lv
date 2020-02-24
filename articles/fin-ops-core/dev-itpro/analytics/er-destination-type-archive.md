---
title: Arhīva ER adresāta tips
description: Šajā tēmā ir sniegta informācija par to, kā konfigurēt arhīva adresātu katram MAPES vai FAILA komponentam elektroniskās ziņošanas (ER) formātā, kas ir konfigurēts izejošo dokumentu ģenerēšanai.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 15611a4f0000ca5ccb0ac3f4012251d5bf5689ec
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019888"
---
# <span data-ttu-id="9e12d-103"><a name="ArchiveDestinationType">Arhīva galamērķis</a></span><span class="sxs-lookup"><span data-stu-id="9e12d-103"><a name="ArchiveDestinationType">Archive destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e12d-104">Varat konfigurēt arhīva adresātu katram MAPES vai FAILA komponentam elektroniskās ziņošanas (ER) formātā, kas ir konfigurēts izejošo dokumentu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="9e12d-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="9e12d-105">Pamatojoties uz adresāta iestatījumu, ģenerētais dokuments tiek saglabāts kā ER darbu saraksta ieraksta pielikums.</span><span class="sxs-lookup"><span data-stu-id="9e12d-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="9e12d-106">Varat izmantot šo opciju, lai nosūtītu -ģenerēto dokumentu uz Microsoft SharePoint mapi vai Microsoft Azure krātuvi.</span><span class="sxs-lookup"><span data-stu-id="9e12d-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="9e12d-107">Opciju **Iespējots** iestatiet uz **Jā**, lai izvadi sūtītu uz galamērķi, kas ir definēts ar atlasīto dokumentu tipu.</span><span class="sxs-lookup"><span data-stu-id="9e12d-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="9e12d-108">Atlasei ir pieejami tikai tie dokumentu tipi, kur grupa ir iestatīta uz **Fails**.</span><span class="sxs-lookup"><span data-stu-id="9e12d-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="9e12d-109">Dokuments jādefinē sadaļā [tipi](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organizācijas administrēšana** \> **Dokumentu pārvaldība** \> **Dokumentu tipi**.</span><span class="sxs-lookup"><span data-stu-id="9e12d-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="9e12d-110">Konfigurēšana ER galamērķiem ir tāda pati kā konfigurēšana dokumentu pārvaldības sistēmai.</span><span class="sxs-lookup"><span data-stu-id="9e12d-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="9e12d-111">[![Lapa Dokumentu tipi](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="9e12d-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="9e12d-112">Atrašanās vieta nosaka, kur fails tiek saglabāts.</span><span class="sxs-lookup"><span data-stu-id="9e12d-112">The location determines where the file is saved.</span></span> <span data-ttu-id="9e12d-113">Kad ir iespējots galamērķis **Arhīvs**, rezultātus var saglabāt darbu arhīvā.</span><span class="sxs-lookup"><span data-stu-id="9e12d-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="9e12d-114">Rezultātus varat skatīt sadaļā **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Elektronisko pārskatu arhivētie darbi**.</span><span class="sxs-lookup"><span data-stu-id="9e12d-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="9e12d-115">Atlasiet darbu arhīva dokumenta veidu, pārejot uz sadaļu **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana** \> **Elektronisko pārskatu parametri**.</span><span class="sxs-lookup"><span data-stu-id="9e12d-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="9e12d-116">Papildinformāciju skatiet tēmā [Elektronisko pārskatu (EP) veidošanas struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="9e12d-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="9e12d-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="9e12d-117">SharePoint</span></span>

<span data-ttu-id="9e12d-118">Varat saglabāt failu norādītajā SharePoint mapē.</span><span class="sxs-lookup"><span data-stu-id="9e12d-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="9e12d-119">Lai definētu noklusējuma serveri SharePoint, pārejiet uz **Organizācijas administrēšana** \> **Dokumentu pārvaldība** \> **Dokumentu pārvaldības parametri**.</span><span class="sxs-lookup"><span data-stu-id="9e12d-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="9e12d-120">Cilnē **SharePoint** konfigurējiet mapi SharePoint.</span><span class="sxs-lookup"><span data-stu-id="9e12d-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="9e12d-121">Pēc tam varat atlasīt to kā mapi, kurā tiks saglabāta ER izvade.</span><span class="sxs-lookup"><span data-stu-id="9e12d-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="9e12d-122">Šajā dokumentu tipā jaatlasa atrašanās vieta **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="9e12d-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="9e12d-123">[![SharePoint mapes atlase](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="9e12d-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="9e12d-124">Azure krātuve</span><span class="sxs-lookup"><span data-stu-id="9e12d-124">Azure Storage</span></span>

<span data-ttu-id="9e12d-125">Kad dokumentu tipa atrašanās vieta ir iestatīta uz **Azure krātuve**, varat failu saglabāt Azure krātuvē.</span><span class="sxs-lookup"><span data-stu-id="9e12d-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e12d-126">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="9e12d-126">Additional resources</span></span>

- [<span data-ttu-id="9e12d-127">Elektronisko pārskatu veidošanas (ER) apskats</span><span class="sxs-lookup"><span data-stu-id="9e12d-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="9e12d-128">Elektroniskās pārskatu veidošanas (ER) adresāti</span><span class="sxs-lookup"><span data-stu-id="9e12d-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="9e12d-129">Dokumentu pārvaldības konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="9e12d-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
