---
title: Līdzekļu dokumenti
description: Šī tēma paskaidro līdzekļu dokumentus Līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5b791fd3e060c4f4ecdb1ca599a6041d421db74
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024537"
---
# <a name="asset-documents"></a><span data-ttu-id="af4d2-103">Līdzekļu dokumenti</span><span class="sxs-lookup"><span data-stu-id="af4d2-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="af4d2-104">Šī tēma paskaidro līdzekļu dokumentus Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="af4d2-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="af4d2-105">Līdzekļu pārvaldībā varat iestatīt dokumentus tā, lai tie tiktu automātiski saistīti, piemēram, ar darbu veidiem, līdzekļu ražotājiem, līdzekļu veidiem vai līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="af4d2-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="af4d2-106">Šī funkcionalitāte tiek izmantota, kad tiek izlaistas atjauninātas dokumenta versijas.</span><span class="sxs-lookup"><span data-stu-id="af4d2-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="af4d2-107">Šādā gadījumā jums vienkārši jāievieto atjauninātais dokuments standarta atrašanās vietā, ko izmantojat Finance and Operations dokumentiem, un jāpievieno dokuments jūsu izveidotajam līdzekļu dokumenta ierakstam.</span><span class="sxs-lookup"><span data-stu-id="af4d2-107">In that case, you just have to put the updated document in the standard location that you use for your Finance and Operations documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="af4d2-108">Pēc tam atjauninātajam dokumentam var piekļūt no izvēlnes elementiem **Visi līdzekļi**, **Aktīvie līdzekļi**, **Mani aktīvie līdzekļi**, **Visi darba pasūtījumi** un **Aktīvie darba pasūtījuma darbi** .</span><span class="sxs-lookup"><span data-stu-id="af4d2-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="af4d2-109">Dokumentu pievienošanas process līdzekļa dokumenta ierakstam izmanto standarta dokumentu apstrādes sistēmu.</span><span class="sxs-lookup"><span data-stu-id="af4d2-109">The process for attaching documents to an asset document record uses the standard document handling system.</span></span>

<span data-ttu-id="af4d2-110">**1. piemērs** : dokuments, kas saistīts ar darba veidu, var aprakstīt procedūru šim darba veidam.</span><span class="sxs-lookup"><span data-stu-id="af4d2-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="af4d2-111">**2. piemērs** : dokuments, kas ir saistīts ar līdzekļa veida, ražotāja un modeļa kombināciju, var būt standarta rokasgrāmata atlasītajam līdzekļu ražotāja modelim.</span><span class="sxs-lookup"><span data-stu-id="af4d2-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="af4d2-112">Līdzekļa dokumentu attiecību izveide</span><span class="sxs-lookup"><span data-stu-id="af4d2-112">Create asset document relation</span></span>

1. <span data-ttu-id="af4d2-113">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļa dokumenti**.</span><span class="sxs-lookup"><span data-stu-id="af4d2-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="af4d2-114">Atlasiet **Jauns**, lai izveidotu līdzekļa dokumenta ierakstu.</span><span class="sxs-lookup"><span data-stu-id="af4d2-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="af4d2-115">Atkarībā no tā, cik konkrētas dokumentu attiecības vēlaties, veiciet atbilstīgu atlasi vienā vai vairākos šādos laukos: **Līdzekļa veids**, **Ražotājs**, **Modelis**, **Līdzeklis**, **Darba veida kategorija**, **Darba veids**, **Darba veida variants** un **Darba vajadzība**.</span><span class="sxs-lookup"><span data-stu-id="af4d2-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="af4d2-116">Opcijas, kas pieejamas laukos **Darba veida variants** un **Darba vajadzība**, ir atkarīgas no atlases laukā **Darba veids**.</span><span class="sxs-lookup"><span data-stu-id="af4d2-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="af4d2-117">Kad sistēma meklē dokumentus, kas ir jāattiecina uz līdzekli vai darba pasūtījumu, Līdzekļu pārvaldība iziet cauri visiem līdzekļa dokumentu ierakstiem, lai pārbaudītu iespējamo sakritību.</span><span class="sxs-lookup"><span data-stu-id="af4d2-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="af4d2-118">Tā vienmēr vispirms pārbauda visraksturīgāko kombināciju.</span><span class="sxs-lookup"><span data-stu-id="af4d2-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="af4d2-119">Citiem vārdiem sakot, Līdzekļu pārvaldība vispirms pārbauda atbilstību laukam **Darba vajadzība**.</span><span class="sxs-lookup"><span data-stu-id="af4d2-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="af4d2-120">Ja atbilstība netiek atrasta, tā meklē atbilstību laukam **Darba veida variants**.</span><span class="sxs-lookup"><span data-stu-id="af4d2-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="af4d2-121">Ja atbilstība netiek atrasta, tā meklē atbilstību laukam **Darba veids** un tā tālāk.</span><span class="sxs-lookup"><span data-stu-id="af4d2-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="af4d2-122">Kā jūs varat redzēt lapas **Līdzekļa dokumenti** zkārtojumā, šī uzvedība nozīmē, ka, lai atrastu visspecifiskāko kombināciju, Līdzekļu pārvaldība atbilstības meklēšanai pārbauda katru ierakstu no labās puses uz kreiso.</span><span class="sxs-lookup"><span data-stu-id="af4d2-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="af4d2-123">Ar līdzekli vai darba pasūtījumu var būt saistīti vairāki dokumenti.</span><span class="sxs-lookup"><span data-stu-id="af4d2-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="af4d2-124">Vajadzības gadījumā varat rediģēt pakalpojumu līmeni uzturēšanas pieprasījumā vai darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="af4d2-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="af4d2-125">Atlasiet **Pielikumi**.</span><span class="sxs-lookup"><span data-stu-id="af4d2-125">Select **Attachments**.</span></span> <span data-ttu-id="af4d2-126">Tiek parādīta standarta lapa **Dokumentu apstrāde**.</span><span class="sxs-lookup"><span data-stu-id="af4d2-126">The standard **Document handling** page appears.</span></span>
5. <span data-ttu-id="af4d2-127">Iestatiet dokumentus vai piezīmes, kas jāpievieno līdzekļa dokumenta ierakstam.</span><span class="sxs-lookup"><span data-stu-id="af4d2-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="af4d2-128">Pēc dokumentu pievienošanas lauks **Pielikumi** parāda ar ierakstu saistīto dokumentu skaitu.</span><span class="sxs-lookup"><span data-stu-id="af4d2-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>
