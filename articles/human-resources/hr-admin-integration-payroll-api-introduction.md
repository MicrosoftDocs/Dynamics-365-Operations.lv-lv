---
title: Payroll integrācijas API ieviešana
description: Šajā tēmā aprakstīts Dynamics 365 Human Resources Payroll integrācijas API.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a7be5ad42642de48ffdb2731a1300a953c5ede4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022767"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="da14a-103">Payroll integrācijas API ieviešana</span><span class="sxs-lookup"><span data-stu-id="da14a-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="da14a-104">Šajā dokumentā aprakstīts Dynamics 365 Human Resources Payroll integrācijas API.</span><span class="sxs-lookup"><span data-stu-id="da14a-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="da14a-105">API iespējo racionalizētu “no gala līdz galam” integrēšanu starp Human Resources un partnerattiecībām algu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="da14a-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="da14a-106">Pakalpojumā Human Resources sākas integrētā pieredze ar darbinieka profilu, algu, ieturējumu un ieguldījumu informāciju.</span><span class="sxs-lookup"><span data-stu-id="da14a-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="da14a-107">Nolīgjot darbinieku un ievadot nepieciešamo profilu un apmaksas informāciju sistēmā Human Resources, algu sistēma izvelk šo informāciju, lai to izmantotu algas apstrādes laikā.</span><span class="sxs-lookup"><span data-stu-id="da14a-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="da14a-108">Visi darbiniekam veiktie atjauninājumi vai maksājuma informācija arī tiek izvilkti izmantošanai vēlākās algas izpildes.</span><span class="sxs-lookup"><span data-stu-id="da14a-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![Payroll integrācijas plūsma](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="da14a-110">Lai iespējotu integrāciju, Human Resources satur šādus komponentus:</span><span class="sxs-lookup"><span data-stu-id="da14a-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="da14a-111">Funkcionalitāte, lai atzīmētu darbinieku kā gatavu apmaksai</span><span class="sxs-lookup"><span data-stu-id="da14a-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="da14a-112">Integrācijas API, kas atver jauno funkcionalitāti programmu integrēšanai</span><span class="sxs-lookup"><span data-stu-id="da14a-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="da14a-113">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="da14a-113">Microsoft Dataverse</span></span>

