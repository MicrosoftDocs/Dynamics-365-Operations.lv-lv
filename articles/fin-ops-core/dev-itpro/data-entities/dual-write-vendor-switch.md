---
title: Pārslēgties starp kreditora modeļiem
description: ''
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
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772368"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="786f2-102">Pārslēgties starp kreditora modeļiem</span><span class="sxs-lookup"><span data-stu-id="786f2-102">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="786f2-103">Kreditora datu plūsma</span><span class="sxs-lookup"><span data-stu-id="786f2-103">Vendor data flow</span></span> 

<span data-ttu-id="786f2-104">Ja izmantojat citas Dynamics 365 programmas kreditora pamatdatu apgūšanai un vēlaties nošķirt kreditora informāciju no debitoriem, izmantojiet šo pamata kreditora modeli.</span><span class="sxs-lookup"><span data-stu-id="786f2-104">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Pamata kreditora plūsma](media/dual-write-switch-1.png)
 
<span data-ttu-id="786f2-106">Ja izmantojat citas Dynamics 365 programmas kreditora pamatdatu apgūšanai un vēlaties arī turpmāk izmantot elementu **Konts** kreditora informācijas glabāšanai, izmantojiet šo paplašināto kreditora modeli.</span><span class="sxs-lookup"><span data-stu-id="786f2-106">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="786f2-107">Šajā modelī paplašināta kreditora informācija, piemēram, kreditora aizturēšanas statuss un kreditora profils, tiek glabāts elementā **kreditori** pakalpojumā Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="786f2-107">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Kreditora paplašinātā plūsma](media/dual-write-switch-2.png)
 
<span data-ttu-id="786f2-109">Izpildiet tālāk norādītās darbības, lai izmantotu paplašināto kreditora modeli.</span><span class="sxs-lookup"><span data-stu-id="786f2-109">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="786f2-110">**SupplyChainCommon** risinājuma pakotnē ir iekļautas darbplūsmas procesa veidnes, kā redzams nākamajā attēlā.</span><span class="sxs-lookup"><span data-stu-id="786f2-110">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="786f2-111">![Darbplūsmas procesa veidnes](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="786f2-111">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="786f2-112">Izveidojiet jaunus darbplūsmas procesus, izmantojot darbplūsmas procesa veidnes:</span><span class="sxs-lookup"><span data-stu-id="786f2-112">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="786f2-113">Izveidojiet jaunu darbplūsmas procesu elementā **Kreditors**, izmantojot darbplūsmas procesa veidni **Izveidot kreditorus konta elementā** un noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="786f2-113">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="786f2-114">Šī darbplūsma apstrādā kreditora izveides scenāriju elementam **Konts**.</span><span class="sxs-lookup"><span data-stu-id="786f2-114">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="786f2-115">![Izveidot kreditorus konta elementā](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="786f2-115">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="786f2-116">Izveidojiet jaunu darbplūsmas procesu elementā **Kreditors**, izmantojot darbplūsmas procesa veidni **Atjaunināt kontu elementu** un noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="786f2-116">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="786f2-117">Šī darbplūsma apstrādā kreditora atjaunināšanas scenāriju elementam **Konts**.</span><span class="sxs-lookup"><span data-stu-id="786f2-117">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="786f2-118">![Atjaunināt kontu elementu](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="786f2-118">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="786f2-119">Izveidojiet jaunus darbplūsmas procesus no veidnēm, kas izveidotas elementā **Konti**.</span><span class="sxs-lookup"><span data-stu-id="786f2-119">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="786f2-120">![Izveidot kreditorus kreditoru elementā](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="786f2-120">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="786f2-121">![Atjaunināt kreditoru elementu](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="786f2-121">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="786f2-122">Darbplūsmas var konfigurēt kā reāllaika vai fona darbplūsmas, pamatojoties uz jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="786f2-122">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="786f2-123">![Konvertēt uz fona darbplūsmu](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="786f2-123">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="786f2-124">Aktivizējiet darbplūsmas, ko izveidojāt elementos **Konts** un **Kreditors**, lai sāktu izmantot Customer Engagement elementu **Konts** kreditora informācijas glabāšanai.</span><span class="sxs-lookup"><span data-stu-id="786f2-124">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the Customer Engagement **Account** entity for storing vendor information.</span></span> 
 
