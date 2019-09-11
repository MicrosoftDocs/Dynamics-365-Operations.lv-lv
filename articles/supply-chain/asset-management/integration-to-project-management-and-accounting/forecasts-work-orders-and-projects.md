---
title: Prognozes, darba pasūtījumi un projekti
description: Šajā tēmā tiek paskaidrotas prognozes un darba pasūtījuma integrācija ar Projektu pārvaldību un uzskaites moduli modulī Līdzekļu pārvaldība.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886820"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="7c5a5-103">Prognozes, darba pasūtījumi un projekti</span><span class="sxs-lookup"><span data-stu-id="7c5a5-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="7c5a5-104">Modulī Līdzekļu pārvaldība tiek veikta integrācija ar **Projektu pārvaldību un uzskaites** moduli izmaksu kontroles optimizācijai, ļaujot lietotājiem izsekot izmaksas par uzturēšanas darba tipa prognozēm un darba pasūtījumu uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-104">In Asset Management, integration to the **Project management and accounting** module is done to optimize cost control, allowing users to track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="7c5a5-105">Lai izsekotu uzturēšanas darba tipa prognozes, ir jāveic divi iestatījumi:</span><span class="sxs-lookup"><span data-stu-id="7c5a5-105">To track maintenance job type forecasts, two settings must be made:</span></span>

1. <span data-ttu-id="7c5a5-106">Atlasiet projektu sadaļā **Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļu pārvaldības parametri** >  saite **Līdzekļi** > **Projekts** FastTab > lauks **Uzturēšanas prognozes projekts**.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-106">Select a project in **Asset management** > **Setup** > **Asset management parameters** > **Assets** link > **Project** FastTab > **Maintenance forecast project** field.</span></span>

