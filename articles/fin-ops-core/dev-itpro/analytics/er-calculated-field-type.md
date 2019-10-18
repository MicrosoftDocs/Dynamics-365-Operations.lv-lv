---
title: Atbalsta Aprēķināto lauka tipa ER datu avotu parametru izsaukumus
description: Šī tēma sniedz informāciju par to, kā izmantot Aprēķināto lauka tipu ER datu avotiem.
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
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
ms.openlocfilehash: 86efa927fa97be0d54e965bf33b1a18519025c22
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248681"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="972bc-103">Atbalsta Aprēķināto lauka tipa ER datu avotu parametru izsaukumus.</span><span class="sxs-lookup"><span data-stu-id="972bc-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="972bc-104">Šajā tēmā izskaidrots, kā var izveidot Elektronisko pārskatu (ER) datu avotu, izmantojot **Aprēķināto lauka** tipu.</span><span class="sxs-lookup"><span data-stu-id="972bc-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="972bc-105">Šis datu avots var saturēt ER izteiksmi, ko aktivizējot, var kontrolēt ar parametra argumentu vērtībām, kas konfigurētas saistījumā, kas izsauc šo datu avotu.</span><span class="sxs-lookup"><span data-stu-id="972bc-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="972bc-106">Konfigurējot šāda datu avota parametru izsaukumus, var atkārtoti izmantot vienu datu avotu daudzos saistījumos, kas samazina kopējo datu avotu skaitu, kas ir jākonfigurē ER modeļu kartēšanas vai ER formātos.</span><span class="sxs-lookup"><span data-stu-id="972bc-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="972bc-107">Tas arī vienkāršo konfigurēto ER komponentu, kas samazina uzturēšanas izmaksas, kā arī izmaksas, kas saistītas ar citiem patērētājiem.</span><span class="sxs-lookup"><span data-stu-id="972bc-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="972bc-108">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="972bc-108">Prerequisites</span></span>
<span data-ttu-id="972bc-109">Lai izpildītu šajā tēmā aprakstītos piemērus, jums ir nepieciešama tālāk norādītā piekļuve.</span><span class="sxs-lookup"><span data-stu-id="972bc-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="972bc-110">Piekļuve vienai no šīm lomām:</span><span class="sxs-lookup"><span data-stu-id="972bc-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="972bc-111">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="972bc-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="972bc-112">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="972bc-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="972bc-113">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="972bc-113">System administrator</span></span>

- <span data-ttu-id="972bc-114">Piekļuve Regulatory Configuration Services (RCS) instancei, kas ir bijusi nodrošināta tam pašam nomniekam, kuram nodrošināta Finance and Operations instance, vienai no šādām lomām:</span><span class="sxs-lookup"><span data-stu-id="972bc-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="972bc-115">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="972bc-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="972bc-116">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="972bc-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="972bc-117">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="972bc-117">System administrator</span></span>

