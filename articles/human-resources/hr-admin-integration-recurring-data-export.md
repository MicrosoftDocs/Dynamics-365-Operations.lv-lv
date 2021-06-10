---
title: Periodiskas datu eksportēšanas programmas izveide
description: Šajā rakstā parādīts, kā izveidot Microsoft Azure loģikas programmu, kas eksportē datus no Microsoft Dynamics 365 Human Resources uz periodisku grafiku.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a4a963bcfe5932f5642b43751ccd96c472fec0d9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055008"
---
# <a name="create-a-recurring-data-export-app"></a><span data-ttu-id="b38b4-103">Periodiskas datu eksportēšanas programmas izveide</span><span class="sxs-lookup"><span data-stu-id="b38b4-103">Create a recurring data export app</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b38b4-104">Šajā rakstā parādīts, kā izveidot Microsoft Azure loģikas programmu, kas eksportē datus no Microsoft Dynamics 365 Human Resources uz periodisku grafiku.</span><span class="sxs-lookup"><span data-stu-id="b38b4-104">This article shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 Human Resources on a recurring schedule.</span></span> <span data-ttu-id="b38b4-105">Lai eksportētu datus, apmācība izmanto Human Resources DMF pakotnes REST programmas programmēšanas interfeisa (API) sniegtās priekšrocības.</span><span class="sxs-lookup"><span data-stu-id="b38b4-105">The tutorial takes advantage of Human Resources' DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="b38b4-106">Kad dati ir eksportēti, loģikas programma saglabā eksportēto datu pakotni Microsoft OneDrive biznesam mapē.</span><span class="sxs-lookup"><span data-stu-id="b38b4-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="b38b4-107">Biznesa scenārijs</span><span class="sxs-lookup"><span data-stu-id="b38b4-107">Business scenario</span></span>

<span data-ttu-id="b38b4-108">Vienā tipiskā biznesa scenārijā Microsoft Dynamics 365 integrācijām, dati periodiskā grafikā ir jāeksportē uz pakārtoto sistēmu.</span><span class="sxs-lookup"><span data-stu-id="b38b4-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="b38b4-109">Šajā apmācībā parādīts, kā eksportēt visus nodarbinātā ierakstus no Microsoft Dynamics 365 Human Resources un saglabāt nodarbināto sarakstu OneDrive biznesam mapē.</span><span class="sxs-lookup"><span data-stu-id="b38b4-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 Human Resources and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="b38b4-110">Konkrētie dati, kas tiek eksportēti šajā apmācībā, un eksportēto datu galamērķis ir tikai piemēri.</span><span class="sxs-lookup"><span data-stu-id="b38b4-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="b38b4-111">Tos var viegli mainīt, lai atbilstu jūsu biznesa vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="b38b4-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="b38b4-112">Izmantotās tehnoloģijas</span><span class="sxs-lookup"><span data-stu-id="b38b4-112">Technologies used</span></span>

<span data-ttu-id="b38b4-113">Šī apmācība izmanto tālāk minētās tehnoloģijas.</span><span class="sxs-lookup"><span data-stu-id="b38b4-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="b38b4-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** — pamatdatu avots par nodarbinātajiem, kas tiks eksportēts.</span><span class="sxs-lookup"><span data-stu-id="b38b4-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="b38b4-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** — tehnoloģija, kas nodrošina periodiskās eksportēšanas saskaņošanu un plānošanu.</span><span class="sxs-lookup"><span data-stu-id="b38b4-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="b38b4-116">**[Savienotāji](/azure/connectors/apis-list)** — tehnoloģija, kas tiek izmantota, lai savienotu loģikas programmu ar nepieciešamajiem galapunktiem.</span><span class="sxs-lookup"><span data-stu-id="b38b4-116">**[Connectors](/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="b38b4-117">[HTTP ar Azure AD](/connectors/webcontents/) savienotāju</span><span class="sxs-lookup"><span data-stu-id="b38b4-117">[HTTP with Azure AD](/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="b38b4-118">[OneDrive biznesam](/azure/connectors/connectors-create-api-onedriveforbusiness) savienotājs</span><span class="sxs-lookup"><span data-stu-id="b38b4-118">[OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="b38b4-119">**[DMF pakotnes REST API](../fin-ops-core/dev-itpro/data-entities/data-management-api.md)** — tehnoloģija, kas tiek izmantota, lai izraisītu eksportēšanu un pārraudzītu tā norisi.</span><span class="sxs-lookup"><span data-stu-id="b38b4-119">**[DMF package REST API](../fin-ops-core/dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="b38b4-120">**[OneDrive biznesam](https://onedrive.live.com/about/business/)** — eksportēto nodarbināto galamērķis.</span><span class="sxs-lookup"><span data-stu-id="b38b4-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b38b4-121">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="b38b4-121">Prerequisites</span></span>

