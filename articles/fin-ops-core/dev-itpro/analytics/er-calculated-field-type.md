---
title: Atbalsta Aprēķināto lauka tipa ER datu avotu parametru izsaukumus.
description: Šī tēma sniedz informāciju par to, kā izmantot Aprēķināto lauka tipu ER datu avotiem.
author: NickSelin
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 02d53f4326d8f31abf6ec7404575728837954bef
ms.sourcegitcommit: c9baf9a3b4552f0317b5ec87d252834f52df1b98
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665614"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="81b43-103">Atbalsta Aprēķināto lauka tipa ER datu avotu parametru izsaukumus.</span><span class="sxs-lookup"><span data-stu-id="81b43-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81b43-104">Šajā tēmā izskaidrots, kā var izveidot Elektronisko pārskatu (ER) datu avotu, izmantojot **Aprēķināto lauka** tipu.</span><span class="sxs-lookup"><span data-stu-id="81b43-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="81b43-105">Šis datu avots var saturēt ER izteiksmi, ko aktivizējot, var kontrolēt ar parametra argumentu vērtībām, kas konfigurētas saistījumā, kas izsauc šo datu avotu.</span><span class="sxs-lookup"><span data-stu-id="81b43-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="81b43-106">Konfigurējot šāda datu avota parametru izsaukumus, var atkārtoti izmantot vienu datu avotu daudzos saistījumos, kas samazina kopējo datu avotu skaitu, kas ir jākonfigurē ER modeļu kartēšanas vai ER formātos.</span><span class="sxs-lookup"><span data-stu-id="81b43-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="81b43-107">Tas arī vienkāršo konfigurēto ER komponentu, kas samazina uzturēšanas izmaksas, kā arī izmaksas, kas saistītas ar citiem patērētājiem.</span><span class="sxs-lookup"><span data-stu-id="81b43-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="81b43-108">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="81b43-108">Prerequisites</span></span>
<span data-ttu-id="81b43-109">Lai izpildītu šajā tēmā aprakstītos piemērus, jums ir nepieciešama tālāk norādītā piekļuve.</span><span class="sxs-lookup"><span data-stu-id="81b43-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="81b43-110">Piekļuve vienai no šīm lomām:</span><span class="sxs-lookup"><span data-stu-id="81b43-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="81b43-111">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="81b43-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="81b43-112">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="81b43-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="81b43-113">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="81b43-113">System administrator</span></span>

- <span data-ttu-id="81b43-114">Piekļuve Regulatory Configuration Services (RCS) instancei, kas ir bijusi nodrošināta tam pašam nomniekam, kuram nodrošināta Finance and Operations instance, vienai no šādām lomām:</span><span class="sxs-lookup"><span data-stu-id="81b43-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="81b43-115">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="81b43-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="81b43-116">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="81b43-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="81b43-117">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="81b43-117">System administrator</span></span>

