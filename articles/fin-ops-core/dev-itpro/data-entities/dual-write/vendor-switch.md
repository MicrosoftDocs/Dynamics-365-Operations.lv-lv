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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997556"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="2c5fc-103">Pārslēgšanās starp kreditoru noformējumiem</span><span class="sxs-lookup"><span data-stu-id="2c5fc-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="2c5fc-104">Kreditora datu plūsma</span><span class="sxs-lookup"><span data-stu-id="2c5fc-104">Vendor data flow</span></span> 

<span data-ttu-id="2c5fc-105">Ja izvēlaties izmantot elementu **Konts** elementu, lai uzglabātu veidu **Organizācija** un elementu **Kontaktpersona** veida **Persona** tipa kreditoriem, konfigurējiet šādas darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="2c5fc-106">Pretējā gadījumā šī konfigurācija nav obligāta.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="2c5fc-107">Izmantot paplašināto kreditoru noformējumu Organizācijas veida kreditoriem</span><span class="sxs-lookup"><span data-stu-id="2c5fc-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="2c5fc-108">**Dynamics365FinanceExtended** risinājuma pakotnē ir šādas darbplūsmas procesa veidnes.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="2c5fc-109">Katrai veidnei tiks izveidota darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="2c5fc-110">Izveidot kreditorus konta elementā</span><span class="sxs-lookup"><span data-stu-id="2c5fc-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="2c5fc-111">Izveidot kreditorus kreditoru elementā</span><span class="sxs-lookup"><span data-stu-id="2c5fc-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="2c5fc-112">Atjaunināt kreditorus konta elementā</span><span class="sxs-lookup"><span data-stu-id="2c5fc-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="2c5fc-113">Atjaunināt kreditorus kreditoru elementā</span><span class="sxs-lookup"><span data-stu-id="2c5fc-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="2c5fc-114">Lai izveidotu jaunus darbplūsmas procesus, izmantojot darbplūsmas procesa veidnes, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="2c5fc-115">Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus konta elementā**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="2c5fc-116">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-116">Then select **OK**.</span></span> <span data-ttu-id="2c5fc-117">Šī darbplūsma apstrādā kreditora izveides scenāriju elementam **Konts**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Izveidot kreditorus konta elementa darbplūsmas procesā](media/create_process.png)

2. <span data-ttu-id="2c5fc-119">Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Atjaunināt kreditorus konta elementā**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="2c5fc-120">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-120">Then select **OK**.</span></span> <span data-ttu-id="2c5fc-121">Šī darbplūsma apstrādā kreditora atjaunināšanas scenāriju elementam **Konts**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="2c5fc-122">Izveidojiet darbplūsmas procesu elementam **Konts** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus kreditoru elementā**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="2c5fc-123">Izveidojiet darbplūsmas procesu elementam **Konts** un atlasiet darbplūsmas procesa veidni **Atjaunināt kreditorus kreditoru elementā**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="2c5fc-124">Darbplūsmas var konfigurēt vai nu kā reāllaika vai fona darbplūsmas, atkarībā no jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="2c5fc-125">Lai konfigurētu darbplūsmu kā fona darbplūsmu, atlasiet **Pārvērst par fona darbplūsmu.**</span><span class="sxs-lookup"><span data-stu-id="2c5fc-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Poga Konvertēt uz fona darbplūsmu](media/background_workflow.png)

6. <span data-ttu-id="2c5fc-127">Aktivizējiet darbplūsmas, ko izveidojāt elementos **Konts** un **Kreditors** , lai sāktu izmantot elementu **Konts** , lai glabātu informāciju kreditoriem no veida **Organizācija**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="2c5fc-128">Izmantot paplašināto kreditoru noformējumu Personas veida kreditoriem</span><span class="sxs-lookup"><span data-stu-id="2c5fc-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="2c5fc-129">**Dynamics365FinanceExtended** risinājuma pakotnē ir šādas darbplūsmas procesa veidnes.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="2c5fc-130">Katrai veidnei tiks izveidota darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="2c5fc-131">Izveidot kreditorus ar veidu Persona kreditoru elementā</span><span class="sxs-lookup"><span data-stu-id="2c5fc-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="2c5fc-132">Izveidot kreditorus ar veidu Persona kontaktpersonu elementā</span><span class="sxs-lookup"><span data-stu-id="2c5fc-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="2c5fc-133">Atjaunināt kreditorus ar veidu Persona kontaktpersonu elementā</span><span class="sxs-lookup"><span data-stu-id="2c5fc-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="2c5fc-134">Atjaunināt kreditorus ar veidu Persona kreditoru elementā</span><span class="sxs-lookup"><span data-stu-id="2c5fc-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="2c5fc-135">Lai izveidotu jaunus darbplūsmas procesus, izmantojot darbplūsmas procesa veidnes, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="2c5fc-136">Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus ar veidu Persona kontaktpersonu elementā**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="2c5fc-137">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-137">Then select **OK**.</span></span> <span data-ttu-id="2c5fc-138">Šī darbplūsma apstrādā kreditora izveides scenāriju elementam **Kontaktpersona**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="2c5fc-139">Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Atjaunināt kreditorus ar veidu Persona kontaktpersonu elementā**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="2c5fc-140">Tad atl. **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-140">Then select **OK**.</span></span> <span data-ttu-id="2c5fc-141">Šī darbplūsma apstrādā kreditora atjaunināšanas scenāriju elementam **Kontaktpersona**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="2c5fc-142">Izveidojiet darbplūsmas procesu elementam **Kontaktpersona** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus ar veidu Persona kreditoru elementā**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="2c5fc-143">Izveidojiet darbplūsmas procesu elementam **Kontaktpersona** un atlasiet darbplūsmas procesa veidni **Atjaunināt kreditorus ar veidu Persona kreditoru elementā**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="2c5fc-144">Darbplūsmas var konfigurēt vai nu kā reāllaika vai fona darbplūsmas, atkarībā no jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="2c5fc-145">Lai konfigurētu darbplūsmu kā fona darbplūsmu, atlasiet **Pārvērst par fona darbplūsmu.**</span><span class="sxs-lookup"><span data-stu-id="2c5fc-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="2c5fc-146">Aktivizējiet darbplūsmas, ko izveidojāt elementos **Kontaktpersona** un **Kreditors** , lai sāktu izmantot elementu **Kontaktpersona** , lai glabātu informāciju kreditoriem no veida **Persona**.</span><span class="sxs-lookup"><span data-stu-id="2c5fc-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
