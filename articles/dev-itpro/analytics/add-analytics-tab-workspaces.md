---
title: "Analīzes pievienošana darbvietām, izmantojot Power BI Embedded"
description: "Šajā tēmā ir parādīts, kā iegult Power BI pārskatu darbvietas cilnē Analīze."
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 8a79ca0b985b0568c35e6a5095332fc6326c9ff1
ms.openlocfilehash: a190e15dc304f60739c80d75222830ee737c5a32
ms.contentlocale: lv-lv
ms.lasthandoff: 09/22/2018

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="f4134-103">Analīzes pievienošana darbvietām, izmantojot Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="f4134-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="f4134-104">Šis līdzeklis tiek atbalstīts programmā Dynamics 365 for Finance and Operations (versija 7.2 un jaunākas versijas).</span><span class="sxs-lookup"><span data-stu-id="f4134-104">This feature is supported in Dynamics 365 for Finance and Operations (version 7.2 and later).</span></span>

## <a name="introduction"></a><span data-ttu-id="f4134-105">Ievads</span><span class="sxs-lookup"><span data-stu-id="f4134-105">Introduction</span></span>
<span data-ttu-id="f4134-106">Šajā tēmā ir parādīts, kā iegult Microsoft Power BI pārskatu darbvietas cilnē **Analīze**.</span><span class="sxs-lookup"><span data-stu-id="f4134-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="f4134-107">Šeit sniegtā piemēra ietvaros paplašināsim darbvietu **Rezervēšanas pārvaldība** autoparka pārvaldības programmā, lai cilnē **Analīze** iegultu analītisku darbvietu.</span><span class="sxs-lookup"><span data-stu-id="f4134-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f4134-108">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="f4134-108">Prerequisites</span></span>
+ <span data-ttu-id="f4134-109">Piekļuve izstrādātāju videi, kas darbina platformas 8. atjauninājumu vai jaunāku atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="f4134-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="f4134-110">Analītisks pārskats (.pbix fails), kas tika izveidots, izmantojot programmu Microsoft Power BI Desktop, un kam ir no elementu krātuves datu bāzes iegūts datu modelis.</span><span class="sxs-lookup"><span data-stu-id="f4134-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