<span data-ttu-id="b38b4-122">Pirms sākt vingrinājumu šajā apmācībā, nepieciešami tālāk minētie vienumi.</span><span class="sxs-lookup"><span data-stu-id="b38b4-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="b38b4-123">Human Resources vide, kam ir administratora līmeņa atļaujas vidē</span><span class="sxs-lookup"><span data-stu-id="b38b4-123">A Human Resources environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="b38b4-124">[Azure abonements](https://azure.microsoft.com/free/), lai viesotu loģikas programmu</span><span class="sxs-lookup"><span data-stu-id="b38b4-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="b38b4-125">Vingrinājums</span><span class="sxs-lookup"><span data-stu-id="b38b4-125">The exercise</span></span>

<span data-ttu-id="b38b4-126">Šī vingrinājuma beigās jums būs loģikas programma, kas ir savienota ar jūsu Human Resources vidi un jūsu OneDrive biznesam kontu.</span><span class="sxs-lookup"><span data-stu-id="b38b4-126">At the end of this exercise, you will have a logic app that is connected to your Human Resources environment and your OneDrive for Business account.</span></span> <span data-ttu-id="b38b4-127">Loģikas programma eksportēs datu pakotni no Human Resources, gaidiet, kamēr tiks pabeigta eksportēšana, lejupielādējiet eksportēto datu pakotni un saglabājiet to OneDrive biznesam norādītajā mapē.</span><span class="sxs-lookup"><span data-stu-id="b38b4-127">The logic app will export a data package from Human Resources, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="b38b4-128">Pabeigtā loģikas programma būs līdzīga tālāk redzamajam attēlam.</span><span class="sxs-lookup"><span data-stu-id="b38b4-128">The completed logic app will resemble the following illustration.</span></span>

