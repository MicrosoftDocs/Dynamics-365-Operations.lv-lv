---
title: Pārslēgšanās starp kreditoru noformējumiem
description: Šajā tēmā ir aprakstīts, kā pārslēgties starp kreditora datu integrāciju starp Finance and Operations programmām un Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 78d4c547f544d95c66490e5610374a5c4598b266
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565603"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="559c7-103">Pārslēgšanās starp kreditoru noformējumiem</span><span class="sxs-lookup"><span data-stu-id="559c7-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="559c7-104">Kreditora datu plūsma</span><span class="sxs-lookup"><span data-stu-id="559c7-104">Vendor data flow</span></span> 

<span data-ttu-id="559c7-105">Ja izvēlaties izmantot elementu **Konts** elementu, lai uzglabātu veidu **Organizācija** un tabulu **Kontaktpersona** veida **Persona** tipa kreditoriem, konfigurējiet šādas darbplūsmas.</span><span class="sxs-lookup"><span data-stu-id="559c7-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="559c7-106">Pretējā gadījumā šī konfigurācija nav obligāta.</span><span class="sxs-lookup"><span data-stu-id="559c7-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="559c7-107">Izmantot paplašināto kreditoru noformējumu Organizācijas veida kreditoriem</span><span class="sxs-lookup"><span data-stu-id="559c7-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="559c7-108">**Dynamics365FinanceExtended** risinājuma pakotnē ir šādas darbplūsmas procesa veidnes.</span><span class="sxs-lookup"><span data-stu-id="559c7-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="559c7-109">Katrai veidnei tiks izveidota darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="559c7-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="559c7-110">Kreditoru izveide kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="559c7-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="559c7-111">Kreditoru izveide kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="559c7-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="559c7-112">Kreditoru atjaunināšana kontu tabulā</span><span class="sxs-lookup"><span data-stu-id="559c7-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="559c7-113">Kreditoru atjaunināšana kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="559c7-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="559c7-114">Lai izveidotu jaunus darbplūsmas procesus, izmantojot darbplūsmas procesa veidnes, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="559c7-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="559c7-115">Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus konta tabulā**.</span><span class="sxs-lookup"><span data-stu-id="559c7-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="559c7-116">Pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="559c7-116">Then select **OK**.</span></span> <span data-ttu-id="559c7-117">Šī darbplūsma apstrādā kreditora izveides scenāriju tabulai **Konts**.</span><span class="sxs-lookup"><span data-stu-id="559c7-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![Izveidot kreditorus konta tabulas darbplūsmas procesā](media/create_process.png)

2. <span data-ttu-id="559c7-119">Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus konta tabulā**.</span><span class="sxs-lookup"><span data-stu-id="559c7-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="559c7-120">Pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="559c7-120">Then select **OK**.</span></span> <span data-ttu-id="559c7-121">Šī darbplūsma apstrādā kreditora atjaunināšanas scenāriju tabulai **Konts**.</span><span class="sxs-lookup"><span data-stu-id="559c7-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="559c7-122">Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus konta tabulā**.</span><span class="sxs-lookup"><span data-stu-id="559c7-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="559c7-123">Izveidojiet darbplūsmas procesu elementam **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus konta tabulā**.</span><span class="sxs-lookup"><span data-stu-id="559c7-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="559c7-124">Darbplūsmas var konfigurēt vai nu kā reāllaika vai fona darbplūsmas, atkarībā no jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="559c7-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="559c7-125">Lai konfigurētu darbplūsmu kā fona darbplūsmu, atlasiet **Pārvērst par fona darbplūsmu.**</span><span class="sxs-lookup"><span data-stu-id="559c7-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Poga Konvertēt uz fona darbplūsmu](media/background_workflow.png)

6. <span data-ttu-id="559c7-127">Aktivizējiet darbplūsmas, ko izveidojāt tabulās **Konts** un **Kreditors**, lai sāktu izmantot elementu **Konts**, lai glabātu informāciju kreditoriem no veida **Organizācija**.</span><span class="sxs-lookup"><span data-stu-id="559c7-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="559c7-128">Izmantot paplašināto kreditoru noformējumu Personas veida kreditoriem</span><span class="sxs-lookup"><span data-stu-id="559c7-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="559c7-129">**Dynamics365FinanceExtended** risinājuma pakotnē ir šādas darbplūsmas procesa veidnes.</span><span class="sxs-lookup"><span data-stu-id="559c7-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="559c7-130">Katrai veidnei tiks izveidota darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="559c7-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="559c7-131">Izveidot kreditorus ar veidu Persona kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="559c7-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="559c7-132">Izveidot kreditorus ar veidu Persona kontaktpersonu tabulā</span><span class="sxs-lookup"><span data-stu-id="559c7-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="559c7-133">Atjaunināt kreditorus ar veidu Persona kontaktpersonu tabulā</span><span class="sxs-lookup"><span data-stu-id="559c7-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="559c7-134">Atjaunināt kreditorus ar veidu Persona kreditoru tabulā</span><span class="sxs-lookup"><span data-stu-id="559c7-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="559c7-135">Lai izveidotu jaunus darbplūsmas procesus, izmantojot darbplūsmas procesa veidnes, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="559c7-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="559c7-136">Izveidojiet darbplūsmas procesu tabulai **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus ar veidu Persona Kontaktpersonu tabulā** darbplūsmas procesa veidnē.</span><span class="sxs-lookup"><span data-stu-id="559c7-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="559c7-137">Pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="559c7-137">Then select **OK**.</span></span> <span data-ttu-id="559c7-138">Šī darbplūsma apstrādā kreditora izveides scenāriju tabulai **Kontaktpersona**.</span><span class="sxs-lookup"><span data-stu-id="559c7-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="559c7-139">Izveidojiet darbplūsmas procesu tabulai **Kreditors** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus ar veidu Persona Kontaktpersonu tabulā** darbplūsmas procesa veidnē.</span><span class="sxs-lookup"><span data-stu-id="559c7-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="559c7-140">Pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="559c7-140">Then select **OK**.</span></span> <span data-ttu-id="559c7-141">Šī darbplūsma apstrādā kreditora atjaunināšanas scenāriju tabulai **Kontaktpersona**.</span><span class="sxs-lookup"><span data-stu-id="559c7-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="559c7-142">Izveidojiet darbplūsmas procesu tabulai **Kontaktpersona** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus ar veidu Persona kreditoru tabulā**.</span><span class="sxs-lookup"><span data-stu-id="559c7-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="559c7-143">Izveidojiet darbplūsmas procesu tabulai **Kontaktpersona** un atlasiet darbplūsmas procesa veidni **Izveidot kreditorus ar veidu Persona kreditoru tabulā**.</span><span class="sxs-lookup"><span data-stu-id="559c7-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="559c7-144">Darbplūsmas var konfigurēt vai nu kā reāllaika vai fona darbplūsmas, atkarībā no jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="559c7-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="559c7-145">Lai konfigurētu darbplūsmu kā fona darbplūsmu, atlasiet **Pārvērst par fona darbplūsmu.**</span><span class="sxs-lookup"><span data-stu-id="559c7-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="559c7-146">Aktivizējiet darbplūsmas, ko izveidojāt tabulās **Kontaktpersona** un **Kreditors**, lai sāktu izmantot elementu **Kontaktpersona**, lai glabātu informāciju kreditoriem no veida **Persona**.</span><span class="sxs-lookup"><span data-stu-id="559c7-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]