## <a name="overview"></a><span data-ttu-id="f4134-111">Pārskats</span><span class="sxs-lookup"><span data-stu-id="f4134-111">Overview</span></span>
<span data-ttu-id="f4134-112">Neatkarīgi no tā, vai paplašināt esošu programmas darbvietu vai ieviešat jaunu darbvietu, varat izmantot iegultos analītiskos skatus, lai nodrošinātu visaptverošus un interaktīvus biznesa datu skatus.</span><span class="sxs-lookup"><span data-stu-id="f4134-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="f4134-113">Analītiskās darbvietas cilnes pievienošanas procesā ir četras darbības.</span><span class="sxs-lookup"><span data-stu-id="f4134-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="f4134-114">Pievienojiet .pbix failu kā Dynamics 365 resursu.</span><span class="sxs-lookup"><span data-stu-id="f4134-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="f4134-115">Definējiet analītiskās darbvietas cilni.</span><span class="sxs-lookup"><span data-stu-id="f4134-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="f4134-116">Ieguliet .pbix resursu darbvietas cilnē.</span><span class="sxs-lookup"><span data-stu-id="f4134-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="f4134-117">Neobligāti: pievienojiet paplašinājumus, lai pielāgotu skatu.</span><span class="sxs-lookup"><span data-stu-id="f4134-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="f4134-118">Papildinformāciju par to, kā izveidot analītiskus pārskatus, skatiet rakstā [Darba sākšana ar Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="f4134-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="f4134-119">Šī lapa ir lielisks informācijas avots, kas var palīdzēt jums izveidot pārliecinošus analītisko pārskatu risinājumus.</span><span class="sxs-lookup"><span data-stu-id="f4134-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

## <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="f4134-120">.pbix faila kā resursa pievienošana</span><span class="sxs-lookup"><span data-stu-id="f4134-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="f4134-121">Pirms sākat, izveidojiet vai iegūstiet Power BI pārskatu, ko iegulsit darbvietā.</span><span class="sxs-lookup"><span data-stu-id="f4134-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="f4134-122">Papildinformāciju par to, kā izveidot analītiskus pārskatus, skatiet rakstā [Darba sākšana ar Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="f4134-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span>

<span data-ttu-id="f4134-123">Izpildiet tālāk norādītās darbības, lai pievienotu .pbix failu kā Visual Studio projekta artefaktu.</span><span class="sxs-lookup"><span data-stu-id="f4134-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="f4134-124">Izveidojiet jaunu projektu atbilstošajā modelī.</span><span class="sxs-lookup"><span data-stu-id="f4134-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="f4134-125">Risinājumu pārlūkā atlasiet projektu, noklikšķiniet uz tā ar peles labo pogu un pēc tam atlasiet **Pievienot** \> **Jauns vienums**.</span><span class="sxs-lookup"><span data-stu-id="f4134-125">In Solution Explorer, select the project, right-click, and then select **Add** \> **New Item**.</span></span>
3. <span data-ttu-id="f4134-126">Dialoglodziņa **Pievienot jaunu vienumu** sadaļā **Operāciju artefakti** atlasiet veidni **Resurss**.</span><span class="sxs-lookup"><span data-stu-id="f4134-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="f4134-127">Ievadiet nosaukumu, kas tiks izmantots kā atsauce uz pārskatu X++ metadatos, un pēc tam noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="f4134-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![Dialoglodziņš Pievienot jaunu vienumu](media/analytical-workspace-add.png)

5. <span data-ttu-id="f4134-129">Atrodiet .pbix failu, kas satur analītiskā pārskata definīciju, un pēc tam noklikšķiniet uz **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="f4134-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![Dialoglodziņš Atlasīt resursa failu](media/analytical-workspace-select-resource.png)

<span data-ttu-id="f4134-131">Tagad, kad esat pievienojis .pbix failu kā Dynamics 365 resursu, varat iegult pārskatus darbvietās un pievienot tiešās saites, izmantojot izvēlnes elementus.</span><span class="sxs-lookup"><span data-stu-id="f4134-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

## <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="f4134-132">Cilnes vadīklas pievienošana programmas darbvietai</span><span class="sxs-lookup"><span data-stu-id="f4134-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="f4134-133">Šajā piemērā paplašināsim darbvietu **Rezervēšanas pārvaldība** autoparka pārvaldības modelī, pievienojot cilni **Analīze** formas **FMClerkWorkspace** definīcijai.</span><span class="sxs-lookup"><span data-stu-id="f4134-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>

<span data-ttu-id="f4134-134">Tālāk esošajā attēlā parādīts, kā forma **FMClerkWorkspace** izskatās Microsoft Visual Studio noformētājā.</span><span class="sxs-lookup"><span data-stu-id="f4134-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![Forma FMClerkWorkspace pirms izmaiņām](media/analytical-workspace-definition-before.png)

<span data-ttu-id="f4134-136">Veiciet tālāk norādītās darbības, lai paplašinātu formas definīciju darbvietai **Rezervēšanas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="f4134-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="f4134-137">Atveriet formu noformētāju, lai paplašinātu noformējuma definīciju.</span><span class="sxs-lookup"><span data-stu-id="f4134-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="f4134-138">Noformējuma definīcijā atlasiet augšējo elementu, kas ir apzīmēts kā **Noformējums|modelis: operatīvā darbvieta**.</span><span class="sxs-lookup"><span data-stu-id="f4134-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="f4134-139">Noklikšķiniet ar peles labo pogu un atlasiet **Jauns** \> **Cilne**, lai pievienotu jaunu vadīklu ar nosaukumu **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="f4134-139">Right-click, and then select **New** \> **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="f4134-140">Formu noformētājā atlasiet vienumu **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="f4134-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="f4134-141">Noklikšķiniet ar peles labo pogu un atlasiet vienumu **Jauna cilnes lapa**, lai pievienotu jaunu cilnes lapu.</span><span class="sxs-lookup"><span data-stu-id="f4134-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="f4134-142">Pārdēvējiet cilnes lapu uz kaut ko atpazīstamu, piemēram, **Darbvieta**.</span><span class="sxs-lookup"><span data-stu-id="f4134-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="f4134-143">Formu noformētājā atlasiet vienumu **FormTabControl1**.</span><span class="sxs-lookup"><span data-stu-id="f4134-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="f4134-144">Noklikšķiniet ar peles labo pogu un atlasiet vienumu **Jauna cilnes lapa**.</span><span class="sxs-lookup"><span data-stu-id="f4134-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="f4134-145">Pārdēvējiet cilnes lapu uz kaut ko atpazīstamu, piemēram, **Analīze**.</span><span class="sxs-lookup"><span data-stu-id="f4134-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="f4134-146">Formu noformētājā atlasiet vienumu **Analīze (cilnes lapa)**.</span><span class="sxs-lookup"><span data-stu-id="f4134-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="f4134-147">Rekvizītu **Paraksts** iestatiet uz **Analīze**.</span><span class="sxs-lookup"><span data-stu-id="f4134-147">Set the **Caption** property to **Analytics**.</span></span>
12. <span data-ttu-id="f4134-148">Noklikšķiniet ar peles labo pogu uz vadīklas un atlasiet **Jauns** \> **Grupa**, lai pievienoju jaunu formu grupas vadīklu.</span><span class="sxs-lookup"><span data-stu-id="f4134-148">Right-click the control, and then select **New** \> **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="f4134-149">Pārdēvējiet formu grupu uz kaut ko atpazīstamu, piemēram, **powerBIReportGroup**.</span><span class="sxs-lookup"><span data-stu-id="f4134-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="f4134-150">Formu noformētājā atlasiet vienumu **PanoramaBody (cilne)** un pēc tam velciet vadīklu uz cilni **Darbvieta**.</span><span class="sxs-lookup"><span data-stu-id="f4134-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="f4134-151">Noformējuma definīcijā atlasiet augšējo elementu, kas ir apzīmēts kā **Noformējums|modelis: operatīvā darbvieta**.</span><span class="sxs-lookup"><span data-stu-id="f4134-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="f4134-152">Noklikšķiniet ar peles labo pogu un atlasiet vienumu **Noņemt modeli**.</span><span class="sxs-lookup"><span data-stu-id="f4134-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="f4134-153">Vēlreiz noklikšķiniet ar peles labo pogu un atlasiet **Pievienot modeli** \> **Darbvieta ar cilnēm**.</span><span class="sxs-lookup"><span data-stu-id="f4134-153">Right-click again, and then select **Add pattern** \> **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="f4134-154">Veiciet būvējumu, lai pārbaudītu veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="f4134-154">Perform a build to verify your changes.</span></span>

<span data-ttu-id="f4134-155">Tālāk esošajā attēlā parādīts, kā noformējums izskatās pēc šo izmaiņu lietošanas.</span><span class="sxs-lookup"><span data-stu-id="f4134-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![FMClerkWorkspace pēc izmaiņām](media/analytical-workspace-definition-after.png)

<span data-ttu-id="f4134-157">Tagad, kad esat pievienojis formu vadīklas, kas tiks izmantotas darbvietas pārskata iegulšanai, jums ir jādefinē vecākobjekta vadīklas lielums tā, lai varētu izvietot izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="f4134-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="f4134-158">Pēc noklusējuma pārskatā būs redzama gan lapa **Filtru rūts**, gan lapa **Cilne**.</span><span class="sxs-lookup"><span data-stu-id="f4134-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="f4134-159">Tomēr šo vadīklu redzamību var mainīt pēc nepieciešamības pārskata mērķa patērētājam.</span><span class="sxs-lookup"><span data-stu-id="f4134-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>

> [!NOTE]
> <span data-ttu-id="f4134-160">Iegultajām darbvietām ieteicams izmantot paplašinājumus, lai konsekvences nolūkā paslēptu gan lapu **Filtru rūts**, gan lapu **Cilne**.</span><span class="sxs-lookup"><span data-stu-id="f4134-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>

<span data-ttu-id="f4134-161">Esat pabeidzis programmas formas definīcijas paplašināšanas uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="f4134-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="f4134-162">Papildinformāciju par to, kā izmantot paplašinājumus pielāgojumu veikšanai, skatiet rakstā [Pielāgošana: pārklāšanās un paplašinājumi](../extensibility/customization-overlayering-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="f4134-162">For more information about how to use extensions to do customizations, see [Customization: Overlayering and extensions](../extensibility/customization-overlayering-extensions.md).</span></span>

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="f4134-163">X++ biznesa loģikas pievienošana skatītāja vadīklas iegulšanai</span><span class="sxs-lookup"><span data-stu-id="f4134-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="f4134-164">Izpildiet tālāk norādītās darbības, lai pievienotu biznesa loģiku, kas inicializē pārskatu skatītāja vadīklu, kas ir iegulta darbvietā **Rezervēšanas pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="f4134-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="f4134-165">Atveriet formu noformētāju **FMClerkWorkspace**, lai paplašinātu noformējuma definīciju.</span><span class="sxs-lookup"><span data-stu-id="f4134-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="f4134-166">Nospiediet taustiņu F7, lai piekļūtu koda definīcijas kodam.</span><span class="sxs-lookup"><span data-stu-id="f4134-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="f4134-167">Pievienojiet tālāk norādīto X++ kodu.</span><span class="sxs-lookup"><span data-stu-id="f4134-167">Add the following X++ code.</span></span>

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="f4134-168">Veiciet būvējumu, lai pārbaudītu veiktās izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="f4134-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="f4134-169">Esat pabeidzis uzdevumu ar biznesa loģikas pievienošanu, kas inicializē iegulto pārskatu skatītāja vadīklu.</span><span class="sxs-lookup"><span data-stu-id="f4134-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="f4134-170">Tālāk esošajā attēlā parādīts, kā darbvieta izskatās pēc šo izmaiņu lietošanas.</span><span class="sxs-lookup"><span data-stu-id="f4134-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![Pārskats iegults darbvietā](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="f4134-172">Esošajam darbības skatam varat piekļūt, izmantojot darbvietas cilnes zem lapas virsraksta.</span><span class="sxs-lookup"><span data-stu-id="f4134-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

## <a name="reference"></a><span data-ttu-id="f4134-173">Atsauce</span><span class="sxs-lookup"><span data-stu-id="f4134-173">Reference</span></span>

### <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="f4134-174">PBIReportHelper.initializeReportControl metode</span><span class="sxs-lookup"><span data-stu-id="f4134-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="f4134-175">Šajā sadaļā sniegta informācija par palīga klasi, kas tiek izmantota, lai Power BI pārskatu (.pbix resursu) iegultu formu grupas vadīklā.</span><span class="sxs-lookup"><span data-stu-id="f4134-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

#### <a name="syntax"></a><span data-ttu-id="f4134-176">Sintakse</span><span class="sxs-lookup"><span data-stu-id="f4134-176">Syntax</span></span>
```
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a><span data-ttu-id="f4134-177">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4134-177">Parameters</span></span>

| <span data-ttu-id="f4134-178">Nosaukums</span><span class="sxs-lookup"><span data-stu-id="f4134-178">Name</span></span>             | <span data-ttu-id="f4134-179">Apraksts</span><span class="sxs-lookup"><span data-stu-id="f4134-179">Description</span></span>                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4134-180">resourceName</span><span class="sxs-lookup"><span data-stu-id="f4134-180">resourceName</span></span>     | <span data-ttu-id="f4134-181">.pbix resoursa nosaukums.</span><span class="sxs-lookup"><span data-stu-id="f4134-181">The name of the .pbix resource.</span></span>                                                                              |
| <span data-ttu-id="f4134-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="f4134-182">formGroupControl</span></span> | <span data-ttu-id="f4134-183">Formu grupas vadīkla, kam jālieto Power BI pārskatu vadīkla.</span><span class="sxs-lookup"><span data-stu-id="f4134-183">The form group control to apply the Power BI report control to.</span></span>                                              |
| <span data-ttu-id="f4134-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="f4134-184">defaultPageName</span></span>  | <span data-ttu-id="f4134-185">Noklusējuma lapas nosaukums.</span><span class="sxs-lookup"><span data-stu-id="f4134-185">The default page name.</span></span>                                                                                       |
| <span data-ttu-id="f4134-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="f4134-186">showFilterPane</span></span>   | <span data-ttu-id="f4134-187">Būla vērtība, kas norāda, vai filtra rūts jārāda (**Patiess**) vai jāpaslēpj (**Aplams**).</span><span class="sxs-lookup"><span data-stu-id="f4134-187">A Boolean value that indicates whether the filter pane should be shown (**true**) or hidden (**false**).</span></span>     |
| <span data-ttu-id="f4134-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="f4134-188">showNavPane</span></span>      | <span data-ttu-id="f4134-189">Būla vērtība, kas norāda, vai navigācijas rūts jārāda (**Patiess**) vai jāpaslēpj (**Aplams**).</span><span class="sxs-lookup"><span data-stu-id="f4134-189">A Boolean value that indicates whether the navigation pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="f4134-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="f4134-190">defaultFilters</span></span>   | <span data-ttu-id="f4134-191">Noklusējuma filtri Power BI pārskatam.</span><span class="sxs-lookup"><span data-stu-id="f4134-191">The default filters for the Power BI report.</span></span>                                                                 |