<span data-ttu-id="da14a-114">Šis API ir veidots Microsoft Dataverse (iepriekš Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="da14a-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="da14a-115">Visa RESTful mijiedarbība ar šo API tiek veikta, izmantojot Microsoft Dataverse Web API, kas izmanto OData.</span><span class="sxs-lookup"><span data-stu-id="da14a-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="da14a-116">Šis API ir Dataverse Web API apakškopa.</span><span class="sxs-lookup"><span data-stu-id="da14a-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="da14a-117">Dataverse Web API nosaka tādus raksturlielumus kā autentifikācija, SLA, pakete, vienlaicīguma kontrole un kļūdu apstrāde.</span><span class="sxs-lookup"><span data-stu-id="da14a-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="da14a-118">Vispārīgāku informāciju par Microsoft Dataverse Web API skatiet šeit:</span><span class="sxs-lookup"><span data-stu-id="da14a-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="da14a-119">Kas ir Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="da14a-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="da14a-120">Izmantot Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="da14a-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="da14a-121">Microsoft Dataverse izstrādātāja rokasgrāmata</span><span class="sxs-lookup"><span data-stu-id="da14a-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="da14a-122">Šajā dokumentācijā ir ietverta detalizēta informācija un izstrādātāja norādījumi par Dataverse Web API izmantošanu, ietverot šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="da14a-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="da14a-123">Autentificēties pakalpojumā Microsoft Dataverse ar Web API</span><span class="sxs-lookup"><span data-stu-id="da14a-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="da14a-124">Veikt operācijas, izmantojot Web API</span><span class="sxs-lookup"><span data-stu-id="da14a-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="da14a-125">Izmantot Postman ar Web API</span><span class="sxs-lookup"><span data-stu-id="da14a-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="da14a-126">Izmantot izmaiņu izsekošanu, lai sinhronizētu datus ar ārējām sistēmām</span><span class="sxs-lookup"><span data-stu-id="da14a-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="da14a-127">Virtuālie tabulas Human Resources programmā Dataverse</span><span class="sxs-lookup"><span data-stu-id="da14a-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="da14a-128">Galapunkti Payroll integrācijai API izmanto Microsoft Dataverse virtuālās tabulas platformas iespējas.</span><span class="sxs-lookup"><span data-stu-id="da14a-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="da14a-129">Pēc noklusējuma virtuālās tabulas un to saistītie API galapunkti nav izvietoti Human Resources vidēs, iespējojot organizācijas, lai noteiktu, kuri OData galapunkti būs redzami vidē.</span><span class="sxs-lookup"><span data-stu-id="da14a-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="da14a-130">Lai izmantotu API, videi ir jāizveido Human Resources elementu virtuālās tabulas.</span><span class="sxs-lookup"><span data-stu-id="da14a-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="da14a-131">Informāciju par API virtuālo tabulu ģenerēšanu skatiet [Konfigurēt Dataverse virtuālās tabulas](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="da14a-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="da14a-132">Datu modelis</span><span class="sxs-lookup"><span data-stu-id="da14a-132">Data model</span></span>

<span data-ttu-id="da14a-133">Sekojošā diagramma attēlo attiecības API.</span><span class="sxs-lookup"><span data-stu-id="da14a-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="da14a-134">Vairākiem veidiem ir ārējās atslēgas citām, iepriekš esošām Human Resources entītijām, kas šeit nav attēlotas.</span><span class="sxs-lookup"><span data-stu-id="da14a-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="da14a-135">Šajā dokumentā ir sniegta informācija par elementiem, kas ir specifiski darbā algas integrācijas scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="da14a-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="da14a-136">Tomēr Web API ir daudzi citi elementi Dataverse Web API programmai Human Resources, kas var būt atbilstīgi jūsu integrācijai.</span><span class="sxs-lookup"><span data-stu-id="da14a-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="da14a-137">Dažiem no šiem elementiem ir atsauces ārējās atslēgas attiecībās vai navigācijas rekvizītos.</span><span class="sxs-lookup"><span data-stu-id="da14a-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Payroll integrācijas API datu modelis](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="da14a-139">Payroll darbinieks un saistītie elementi</span><span class="sxs-lookup"><span data-stu-id="da14a-139">Payroll employee and related entities</span></span>

<span data-ttu-id="da14a-140">Elementi:</span><span class="sxs-lookup"><span data-stu-id="da14a-140">Entities:</span></span>

- [<span data-ttu-id="da14a-141">Algots darbinieks</span><span class="sxs-lookup"><span data-stu-id="da14a-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="da14a-142">Algas nodarbinātā adrese</span><span class="sxs-lookup"><span data-stu-id="da14a-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="da14a-143">Algu aprēķina fiksētās atlīdzības plāns</span><span class="sxs-lookup"><span data-stu-id="da14a-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="da14a-144">Algas pozīcijas darbs</span><span class="sxs-lookup"><span data-stu-id="da14a-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="da14a-145">Algas pozīcija</span><span class="sxs-lookup"><span data-stu-id="da14a-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="da14a-146">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="da14a-146">See also</span></span>

[<span data-ttu-id="da14a-147">Algu aprēķina elementu ģenerēšana un pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="da14a-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="da14a-148">Konfigurēt Human Resources parametrus</span><span class="sxs-lookup"><span data-stu-id="da14a-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="da14a-149">Konfigurēt Human Resources koplietotos parametrus</span><span class="sxs-lookup"><span data-stu-id="da14a-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="da14a-150">Kas ir Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="da14a-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="da14a-151">Izmantot Microsoft Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="da14a-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]