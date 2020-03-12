---
title: Iestatīt ER formāta parametrus juridiskai personai
description: Šajā tēmā izskaidrots, kā iestatīt elektronisko pārskatu (ER) formātu parametrus juridiskai personai.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: ca837026f18034cddb34d7a2d5a62002ed69106a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042761"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="da5bc-103">Iestatīt ER formāta parametrus juridiskai personai</span><span class="sxs-lookup"><span data-stu-id="da5bc-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="da5bc-104">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="da5bc-104">Prerequisites</span></span>

<span data-ttu-id="da5bc-105">Lai veiktu šīs darbības, vispirms ir jāpabeidz darbības, kas aprakstītas tēmā [Konfigurēt ER formātus, lai izmantotu parametrus, kas konkretizēti juridiskai personai](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="da5bc-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="da5bc-106">Lai izpildītu šīs tēmas piemērus, ir jābūt piekļuvei Microsoft Dynamics 365 Finance (Finance) vienai no šādām lomām:</span><span class="sxs-lookup"><span data-stu-id="da5bc-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="da5bc-107">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="da5bc-107">Electronic reporting developer</span></span>
- <span data-ttu-id="da5bc-108">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="da5bc-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="da5bc-109">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="da5bc-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="da5bc-110">ER konfigurāciju importēšana</span><span class="sxs-lookup"><span data-stu-id="da5bc-110">Import ER configurations</span></span>

1.  <span data-ttu-id="da5bc-111">Pierakstieties savā vidē.</span><span class="sxs-lookup"><span data-stu-id="da5bc-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="da5bc-112">Noklusējuma informācijas panelī atlasiet **Elektroniskais pārskats**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="da5bc-113">Atlasiet **Pārskatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="da5bc-114">Importējiet uz pašreizējo Finance instanci konfigurācijas, kas tika eksportētas no Regulatory Configuration Service (RCS), kad izpildījāt darbības no tēmas [Konfigurēt ER formātus, lai izmantotu parametrus, kas konkretizēti juridiskai personai](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="da5bc-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="da5bc-115">Veiciet šīs darbības katrai elektroniskās ziņošanas (ER) konfigurācijai šādā secībā: datu modelis, modeļa kartēšana un formāti.</span><span class="sxs-lookup"><span data-stu-id="da5bc-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="da5bc-116">Atlasiet **Apmaiņa \> Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="da5bc-117">Atlasiet **Pārlūkot**, lai atlasītu failu nepieciešamajai ER konfigurācijai XML formātā.</span><span class="sxs-lookup"><span data-stu-id="da5bc-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="da5bc-118">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-118">Select **OK**.</span></span>
    
    <span data-ttu-id="da5bc-119">Šajā attēlā ir parādītas konfigurācijas, kurām jums ir jābūt, kad esat beiguši.</span><span class="sxs-lookup"><span data-stu-id="da5bc-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![ER konfigurāciju lapa](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="da5bc-121">DEMF uzņēmuma parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="da5bc-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="da5bc-122">Varat izmantot ER struktūru, lai iestatītu programmai specifiskus parametrus ER formātam.</span><span class="sxs-lookup"><span data-stu-id="da5bc-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="da5bc-123">Atlasiet **DEMF** juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="da5bc-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="da5bc-124">Konfigurācijas kokā atlasiet formātu **Formatēt, lai uzzinātu, kā uzmeklēt LE datus**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="da5bc-125">Darbību rūts cilnē **Konfigurācijas**, grupā **Programmai specifiski parametri** atlasiet **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![ER programmai specifisku parametru lapa](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="da5bc-127">Lapā **Programmai specifiski parametri** varat konfigurēt noteikumus datu avotam **Atlasītājs** formātā **Formēt, lai uzzinātu, kā atrast LE datus**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="da5bc-128">Ja bāzes ER formātā būs vairāki veida **Uzmeklēšana** datu avoti, jums jāatlasa vēlamais datu avots kopsavilkuma cilnē **Pārlūki** pirms varat sākt konfigurēt kārtulu kopu datu avotam.</span><span class="sxs-lookup"><span data-stu-id="da5bc-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="da5bc-129">Katram datu avotam varat konfigurēt atsevišķas kārtulas katrai atlasītā ER formāta versijai.</span><span class="sxs-lookup"><span data-stu-id="da5bc-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="da5bc-130">Visu kārtulu kopa visiem uzmeklēšanas datu avotiem, kuri ir pieejami atlasītajā bāzes ER formāta versijā, veido programmai raksturīgus parametrus attiecībā uz ER formātu.</span><span class="sxs-lookup"><span data-stu-id="da5bc-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="da5bc-131">Atlasiet ER formāta versiju **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="da5bc-132">Kopsavilkuma cilnē **Nosacījumi** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="da5bc-133">Jaunā ieraksta laukā **Kods** atlasiet nolaižamā saraksta bultu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="da5bc-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="da5bc-134">Uzmeklēšana parāda atlases nodokļu kodu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="da5bc-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="da5bc-135">Šis saraksts tiek atgriezts, izmantojot datu avotu**Model.Data.Tax**, kas ticis konfigurēts bāzes ER formātā.</span><span class="sxs-lookup"><span data-stu-id="da5bc-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="da5bc-136">Tā kā šis datu avots ietver lauku **Nosaukums**, uzmeklēšanas laikā parādās katra nodokļu koda nosaukums.</span><span class="sxs-lookup"><span data-stu-id="da5bc-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![ER programmai specifisku parametru lapa](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="da5bc-138">Atlasiet nodokļa kodu **VAT19**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="da5bc-139">Jaunā ieraksta laukā **Uzmeklēšanas rezultāts** atlasiet nolaižamā saraksta bultu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="da5bc-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="da5bc-140">Uzmeklēšana parāda atlases TaxationLevel formāta uzskaitījuma vērtību sarakstu.</span><span class="sxs-lookup"><span data-stu-id="da5bc-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="da5bc-141">Ņemiet vērā, ka, ja vācu valoda ir izvēlēta kā vēlamā lietotāja valoda, kurā esat pieteicies, tad uzmeklēšanas vērtību marķējums būs vācu valodā ar nosacījumu, ka tās ir pārtulkotas bāzes ER formātā.</span><span class="sxs-lookup"><span data-stu-id="da5bc-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="da5bc-142">Turklāt, ja uzmeklēšanas datu avota marķējums ir tulkots, šis marķējums tiks parādīts lietotāja vēlamajā valodā cilnē **Pārlūki**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![ER programmai specifisku parametru lapa](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="da5bc-144">Atlasiet vērtību **Parastā taksācija**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="da5bc-145">Pievienojot šo ierakstu, tiek definēta šāda kārtula: Vienmēr, kad tiek pieprasīts uzmeklēšanas datu avots **Atlasītājs**un nodokļa kods **VAT19** tiek nodots kā arguments, **Regulārā taksācija** tiks atgriezta kā pieprasītais taksācijas līmenis.</span><span class="sxs-lookup"><span data-stu-id="da5bc-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="da5bc-146">Atlasiet **Pievienot**, tad veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="da5bc-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="da5bc-147">Laukā **Kods** atlasiet nodokļu kodu **InVAT19**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="da5bc-148">Laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Regulārā taksācija**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="da5bc-149">Vēlreiz atlasiet **Pievienot**, tad veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="da5bc-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="da5bc-150">Laukā **Kods** atlasiet nodokļu kodu **VAT7**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="da5bc-151">Laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Samazinātā taksācija**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="da5bc-152">Vēlreiz atlasiet **Pievienot**, tad veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="da5bc-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="da5bc-153">Laukā **Kods** atlasiet nodokļu kodu **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="da5bc-154">Laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Samazinātā taksācija**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="da5bc-155">Vēlreiz atlasiet **Pievienot**, tad veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="da5bc-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="da5bc-156">Laukā **Kods** atlasiet nodokļu kodu **THIRD**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="da5bc-157">Laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Nav taksācijas**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="da5bc-158">Vēlreiz atlasiet **Pievienot**, tad veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="da5bc-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="da5bc-159">Laukā **Kods** atlasiet nodokļu kodu **InVAT10**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="da5bc-160">Laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Nav taksācijas**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="da5bc-161">Vēlreiz atlasiet **Pievienot**, tad veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="da5bc-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="da5bc-162">Laukā **Kods** atlasiet opciju **\*Nav tukšs\***.</span><span class="sxs-lookup"><span data-stu-id="da5bc-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="da5bc-163">Laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Cita**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="da5bc-164">Pievienojot šo pēdējo ierakstu, tiek definēta šāda kārtula: Vienmēr, kad nodokļa kods, kas tiek nodots kā arguments, neizpilda nevienu no iepriekšējām kārtulām, uzmeklēšanas datu avots atgriezīs **Citu** kā pieprasīto taksācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="da5bc-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![ER programmai specifisku parametru lapa](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="da5bc-166">Laukā **Statuss** atlasiet **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="da5bc-167">Palaižot ER formāta versiju ar statusu **Pabeigts** vai **Koplietots**, šai kārtulu kopai jābūt ar statusu **Pabeigta**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="da5bc-168">Pretējā gadījumā bāzes ER formāta izpilde tiks pārtraukta, kad formāts mēģinās ielādēt datus no šīs kārtulu kopas, kamēr tiks palaists uzmeklēšanas datu avots **Atlasītājs**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="da5bc-169">Palaižot ER formāta versiju ar statusu **Uzmetums**, bāzes formāts var piekļūt šai noteikumu kopai neatkarīgi no tās statusa.</span><span class="sxs-lookup"><span data-stu-id="da5bc-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="da5bc-170">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-170">Select **Save**.</span></span>
18. <span data-ttu-id="da5bc-171">Aizveriet lapu **Programmai specifiski parametri**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="da5bc-172">DEMF uzņēmumā palaidiet ER formātu</span><span class="sxs-lookup"><span data-stu-id="da5bc-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="da5bc-173">Konfigurācijas kokā atlasiet formātu **Formatēt, lai uzzinātu, kā uzmeklēt LE datus**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="da5bc-174">Darbību rūtī atlasiet **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="da5bc-175">Parādītajā dialoglodziņā atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="da5bc-176">Lejupielādējiet izveidoto pārskatu un saglabājiet to lokāli.</span><span class="sxs-lookup"><span data-stu-id="da5bc-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="da5bc-177">Ģenerētajā pārskatā ievērojiet, ka nodokļa koda **InVAT7** kopsavilkums ir uzlikts līmenī **Samazināts** un ka nodokļa kodu **VAT19** un **InVA19** kopsavilkumi ir iekļauti līmenī **Regulārs**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="da5bc-178">Šo darbību nosaka konfigurācija no juridiskās personas atkarīgā kārtulu kopā.</span><span class="sxs-lookup"><span data-stu-id="da5bc-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="da5bc-179">Dodieties uz **Nodokļi \> Netiešie nodokļi \> PVN \> PVN kodi**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="da5bc-180">Atlasiet nodokļa kodu **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="da5bc-181">Darbību rūtī, cilnē **PVN kods**, grupā **Pieprasījumi** atlasiet **Iegrāmatots PVN,** lai skatītu informāciju par nodokļa vērtību un piemēroto nodokļa likmi katram nodokļa kodam.</span><span class="sxs-lookup"><span data-stu-id="da5bc-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![Grāmatota PVN lapa](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="da5bc-183">Aizveriet lapu Grāmatotais PVN.</span><span class="sxs-lookup"><span data-stu-id="da5bc-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="da5bc-184">USMF uzņēmuma parametru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="da5bc-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="da5bc-185">Atlasiet **USMF** juridisko personu.</span><span class="sxs-lookup"><span data-stu-id="da5bc-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="da5bc-186">Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="da5bc-187">Konfigurācijas kokā izvērsiet vienumu **Modelis, lai uzzinātu parametru izsaukumus**, izvērsiet vienumu **Formatēt, lai uzzinātu parametru izsaukumus** un atlasiet formātu **Formāts, lai uzzinātu, kā meklēt LE datus**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="da5bc-188">Darbību rūts cilnē **Konfigurācijas**, grupā **Programmai specifiski parametri** atlasiet **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="da5bc-189">Atlasiet atlasītā ER formāta versiju **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="da5bc-190">Kopsavilkuma cilnē **Nosacījumi** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="da5bc-191">Jaunā ieraksta laukā **Kods** atlasiet nolaižamā saraksta bultu, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="da5bc-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="da5bc-192">Pārlūks tagad parāda nodokļu kodu sarakstu **USMF** uzņēmuma nodokļiem atlasei.</span><span class="sxs-lookup"><span data-stu-id="da5bc-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![ER programmai specifisku parametru lapa](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="da5bc-194">Atlasiet nodokļa kodu **EXEMPT**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="da5bc-195">Jaunā ieraksta laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Nav taksācijas**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-195">In the **Lookup resul**t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="da5bc-196">Vēlreiz atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-196">Select **Add** again.</span></span>
11. <span data-ttu-id="da5bc-197">Jaunā ieraksta **Kods** atlasiet opciju **\*Nav tukšs\***.</span><span class="sxs-lookup"><span data-stu-id="da5bc-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="da5bc-198">Jaunā ieraksta laukā **Uzmeklēšanas rezultāts** atlasiet vērtību **Regulāra taksācija**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="da5bc-199">Laukā **Statuss** atlasiet **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="da5bc-200">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-200">Select **Save**.</span></span>

    ![ER programmai specifisku parametru lapa](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="da5bc-202">Aizveriet lapu **Programmai specifiski parametri**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="da5bc-203">USMF uzņēmumā palaidiet ER formātu</span><span class="sxs-lookup"><span data-stu-id="da5bc-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="da5bc-204">Konfigurācijas kokā atlasiet formātu **Formatēt, lai uzzinātu, kā uzmeklēt LE datus**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="da5bc-205">Darbību rūtī atlasiet **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="da5bc-206">Parādītajā dialoglodziņā atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="da5bc-207">Lejupielādējiet izveidoto pārskatu un saglabājiet to lokāli.</span><span class="sxs-lookup"><span data-stu-id="da5bc-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="da5bc-208">Ģenerētajā pārskatā ievērojiet, ka jūs atkārtoti izmantojāt to pašu ER formātu citai juridiskajai personai, bet neveicot nekādus pielāgojumus ER formātā.</span><span class="sxs-lookup"><span data-stu-id="da5bc-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="da5bc-209">Atkārtoti izmantojiet no juridiskās personas atkarīgos parametrus</span><span class="sxs-lookup"><span data-stu-id="da5bc-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="da5bc-210">Eksporta parametri</span><span class="sxs-lookup"><span data-stu-id="da5bc-210">Export parameters</span></span>

1.  <span data-ttu-id="da5bc-211">Dodieties uz **Organizācijas administrēšana \> Darbvietas \> Elektronisko atskaišu veidošana**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="da5bc-212">Atlasiet **Pārskatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="da5bc-213">Konfigurācijas kokā atlasiet formātu **Formatēt, lai uzzinātu, kā uzmeklēt LE datus**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="da5bc-214">Darbību rūts cilnē **Konfigurācijas**, grupā **Programmai specifiski parametri** atlasiet **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="da5bc-215">Atlasiet ER formāta versiju **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="da5bc-216">Darbību rūtī atlasiet **Eksportēt**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="da5bc-217">Lejupielādējiet izveidoto failu un saglabājiet to lokāli.</span><span class="sxs-lookup"><span data-stu-id="da5bc-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="da5bc-218">Programmai raksturīgo parametru konfigurētais iestatījums tagad ir eksportēts kā XML fails.</span><span class="sxs-lookup"><span data-stu-id="da5bc-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="da5bc-219">Importa parametri</span><span class="sxs-lookup"><span data-stu-id="da5bc-219">Import parameters</span></span>

1.  <span data-ttu-id="da5bc-220">Atlasiet ER formāta versiju **1.1.2**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="da5bc-221">Darbību rūtī atlasiet **Importēt**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="da5bc-222">Atlasiet **Jā**, lai apstiprinātu, ka vēlaties ignorēt esošos lietojumprogrammai raksturīgos parametrus šai formāta versijai.</span><span class="sxs-lookup"><span data-stu-id="da5bc-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="da5bc-223">Atlasiet **Pārlūkot**, lai atrastu failu, kas satur eksportētos programmai raksturīgos parametrus versijai **1.1.1**</span><span class="sxs-lookup"><span data-stu-id="da5bc-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="da5bc-224">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-224">Select **OK**.</span></span>

    <span data-ttu-id="da5bc-225">Tagad ER formāta versijai**1.1.2** formāta 1.2. versijai ir tie paši programmai raksturīgie parametri, kurus sākotnēji konfigurējāt versijai **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="da5bc-226">Ņemiet vērā, ka programmai specifiskie ER formāta parametri ir atkarīgi no juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="da5bc-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="da5bc-227">Lai atkārtoti izmantotu programmai specifiskos parametrus, kas ir konfigurēti vienai juridiskajai personai citā juridiskā personā, tie ir jāeksportē, kad esat pieteicies pirmajā juridiskajā personā, un pēc tam tie jāimportē pēc pieteikšanās otrā juridiskajā personā.</span><span class="sxs-lookup"><span data-stu-id="da5bc-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="da5bc-228">Varat arī izmantot šo pieeju, lai pārsūtītu ER formātam piesaistītos programmas parametrus, kas sākotnēji tika konfigurēti vienā Finance instancē citai Finance instancei.</span><span class="sxs-lookup"><span data-stu-id="da5bc-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="da5bc-229">Ņemiet vērā, ka, konfigurējot programmai specifiskos parametrus vienai ER formāta versijai un importējot lielāku tā paša formāta versiju pašreizējā Finance instancē, importētajai versijai netiek lietoti esošie programmai specifiskie parametri.</span><span class="sxs-lookup"><span data-stu-id="da5bc-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="da5bc-230">Ņemiet vērā arī to, ka, atlasot failu importēšanai, programmai specifisko parametru struktūra šajā failā tiek salīdzināta ar atbilstošā **Uzmeklēšanas** tipa datu avota struktūru, kas atlasīta importēšanai.</span><span class="sxs-lookup"><span data-stu-id="da5bc-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="da5bc-231">Importēšana tiek veikta, kad katrs programmai specifiskais parametrs atbilst atbilstošā datu avota struktūrai, kas ir atlasīta importēšanai.</span><span class="sxs-lookup"><span data-stu-id="da5bc-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="da5bc-232">Ja struktūras nesakrīt, saņemsit brīdinājuma ziņojumu, kurā teikts, ka importēšanu nevar veikt.</span><span class="sxs-lookup"><span data-stu-id="da5bc-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="da5bc-233">Ja vēlaties, lai imports tiktu veikts, esošie programmai specifiskajam parametri atlasītajam ER formātam tiks notīrīti, un tie būs jāiestata no sākuma.</span><span class="sxs-lookup"><span data-stu-id="da5bc-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="da5bc-234">Attiecības starp programmai specifiskajiem parametriem un ER formātu</span><span class="sxs-lookup"><span data-stu-id="da5bc-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="da5bc-235">Attiecības starp ER formātu un tā programmai specifiskajiem parametriem ir noteiktas ar no ER formāta instances neatkarīgu unikālu identifikācijas kodu.</span><span class="sxs-lookup"><span data-stu-id="da5bc-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="da5bc-236">Tāpēc, noņemot ER formātu no Finance, lietojumprogrammai raksturīgie parametri, kas konfigurēti ER formātam, tiek saglabāti pašreizējā Finance instancē.</span><span class="sxs-lookup"><span data-stu-id="da5bc-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="da5bc-237">Tiem var piekļūt vienmēr, kad tiek atkal importēts bāzes ER formāts šajā Finance instancē.</span><span class="sxs-lookup"><span data-stu-id="da5bc-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="da5bc-238">Piekļūt programmai specifiskajiem parametriem, izmantojot ER struktūru</span><span class="sxs-lookup"><span data-stu-id="da5bc-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="da5bc-239">Iepriekšējā piemērā, lietojot ER struktūru, jums ir pieejami programmai specifiskie parametri ER formātā.</span><span class="sxs-lookup"><span data-stu-id="da5bc-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="da5bc-240">Izmantojot šo pieeju, nevar ierobežot piekļuvi noteiktiem ER formātam specifiskiem parametriem.</span><span class="sxs-lookup"><span data-stu-id="da5bc-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="da5bc-241">Ja jums ir jāpiemēro šādi ierobežojumi, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="da5bc-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="da5bc-242">Vai nu atkārtoti izmantojiet esošu izvēlnes elementu **ERSolutionAppSpecificParametersDesigner**, vai ieviesiet savu izvēlnes elementu **ERSolutionAppSpecificParametersDesigner**.</span><span class="sxs-lookup"><span data-stu-id="da5bc-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![Visual Studio lapa](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="da5bc-244">Izpildiet kādu no norādītajām transakcijām.</span><span class="sxs-lookup"><span data-stu-id="da5bc-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="da5bc-245">Izveidojiet jaunu izvēlnes elementu pogu un saistiet to ar atbilstošo ierakstu no tabulas **ERSolutionTable**, iestatot tās rekvizītu **Datu avots** uz **ERSolutionTable.**</span><span class="sxs-lookup"><span data-stu-id="da5bc-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![Visual Studio lapa](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="da5bc-247">Izveidojiet vienkāršu pogu un pārlabojiet metodi **Noklikšķināts**, kā tas redzams piemērā.</span><span class="sxs-lookup"><span data-stu-id="da5bc-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="da5bc-248">Izmantojot šo pieeju, varat norādīt unikālu risinājuma ID (kas definēts, izmantojot vērtību **GUID** vērtību), lai ļautu piekļūt tikai konkrētam ER formāta un sekojošām kopijām, kas no tās iegūtas.</span><span class="sxs-lookup"><span data-stu-id="da5bc-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="da5bc-249">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="da5bc-249">Additional resources</span></span>

[<span data-ttu-id="da5bc-250">Formulu veidotājs elektronisko atskaišu veidošanā</span><span class="sxs-lookup"><span data-stu-id="da5bc-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="da5bc-251">ER formātu konfigurēšana, lai izmantotu parametrus, kas ir norādīti par juridisko personu</span><span class="sxs-lookup"><span data-stu-id="da5bc-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)