2. <span data-ttu-id="7c5a5-107">Sadaļā **Uzturēšanas darba tipa noklusējumi**, veidojot uzturēšanas darba tipa noklusējuma rindu, rindai automātiski tiek izveidots darbības numurs (**Līdzekļu pārvaldība** > **Iestatīšana** > **Darbi** > **Uzturēšanas darba tipa noklusējumi**).</span><span class="sxs-lookup"><span data-stu-id="7c5a5-107">In **Maintenance job type defaults**, when you create a mainteance job type default line, an activity number is automatically created for the line (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="7c5a5-108">Uzturēšanas darba tipa prognozes kalpo diviem mērķiem: varat izsekot izmaksas par uzturēšanas darba tipa prognozēm modulī **Projektu pārvaldība un uzskaite**.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-108">Maintenance job type forecasts serve two purposes: You are able to track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> <span data-ttu-id="7c5a5-109">Turklāt prognozes tiek automātiski pārceltas darba pasūtījuma uzdevuma projektā, izvēloties uzturēšanas darba tipu darba pasūtījuma uzdevumam.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-109">Furthermore, forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="7c5a5-110">Lai izsekotu izmaksas par darba pasūtījumu uzdevumiem, sākumā jums ir jāiestata darba pasūtījumu projekti.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-110">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="7c5a5-111">Procedūras aprakstam skatiet rakstu [Darba pasūtījuma projekta iestatīšana](../setup-for-work-orders/work-order-project-setup.md).</span><span class="sxs-lookup"><span data-stu-id="7c5a5-111">Refer to the [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) section for a description of the procedure.</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="7c5a5-112">Darba pasūtījumu uzdevumu projekti</span><span class="sxs-lookup"><span data-stu-id="7c5a5-112">Work order job projects</span></span>

<span data-ttu-id="7c5a5-113">Veidojot darba pasūtījuma uzdevumu darba pasūtījumam, darba pasūtījuma projektu nosaka pamatprojekta iestatīšana darba pasūtījumiem sadaļā **Līdzekļu pārvaldība** > **Iestatīšana** > **Darba pasūtījumi** > **Projekta iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-113">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders in **Asset management** > **Setup** > **Work orders** > **Project setup**.</span></span>

<span data-ttu-id="7c5a5-114">Darba pasūtījuma uzdevumu projektus veido, izmantojot šādas darba pasūtījuma informācijas kombināciju:</span><span class="sxs-lookup"><span data-stu-id="7c5a5-114">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="7c5a5-115">Darba pasūtījumam ir atlasīts tips Darba pasūtījums</span><span class="sxs-lookup"><span data-stu-id="7c5a5-115">The Work order type selected on the work order</span></span> 
- <span data-ttu-id="7c5a5-116">Funkcionālais novietojums atbilst līdzeklim darba pasūtījuma uzdevumā</span><span class="sxs-lookup"><span data-stu-id="7c5a5-116">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="7c5a5-117">Līdzeklim atbilstošs Līdzekļa tips darba pasūtījuma uzdevumā</span><span class="sxs-lookup"><span data-stu-id="7c5a5-117">The Asset type related to the asset on the work order job</span></span>  
- <span data-ttu-id="7c5a5-118">Darba pasūtījumā iestatītais Paredzamais sākuma un beigu laiks.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-118">The Expected start and end time set on the work order</span></span>  

<span data-ttu-id="7c5a5-119">Iespējams, ne visa iepriekš minētā informācija ir atrodama darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-119">It is possible that not all of the information mentioned above is found on a work order.</span></span> <span data-ttu-id="7c5a5-120">Tādēļ darba pasūtījuma pamatprojekta meklēšana tiek veikta, izmantojot pieejamo datu kombināciju un atlasot projekta ID, kas atbilst darba pasūtījuma datiem.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-120">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds with work order data.</span></span>

<span data-ttu-id="7c5a5-121">Piemērs. Tālāk redzamajā ilustrācijā līdzekļa tipa iestatījums “Kravas automašīnu programma” nozīmē, ka katrs darba pasūtījuma uzdevums, kas izveidots, izmantojot šo līdzekļa tipu, būs Projekta ID “000186” apakšprojekts.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-121">Example: In the figure below, the setup of asset type "Truck Engine" means that every work order job created with that asset type will be a sub project of Project ID "000186".</span></span>

![1. attēls](media/01-integration-to-pma.png)

<span data-ttu-id="7c5a5-123">Projekta ID darba pasūtījuma uzdevumā un atbilstošās darbības numura mērķis (**Līdzekļu pārvaldība** > **Bieži lietotie** > **Darba pasūtījumi** > **Visi darba pasūtījumi** > sarakstā atlasiet darba pasūtījumu > **Rindas informācija** FastTab > lauks **Projekta ID** un lauks **Darbības numurs**) ir modulī **Projektu pārvaldība un uzskaite** izsekot izmaksas, kas saistītas ar darba pasūtījuma uzdevumu un atlasīto līdzekli darba pasūtījuma uzdevumā.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-123">The purpose of the project ID on the work order job, and the related activity number (**Asset management** > **Common** > **Work orders** > **All Work orders** > select work order in list > **Line details** FastTab > **Project ID** field and **Activity number** field), is to track costs related to the work order job, and the asset selected on the work order job, in the **Project management and accounting** module.</span></span> 

<span data-ttu-id="7c5a5-124">Tālāk redzamajā ilustrācijā varat redzēt grafisku pārskatu par darba pasūtījumu projektiem un atbilstošām projektu aktivitātēm.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-124">In the figure below, you see a graphic overview of work order projects and related project activities.</span></span>

![2. attēls](media/02-integration-to-pma.png)

<span data-ttu-id="7c5a5-126">Darba pasūtījumā veidojot jaunu darba pasūtījuma uzdevumu, automātiski uzdevumam tiek izveidots darba pasūtījuma projekts.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-126">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="7c5a5-127">Finanšu dimensijas līdzeklim, kas atbilst darba pasūtījuma uzdevumam, automātiski tiek pārceltas uz darba pasūtījuma projektu.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-127">The financial dimensions for the asset related to the work order job are automatically transferred to the work order project.</span></span> <span data-ttu-id="7c5a5-128">Projekta darbībai, kas izveidota darba pasūtījuma uzdevumam, ir atbilstoša tai pievienotā informācija par uzturēšanas darba tipu, uzturēšanas darba tipa variantu un tirdzniecību.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-128">The project activity created for a work order job has related information attached to it regarding maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="7c5a5-129">Šie dati ir noderīgi, ja, piemēram, no darba pasūtījuma izveidojat pirkšanas pasūtījumu (skatiet [Sagāde](../work-orders/procurement.md)) vai izmantojat moduli **Projektu pārvaldība un uzskaite** laika reģistrācijai.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-129">Those data are useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>  

<span data-ttu-id="7c5a5-130">Ja līdzeklis tika instalēts funkcionālajā novietojumā un šis līdzeklis vēlāk tiek instalēts citā funkcionālajā novietojumā, finanšu dimensijas, kas atbilst jaunajam funkcionālajam novietojumam tiek automātiski atjaunināti līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-130">If the asset was installed on a functional location, and that asset is later installed on another functional location, the financial dimensions related to the new functional location is automatically updated on the asset.</span></span> <span data-ttu-id="7c5a5-131">Pēc tam, veidojot darba pasūtījuma uzdevumu līdzeklim, darba pasūtījuma projekts darba pasūtījuma uzdevumam automātiski iegūs finanšu dimensijas, kas tagad atbilst līdzeklim.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-131">Subsequently, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="7c5a5-132">Tas nozīmē, ka izmantojot funkcionālos novietojumus, vienmēr var izsekot izmaksas funkcionālajos novietojumos, kuros līdzeklis ticis instalēts jebkurā noteiktajā laikā.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-132">This means that when you use functional locations, costs can always be tracked on the functional locations on which an asset was installed at any given time.</span></span> <span data-ttu-id="7c5a5-133">Finanšu dimensiju automātiskā atjaunināšana nodrošina pilnīgu izmaksu izsekojamību projekta kontrolēšanai un pārskatu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-133">The automatic update of financial dimensions ensures complete traceability of costs for project controlling and reporting.</span></span>  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="7c5a5-134">Darba pasūtījumu projekti, darba pasūtījumu dzīves cikla stāvokļi, projekta posmi un projektu tipi</span><span class="sxs-lookup"><span data-stu-id="7c5a5-134">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="7c5a5-135">Lai nodrošinātu pareizu darba pasūtījumu dzīves cikla stāvokļu izmantošanu un atbilstošus projekta posmus darba pasūtījumiem, ņemiet vērā atkarības attiecībā uz moduli **Projektu pārvaldība un uzskaite**:</span><span class="sxs-lookup"><span data-stu-id="7c5a5-135">To ensure correct use of work order lifecycle states and related project stages on work orders, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="7c5a5-136">Modulī **Projektu pārvaldība un uzskaite** projektu posmi iestatīti projektu veidiem sadaļā **Projektu pārvaldības un uzskaites parametri**.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-136">In the **Project management and accounting** module, project stages are set up on project types in **Project management and accounting parameters**.</span></span>  
- <span data-ttu-id="7c5a5-137">Sadaļā **Projektu pārvaldības un uzskaites parametri** neaizmirstiet atlasīt atbilstošā projekta posma izvēles rūtiņas visiem projektu tipiem, kurus plānojat izmantot.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-137">In **Project management and accounting parameters**, remember to select relevant project stage check boxes for all the project types you are going to use.</span></span> <span data-ttu-id="7c5a5-138">Tālāk redzamajā ilustrācijā pieci posmi **Izveidots** - **Novērtēts** - **Ieplānots** - **Procesā** - **Pabeigts** tika atlasīti projektu tipiem “Laiks un materiāls” un “Iekšējais”.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-138">In the figure below, five stages **Created** - **Estimated** - **Scheduled** - **In process** - **Finished** have been selected for the project types "Time and material" and "Internal".</span></span> <span data-ttu-id="7c5a5-139">Šie pieci posmi atbilst gan iekšējai uzturēšanai, gan pakalpojumu uzturēšanas darbiem.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-139">Those five stages are relevant for both internal maintenance and service maintenance jobs.</span></span>  
- <span data-ttu-id="7c5a5-140">Sadaļā **Līdzekļu pārvaldība** projektu tipi ir noteikti pēc projektu grupām, ko iestatāt veidlapā **Darba pasūtījuma projekta iestatīšana** > saite **Projekta grupa**.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-140">In **Asset Management**, project types are defined by the project groups you set up in the **Work order project setup** form > **Project group** link.</span></span>  
- <span data-ttu-id="7c5a5-141">Projektu grupu iestatīšana sadaļā **Darba pasūtījuma projekta iestatīšana** izmanto, veidojot darba pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-141">The project groups setup in **Work order project setup** are used when you create work orders.</span></span> <span data-ttu-id="7c5a5-142">Izveidojot darba pasūtījumu, darba pasūtījumam automātiski tiek izveidots darba pasūtījuma projekts.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-142">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="7c5a5-143">Katram darba pasūtījuma dzīves cikla stāvoklim ir atbilstošs projekta posms.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-143">Work order lifecycle states must each have a related project stage.</span></span>  
- <span data-ttu-id="7c5a5-144">Projekta posms, kas atbilst darba pasūtījuma dzīves cikla stāvoklim, ir jādefinē kā aktīvs posms projekta grupai, kas noteikta darba pasūtījuma projektā.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-144">The project stage related to a work order lifecycle state must be defined as an active stage for the project group defined in the work order project.</span></span> <span data-ttu-id="7c5a5-145">Darba pasūtījumam automātiski tiek izveidots darba pasūtījuma projekts.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-145">The work order project is automatically created on a work order.</span></span>  
- <span data-ttu-id="7c5a5-146">Veidojot jaunu darba pasūtījumu, darba pasūtījuma projekta automātiskā piešķiršana balstās uz iestatīšanu sadaļā **Darba pasūtījuma projekta iestatīšana** (**Līdzekļu pārvaldība** > **Iestatīšana** > **Darbu pasūtījumi** > **Projektu iestatīšana**).</span><span class="sxs-lookup"><span data-stu-id="7c5a5-146">When you create a new work order, the automatic allocation of a work order project is based on the setup in **Work order project setup** (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  

<span data-ttu-id="7c5a5-147">Saistības starp darba pasūtījumu projektu grupām, atbilstošajiem projektu tipiem, projektu posmiem un darba pasūtījumu dzīves cikla stāvokļiem ir parādīti tālāk redzamajās ilustrācijās.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-147">Associations between work order project groups, related project types, project stages, and work order lifecycle states are shown in the figures below.</span></span>  

![3. attēls](media/03-integration-to-pma.png)

![4. attēls](media/04-integration-to-pma.png)

![5. attēls](media/05-integration-to-pma.png)

<span data-ttu-id="7c5a5-151">Skatiet rakstu [Darba pasūtījuma projekta iestatīšana](../setup-for-work-orders/work-order-project-setup.md), kā iestatīt darba pasūtījumu projektus un [Darba pasūtījumu dzīves cikla stāvokļi ](../setup-for-work-orders/work-order-lifecycle-states.md) kā izveidot darba pasūtījumu dzīves cikla stāvokļus.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-151">Refer to [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) regarding how to set up work order projects, and to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) regarding how to create work order lifecycle states.</span></span>

<span data-ttu-id="7c5a5-152">Tālāk redzamajā ilustrācijā ir sniegts grafisks pārskats par dažādiem projektiem, kas izveidoti modulī **Līdzekļu pārvaldība**, lai atļautu integrāciju ar moduli **Projektu vadība un uzskaite**, kā arī par darba procesiem, kuriem atbilst projekti.</span><span class="sxs-lookup"><span data-stu-id="7c5a5-152">The figure below shows a graphic overview of the various projects that are created in the **Asset management** module to allow integration with the **Project management and accounting** module, as well as the work processes to which the projects are related.</span></span>

![6. attēls](media/06-integration-to-pma.png)

