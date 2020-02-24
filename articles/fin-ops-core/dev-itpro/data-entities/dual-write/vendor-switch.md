---
title: Pārslēgšanās starp kreditoru noformējumiem
description: Šajā tēmā ir aprakstīts, kā pārslēgties starp kreditora datu integrāciju starp Finance and Operations programmām un Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 587a9b98f28b11e303aff4b59e9726f220d956eb
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019893"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="83b32-103">Pārslēgšanās starp kreditoru noformējumiem</span><span class="sxs-lookup"><span data-stu-id="83b32-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="83b32-104">Kreditora datu plūsma</span><span class="sxs-lookup"><span data-stu-id="83b32-104">Vendor data flow</span></span> 

<span data-ttu-id="83b32-105">Ja izmantojat citas Dynamics 365 programmas kreditora pamatdatu apgūšanai un vēlaties nošķirt kreditora informāciju no debitoriem, izmantojiet šo pamata kreditora modeli.</span><span class="sxs-lookup"><span data-stu-id="83b32-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Pamata kreditora plūsma](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="83b32-107">Ja izmantojat citas Dynamics 365 programmas kreditora pamatdatu apgūšanai un vēlaties arī turpmāk izmantot elementu **Konts** kreditora informācijas glabāšanai, izmantojiet šo paplašināto kreditora modeli.</span><span class="sxs-lookup"><span data-stu-id="83b32-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="83b32-108">Šajā modelī paplašināta kreditora informācija, piemēram, kreditora aizturēšanas statuss un kreditora profils, tiek glabāts elementā **kreditori** pakalpojumā Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="83b32-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Kreditora paplašinātā plūsma](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="83b32-110">Izpildiet tālāk norādītās darbības, lai izmantotu paplašināto kreditora modeli.</span><span class="sxs-lookup"><span data-stu-id="83b32-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="83b32-111">**SupplyChainCommon** risinājuma pakotnē ir iekļautas darbplūsmas procesa veidnes, kā redzams nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="83b32-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="83b32-112">![Darbplūsmas procesa veidnes](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="83b32-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="83b32-113">Izveidojiet jaunus darbplūsmas procesus, izmantojot darbplūsmas procesa veidnes:</span><span class="sxs-lookup"><span data-stu-id="83b32-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="83b32-114">Izveidojiet jaunu darbplūsmas procesu elementā **Kreditors**, izmantojot darbplūsmas procesa veidni **Izveidot kreditorus konta elementā** un noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="83b32-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="83b32-115">Šī darbplūsma apstrādā kreditora izveides scenāriju elementam **Konts**.</span><span class="sxs-lookup"><span data-stu-id="83b32-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="83b32-116">![Izveidot kreditorus konta elementā](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="83b32-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="83b32-117">Izveidojiet jaunu darbplūsmas procesu elementā **Kreditors**, izmantojot darbplūsmas procesa veidni **Atjaunināt kontu elementu** un noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="83b32-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="83b32-118">Šī darbplūsma apstrādā kreditora atjaunināšanas scenāriju elementam **Konts**.</span><span class="sxs-lookup"><span data-stu-id="83b32-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="83b32-119">![Atjaunināt kontu elementu](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="83b32-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="83b32-120">Izveidojiet jaunus darbplūsmas procesus no veidnēm, kas izveidotas elementā **Konti**.</span><span class="sxs-lookup"><span data-stu-id="83b32-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="83b32-121">![Izveidot kreditorus kreditoru elementā](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="83b32-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="83b32-122">![Atjaunināt kreditoru elementu](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="83b32-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="83b32-123">Darbplūsmas var konfigurēt kā reāllaika vai fona darbplūsmas, pamatojoties uz jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="83b32-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="83b32-124">![Konvertēt uz fona darbplūsmu](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="83b32-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="83b32-125">Aktivizējiet darbplūsmas, ko izveidojāt elementos **Konts** un **Kreditors**, lai sāktu izmantot elementu **Konts** kreditora informācijas glabāšanai.</span><span class="sxs-lookup"><span data-stu-id="83b32-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 