![Loģikas programmas pārskats](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a><span data-ttu-id="b38b4-130">1. darbība: datu eksportēšanas projekta izveide Human Resources</span><span class="sxs-lookup"><span data-stu-id="b38b4-130">Step 1: Create a data export project in Human Resources</span></span>

<span data-ttu-id="b38b4-131">Human Resources izveidojiet datu eksportēšanas projektu, kas eksportē nodarbinātos.</span><span class="sxs-lookup"><span data-stu-id="b38b4-131">In Human Resources, create a data export project that exports workers.</span></span> <span data-ttu-id="b38b4-132">Nosauciet projektu **Nodarbināto eksportēšana** un pārliecinieties, ka opcija **Ģenerēt datu pakotni** ir iestatīta uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="b38b4-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="b38b4-133">Pievienojiet projektam atsevišķu elementu (**Nodarbinātais**) un atlasiet formātu tā eksportēšanai.</span><span class="sxs-lookup"><span data-stu-id="b38b4-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="b38b4-134">(Šajā pamācībā tiek izmantotsMicrosoft Excel formāts.)</span><span class="sxs-lookup"><span data-stu-id="b38b4-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![Nodarbināto datu projekta eksportēšana](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="b38b4-136">Atcerieties datu eksportēšanas projekta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="b38b4-136">Remember the name of the data export project.</span></span> <span data-ttu-id="b38b4-137">Tas būs nepieciešams, nākamajā darbībā veidojot loģikas programmu.</span><span class="sxs-lookup"><span data-stu-id="b38b4-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="b38b4-138">2. darbība: loģikas programmas izveide</span><span class="sxs-lookup"><span data-stu-id="b38b4-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="b38b4-139">Vingrinājuma lielākā daļa ietver loģikas programmas izveidi.</span><span class="sxs-lookup"><span data-stu-id="b38b4-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="b38b4-140">Izveidojiet loģikas programmu Azure portālā.</span><span class="sxs-lookup"><span data-stu-id="b38b4-140">In the Azure portal, create a logic app.</span></span>

    ![Loģikas programmas izveides lapa](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="b38b4-142">Logic Apps Designer sāciet ar tukšu loģikas programmu.</span><span class="sxs-lookup"><span data-stu-id="b38b4-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="b38b4-143">Pievienojiet [Periodiskuma grafika trigeri](/azure/connectors/connectors-native-recurrence), lai palaistu loģikas programmu ik pēc 24 stundām (vai saskaņā ar izvēlēto grafiku).</span><span class="sxs-lookup"><span data-stu-id="b38b4-143">Add a [Recurrence Schedule trigger](/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![Periodiskuma dialoglodziņš](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="b38b4-145">Izsauciet [ExportToPackage](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API, lai ieplānotu savas datu pakotnes eksportēšanu.</span><span class="sxs-lookup"><span data-stu-id="b38b4-145">Call the [ExportToPackage](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="b38b4-146">Izmantojiet darbību **Izsaukt HTTP pieprasījumu** no HTTP ar Azure AD savienotāju.</span><span class="sxs-lookup"><span data-stu-id="b38b4-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="b38b4-147">**Pamatresursa URL:** jūsu Human Resources vides URL (neietver ceļa/nosaukumvietas informāciju.)</span><span class="sxs-lookup"><span data-stu-id="b38b4-147">**Base Resource URL:** The URL of your Human Resources environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="b38b4-148">**Azure AD Resursa URI:** `http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="b38b4-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="b38b4-149">Human Resources pakalpojums vēl nenodrošina savienotāju, kas sniedz visus API, kas veido DMF pakotnes REST API, piemēram, **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="b38b4-149">The Human Resources service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="b38b4-150">Tā vietā jāizsauc API, izmantojot neapstrādātus HTTPS pieprasījumus, izmantojot HTTP ar Azure AD savienotāju.</span><span class="sxs-lookup"><span data-stu-id="b38b4-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="b38b4-151">Šis savienotājs izmanto Azure Active Directory (Azure AD) autentifikācijai un autorizēšanai Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b38b4-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Human Resources.</span></span>

        ![HTTP ar Azure AD savienotāju](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="b38b4-153">Pierakstieties savā Human Resources vidē, izmantojot HTTP ar Azure AD savienotāju.</span><span class="sxs-lookup"><span data-stu-id="b38b4-153">Sign in to your Human Resources environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="b38b4-154">Iestatiet HTTP **POST** pieprasījumu, lai izsauktu **ExportToPackage** DMF REST API.</span><span class="sxs-lookup"><span data-stu-id="b38b4-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="b38b4-155">**Metode:** POST</span><span class="sxs-lookup"><span data-stu-id="b38b4-155">**Method:** POST</span></span>
        - <span data-ttu-id="b38b4-156">**Pieprasījuma URL:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="b38b4-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="b38b4-157">**Pieprasījuma pamatteksts**</span><span class="sxs-lookup"><span data-stu-id="b38b4-157">**Body of the request:**</span></span>

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![HTTP pieprasījuma darbības izsaukšana](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > <span data-ttu-id="b38b4-159">Iespējams, vēlēsieties pārdēvēt katru darbību, lai tai būtu nozīme salīdzinājumā ar noklusējuma nosaukumu **Izsaukt HTTP pieprasījumu**.</span><span class="sxs-lookup"><span data-stu-id="b38b4-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="b38b4-160">Piemēram, varat pārdēvēt šo darbību **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="b38b4-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="b38b4-161">[Mainīga lieluma inicializācija](/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable), lai glabātu **ExportToPackage** pieprasījuma izpildes statusu.</span><span class="sxs-lookup"><span data-stu-id="b38b4-161">[Initialize a variable](/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![Mainīgā lieluma darbības inicializācija](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="b38b4-163">Uzgaidiet, līdz datu eksportēšanas izpildes statuss ir **Sekmīgs**.</span><span class="sxs-lookup"><span data-stu-id="b38b4-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="b38b4-164">Pievienojiet [Līdz cilpai](/azure/logic-apps/logic-apps-control-flow-loops#until-loop), kas atkārtojas, līdz **ExecutionStatus** mainīgā lieluma vērtība ir **Sekmīgs**.</span><span class="sxs-lookup"><span data-stu-id="b38b4-164">Add an [Until loop](/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="b38b4-165">Pievienojiet darbību **Aizkave**, kas gaida piecas sekundes, pirms aptaujā pašreizējo eksportēšanas izpildes statusu.</span><span class="sxs-lookup"><span data-stu-id="b38b4-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![Līdz cilpas konteiners](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="b38b4-167">Iestatiet ierobežojumu skaitu uz **15**, lai uzgaidītu ne vairāk kā 75 sekundes (15 atkārtojumi x 5 sekundes), kamēr eksportēšana tiks pabeigta.</span><span class="sxs-lookup"><span data-stu-id="b38b4-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="b38b4-168">Ja eksportēšanai nepieciešams ilgāks laiks, koriģējiet ierobežojumu pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="b38b4-168">If your export takes more time, adjust the limit count as appropriate.</span></span>        

    3. <span data-ttu-id="b38b4-169">Pievienojiet darbību **Izsaukt HTTP pieprasījumu**, lai izsauktu [GetExecutionSummaryStatus](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, un iestatiet mainīgo lielumu **ExecutionStatus** uz rezultātu no **GetExecutionSummaryStatus** atbildes.</span><span class="sxs-lookup"><span data-stu-id="b38b4-169">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="b38b4-170">Šis paraugs neveic kļūdu pārbaudi.</span><span class="sxs-lookup"><span data-stu-id="b38b4-170">This sample doesn't do error checking.</span></span> <span data-ttu-id="b38b4-171">**GetExecutionSummaryStatus** API var atgriezt neveiksmīgus termināļa stāvokļus (t.i., stāvokļus, kas nav **Sekmīgs**).</span><span class="sxs-lookup"><span data-stu-id="b38b4-171">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="b38b4-172">Papildinformāciju skatiet [API dokumentācijā](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span><span class="sxs-lookup"><span data-stu-id="b38b4-172">For more information, see the [API documentation](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

        - <span data-ttu-id="b38b4-173">**Metode:** POST</span><span class="sxs-lookup"><span data-stu-id="b38b4-173">**Method:** POST</span></span>
        - <span data-ttu-id="b38b4-174">**Pieprasījuma URL:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="b38b4-174">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="b38b4-175">**Pieprasījuma pamatteksts:** body('Invoke\_an\_HTTP\_request')?['value']</span><span class="sxs-lookup"><span data-stu-id="b38b4-175">**Body of the request:** body('Invoke\_an\_HTTP\_request')?['value']</span></span>

            > [!NOTE]
            > <span data-ttu-id="b38b4-176">Iespējams, vērtība **Pieprasījuma pamatteksts** būs jāievada vai nu koda skatā, vai arī noformētāja funkciju redaktorā.</span><span class="sxs-lookup"><span data-stu-id="b38b4-176">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![HTTP pieprasījuma 2. darbības izsaukšana](media/integration-logic-app-get-execution-status-step.png)

        ![Mainīgā lieluma darbības iestatīšana](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="b38b4-179">Darbības **Iestatīt mainīgo lielumu** vērtība (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) atšķirsies no **Izsaukt HTTP 2. pieprasījumu** pamatteksta vērtības, lai arī noformētājs parādīs vērtības vienādi.</span><span class="sxs-lookup"><span data-stu-id="b38b4-179">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="b38b4-180">Iegūstiet eksportējamās pakotnes lejupielādes URL.</span><span class="sxs-lookup"><span data-stu-id="b38b4-180">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="b38b4-181">Pievienojiet darbību **Izsaukt HTTP pieprasījumu**, lai izsauktu [GetExportedPackageUrl](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span><span class="sxs-lookup"><span data-stu-id="b38b4-181">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="b38b4-182">**Metode:** POST</span><span class="sxs-lookup"><span data-stu-id="b38b4-182">**Method:** POST</span></span>
        - <span data-ttu-id="b38b4-183">**Pieprasījuma URL:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="b38b4-183">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="b38b4-184">**Pieprasījuma pamatteksts:** {"executionId": body('GetExportedPackageURL')?['value']}</span><span class="sxs-lookup"><span data-stu-id="b38b4-184">**Body of the request:** {"executionId": body('GetExportedPackageURL')?['value']}</span></span>

        ![Darbība GetExportedPackageURL](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="b38b4-186">Lejupielādējiet eksportēto pakotni.</span><span class="sxs-lookup"><span data-stu-id="b38b4-186">Download the exported package.</span></span>

    - <span data-ttu-id="b38b4-187">Pievienojiet HTTP pieprasījumu **GET** (iebūvēta [HTTP savienotāja darbība](/azure/connectors/connectors-native-http)), lai no URL lejupielādētu pakotni, kas tika atgriezta iepriekšējā darbībā.</span><span class="sxs-lookup"><span data-stu-id="b38b4-187">Add an HTTP **GET** request (a built-in [HTTP connector action](/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="b38b4-188">**Metode:** GET</span><span class="sxs-lookup"><span data-stu-id="b38b4-188">**Method:** GET</span></span>
        - <span data-ttu-id="b38b4-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="b38b4-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="b38b4-190">Iespējams, vērtība **URI** būs jāievada vai nu koda skatā, vai arī noformētāja funkciju redaktorā.</span><span class="sxs-lookup"><span data-stu-id="b38b4-190">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![Darbība HTTP GET](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="b38b4-192">Šim pieprasījumam nav nepieciešama papildu autentifikācija, jo URL, ko atgriež **GetExportedPackageUrl** API, ietver kopīgotas piekļuves paraksta marķieri, kas piešķir piekļuvi faila lejupielādei.</span><span class="sxs-lookup"><span data-stu-id="b38b4-192">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="b38b4-193">Saglabājiet lejupielādēto pakotni, izmantojot [OneDrive biznesam](/azure/connectors/connectors-create-api-onedriveforbusiness) savienotāju.</span><span class="sxs-lookup"><span data-stu-id="b38b4-193">Save the downloaded package by using the [OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="b38b4-194">Pievienojiet OneDrive biznesam [Faila izveides](/connectors/onedriveforbusinessconnector/#create-file) darbību.</span><span class="sxs-lookup"><span data-stu-id="b38b4-194">Add a OneDrive for Business [Create File](/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="b38b4-195">Ja nepieciešams, pieslēdzieties savam OneDrive biznesam kontam.</span><span class="sxs-lookup"><span data-stu-id="b38b4-195">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="b38b4-196">**Mapes ceļš:** izvelētā mape</span><span class="sxs-lookup"><span data-stu-id="b38b4-196">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="b38b4-197">**Faila nosaukums:** worker\_package.zip</span><span class="sxs-lookup"><span data-stu-id="b38b4-197">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="b38b4-198">**Faila saturs:** iepriekšējās darbības pamatteksts (dinamiskais saturs)</span><span class="sxs-lookup"><span data-stu-id="b38b4-198">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![Faila darbības izveide](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="b38b4-200">3. darbība: loģikas programmas pārbaude</span><span class="sxs-lookup"><span data-stu-id="b38b4-200">Step 3: Test the logic app</span></span>

<span data-ttu-id="b38b4-201">Lai pārbaudītu loģikas programmu, atlasiet noformētāja pogu **Izpildīt**.</span><span class="sxs-lookup"><span data-stu-id="b38b4-201">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="b38b4-202">Tiks uzsākta loģikas programmas darbību izpilde.</span><span class="sxs-lookup"><span data-stu-id="b38b4-202">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="b38b4-203">Pēc 30 līdz 40 sekundēm loģikas programmai izpilde jāpabeidz, un jūsu OneDrive biznesam mapei jāietver jauns pakotnes fails, kas satur eksportētos nodarbinātos.</span><span class="sxs-lookup"><span data-stu-id="b38b4-203">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="b38b4-204">Ja tiek ziņots par kļūmi jebkurā darbībā, noformētājā atlasiet kļūdaino darbību un pārbaudiet tās laukus **Ievades** un **Izvades**.</span><span class="sxs-lookup"><span data-stu-id="b38b4-204">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="b38b4-205">Atkļūdojiet un pielāgojiet darbības, kā nepieciešams kļūdu labošanai.</span><span class="sxs-lookup"><span data-stu-id="b38b4-205">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="b38b4-206">Tālāk redzamajā attēlā ir parādīts, kā izskatās Logic Apps Designer, kad visas loģiskās programmas darbības tiek izpildītas sekmīgi.</span><span class="sxs-lookup"><span data-stu-id="b38b4-206">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![Sekmīga loģikas programmas izpilde](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="b38b4-208">Kopsavilkums</span><span class="sxs-lookup"><span data-stu-id="b38b4-208">Summary</span></span>

<span data-ttu-id="b38b4-209">Šajā apmācībā apguvāt, kā izmantot loģikas programmu, lai eksportētu datus no Human Resources un saglabātu eksportētos datus OneDrive biznesam mapē.</span><span class="sxs-lookup"><span data-stu-id="b38b4-209">In this tutorial, you learned how to use a logic app to export data from Human Resources and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="b38b4-210">Pēc nepieciešamības varat modificēt šīs apmācības darbības, lai pielāgotos sava biznesa vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="b38b4-210">You can modify the steps of this tutorial as required to suit your business needs.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]