<span data-ttu-id="972bc-118">No [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=874684) lejupielādējiet saspiesto (zip) failu **Atbalstīt parametru izsaukumus no Aprēķinātā lauka tipa ER datu avotiem**.</span><span class="sxs-lookup"><span data-stu-id="972bc-118">From the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684), download the zipped (compressed) file **Support parameterized calls of ER data sources of Calculated field type**.</span></span> <span data-ttu-id="972bc-119">Tajā ir šādas ER konfigurācijas, kas ir jāizvelk un jāuzglabā lokāli.</span><span class="sxs-lookup"><span data-stu-id="972bc-119">It contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="972bc-120">**Saturs**</span><span class="sxs-lookup"><span data-stu-id="972bc-120">**Content**</span></span>                           | <span data-ttu-id="972bc-121">**Faila nosaukums**</span><span class="sxs-lookup"><span data-stu-id="972bc-121">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="972bc-122">Parauga ER datu modeļa konfigurācija</span><span class="sxs-lookup"><span data-stu-id="972bc-122">Sample ER data model configuration</span></span>    | <span data-ttu-id="972bc-123">Modelis, lai uzzinātu parametru izsaukumus.versija.1.xml</span><span class="sxs-lookup"><span data-stu-id="972bc-123">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="972bc-124">Parauga ER metadatu konfigurācija</span><span class="sxs-lookup"><span data-stu-id="972bc-124">Sample ER metadata configuration</span></span>      | <span data-ttu-id="972bc-125">Metadati, lai uzzinātu parametru izsaukumus.versija.1.xml</span><span class="sxs-lookup"><span data-stu-id="972bc-125">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="972bc-126">Parauga ER modeļa kartējuma konfigurācija</span><span class="sxs-lookup"><span data-stu-id="972bc-126">Sample ER model mapping configuration</span></span> | <span data-ttu-id="972bc-127">Kartēšana, lai uzzinātu parametru izsaukumus.versija.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="972bc-127">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="972bc-128">Parauga ER formāta konfigurācija</span><span class="sxs-lookup"><span data-stu-id="972bc-128">Sample ER format configuration</span></span>        | <span data-ttu-id="972bc-129">Formāts, lai uzzinātu parametru izsaukumus.versija.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="972bc-129">Format to learn parameterized calls.version.1.1.xml</span></span>  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="972bc-130">Piesakieties savā RCS instancē.</span><span class="sxs-lookup"><span data-stu-id="972bc-130">Sign in to your RCS instance</span></span>
<span data-ttu-id="972bc-131">Šajā piemērā jūs izveidosiet konfigurāciju parauga uzņēmumam “Litware, Inc.”. Pirmkārt, lai izpildītu šīs darbības RCS instancē, ir jāizpilda sekojošie soļi procedūrā [Konfigurācijas nodrošinātāja izveide un atzīmēšana ar aktīvu statusu](tasks/er-configuration-provider-mark-it-active-2016-11.md):</span><span class="sxs-lookup"><span data-stu-id="972bc-131">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="972bc-132">Noklusējuma informācijas panelī atlasiet **Elektroniskais pārskats**.</span><span class="sxs-lookup"><span data-stu-id="972bc-132">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="972bc-133">Atlasiet **Pārskatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="972bc-133">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="972bc-134">Importējiet lejupielādētās konfigurācijas uz RCS šādā secībā: datu modelis, metadati, modeļa kartēšana, formāts.</span><span class="sxs-lookup"><span data-stu-id="972bc-134">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="972bc-135">Veiciet šādas darbības katrai ER konfigurācijai:</span><span class="sxs-lookup"><span data-stu-id="972bc-135">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="972bc-136">Atlasiet **Mainīt**.</span><span class="sxs-lookup"><span data-stu-id="972bc-136">Select **Exchange.**</span></span>
    2. <span data-ttu-id="972bc-137">Atlasiet **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="972bc-137">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="972bc-138">Atlasiet **Pārlūkot**, un tad atlasiet nepieciešamo ER konfigurāciju XML formātā.</span><span class="sxs-lookup"><span data-stu-id="972bc-138">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="972bc-139">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="972bc-139">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="972bc-140">Pārskatiet sniegto ER risinājumu.</span><span class="sxs-lookup"><span data-stu-id="972bc-140">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="972bc-141">Pārskatiet modeļa kartēšanu.</span><span class="sxs-lookup"><span data-stu-id="972bc-141">Review model mapping</span></span>

1. <span data-ttu-id="972bc-142">Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.</span><span class="sxs-lookup"><span data-stu-id="972bc-142">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="972bc-143">Atlasiet **Kartēšana, lai uzzinātu parametru izsaukumus**.</span><span class="sxs-lookup"><span data-stu-id="972bc-143">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="972bc-144">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="972bc-144">Select **Designer**.</span></span>
4. <span data-ttu-id="972bc-145">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="972bc-145">Select **Designer**.</span></span>  
   
<span data-ttu-id="972bc-146">Šī ER modeļa kartēšana ir veidota, lai veiktu šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="972bc-146">This ER model mapping is designed to do the following:</span></span>

- <span data-ttu-id="972bc-147">Izgūt nodokļu kodu sarakstu (**Nodokļu** datu avots), kas atrodas tabulā **TaxTable**.</span><span class="sxs-lookup"><span data-stu-id="972bc-147">Fetch the list of tax codes (**Tax** data source) residing in the   **TaxTable** table.</span></span>
- <span data-ttu-id="972bc-148">Izgūt nodokļu transakciju kodu sarakstu (**Trans** datu avots), kas atrodas tabulā **TaxTrans**:</span><span class="sxs-lookup"><span data-stu-id="972bc-148">Fetch the list of tax transactions (**Trans** data source) residing in the   **TaxTrans** table:</span></span>
    
    - <span data-ttu-id="972bc-149">Grupēt ienesto transakciju sarakstu (**Gr** datu avots) pēc nodokļu koda.</span><span class="sxs-lookup"><span data-stu-id="972bc-149">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
    - <span data-ttu-id="972bc-150">Aprēķināt apkopotās vērtības grupētām transakcijām pēc nodokļu koda:</span><span class="sxs-lookup"><span data-stu-id="972bc-150">Calculate for grouped transactions following aggregated values per   tax code:</span></span>

        - <span data-ttu-id="972bc-151">Nodokļu bāzes vērtību summa.</span><span class="sxs-lookup"><span data-stu-id="972bc-151">Sum of tax base values.</span></span>
        - <span data-ttu-id="972bc-152">Nodokļu vērtību summa.</span><span class="sxs-lookup"><span data-stu-id="972bc-152">Sum of tax values.</span></span>
        - <span data-ttu-id="972bc-153">Piemērotās nodokļa likmes minimālā vērtība.</span><span class="sxs-lookup"><span data-stu-id="972bc-153">Minimum value of applied tax rate.</span></span>