<span data-ttu-id="81b43-118">Nepieciešams arī lejupielādēt un lokāli saglabāt tālāk norādītos failus.</span><span class="sxs-lookup"><span data-stu-id="81b43-118">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="81b43-119">**Saturs**</span><span class="sxs-lookup"><span data-stu-id="81b43-119">**Content**</span></span>                           | <span data-ttu-id="81b43-120">**Faila nosaukums**</span><span class="sxs-lookup"><span data-stu-id="81b43-120">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="81b43-121">Parauga ER datu modeļa konfigurācija</span><span class="sxs-lookup"><span data-stu-id="81b43-121">Sample ER data model configuration</span></span>    | [<span data-ttu-id="81b43-122">Modelis, lai uzzinātu parametru izsaukumus.versija.1.xml</span><span class="sxs-lookup"><span data-stu-id="81b43-122">Model to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| <span data-ttu-id="81b43-123">Parauga ER metadatu konfigurācija</span><span class="sxs-lookup"><span data-stu-id="81b43-123">Sample ER metadata configuration</span></span>      | [<span data-ttu-id="81b43-124">Metadati, lai uzzinātu parametru izsaukumus.versija.1.xml</span><span class="sxs-lookup"><span data-stu-id="81b43-124">Metadata to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| <span data-ttu-id="81b43-125">Parauga ER modeļa kartējuma konfigurācija</span><span class="sxs-lookup"><span data-stu-id="81b43-125">Sample ER model mapping configuration</span></span> | [<span data-ttu-id="81b43-126">Kartēšana, lai uzzinātu parametru izsaukumus.versija.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="81b43-126">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="81b43-127">Parauga ER formāta konfigurācija</span><span class="sxs-lookup"><span data-stu-id="81b43-127">Sample ER format configuration</span></span>        | [<span data-ttu-id="81b43-128">Formāts, lai uzzinātu parametru izsaukumus.versija.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="81b43-128">Format to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="81b43-129">Piesakieties savā RCS instancē.</span><span class="sxs-lookup"><span data-stu-id="81b43-129">Sign in to your RCS instance</span></span>
<span data-ttu-id="81b43-130">Šajā piemērā jūs izveidosiet konfigurāciju parauga uzņēmumam “Litware, Inc.”. Pirmkārt, lai izpildītu šīs darbības RCS instancē, ir jāizpilda sekojošie soļi procedūrā [Konfigurācijas nodrošinātāju izveide un atzīmēšana ar aktīvu statusu](tasks/er-configuration-provider-mark-it-active-2016-11.md):</span><span class="sxs-lookup"><span data-stu-id="81b43-130">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="81b43-131">Noklusējuma informācijas panelī atlasiet **Elektroniskais pārskats**.</span><span class="sxs-lookup"><span data-stu-id="81b43-131">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="81b43-132">Atlasiet **Pārskatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="81b43-132">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="81b43-133">Importējiet lejupielādētās konfigurācijas uz RCS šādā secībā: datu modelis, metadati, modeļa kartēšana, formāts.</span><span class="sxs-lookup"><span data-stu-id="81b43-133">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="81b43-134">Veiciet šādas darbības katrai ER konfigurācijai:</span><span class="sxs-lookup"><span data-stu-id="81b43-134">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="81b43-135">Atlasiet **Mainīt**.</span><span class="sxs-lookup"><span data-stu-id="81b43-135">Select **Exchange.**</span></span>
    2. <span data-ttu-id="81b43-136">Atlasiet **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="81b43-136">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="81b43-137">Atlasiet **Pārlūkot**, un tad atlasiet nepieciešamo ER konfigurāciju XML formātā.</span><span class="sxs-lookup"><span data-stu-id="81b43-137">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="81b43-138">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="81b43-138">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="81b43-139">Pārskatiet sniegto ER risinājumu.</span><span class="sxs-lookup"><span data-stu-id="81b43-139">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="81b43-140">Pārskatiet modeļa kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="81b43-140">Review model mapping</span></span>

1. <span data-ttu-id="81b43-141">Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.</span><span class="sxs-lookup"><span data-stu-id="81b43-141">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="81b43-142">Atlasiet **Kartēšana, lai uzzinātu parametru izsaukumus**.</span><span class="sxs-lookup"><span data-stu-id="81b43-142">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="81b43-143">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="81b43-143">Select **Designer**.</span></span>
4. <span data-ttu-id="81b43-144">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="81b43-144">Select **Designer**.</span></span>  
   
    <span data-ttu-id="81b43-145">Šī ER modeļa kartēšana ir veidota, lai veiktu šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="81b43-145">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="81b43-146">Izgūt nodokļu kodu sarakstu (**Nodokļu** datu avots), kas atrodas tabulā **TaxTable**.</span><span class="sxs-lookup"><span data-stu-id="81b43-146">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="81b43-147">Izgūt nodokļu transakciju kodu sarakstu (**Trans** datu avots), kas atrodas tabulā **TaxTrans**:</span><span class="sxs-lookup"><span data-stu-id="81b43-147">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="81b43-148">Grupēt ienesto transakciju sarakstu (**Gr** datu avots) pēc nodokļu koda.</span><span class="sxs-lookup"><span data-stu-id="81b43-148">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="81b43-149">Aprēķināt apkopotās vērtības grupētām transakcijām pēc nodokļu koda:</span><span class="sxs-lookup"><span data-stu-id="81b43-149">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="81b43-150">Nodokļu bāzes vērtību summa.</span><span class="sxs-lookup"><span data-stu-id="81b43-150">Sum of tax base values.</span></span>
            - <span data-ttu-id="81b43-151">Nodokļu vērtību summa.</span><span class="sxs-lookup"><span data-stu-id="81b43-151">Sum of tax values.</span></span>
            - <span data-ttu-id="81b43-152">Piemērotās nodokļa likmes minimālā vērtība.</span><span class="sxs-lookup"><span data-stu-id="81b43-152">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="81b43-153">Modeļa kartēšana šajā konfigurācijā implementē pamatdatu modeli jebkuram no šajā modelī izveidotajiem ER formātiem un ir izpildīts Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="81b43-153">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="81b43-154">Tādējādi **Nodokļu** un **Gr** datu avotu saturs ir pakļauts ER formātiem, piemēram, abstraktiem datu avotiem.</span><span class="sxs-lookup"><span data-stu-id="81b43-154">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![Modeļa kartēšanas veidotāja lapa, kurā parādīti Tax un Gr datu avoti](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="81b43-156">Aizveriet lapu **Modeļa kartējuma noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="81b43-156">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="81b43-157">Aizveriet lapu **Modeļa kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="81b43-157">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="81b43-158">Pārskata formāts</span><span class="sxs-lookup"><span data-stu-id="81b43-158">Review format</span></span>

1. <span data-ttu-id="81b43-159">Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.</span><span class="sxs-lookup"><span data-stu-id="81b43-159">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="81b43-160">Atlasiet **Formatēt, lai uzzinātu parametru izsaukumus**.</span><span class="sxs-lookup"><span data-stu-id="81b43-160">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="81b43-161">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="81b43-161">Select **Designer**.</span></span> <span data-ttu-id="81b43-162">Šī ER formāta kartēšana ir veidota, lai veiktu šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="81b43-162">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="81b43-163">Izveidot nodokļu paziņojumu xml formātā.</span><span class="sxs-lookup"><span data-stu-id="81b43-163">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="81b43-164">Parādīt sekojošos nodokļu līmeņus nodokļu pārskatā: parasts, samazināts un nav.</span><span class="sxs-lookup"><span data-stu-id="81b43-164">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="81b43-165">Parādīt vairākas detaļas katrā nodokļu līmenī, kam katrā līmenī ir dažāds šo detaļu skaits. </span><span class="sxs-lookup"><span data-stu-id="81b43-165">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![Formāta veidotāja lapa](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="81b43-167">Atlasīt **Kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="81b43-167">Select **Mapping**.</span></span>
5. <span data-ttu-id="81b43-168">Izvērst **modeli**, **datus** un **kopsavilkuma** elementus.</span><span class="sxs-lookup"><span data-stu-id="81b43-168">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="81b43-169">Aprēķinātā lauka **Model.Data.Summary.Level** ir izteiksme, kas atgriež nodokļu līmeņa kodu (**Parasts**, **Samazināts**, **Nav** vai **cits**) kā teksta vērtība jebkuram nodokļa kodam, ko var izgūt no **Model.Data.Summary** datu avota izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="81b43-169">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![Formāta veidotāja lapa, kas uzrāda Dara model modeļa detaļas, lai apgūtu parametru izsaukumus.](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="81b43-171">Izvērsiet **Modeli**. **Data2** krājums.</span><span class="sxs-lookup"><span data-stu-id="81b43-171">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="81b43-172">Izvērsiet **Modeli**. **Data2.Summary2** krājums.</span><span class="sxs-lookup"><span data-stu-id="81b43-172">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="81b43-173">**Modeļa**. **Data2. Summary2** datu avots ir konfigurēts, lai grupētu **Model.Data.Summary** kopsavilkuma datu avota transakcijas detalizētu informāciju pēc taksācijas līmeņa (atgriezis **Model.Data.Summary.Level** aprēķinātais lauks) un aprēķinātu apkopojumus.</span><span class="sxs-lookup"><span data-stu-id="81b43-173">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![Formāta veidotāja lapa, kas rāda detalizētu informāciju par Model.Data2.Summary2 datu avotu.](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="81b43-175">Pārskatīt aprēķināto lauku **Modelis**. **Data2.Level1**, **Modelis**. **Data2.Level2**un **Modelis**. **Data2. Level3.**</span><span class="sxs-lookup"><span data-stu-id="81b43-175">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="81b43-176">Šie aprēķinātie lauki tiek izmantoti **Modeļa** filtrēšanai. **Data2.Summary2** ieraksti saraksts un atgriezt tikai tos ierakstus, kas atbilst noteiktam nodokļu līmenim.</span><span class="sxs-lookup"><span data-stu-id="81b43-176">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="81b43-177">Aizveriet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="81b43-177">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="81b43-178">Atvasināta formāta izveide</span><span class="sxs-lookup"><span data-stu-id="81b43-178">Create a derived format</span></span>
<span data-ttu-id="81b43-179">Varat uzlabot norādīto formātu, pievienojot vienu aprēķināto lauku, lai filtrētu nepieciešamo nodokļu līmeni, nevis izmantotu esošos trīs laukus: **Modelis**.**Data2.Level1**, **Modelis**. **Data2.Level2** un **Modelis**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="81b43-179">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="81b43-180">Nepieciešamo nodokļu līmeni var norādīt vietā, kur tiks izsaukts šis jaunais aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="81b43-180">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="81b43-181">Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.</span><span class="sxs-lookup"><span data-stu-id="81b43-181">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="81b43-182">Atlasiet **Formatēt, lai uzzinātu parametru izsaukumus**.</span><span class="sxs-lookup"><span data-stu-id="81b43-182">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="81b43-183">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="81b43-183">Select **Create configuration**.</span></span>
4. <span data-ttu-id="81b43-184">Atlasiet **Atvasināt no nosaukuma: formatēt, lai uzzinātu parametru izsaukumus, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="81b43-184">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="81b43-185">Laukā **Nosaukums** ievadiet **Formāts parametru izsaukumu (klentu) apgūšanai**.</span><span class="sxs-lookup"><span data-stu-id="81b43-185">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="81b43-186">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="81b43-186">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="81b43-187">Konfigurēt parametru aprēķināto lauku, kas atgriež ierakstu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="81b43-187">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="81b43-188">Sākt pievienot jaunu aprēķināto lauku</span><span class="sxs-lookup"><span data-stu-id="81b43-188">Start adding a new calculated field</span></span>

1. <span data-ttu-id="81b43-189">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="81b43-189">Select **Designer**.</span></span>
2. <span data-ttu-id="81b43-190">Atlasiet **Izvērst/sakļaut**, lai izvērstu visus formāta vienumus.</span><span class="sxs-lookup"><span data-stu-id="81b43-190">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="81b43-191">Atlasiet **Kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="81b43-191">Select **Mapping**.</span></span>
4. <span data-ttu-id="81b43-192">Izvērsiet **Modelis** vienumu.</span><span class="sxs-lookup"><span data-stu-id="81b43-192">Expand the **Model** item.</span></span>
5. <span data-ttu-id="81b43-193">Atlasiet **Model.Data2** vienumu.</span><span class="sxs-lookup"><span data-stu-id="81b43-193">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="81b43-194">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="81b43-194">Select **Add**.</span></span>
7. <span data-ttu-id="81b43-195">Atlasiet **Funkcijas\\Aprēķinātais lauks**.</span><span class="sxs-lookup"><span data-stu-id="81b43-195">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="81b43-196">Laukā **Nosaukums** ievadiet **Līmeņi**.</span><span class="sxs-lookup"><span data-stu-id="81b43-196">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="81b43-197">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="81b43-197">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="81b43-198">Definējiet aprēķinātā lauka pievienošanas parametru</span><span class="sxs-lookup"><span data-stu-id="81b43-198">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="81b43-199">Atlasiet **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="81b43-199">Select **Parameters**.</span></span>
2. <span data-ttu-id="81b43-200">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="81b43-200">Select **New**.</span></span>
3. <span data-ttu-id="81b43-201">Laukā **Nosaukums** ievadiet **Nodokļu līmenis**.</span><span class="sxs-lookup"><span data-stu-id="81b43-201">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="81b43-202">Laukā **Tips** atlasiet **Virkne**.</span><span class="sxs-lookup"><span data-stu-id="81b43-202">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="81b43-203">Lai norādītu parametra argumenta tipu, var izmantot tikai primitīvos datu tipus.</span><span class="sxs-lookup"><span data-stu-id="81b43-203">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="81b43-204">Tāpēc **Ierakstu saraksts**, **Ieraksts**un **Uzskaitījums** tipus šim nolūkam nevar izmantot.</span><span class="sxs-lookup"><span data-stu-id="81b43-204">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="81b43-205">Maksimālais parametru skaits, ko var norādīt vienam aprēķinātajam laukam, ir 8.</span><span class="sxs-lookup"><span data-stu-id="81b43-205">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Parametru datu avota saraksts](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="81b43-207">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="81b43-207">Select **OK**.</span></span>

<span data-ttu-id="81b43-208">Pievienojot šo parametru, jūs norādiet nosacījumu, kam jābūt, lai izsauktu šo aprēķināto lauku.</span><span class="sxs-lookup"><span data-stu-id="81b43-208">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="81b43-209">Kad izsaucat šo aprēķināto lauku, ir jānorāda **Nodokļu līmeņa** parametra arguments kā vērtība ar **Virknes** formātu.</span><span class="sxs-lookup"><span data-stu-id="81b43-209">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="81b43-210">Pārliecinieties, vai nosakāt parametrus tikai tiem aprēķinātajiem laukiem, kas atrodas konteinerā (vai nu **Ierakstu sarakstā**, **Ierakstā** vai **Konteinerā**).</span><span class="sxs-lookup"><span data-stu-id="81b43-210">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="81b43-211">Konfigurētais parametrs ir pieejams datu avotu sarakstā šim aprēķinātajam laukam.</span><span class="sxs-lookup"><span data-stu-id="81b43-211">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="81b43-212">Varat pievienot parametru konfigurētajai izteiksmei, atlasot **Pievienot datu avotu**.</span><span class="sxs-lookup"><span data-stu-id="81b43-212">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Datu avota lauki](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="81b43-214">Definēt aprēķinātā lauka pievienošanas izteiksmi</span><span class="sxs-lookup"><span data-stu-id="81b43-214">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="81b43-215">Laukā **Fomula** ievadiet:</span><span class="sxs-lookup"><span data-stu-id="81b43-215">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="81b43-216">**KUR (\@. Summary2, \@. Summary2. grupēts. līmenis =**</span><span class="sxs-lookup"><span data-stu-id="81b43-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="81b43-217">Atlasiet **Nodokļu līmeņa** parametru datu avotu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="81b43-217">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="81b43-218">Atlasiet **Pievienot datu avotu**.</span><span class="sxs-lookup"><span data-stu-id="81b43-218">Select **Add data source**.</span></span>
4. <span data-ttu-id="81b43-219">Laukā **Formula** pabeidziet izteiksmi ar:</span><span class="sxs-lookup"><span data-stu-id="81b43-219">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="81b43-220">**KUR(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="81b43-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="81b43-221">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="81b43-221">Select **Save**.</span></span>

    ![Datu avota lauka informācija](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="81b43-223">Aizveriet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="81b43-223">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="81b43-224">Pabeigt pievienot jaunu aprēķināto lauku</span><span class="sxs-lookup"><span data-stu-id="81b43-224">Finish adding a new calculated field</span></span>

- <span data-ttu-id="81b43-225">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="81b43-225">Select **OK**.</span></span>

<span data-ttu-id="81b43-226">Lapā **Formāta veidotājs**  konfigurētajam parametru aprēķinātajam laukam **Līmeņi** nepieciešams **Virknes** arguments.</span><span class="sxs-lookup"><span data-stu-id="81b43-226">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Izvērsts aprēķināto lauku līmeņu saraksts](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="81b43-228">Izmantojiet konfigurēto aprēķināto lauku saistījuma formāta elementiem</span><span class="sxs-lookup"><span data-stu-id="81b43-228">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="81b43-229">Atlasiet **Model.Data2.Levels**, lai atlasītu konfigurēto aprēķināto lauku.</span><span class="sxs-lookup"><span data-stu-id="81b43-229">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="81b43-230">Atlasiet **Statement.Taxation.Regular** formāta elementu.</span><span class="sxs-lookup"><span data-stu-id="81b43-230">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="81b43-231">Atlasiet **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="81b43-231">Select **Bind**.</span></span>
4. <span data-ttu-id="81b43-232">Atlasiet **Jā**, lai apstiprinātu pašlaik izmantotā datu avota  **Level1** aizstāšanu ar jauno avotu **Līmeņi** visos atlasītā formāta elementa ligzdotu formātu elementos. </span><span class="sxs-lookup"><span data-stu-id="81b43-232">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="81b43-233">Piemērotais saistījums ir izveidots kā izsaukums aprēķinātajam parametru laukam.</span><span class="sxs-lookup"><span data-stu-id="81b43-233">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="81b43-234">Pēc noklusējuma saistītā formāta elementa nosaukums tiek izmantots kā arguments parametru aprēķinātajam laukam šādos apstākļos:</span><span class="sxs-lookup"><span data-stu-id="81b43-234">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="81b43-235">Aprēķinātais lauks ir konfigurēts, lai izmantotu vienu parametru.</span><span class="sxs-lookup"><span data-stu-id="81b43-235">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="81b43-236">Šī parametra datu tips ir definēts kā **Virkne.**</span><span class="sxs-lookup"><span data-stu-id="81b43-236">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="81b43-237">Ja saistītā formāta elementa nosaukums ir tukšs, lietotajā saistījumā tiek izmantots šī elementa datu avota nosaukums.</span><span class="sxs-lookup"><span data-stu-id="81b43-237">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="81b43-238">Atlasiet **Statement.Taxation.Reduced** formāta elementu.</span><span class="sxs-lookup"><span data-stu-id="81b43-238">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="81b43-239">Atlasiet **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="81b43-239">Select **Bind**.</span></span>
7. <span data-ttu-id="81b43-240">Atlasiet **Jā**, lai apstiprinātu pašlaik izmantotā datu avota  **Level2** aizstāšanu ar jauno avotu **Līmeņi** visos ligzdotu formātu elementos zem atlasītā formāta elementa.</span><span class="sxs-lookup"><span data-stu-id="81b43-240">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="81b43-241">Atlasiet **Statement.Taxation.None** formāta elementu.</span><span class="sxs-lookup"><span data-stu-id="81b43-241">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="81b43-242">Atlasiet **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="81b43-242">Select **Bind**.</span></span>
10. <span data-ttu-id="81b43-243">Atlasiet **Jā**, lai apstiprinātu pašlaik izmantotā datu avota  **Level3** aizstāšanu ar jauno avotu **Līmeņi** visos ligzdotu formātu elementos zem atlasītā formāta elementa.</span><span class="sxs-lookup"><span data-stu-id="81b43-243">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="81b43-244">Norādot aprēķinātā lauka parametru argumentu XML elementam, kas apzīmē nodokļu līmeni (piemēram, **Model.Data2.Levels("Reduced")** kā teksta vērtība), jums nav jādara tas pats ligzdotajiem XML atribūtiem — to saistījumi automātiski mantos argumenta vērtību, kas definēta pamatlīmenī (**Model.Data2.Levels.aggregated.Base**, nevis **Model.Data2.Levels("Reduced").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="81b43-244">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="81b43-245">Jebkura parametra aprēķinātā lauka atkārtotie izsaukumi netiek atbalstīti.</span><span class="sxs-lookup"><span data-stu-id="81b43-245">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="81b43-246">Varat atlasīt **Rediģēt formulu**un mainīt noklusējuma argumenta aprēķināto parametru, kas lietots atlasītajā saistījumā.</span><span class="sxs-lookup"><span data-stu-id="81b43-246">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="81b43-247">Ja šī argumenta nav, tas var radīt kļūdas izpildes laikā — lietotāji tiek informēti par šādu situāciju, kad pašreizējais formāts ir apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="81b43-247">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Apstiprinājuma brīdinājuma paziņojums](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="81b43-249">Konfigurēt parametru aprēķināto lauku, lai atgrieztu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="81b43-249">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="81b43-250">Kad aprēķinātais parametru lauks atgriež ierakstu, jums ir jāatbalsta atsevišķu šī ieraksta lauku saistījums, lai formatētu elementus.</span><span class="sxs-lookup"><span data-stu-id="81b43-250">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="81b43-251">Šādos gadījumos nebūs pamata saistījuma, kas ietver argumenta vērtību, lai izsauktu aprēķināto parametru lauku — šī vērtība ir jādefinē viena ieraksta lauka saistījumā.</span><span class="sxs-lookup"><span data-stu-id="81b43-251">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="81b43-252">Sākt pievienot jaunu aprēķināto lauku</span><span class="sxs-lookup"><span data-stu-id="81b43-252">Start adding a new calculated field</span></span>

1. <span data-ttu-id="81b43-253">Atlasīt **Model.Data2** vienumu.</span><span class="sxs-lookup"><span data-stu-id="81b43-253">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="81b43-254">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="81b43-254">Select **Add**.</span></span>
3. <span data-ttu-id="81b43-255">Atlasiet **Funkcijas\\Aprēķinātais lauks**.</span><span class="sxs-lookup"><span data-stu-id="81b43-255">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="81b43-256">Laukā **Nosaukums** ievadiet **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="81b43-256">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="81b43-257">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="81b43-257">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="81b43-258">Definēt aprēķinātā lauka pievienošanas parametru</span><span class="sxs-lookup"><span data-stu-id="81b43-258">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="81b43-259">Atlasiet **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="81b43-259">Select **Parameters**.</span></span>
2. <span data-ttu-id="81b43-260">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="81b43-260">Select **New**.</span></span>
3. <span data-ttu-id="81b43-261">Laukā **Nosaukums** ievadiet **Nodokļu līmenis**.</span><span class="sxs-lookup"><span data-stu-id="81b43-261">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="81b43-262">Laukā **Tips** atlasiet **Virkne**.</span><span class="sxs-lookup"><span data-stu-id="81b43-262">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="81b43-263">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="81b43-263">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="81b43-264">Definēt aprēķinātā lauka pievienošanas izteiksmi</span><span class="sxs-lookup"><span data-stu-id="81b43-264">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="81b43-265">Laukā **Formula** ievadiet šādu izteiksmi:</span><span class="sxs-lookup"><span data-stu-id="81b43-265">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="81b43-266">**FIRSTORNULL (\@.Līmeņi(**</span><span class="sxs-lookup"><span data-stu-id="81b43-266">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="81b43-267">Atlasiet **Nodokļu līmenis** parametru.</span><span class="sxs-lookup"><span data-stu-id="81b43-267">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="81b43-268">Atlasiet **Pievienot datu avotu**.</span><span class="sxs-lookup"><span data-stu-id="81b43-268">Select **Add data source**.</span></span>
4. <span data-ttu-id="81b43-269">Laukā **Formula** pievienojiet **'Nodokļu līmenis'))**, ko ievadījāt 1. solī, lai pabeigtu izteiksmi:</span><span class="sxs-lookup"><span data-stu-id="81b43-269">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="81b43-270">**FIRSTORNULL (\@.Līmenis('Nodokļu līmenis'))**</span><span class="sxs-lookup"><span data-stu-id="81b43-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="81b43-271">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="81b43-271">Select **Save**.</span></span>
6. <span data-ttu-id="81b43-272">Aizveriet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="81b43-272">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="81b43-273">Pabeigt pievienot jaunu aprēķināto lauku</span><span class="sxs-lookup"><span data-stu-id="81b43-273">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="81b43-274">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="81b43-274">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="81b43-275">Izmantojiet konfigurēto aprēķināto lauku, lai saistītu formāta elementus.</span><span class="sxs-lookup"><span data-stu-id="81b43-275">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="81b43-276">Izvērsiet **Model.Data2.LevelRecord**, lai atlasītu konfigurēto aprēķināto lauku.</span><span class="sxs-lookup"><span data-stu-id="81b43-276">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="81b43-277">Izvērsiet **Model.Data2.LevelRecord.aggregated** konfigurēto aprēķinātā lauka konteineru.</span><span class="sxs-lookup"><span data-stu-id="81b43-277">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="81b43-278">Atlasiet **Model.Data2.LevelRecord.aggregated.Base** lauku.</span><span class="sxs-lookup"><span data-stu-id="81b43-278">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="81b43-279">Atlasiet **Statement.Taxation.None** formāta elementu.</span><span class="sxs-lookup"><span data-stu-id="81b43-279">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="81b43-280">Atlasiet **Atsaistīt**.</span><span class="sxs-lookup"><span data-stu-id="81b43-280">Select **Unbind**.</span></span>
6. <span data-ttu-id="81b43-281">Atlasiet **Statement.Taxation.None.Base** formāta elementu.</span><span class="sxs-lookup"><span data-stu-id="81b43-281">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="81b43-282">Atlasiet **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="81b43-282">Select **Bind**.</span></span>
8. <span data-ttu-id="81b43-283">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="81b43-283">Select **Edit formula**.</span></span>
9. <span data-ttu-id="81b43-284">Mainiet izteiksmi uz **Model.Data2.LevelRecord("None").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="81b43-284">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Atjauninātā izteiksme](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="81b43-286">Noņemt aprēķinātos laukus, kas netiek lietoti</span><span class="sxs-lookup"><span data-stu-id="81b43-286">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="81b43-287">Atlasiet **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="81b43-287">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="81b43-288">Atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="81b43-288">Select **Delete**.</span></span>
3. <span data-ttu-id="81b43-289">Atlasiet **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="81b43-289">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="81b43-290">Atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="81b43-290">Select **Delete**.</span></span>
5. <span data-ttu-id="81b43-291">Atlasiet **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="81b43-291">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="81b43-292">Atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="81b43-292">Select **Delete**.</span></span>
7. <span data-ttu-id="81b43-293">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="81b43-293">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="81b43-294">Jūs atkārtoti izmantojāt to pašu aprēķināto lauku **Model.Data2.Levels** formāta saistījumos.</span><span class="sxs-lookup"><span data-stu-id="81b43-294">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="81b43-295">Ir daudz vieglāk lietot un uzturēt vienu aprēķināto lauku, nekā darīt to pašu vairākiem līdzīgiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="81b43-295">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="81b43-296">Aizveriet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="81b43-296">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="81b43-297">Pabeigta atvasinātā formāta pielāgota versija</span><span class="sxs-lookup"><span data-stu-id="81b43-297">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="81b43-298">Kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="81b43-298">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="81b43-299">Atlasiet **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="81b43-299">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="81b43-300">Eksportēt atvasinātā formāta pabeigtu versiju.</span><span class="sxs-lookup"><span data-stu-id="81b43-300">Export completed version of a derived format</span></span>

1. <span data-ttu-id="81b43-301">Atlasiet **Formatēt, lai uzzinātu parametru izsaukumu (pielāgots)**  formātu konfigurācijas kokā.</span><span class="sxs-lookup"><span data-stu-id="81b43-301">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="81b43-302">Kopsavilkuma cilnē **Versijas**  atlasiet pabeigto versiju 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="81b43-302">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="81b43-303">Atlasiet **Maiņa**.</span><span class="sxs-lookup"><span data-stu-id="81b43-303">Select **Exchange**.</span></span>
4. <span data-ttu-id="81b43-304">Atlasiet **Eksportēt kā XML failu**.</span><span class="sxs-lookup"><span data-stu-id="81b43-304">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="81b43-305">Saglabājiet lejupielādēto konfigurāciju lokāli XML formātā.</span><span class="sxs-lookup"><span data-stu-id="81b43-305">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="81b43-306">Testa ER formāti</span><span class="sxs-lookup"><span data-stu-id="81b43-306">Test ER formats</span></span> 
<span data-ttu-id="81b43-307">Jūs varat palaist sākotnējos un uzlabotos ER formātus, lai pārliecinātos, ka konfigurētie parametru aprēķinātie lauki darbojas pareizi.</span><span class="sxs-lookup"><span data-stu-id="81b43-307">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="81b43-308">ER konfigurāciju importēšana</span><span class="sxs-lookup"><span data-stu-id="81b43-308">Import ER configurations</span></span>
<span data-ttu-id="81b43-309">Jūs varat importēt pārskatītās konfigurācijas no RCS, izmantojot **RCS** tipa ER repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="81b43-309">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="81b43-310">Ja esat jau izgājis darbības tēmā, [Importēt elektronisko pārskatu (EP) konfigurācijas no Regulatory Configuration Services (RCS)](rcs-download-configurations.md), izmantojiet konfigurēto ER repozitoriju, lai importētu konfigurācijas, kas iepriekš šajā tēmā jau apspriestas.</span><span class="sxs-lookup"><span data-stu-id="81b43-310">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="81b43-311">Pretējā gadījumā rīkojieties sekojoši:</span><span class="sxs-lookup"><span data-stu-id="81b43-311">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="81b43-312">Atlasiet **DEMF** uzņēmumu un noklusējuma informācijas panelī atlasiet **Elektroniskais pārskats**.</span><span class="sxs-lookup"><span data-stu-id="81b43-312">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="81b43-313">Atlasiet **Pārskatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="81b43-313">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="81b43-314">Importējiet konfigurācijas no Microsoft Download Center šādā secībā: datu modelis, modeļa kartēšana, formāts.</span><span class="sxs-lookup"><span data-stu-id="81b43-314">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="81b43-315">Veiciet šādas darbības katrai ER konfigurācijai:</span><span class="sxs-lookup"><span data-stu-id="81b43-315">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="81b43-316">Atlasiet **Mainīt**.</span><span class="sxs-lookup"><span data-stu-id="81b43-316">Select **Exchange.**</span></span>
    2. <span data-ttu-id="81b43-317">Atlasiet **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="81b43-317">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="81b43-318">Atlasiet **Pārlūkot**, lai atlasītu nepieciešamo ER konfigurāciju XML formātā.</span><span class="sxs-lookup"><span data-stu-id="81b43-318">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="81b43-319">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="81b43-319">Select **OK**.</span></span>

4. <span data-ttu-id="81b43-320">Importēt eksportētā **Formatēt, lai uzzinātu parametru izsaukumus (pielāgots)** formāta no RCS pabeigtās 1.1.1. versijas:</span><span class="sxs-lookup"><span data-stu-id="81b43-320">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="81b43-321">Atlasiet **Mainīt**.</span><span class="sxs-lookup"><span data-stu-id="81b43-321">Select **Exchange.**</span></span>
    2. <span data-ttu-id="81b43-322">Atlasiet **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="81b43-322">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="81b43-323">Atlasiet **Pārlūkot**, lai atlasītu lokāli saglabāto failu **Formatēt, lai uzzinātu parametru izsaukumus (pielāgots)**  XML formātā.</span><span class="sxs-lookup"><span data-stu-id="81b43-323">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="81b43-324">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="81b43-324">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="81b43-325">Palaidiet ER formātus</span><span class="sxs-lookup"><span data-stu-id="81b43-325">Run ER formats</span></span>

1. <span data-ttu-id="81b43-326">Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.</span><span class="sxs-lookup"><span data-stu-id="81b43-326">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="81b43-327">Atlasiet **Formatēt, lai uzzinātu parametru izsaukumus**.</span><span class="sxs-lookup"><span data-stu-id="81b43-327">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="81b43-328">Atlasiet **Palaist** visaugstākajā lentē.</span><span class="sxs-lookup"><span data-stu-id="81b43-328">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="81b43-329">Saglabāt lokāli ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="81b43-329">Save the locally generated output.</span></span>
5. <span data-ttu-id="81b43-330">Atlasiet vienumu **Formatēt, lai uzzinātu parametru izsaukumus (pielāgots)**.</span><span class="sxs-lookup"><span data-stu-id="81b43-330">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="81b43-331">Atlasiet **Palaist** visaugstākajā lentē.</span><span class="sxs-lookup"><span data-stu-id="81b43-331">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="81b43-332">Saglabāt lokāli ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="81b43-332">Save the generated output locally.</span></span> 
8. <span data-ttu-id="81b43-333">Salīdziniet ģenerēto rezultātu saturu.</span><span class="sxs-lookup"><span data-stu-id="81b43-333">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81b43-334">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="81b43-334">Additional resources</span></span>
[<span data-ttu-id="81b43-335">Formulas veidotājs elektronisko pārskatu veidošanā (ER)</span><span class="sxs-lookup"><span data-stu-id="81b43-335">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