<span data-ttu-id="972bc-154">Modeļa kartēšana šajā konfigurācijā implementē pamatdatu modeli jebkuram no šajā modelī izveidotajiem ER formātiem un ir izpildīts Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="972bc-154">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="972bc-155">Tādējādi **Nodokļu** un **Gr** datu avotu saturs ir pakļauts ER formātiem, piemēram, abstraktiem datu avotiem.</span><span class="sxs-lookup"><span data-stu-id="972bc-155">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

  ![Modeļa kartēšanas veidotāja lapa, kurā parādīti Tax un Gr datu avoti](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="972bc-157">Aizveriet lapu **Modeļa kartējuma noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="972bc-157">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="972bc-158">Aizveriet lapu **Modeļa kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="972bc-158">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="972bc-159">Pārskata formāts</span><span class="sxs-lookup"><span data-stu-id="972bc-159">Review format</span></span>

1. <span data-ttu-id="972bc-160">Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.</span><span class="sxs-lookup"><span data-stu-id="972bc-160">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="972bc-161">Atlasiet **Formatēt, lai uzzinātu parametru izsaukumus**.</span><span class="sxs-lookup"><span data-stu-id="972bc-161">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="972bc-162">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="972bc-162">Select **Designer**.</span></span> <span data-ttu-id="972bc-163">Šī ER formāta kartēšana ir veidota, lai veiktu šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="972bc-163">This ER format is designed to do the following:</span></span>

  - <span data-ttu-id="972bc-164">Izveidot nodokļu paziņojumu xml formātā.</span><span class="sxs-lookup"><span data-stu-id="972bc-164">Generate a tax statement in XML format.</span></span>
  - <span data-ttu-id="972bc-165">Parādīt sekojošos nodokļu līmeņus nodokļu pārskatā: parasts, samazināts un nav.</span><span class="sxs-lookup"><span data-stu-id="972bc-165">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
  - <span data-ttu-id="972bc-166">Parādīt vairākas detaļas katrā nodokļu līmenī, kam katrā līmenī ir dažāds šo detaļu skaits. </span><span class="sxs-lookup"><span data-stu-id="972bc-166">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

  ![Formāta veidotāja lapa](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="972bc-168">Atlasīt **Kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="972bc-168">Select **Mapping**.</span></span>
5. <span data-ttu-id="972bc-169">Izvērst **modeli**, **datus** un **kopsavilkuma** elementus.</span><span class="sxs-lookup"><span data-stu-id="972bc-169">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

   <span data-ttu-id="972bc-170">Aprēķinātā lauka **Model.Data.Summary.Level** ir izteiksme, kas atgriež nodokļu līmeņa kodu (**Parasts**, **Samazināts**, **Nav** vai **cits**) kā teksta vērtība jebkuram nodokļa kodam, ko var izgūt no **Model.Data.Summary** datu avota izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="972bc-170">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

  ![Formāta veidotāja lapa, kas uzrāda Dara model modeļa detaļas, lai apgūtu parametru izsaukumus.](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="972bc-172">Izvērsiet **Modeli**. **Data2** krājums.</span><span class="sxs-lookup"><span data-stu-id="972bc-172">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="972bc-173">Izvērsiet **Modeli**. **Data2.Summary2** krājums.</span><span class="sxs-lookup"><span data-stu-id="972bc-173">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
   <span data-ttu-id="972bc-174">**Modeļa**. **Data2. Summary2** datu avots ir konfigurēts, lai grupētu \*\*Model.Data.Summary \*\* kopsavilkuma datu avota transakcijas detalizētu informāciju pēc taksācijas līmeņa (atgriezis **Model.Data.Summary.Level** aprēķinātais lauks) un aprēķinātu apkopojumus.</span><span class="sxs-lookup"><span data-stu-id="972bc-174">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

  ![Formāta veidotāja lapa, kas rāda detalizētu informāciju par Model.Data2.Summary2 datu avotu.](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="972bc-176">Pārskatīt aprēķināto lauku **Modelis**. **Data2.Level1**, **Modelis**. **Data2.Level2**un **Modelis**. **Data2. Level3.**</span><span class="sxs-lookup"><span data-stu-id="972bc-176">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="972bc-177">Šie aprēķinātie lauki tiek izmantoti **Modeļa** filtrēšanai. **Data2.Summary2** ieraksti saraksts un atgriezt tikai tos ierakstus, kas atbilst noteiktam nodokļu līmenim.</span><span class="sxs-lookup"><span data-stu-id="972bc-177">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="972bc-178">Aizveriet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="972bc-178">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="972bc-179">Atvasināta formāta izveide</span><span class="sxs-lookup"><span data-stu-id="972bc-179">Create a derived format</span></span>
<span data-ttu-id="972bc-180">Varat uzlabot norādīto formātu, pievienojot vienu aprēķināto lauku, lai filtrētu nepieciešamo nodokļu līmeni, nevis izmantotu esošos trīs laukus: **Modelis**.**Data2.Level1**, **Modelis**. **Data2.Level2** un **Modelis**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="972bc-180">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="972bc-181">Nepieciešamo nodokļu līmeni var norādīt vietā, kur tiks izsaukts šis jaunais aprēķinātais lauks.</span><span class="sxs-lookup"><span data-stu-id="972bc-181">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="972bc-182">Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.</span><span class="sxs-lookup"><span data-stu-id="972bc-182">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="972bc-183">Atlasiet **Formatēt, lai uzzinātu parametru izsaukumus**.</span><span class="sxs-lookup"><span data-stu-id="972bc-183">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="972bc-184">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="972bc-184">Select **Create configuration**.</span></span>
4. <span data-ttu-id="972bc-185">Atlasiet **Atvasināt no nosaukuma: formatēt, lai uzzinātu parametru izsaukumus, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="972bc-185">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="972bc-186">Laukā **Nosaukums** ievadiet **Formāts parametru izsaukumu (klentu) apgūšanai**.</span><span class="sxs-lookup"><span data-stu-id="972bc-186">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="972bc-187">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="972bc-187">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="972bc-188">Konfigurēt parametru aprēķināto lauku, kas atgriež ierakstu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="972bc-188">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="972bc-189">Sākt pievienot jaunu aprēķināto lauku</span><span class="sxs-lookup"><span data-stu-id="972bc-189">Start adding a new calculated field</span></span>

1. <span data-ttu-id="972bc-190">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="972bc-190">Select **Designer**.</span></span>
2. <span data-ttu-id="972bc-191">Atlasiet **Izvērst/sakļaut**, lai izvērstu visus formāta vienumus.</span><span class="sxs-lookup"><span data-stu-id="972bc-191">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="972bc-192">Atlasīt **Kartēšana**.</span><span class="sxs-lookup"><span data-stu-id="972bc-192">Select **Mapping**.</span></span>
4. <span data-ttu-id="972bc-193">Izvērst **Modelis** vienumu.</span><span class="sxs-lookup"><span data-stu-id="972bc-193">Expand the **Model** item.</span></span>
5. <span data-ttu-id="972bc-194">Atlasīt **Model.Data2** vienumu.</span><span class="sxs-lookup"><span data-stu-id="972bc-194">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="972bc-195">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="972bc-195">Select **Add**.</span></span>
7. <span data-ttu-id="972bc-196">Atlasīt **Funkcijas\\Aprēķinātais lauks**.</span><span class="sxs-lookup"><span data-stu-id="972bc-196">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="972bc-197">Laukā **Nosaukums** ievadiet **Līmeņi**.</span><span class="sxs-lookup"><span data-stu-id="972bc-197">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="972bc-198">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="972bc-198">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="972bc-199">Definēt aprēķinātā lauka pievienošanas parametru</span><span class="sxs-lookup"><span data-stu-id="972bc-199">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="972bc-200">Atlasiet **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="972bc-200">Select **Parameters**.</span></span>
2. <span data-ttu-id="972bc-201">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="972bc-201">Select **New**.</span></span>
3. <span data-ttu-id="972bc-202">Laukā **Nosaukums** ievadiet **Nodokļu līmenis**.</span><span class="sxs-lookup"><span data-stu-id="972bc-202">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="972bc-203">Laukā **Tips** atlasiet **Virkne**.</span><span class="sxs-lookup"><span data-stu-id="972bc-203">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="972bc-204">Lai norādītu parametra argumenta tipu, var izmantot tikai primitīvos datu tipus.</span><span class="sxs-lookup"><span data-stu-id="972bc-204">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="972bc-205">Tāpēc **Ierakstu saraksts**, **Ieraksts**un **Uzskaitījums** tipus šim nolūkam nevar izmantot.</span><span class="sxs-lookup"><span data-stu-id="972bc-205">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="972bc-206">Maksimālais parametru skaits, ko var norādīt vienam aprēķinātajam laukam, ir 8.</span><span class="sxs-lookup"><span data-stu-id="972bc-206">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Parametru datu avota saraksts](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="972bc-208">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="972bc-208">Select **OK**.</span></span>

<span data-ttu-id="972bc-209">Pievienojot šo parametru, jūs norādiet nosacījumu, kam jābūt, lai izsauktu šo aprēķināto lauku.</span><span class="sxs-lookup"><span data-stu-id="972bc-209">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="972bc-210">Kad izsaucat šo aprēķināto lauku, ir jānorāda **Nodokļu līmeņa** parametra arguments kā vērtība ar **Virknes** formātu.</span><span class="sxs-lookup"><span data-stu-id="972bc-210">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="972bc-211">Pārliecinieties, vai nosakāt parametrus tikai tiem aprēķinātajiem laukiem, kas atrodas konteinerā (vai nu **Ierakstu sarakstā**, **Ierakstā** vai **Konteinerā**).</span><span class="sxs-lookup"><span data-stu-id="972bc-211">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="972bc-212">Konfigurētais parametrs ir pieejams datu avotu sarakstā šim aprēķinātajam laukam.</span><span class="sxs-lookup"><span data-stu-id="972bc-212">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="972bc-213">Varat pievienot parametru konfigurētajai izteiksmei, atlasot **Pievienot datu avotu**.</span><span class="sxs-lookup"><span data-stu-id="972bc-213">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Datu avota lauki](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="972bc-215">Definēt aprēķinātā lauka pievienošanas izteiksmi</span><span class="sxs-lookup"><span data-stu-id="972bc-215">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="972bc-216">Laukā **Fomula** ievadiet:</span><span class="sxs-lookup"><span data-stu-id="972bc-216">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="972bc-217">**KUR (\@. Summary2, \@. Summary2. grupēts. līmenis =**</span><span class="sxs-lookup"><span data-stu-id="972bc-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="972bc-218">Atlasiet **Nodokļu līmeņa** parametru datu avotu sarakstā.</span><span class="sxs-lookup"><span data-stu-id="972bc-218">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="972bc-219">Atlasiet **Pievienot datu avotu**.</span><span class="sxs-lookup"><span data-stu-id="972bc-219">Select **Add data source**.</span></span>
4. <span data-ttu-id="972bc-220">Laukā **Formula** pabeidziet izteiksmi ar:</span><span class="sxs-lookup"><span data-stu-id="972bc-220">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="972bc-221">**KUR(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="972bc-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="972bc-222">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="972bc-222">Select **Save**.</span></span>

    ![Datu avota lauka informācija](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="972bc-224">Aizveriet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="972bc-224">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="972bc-225">Pabeigt pievienot jaunu aprēķināto lauku</span><span class="sxs-lookup"><span data-stu-id="972bc-225">Finish adding a new calculated field</span></span>

- <span data-ttu-id="972bc-226">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="972bc-226">Select **OK**.</span></span>

<span data-ttu-id="972bc-227">Lapā **Formāta veidotājs**  konfigurētajam parametru aprēķinātajam laukam **Līmeņi** nepieciešams **Virknes** arguments.</span><span class="sxs-lookup"><span data-stu-id="972bc-227">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Izvērsts aprēķināto lauku līmeņu saraksts](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="972bc-229">Izmantojiet konfigurēto aprēķināto lauku saistījuma formāta elementiem</span><span class="sxs-lookup"><span data-stu-id="972bc-229">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="972bc-230">Atlasiet **Model.Data2.Levels**, lai atlasītu konfigurēto aprēķināto lauku.</span><span class="sxs-lookup"><span data-stu-id="972bc-230">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="972bc-231">Atlasiet **Statement.Taxation.Regular** formāta elementu.</span><span class="sxs-lookup"><span data-stu-id="972bc-231">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="972bc-232">Atlasiet **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="972bc-232">Select **Bind**.</span></span>
4. <span data-ttu-id="972bc-233">Atlasiet **Jā**, lai apstiprinātu pašlaik izmantotā datu avota  **Level1** aizstāšanu ar jauno avotu **Līmeņi** visos atlasītā formāta elementa ligzdotu formātu elementos. </span><span class="sxs-lookup"><span data-stu-id="972bc-233">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="972bc-234">Piemērotais saistījums ir izveidots kā izsaukums aprēķinātajam parametru laukam.</span><span class="sxs-lookup"><span data-stu-id="972bc-234">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="972bc-235">Pēc noklusējuma saistītā formāta elementa nosaukums tiek izmantots kā arguments parametru aprēķinātajam laukam šādos apstākļos:</span><span class="sxs-lookup"><span data-stu-id="972bc-235">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="972bc-236">Aprēķinātais lauks ir konfigurēts, lai izmantotu vienu parametru.</span><span class="sxs-lookup"><span data-stu-id="972bc-236">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="972bc-237">Šī parametra datu tips ir definēts kā **Virkne.**</span><span class="sxs-lookup"><span data-stu-id="972bc-237">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="972bc-238">Ja saistītā formāta elementa nosaukums ir tukšs, lietotajā saistījumā tiek izmantots šī elementa datu avota nosaukums.</span><span class="sxs-lookup"><span data-stu-id="972bc-238">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="972bc-239">Atlasiet **Statement.Taxation.Reduced** formāta elementu.</span><span class="sxs-lookup"><span data-stu-id="972bc-239">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="972bc-240">Atlasiet **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="972bc-240">Select **Bind**.</span></span>
7. <span data-ttu-id="972bc-241">Atlasiet **Jā**, lai apstiprinātu pašlaik izmantotā datu avota  **Level2** aizstāšanu ar jauno avotu **Līmeņi** visos ligzdotu formātu elementos zem atlasītā formāta elementa.</span><span class="sxs-lookup"><span data-stu-id="972bc-241">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="972bc-242">Atlasiet **Statement.Taxation.None** formāta elementu.</span><span class="sxs-lookup"><span data-stu-id="972bc-242">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="972bc-243">Atlasiet **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="972bc-243">Select **Bind**.</span></span>
10. <span data-ttu-id="972bc-244">Atlasiet **Jā**, lai apstiprinātu pašlaik izmantotā datu avota  **Level3** aizstāšanu ar jauno avotu **Līmeņi** visos ligzdotu formātu elementos zem atlasītā formāta elementa.</span><span class="sxs-lookup"><span data-stu-id="972bc-244">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="972bc-245">Norādot aprēķinātā lauka parametru argumentu XML elementam, kas apzīmē nodokļu līmeni (piemēram, **Model.Data2.Levels("Reduced")** kā teksta vērtība), jums nav jādara tas pats ligzdotajiem XML atribūtiem — to saistījumi automātiski mantos argumenta vērtību, kas definēta pamatlīmenī (**Model.Data2.Levels.aggregated.Base**, nevis **Model.Data2.Levels("Reduced").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="972bc-245">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="972bc-246">Jebkura parametra aprēķinātā lauka atkārtotie izsaukumi netiek atbalstīti.</span><span class="sxs-lookup"><span data-stu-id="972bc-246">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="972bc-247">Varat atlasīt **Rediģēt formulu**un mainīt noklusējuma argumenta aprēķināto parametru, kas lietots atlasītajā saistījumā.</span><span class="sxs-lookup"><span data-stu-id="972bc-247">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="972bc-248">Ja šī argumenta nav, tas var radīt kļūdas izpildes laikā — lietotāji tiek informēti par šādu situāciju, kad pašreizējais formāts ir apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="972bc-248">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Apstiprinājuma brīdinājuma paziņojums](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="972bc-250">Konfigurēt parametru aprēķināto lauku, lai atgrieztu ierakstu.</span><span class="sxs-lookup"><span data-stu-id="972bc-250">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="972bc-251">Kad aprēķinātais parametru lauks atgriež ierakstu, jums ir jāatbalsta atsevišķu šī ieraksta lauku saistījums, lai formatētu elementus.</span><span class="sxs-lookup"><span data-stu-id="972bc-251">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="972bc-252">Šādos gadījumos nebūs pamata saistījuma, kas ietver argumenta vērtību, lai izsauktu aprēķināto parametru lauku — šī vērtība ir jādefinē viena ieraksta lauka saistījumā.</span><span class="sxs-lookup"><span data-stu-id="972bc-252">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="972bc-253">Sākt pievienot jaunu aprēķināto lauku</span><span class="sxs-lookup"><span data-stu-id="972bc-253">Start adding a new calculated field</span></span>

1. <span data-ttu-id="972bc-254">Atlasīt **Model.Data2** vienumu.</span><span class="sxs-lookup"><span data-stu-id="972bc-254">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="972bc-255">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="972bc-255">Select **Add**.</span></span>
3. <span data-ttu-id="972bc-256">Atlasīt **Funkcijas\\Aprēķinātais lauks**.</span><span class="sxs-lookup"><span data-stu-id="972bc-256">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="972bc-257">Laukā **Nosaukums** ievadiet **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="972bc-257">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="972bc-258">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="972bc-258">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="972bc-259">Definēt aprēķinātā lauka pievienošanas parametru</span><span class="sxs-lookup"><span data-stu-id="972bc-259">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="972bc-260">Atlasiet **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="972bc-260">Select **Parameters**.</span></span>
2. <span data-ttu-id="972bc-261">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="972bc-261">Select **New**.</span></span>
3. <span data-ttu-id="972bc-262">Laukā **Nosaukums** ievadiet **Nodokļu līmenis**.</span><span class="sxs-lookup"><span data-stu-id="972bc-262">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="972bc-263">Laukā **Tips** atlasiet **Virkne**.</span><span class="sxs-lookup"><span data-stu-id="972bc-263">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="972bc-264">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="972bc-264">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="972bc-265">Definēt aprēķinātā lauka pievienošanas izteiksmi</span><span class="sxs-lookup"><span data-stu-id="972bc-265">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="972bc-266">Laukā **Formula** ievadiet šādu izteiksmi:</span><span class="sxs-lookup"><span data-stu-id="972bc-266">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="972bc-267">**FIRSTORNULL (\@.Līmeņi(**</span><span class="sxs-lookup"><span data-stu-id="972bc-267">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="972bc-268">Atlasiet **Nodokļu līmenis** parametru.</span><span class="sxs-lookup"><span data-stu-id="972bc-268">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="972bc-269">Atlasiet **Pievienot datu avotu**.</span><span class="sxs-lookup"><span data-stu-id="972bc-269">Select **Add data source**.</span></span>
4. <span data-ttu-id="972bc-270">Laukā **Formula** pievienojiet **'Nodokļu līmenis'))**, ko ievadījāt 1. solī, lai pabeigtu izteiksmi:</span><span class="sxs-lookup"><span data-stu-id="972bc-270">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="972bc-271">**FIRSTORNULL (\@.Līmenis('Nodokļu līmenis'))**</span><span class="sxs-lookup"><span data-stu-id="972bc-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="972bc-272">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="972bc-272">Select **Save**.</span></span>
6. <span data-ttu-id="972bc-273">Aizveriet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="972bc-273">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="972bc-274">Pabeigt pievienot jaunu aprēķināto lauku</span><span class="sxs-lookup"><span data-stu-id="972bc-274">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="972bc-275">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="972bc-275">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="972bc-276">Izmantojiet konfigurēto aprēķināto lauku, lai saistītu formāta elementus.</span><span class="sxs-lookup"><span data-stu-id="972bc-276">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="972bc-277">Izvērsiet **Model.Data2.LevelRecord**, lai atlasītu konfigurēto aprēķināto lauku.</span><span class="sxs-lookup"><span data-stu-id="972bc-277">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="972bc-278">Izvērsiet **Model.Data2.LevelRecord.aggregated** konfigurēto aprēķinātā lauka konteineru.</span><span class="sxs-lookup"><span data-stu-id="972bc-278">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="972bc-279">Atlasiet **Model.Data2.LevelRecord.aggregated.Base** lauku.</span><span class="sxs-lookup"><span data-stu-id="972bc-279">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="972bc-280">Atlasiet **Statement.Taxation.None** formāta elementu.</span><span class="sxs-lookup"><span data-stu-id="972bc-280">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="972bc-281">Atlasiet **Atsaistīt**.</span><span class="sxs-lookup"><span data-stu-id="972bc-281">Select **Unbind**.</span></span>
6. <span data-ttu-id="972bc-282">Atlasiet **Statement.Taxation.None.Base** formāta elementu.</span><span class="sxs-lookup"><span data-stu-id="972bc-282">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="972bc-283">Atlasiet **Saistīt**.</span><span class="sxs-lookup"><span data-stu-id="972bc-283">Select **Bind**.</span></span>
8. <span data-ttu-id="972bc-284">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="972bc-284">Select **Edit formula**.</span></span>
9. <span data-ttu-id="972bc-285">Mainiet izteiksmi uz **Model.Data2.LevelRecord("None").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="972bc-285">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Atjauninātā izteiksme](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="972bc-287">Noņemt aprēķinātos laukus, kas netiek lietoti</span><span class="sxs-lookup"><span data-stu-id="972bc-287">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="972bc-288">Atlasiet **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="972bc-288">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="972bc-289">Atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="972bc-289">Select **Delete**.</span></span>
3. <span data-ttu-id="972bc-290">Atlasiet **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="972bc-290">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="972bc-291">Atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="972bc-291">Select **Delete**.</span></span>
5. <span data-ttu-id="972bc-292">Atlasiet **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="972bc-292">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="972bc-293">Atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="972bc-293">Select **Delete**.</span></span>
7. <span data-ttu-id="972bc-294">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="972bc-294">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="972bc-295">Jūs atkārtoti izmantojāt to pašu aprēķināto lauku **Model.Data2.Levels** formāta saistījumos.</span><span class="sxs-lookup"><span data-stu-id="972bc-295">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="972bc-296">Ir daudz vieglāk lietot un uzturēt vienu aprēķināto lauku, nekā darīt to pašu vairākiem līdzīgiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="972bc-296">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="972bc-297">Aizveriet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="972bc-297">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="972bc-298">Pabeigta atvasinātā formāta pielāgota versija</span><span class="sxs-lookup"><span data-stu-id="972bc-298">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="972bc-299">Kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="972bc-299">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="972bc-300">Atlasiet **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="972bc-300">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="972bc-301">Eksportēt atvasinātā formāta pabeigtu versiju.</span><span class="sxs-lookup"><span data-stu-id="972bc-301">Export completed version of a derived format</span></span>

1. <span data-ttu-id="972bc-302">Atlasiet **Formatēt, lai uzzinātu parametru izsaukumu (pielāgots)**  formātu konfigurācijas kokā.</span><span class="sxs-lookup"><span data-stu-id="972bc-302">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="972bc-303">Kopsavilkuma cilnē **Versijas**  atlasiet pabeigto versiju 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="972bc-303">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="972bc-304">Atlasiet **Maiņa**.</span><span class="sxs-lookup"><span data-stu-id="972bc-304">Select **Exchange**.</span></span>
4. <span data-ttu-id="972bc-305">Atlasiet **Eksportēt kā XML failu**.</span><span class="sxs-lookup"><span data-stu-id="972bc-305">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="972bc-306">Saglabājiet lejupielādēto konfigurāciju lokāli XML formātā.</span><span class="sxs-lookup"><span data-stu-id="972bc-306">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="972bc-307">Testa ER formāti</span><span class="sxs-lookup"><span data-stu-id="972bc-307">Test ER formats</span></span> 
<span data-ttu-id="972bc-308">Jūs varat palaist sākotnējos un uzlabotos ER formātus, lai pārliecinātos, ka konfigurētie parametru aprēķinātie lauki darbojas pareizi.</span><span class="sxs-lookup"><span data-stu-id="972bc-308">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="972bc-309">ER konfigurāciju importēšana</span><span class="sxs-lookup"><span data-stu-id="972bc-309">Import ER configurations</span></span>
<span data-ttu-id="972bc-310">Jūs varat importēt pārskatītās konfigurācijas no RCS, izmantojot **RCS** tipa ER repozitoriju.</span><span class="sxs-lookup"><span data-stu-id="972bc-310">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="972bc-311">Ja esat jau izgājis darbības tēmā, [Importēt elektroniskās pārskatu konfigurācijas no Regulatory Configuration Services](rcs-download-configurations.md), izmantojiet konfigurēto ER repozitoriju, lai importētu konfigurācijas, kas iepriekš šajā tēmā jau apspriestas.</span><span class="sxs-lookup"><span data-stu-id="972bc-311">If you already went through the steps in the topic, [Import Electronic reporting configurations from Regulatory Configuration Services](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="972bc-312">Pretējā gadījumā rīkojieties sekojoši:</span><span class="sxs-lookup"><span data-stu-id="972bc-312">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="972bc-313">Atlasiet **DEMF** uzņēmumu un noklusējuma informācijas panelī atlasiet **Elektroniskais pārskats**.</span><span class="sxs-lookup"><span data-stu-id="972bc-313">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="972bc-314">Atlasiet **Pārskatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="972bc-314">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="972bc-315">Importējiet konfigurācijas no Microsoft Download Center šādā secībā: datu modelis, modeļa kartēšana, formāts.</span><span class="sxs-lookup"><span data-stu-id="972bc-315">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="972bc-316">Veiciet šādas darbības katrai ER konfigurācijai:</span><span class="sxs-lookup"><span data-stu-id="972bc-316">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="972bc-317">Atlasiet **Mainīt**.</span><span class="sxs-lookup"><span data-stu-id="972bc-317">Select **Exchange.**</span></span>
    2. <span data-ttu-id="972bc-318">Atlasiet **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="972bc-318">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="972bc-319">Atlasiet **Pārlūkot**, lai atlasītu nepieciešamo ER konfigurāciju XML formātā.</span><span class="sxs-lookup"><span data-stu-id="972bc-319">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="972bc-320">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="972bc-320">Select **OK**.</span></span>

4. <span data-ttu-id="972bc-321">Importēt eksportētā **Formatēt, lai uzzinātu parametru izsaukumus (pielāgots)** formāta no RCS pabeigtās 1.1.1. versijas:</span><span class="sxs-lookup"><span data-stu-id="972bc-321">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="972bc-322">Atlasiet **Mainīt**.</span><span class="sxs-lookup"><span data-stu-id="972bc-322">Select **Exchange.**</span></span>
    2. <span data-ttu-id="972bc-323">Atlasiet **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="972bc-323">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="972bc-324">Atlasiet **Pārlūkot**, lai atlasītu lokāli saglabāto failu **Formatēt, lai uzzinātu parametru izsaukumus (pielāgots)**  XML formātā.</span><span class="sxs-lookup"><span data-stu-id="972bc-324">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="972bc-325">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="972bc-325">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="972bc-326">Palaidiet ER formātus</span><span class="sxs-lookup"><span data-stu-id="972bc-326">Run ER formats</span></span>

1. <span data-ttu-id="972bc-327">Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.</span><span class="sxs-lookup"><span data-stu-id="972bc-327">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="972bc-328">Atlasiet **Formatēt, lai uzzinātu parametru izsaukumus**.</span><span class="sxs-lookup"><span data-stu-id="972bc-328">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="972bc-329">Atlasiet **Palaist** visaugstākajā lentē.</span><span class="sxs-lookup"><span data-stu-id="972bc-329">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="972bc-330">Saglabāt lokāli ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="972bc-330">Save the locally generated output.</span></span>
5. <span data-ttu-id="972bc-331">Atlasiet vienumu **Formatēt, lai uzzinātu parametru izsaukumus (pielāgots)**.</span><span class="sxs-lookup"><span data-stu-id="972bc-331">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="972bc-332">Atlasiet **Palaist** visaugstākajā lentē.</span><span class="sxs-lookup"><span data-stu-id="972bc-332">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="972bc-333">Saglabāt lokāli ģenerēto izvadi.</span><span class="sxs-lookup"><span data-stu-id="972bc-333">Save the generated output locally.</span></span> 
8. <span data-ttu-id="972bc-334">Salīdziniet ģenerēto rezultātu saturu.</span><span class="sxs-lookup"><span data-stu-id="972bc-334">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="972bc-335">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="972bc-335">Additional resources</span></span>
[<span data-ttu-id="972bc-336">Formulu veidotājs elektronisko atskaišu veidošanā</span><span class="sxs-lookup"><span data-stu-id="972bc-336">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
