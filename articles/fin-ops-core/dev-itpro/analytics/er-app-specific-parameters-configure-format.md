---
title: ER formātu konfigurēšana, lai izmantotu parametrus, kas ir norādīti par juridisko personu
description: Šajā tēmā izskaidrots, kā konfigurēt elektronisko pārskatu (ER) formātus, lai varētu izmantot parametrus, kas ir norādīti par juridisko personu.
author: NickSelin
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 0ed1442403ae82dfc820212e3e235737f37f21a4
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679730"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="e06a3-103">ER formātu konfigurēšana, lai izmantotu parametrus, kas ir norādīti par juridisko personu</span><span class="sxs-lookup"><span data-stu-id="e06a3-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="e06a3-104">Pārskats</span><span class="sxs-lookup"><span data-stu-id="e06a3-104">Overview</span></span>

<span data-ttu-id="e06a3-105">Daudzos no elektronisko pārskatu (ER) formātiem, kurus izstrādāsit, ir jāfiltrē dati, izmantojot vērtību kopu, kas ir specifiska katrai jūsu instances juridiskajai personai (piemēram, nodokļu kodu kopa nodokļu darbību filtrēšanai).</span><span class="sxs-lookup"><span data-stu-id="e06a3-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="e06a3-106">Pašlaik, kad šī veida filtrēšana ir konfigurēta ER formātā, vērtības, kas ir atkarīgas no juridiskās personas (piemēram, nodokļu kodi), tiek izmantotas ER formāta izteiksmē, lai norādītu datu filtrēšanas nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="e06a3-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="e06a3-107">Tāpēc ER formāts ir padarīts juridiskai personai specifisks, un lai ģenerētu pieprasītos pārskatus, jums ir jāizveido iegūtas kopijas no sākotnējā ER formāta katrai juridiskajai personai, kurai jums ir jāpalaiž ER formāts.</span><span class="sxs-lookup"><span data-stu-id="e06a3-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="e06a3-108">Katrs atvasinātais ER formāts ir jārediģē, lai tajā ieviestu juridiskajai personai specifiskās vērtības, pārbaudot, kad sākotnējā (bāzes) versija ir atjaunināta, eksportēta no testa vides un importēta ražošanas vidē, kad tā ir jāizvieto izmantošanai ražošanā un tā tālāk.</span><span class="sxs-lookup"><span data-stu-id="e06a3-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="e06a3-109">Tāpēc šāda veida konfigurētā ER risinājuma uzturēšana ir samērā sarežģīta un laikietilpīga vairāku iemeslu dēļ:</span><span class="sxs-lookup"><span data-stu-id="e06a3-109">Therefore, maintenance of this type of configured ER solution is quite complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="e06a3-110">Jo vairāk ir juridisko personu, jo ir jāsaglabā vairāk ER formāta konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="e06a3-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="e06a3-111">ER konfigurāciju uzturēšana prasa, lai uzņēmuma lietotājiem būtu ER zināšanas.</span><span class="sxs-lookup"><span data-stu-id="e06a3-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="e06a3-112">ER programmai raksturīgo parametru līdzeklis ļauj pilnvarot lietotājus konfigurēt datu filtrēšanu ER formātā, lai tā būtu balstīta uz abstraktu noteikumu kopu.</span><span class="sxs-lookup"><span data-stu-id="e06a3-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="e06a3-113">Šo noteikumu kopu var konfigurēt, lai izmantotu informācijas avotus, kas ir pieejami ER formātā.</span><span class="sxs-lookup"><span data-stu-id="e06a3-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="e06a3-114">Pēc tam uzņēmuma lietotāji var noteikt reālos noteikumus ārpus ER struktūras, izmantojot lietotāja interfeisu (UI), kas tiek ģenerēts automātiski, pamatojoties uz atbilstošā ER formāta iestatījumiem un pašreizējo juridisko personu datiem, kuriem varēs piekļūt ER formāta datu avoti.</span><span class="sxs-lookup"><span data-stu-id="e06a3-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="e06a3-115">Noteikumu kopa, kas noteikta ER formātam, var tikt eksportēta no pašreizējās Dynamics 365 Finance (finanšu) instances juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="e06a3-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="e06a3-116">Pēc tam to var importēt citā juridiskajā personā ar to pašu finanšu instanci vai citu instanci kā noteikumu kopumu vienam un tam pašam ER formātam.</span><span class="sxs-lookup"><span data-stu-id="e06a3-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e06a3-117">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="e06a3-117">Prerequisites</span></span>

<span data-ttu-id="e06a3-118">Lai pabeigtu piemēru šajā tēmā, jums jābūt piekļuvei Regulatory Configuration Services (RCS) instancei, kas ir nodrošināta tam pašam nomniekam, kuram nodrošināta Finance and Operations instance, vienai no šādām lomām:</span><span class="sxs-lookup"><span data-stu-id="e06a3-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="e06a3-119">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="e06a3-119">Electronic reporting developer</span></span>
- <span data-ttu-id="e06a3-120">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="e06a3-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="e06a3-121">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="e06a3-121">System administrator</span></span>

<span data-ttu-id="e06a3-122">Ieteicams veikt darbības, kas aprakstītas tēmā [Atbalstīt parametru izsaukumus no APRĒĶINĀTĀ LAUKA veida ER datu avotiem](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="e06a3-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="e06a3-123">Ja esat jau paveikuši šīs darbības, varat izlaist darbības, kas norādītas nākamajā sadaļā **ER konfigurāciju importēšana RCS**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="e06a3-124">ER konfigurāciju importēšana RCS</span><span class="sxs-lookup"><span data-stu-id="e06a3-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="e06a3-125">No [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=851448) lejupielādējiet saspiesto (zip) failu **Atbalstīt parametru izsaukumus no APRĒĶINĀTĀ LAUKA veida ER datu avotiem**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-125">From [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=851448), download the **Support parameterized calls of ER data sources of CALCULATED FIELD type** zip file.</span></span> <span data-ttu-id="e06a3-126">Šajā saspiestajā failā ir šādas ER konfigurācijas, kas ir jāizvelk un jāuzglabā lokāli.</span><span class="sxs-lookup"><span data-stu-id="e06a3-126">This zip file contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="e06a3-127">**Satura apraksts**</span><span class="sxs-lookup"><span data-stu-id="e06a3-127">**Content description**</span></span>                        | <span data-ttu-id="e06a3-128">**Faila nosaukums**</span><span class="sxs-lookup"><span data-stu-id="e06a3-128">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e06a3-129">Parauga **ER datu modeļa** konfigurācijas fails</span><span class="sxs-lookup"><span data-stu-id="e06a3-129">Sample **ER data model** configuration file</span></span>    | <span data-ttu-id="e06a3-130">Modelis, lai uzzinātu parametru izsaukumus.versija.1.xml</span><span class="sxs-lookup"><span data-stu-id="e06a3-130">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="e06a3-131">Parauga **ER metadatu** konfigurācijas fails</span><span class="sxs-lookup"><span data-stu-id="e06a3-131">Sample **ER metadata** configuration file</span></span>      | <span data-ttu-id="e06a3-132">Metadati, lai uzzinātu parametru izsaukumus.versija.1.xml</span><span class="sxs-lookup"><span data-stu-id="e06a3-132">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="e06a3-133">Parauga **ER modeļa kartējuma** konfigurācijas fails</span><span class="sxs-lookup"><span data-stu-id="e06a3-133">Sample **ER model mapping** configuration file</span></span> | <span data-ttu-id="e06a3-134">Kartēšana, lai uzzinātu parametru izsaukumus.versija.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="e06a3-134">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="e06a3-135">Parauga **ER formāta** konfigurācija</span><span class="sxs-lookup"><span data-stu-id="e06a3-135">Sample **ER format** configuration</span></span>             | <span data-ttu-id="e06a3-136">Formāts, lai uzzinātu parametru izsaukumus.versija.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="e06a3-136">Format to learn parameterized calls.version.1.1.xml</span></span>  |

<span data-ttu-id="e06a3-137">Pēc tam pierakstieties savā RCS instancē.</span><span class="sxs-lookup"><span data-stu-id="e06a3-137">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="e06a3-138">Šajā piemērā izveidosiet konfigurāciju Litware, Inc. parauga uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="e06a3-138">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="e06a3-139">Pirms varat izpildīt šo procedūru, jums jāizpilda darbības RCS tēmā [Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e06a3-139">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="e06a3-140">Noklusējuma informācijas panelī atlasiet **Elektroniskais pārskats**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-140">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="e06a3-141">Atlasiet **Pārskatu konfigurācijas**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-141">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="e06a3-142">Importējiet ER konfigurācijas, ko iepriekš esat lejupielādējis RCS, šādā secībā: datu modelis, metadati, modeļa kartēšana un formāts.</span><span class="sxs-lookup"><span data-stu-id="e06a3-142">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="e06a3-143">Katrai ER konfigurācijai rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="e06a3-143">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="e06a3-144">Atlasiet **Maiņa**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-144">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="e06a3-145">Atlasiet **Ielādēt no XML faila**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-145">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="e06a3-146">Atlasiet **Pārlūkot**, lai atlasītu failu nepieciešamajai ER konfigurācijai XML formātā.</span><span class="sxs-lookup"><span data-stu-id="e06a3-146">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="e06a3-147">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-147">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="e06a3-148">Pārskatiet sniegto ER risinājumu.</span><span class="sxs-lookup"><span data-stu-id="e06a3-148">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="e06a3-149">Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.</span><span class="sxs-lookup"><span data-stu-id="e06a3-149">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="e06a3-150">Atlasiet vienumu **Formatēt, lai uzzinātu parametru izsaukumus**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-150">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="e06a3-151">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-151">Select **Designer**.</span></span>
4.  <span data-ttu-id="e06a3-152">Atlasiet **Izvērst/Sakļaut**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-152">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="e06a3-153">ER formāts **Formāts, lai uzzinātu parametru izsaukumus** ir izveidots, lai ģenerētu nodokļu deklarāciju XML formātā, kas parāda vairākus nodokļu līmeņus (regulārs, samazināts un nav).</span><span class="sxs-lookup"><span data-stu-id="e06a3-153">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="e06a3-154">Katram līmenim ir atšķirīgs detaļu skaits.</span><span class="sxs-lookup"><span data-stu-id="e06a3-154">Each level has a different number of details.</span></span>

    ![ER operācijas veidotāja lapa](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="e06a3-156">Cilnē **Kartēšana** izvērsiet vienumus **Modelis**, **Dati** un **Kopsavilkums**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-156">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="e06a3-157">Datu avots **Modelis.Dati.Kopsavilkums** atgriež nodokļu transakciju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="e06a3-157">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="e06a3-158">Šīs transakcijas ir apkopotas pēc PVN koda.</span><span class="sxs-lookup"><span data-stu-id="e06a3-158">These transactions are summarized by tax code.</span></span> <span data-ttu-id="e06a3-159">Šim datu avotam **Modelis.Dati.Kopsavilkums.Līmenis** aprēķinātais lauks ir konfigurēts tā, lai atgrieztu katra apkopotā ieraksta taksācijas līmeņa kodu.</span><span class="sxs-lookup"><span data-stu-id="e06a3-159">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="e06a3-160">Jebkuram nodokļu kodam, kuru izpildlaikā var izgūt no datu avota **Modelis.Dati.Kopsavilkums**, aprēķinātais lauks atgriež nodokļu līmeņa kodu (**Parasts**, **Samazināts**, **Nav** vai **Cits**) kā teksta vērtību.</span><span class="sxs-lookup"><span data-stu-id="e06a3-160">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="e06a3-161">Aprēķinātais lauks **Modelis.Dati.Kopsavilkums.Līmenis** tiek izmantots, lai filtrētu datu avota **Modelis.Dati.Kopsavilkums** ierakstus un ievadītu filtrētos datus katrā XML elementā, kas apzīmē nodokļu līmeni, izmantojot laukus **Modelis.Dati2.Līmenis1**, **Modelis.Dati2.Līmenis2** un **Modelis.Dati2.Līmenis3**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-161">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![ER operācijas veidotāja lapa](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="e06a3-163">Aprēķinātais lauks **Modelis.Dati.Kopsavilkums.Līmenis** ir konfigurēts tā, lai tas ietvertu ER izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="e06a3-163">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="e06a3-164">Ņemiet vērā, ka nodokļu kodi (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** un **InVAT0**) šajā konfigurācijā ir stingri kodēti.</span><span class="sxs-lookup"><span data-stu-id="e06a3-164">Note that tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="e06a3-165">Tāpēc šis ER formāts ir atkarīgs no juridiskās personas, kur šie nodokļu kodi tika konfigurēti.</span><span class="sxs-lookup"><span data-stu-id="e06a3-165">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![ER operācijas veidotāja lapa](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="e06a3-167">Lai atbalstītu atšķirīgu nodokļu kodu kopu katrai juridiskajai personai, ir jāveic tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e06a3-167">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="e06a3-168">Izveidojiet atvasinātu ER formāta versiju katrai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="e06a3-168">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="e06a3-169">Atjauniniet nodokļu kodus aprēķinātajā laukā **Modelis.Dati.Kopsavilkums.Līmenis**, pamatojoties uz juridiskās personas iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="e06a3-169">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="e06a3-170">Aizveriet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-170">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="e06a3-171">Atvasināta formāta izveide</span><span class="sxs-lookup"><span data-stu-id="e06a3-171">Create a derived format</span></span>

<span data-ttu-id="e06a3-172">Pēc tam jūs izmantosit ER programmai raksturīgo parametru līdzekli, lai atbalstītu citu nodokļu kodu kopu katrai juridiskajai personai vienotā ER formātā.</span><span class="sxs-lookup"><span data-stu-id="e06a3-172">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="e06a3-173">Konfigurācijas kokā izvērsiet **Modelis, lai uzzinātu parametru izsaukumus** krājuma saturu.</span><span class="sxs-lookup"><span data-stu-id="e06a3-173">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="e06a3-174">Atlasiet vienumu **Formatēt, lai uzzinātu parametru izsaukumus**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-174">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="e06a3-175">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-175">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="e06a3-176">Atlasiet opciju **Atvasināt no nosaukuma: formatēt, lai uzzinātu parametru izsaukumus, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-176">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="e06a3-177">Laukā **Nosaukums** ievadiet **Formatēt, lai uzzinātu, kā uzmeklēt LE datus**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-177">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="e06a3-178">Atlasiet **Izveidot konfigurāciju**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-178">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="e06a3-179">Konfigurējiet atvasināto formātu</span><span class="sxs-lookup"><span data-stu-id="e06a3-179">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="e06a3-180">Pievienojiet formātu uzskaitījumu</span><span class="sxs-lookup"><span data-stu-id="e06a3-180">Add a format enumeration</span></span>

<span data-ttu-id="e06a3-181">Pēc tam jūs pievienosit jaunu ER formātu uzskaitījumu.</span><span class="sxs-lookup"><span data-stu-id="e06a3-181">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="e06a3-182">Šī formāta uzskaitījuma vērtības tiks rādītas uzņēmuma lietotājiem, kuri norādīs no juridiskās personas atkarīgās nodokļu kodu kopas dažādiem nodokļu līmeņiem, kas tiek izmantoti ER formātā.</span><span class="sxs-lookup"><span data-stu-id="e06a3-182">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="e06a3-183">Atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-183">Select **Designer**.</span></span>
2.  <span data-ttu-id="e06a3-184">Atlasiet **Formātu uzskaitījumi**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-184">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="e06a3-185">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-185">Select **Add**.</span></span>
4.  <span data-ttu-id="e06a3-186">Laukā **Nosaukums** ievadiet **Nodokļu līmeņu saraksts**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-186">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="e06a3-187">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-187">Select **Save**.</span></span>
6.  <span data-ttu-id="e06a3-188">Cilnē **Formātu uzskaitījuma vērtības** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-188">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="e06a3-189">Laukā **Nosaukums** ievadiet **Parasta nodokļu piemērošana**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-189">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="e06a3-190">Vēlreiz atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-190">Select **Add** again.</span></span>
9.  <span data-ttu-id="e06a3-191">Laukā **Nosaukums** ievadiet **Samazināta nodokļu piemērošana**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-191">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="e06a3-192">Vēlreiz atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-192">Select **Add** again.</span></span>
11. <span data-ttu-id="e06a3-193">Laukā **Nosaukums** ievadiet **Nav nodokļa**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-193">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="e06a3-194">Vēlreiz atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-194">Select **Add** again.</span></span>
13. <span data-ttu-id="e06a3-195">Laikā **Nosaukums** ievadiet **Cits**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-195">In the **Name** field, enter **Other**.</span></span>

    ![ER operācijas veidotāja lapa](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="e06a3-197">Tā kā uzņēmuma lietotāji var izmantot dažādas valodas, lai norādītu no juridiskās personas atkarīgās nodokļu kodu kopas, mēs iesakām pārtulkot šīs uzskaitījuma vērtības valodās, kas ir konfigurētas kā vēlamās valodas šiem lietotājiem programmā Finance.</span><span class="sxs-lookup"><span data-stu-id="e06a3-197">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="e06a3-198">Atlasiet ierakstu **Nav nodokļa**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-198">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="e06a3-199">Noklikšķiniet laukā **Etiķete**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-199">Click in the **Label** field.</span></span>
16. <span data-ttu-id="e06a3-200">Atlasiet **Tulkot**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-200">Select **Translate**.</span></span>
17. <span data-ttu-id="e06a3-201">Rūts **Teksta tulkošana** laukā **Etiķetes ID** ievadiet **LBL_LEVELENUM_NO**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-201">In the **Text translation** pane, in the **Label Id** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="e06a3-202">Laukā **Teksts noklusējuma valodā** ievadiet **Nav nodokļa**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-202">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="e06a3-203">Laukā **Valoda** atlasiet **DE**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-203">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="e06a3-204">Laukā **Tulkotais teksts** ievadiet **keine Besteuerung**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-204">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="e06a3-205">Atlasiet **Tulkot**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-205">Select **Translate**.</span></span>

    ![ER operācijas veidotāja lapa](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="e06a3-207">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-207">Select **Save**.</span></span>
23. <span data-ttu-id="e06a3-208">Aizveriet lapu **Formātu uzskaitījumi**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-208">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="e06a3-209">Pievienot jaunu uzmeklēšanas datu avotu</span><span class="sxs-lookup"><span data-stu-id="e06a3-209">Add a new lookup data source</span></span>

<span data-ttu-id="e06a3-210">Pēc tam jūs pievienosit jaunu datu avotu, lai norādītu, kā uzņēmuma lietotāji norādīs no juridiskās personas atkarīgos noteikumus, lai atpazītu pareizo nodokļu līmeni katram kopsavilkuma transakcijas ierakstam.</span><span class="sxs-lookup"><span data-stu-id="e06a3-210">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="e06a3-211">Cilnē **Kartēšana** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-211">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="e06a3-212">Atlasiet **Formātu uzskaitījumi\Uzmeklēšana**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-212">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="e06a3-213">Jūs nupat identificējāt, ka katram noteikumam, ko uzņēmuma lietotāji nosaka nodokļu līmeņa atpazīšanai, tiks atgriezta ER formāta uzskaitījuma vērtība.</span><span class="sxs-lookup"><span data-stu-id="e06a3-213">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="e06a3-214">Ievērojiet, ka datu avota veidam **Uzmeklēšana** var piekļūt zem bloka **Datu modelis** un **Dynamics 365 for Operations** papildus blokam **Formāta uzskaitījums**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-214">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="e06a3-215">Tādēļ ER datu modeļa uzskaitījumus un pieteikumu uzskaitījumus var izmantot, lai norādītu vērtību veidu, kas tiek atgriezts šā veida datu avotiem.</span><span class="sxs-lookup"><span data-stu-id="e06a3-215">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that is are returned for data sources of that type.</span></span>
    
3.  <span data-ttu-id="e06a3-216">Laukā **Nosaukums** ievadiet **Atlasītājs**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-216">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="e06a3-217">Laukā **Formātu uzskaitījums** atlasiet **Nodokļu līmeņu saraksts**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-217">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="e06a3-218">Jūs vienkārši norādījāt, ka katram šajā datu avotā norādītajam nosacījumam uzņēmuma lietotājam jāatlasa viena no **Nodokļu līmeņu saraksta** formāta uzskaitījuma vērtībām kā atgrieztā vērtība.</span><span class="sxs-lookup"><span data-stu-id="e06a3-218">You just specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="e06a3-219">Atlasiet **Rediģēt uzmeklēšanu**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-219">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="e06a3-220">Atlasiet **Kolonnas**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-220">Select **Columns**.</span></span>
7.  <span data-ttu-id="e06a3-221">Izvērst **Modelis** vienumu.</span><span class="sxs-lookup"><span data-stu-id="e06a3-221">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="e06a3-222">Izvērsiet vienumu **Dati**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-222">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="e06a3-223">Izvērsiet vienumu **Nodoklis**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-223">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="e06a3-224">Atlasiet vienumu **Modelis.Dati.Nodoklis.Kods**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-224">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="e06a3-225">Atlasiet pogu **Pievienot** (labā bultiņa).</span><span class="sxs-lookup"><span data-stu-id="e06a3-225">Select the **Add** button (the right arrow).</span></span>

    ![ER operācijas veidotāja lapa](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="e06a3-227">Jūs tikko norādījāt, ka katram šajā datu avotā norādītajam noteikumam nodokļa līmeņa atpazīšanai uzņēmuma lietotājam jāatlasa viens no nodokļa kodiem kā nosacījums.</span><span class="sxs-lookup"><span data-stu-id="e06a3-227">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="e06a3-228">To nodokļu kodu sarakstu, kurus var atlasīt uzņēmuma lietotājs, atgriezīs datu avots **Modelis.Dati.Nodoklis**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-228">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="e06a3-229">Tā kā šis datu avots ietver lauku **Nosaukums**, nodokļu koda nosaukums tiks parādīts katrai uzņēmuma lietotājam iesniegtajai nodokļa koda vērtībai.</span><span class="sxs-lookup"><span data-stu-id="e06a3-229">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="e06a3-230">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-230">Select **OK**.</span></span>

    ![ER operācijas veidotāja lapa](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="e06a3-232">Uzņēmuma lietotāji var pievienot vairākas kārtulas kā šī datu avota ierakstus.</span><span class="sxs-lookup"><span data-stu-id="e06a3-232">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="e06a3-233">Katrs ieraksts tiks numurēts, izmantojot rindas kodu.</span><span class="sxs-lookup"><span data-stu-id="e06a3-233">Each record will be numbered by a line code.</span></span> <span data-ttu-id="e06a3-234">Kārtulas tiks novērtētas, lai palielinātu rindu skaitu.</span><span class="sxs-lookup"><span data-stu-id="e06a3-234">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="e06a3-235">Tā kā jūs atlasījāt lauku **Nodokļa kods** kā nosacījumu šī uzmeklēšanas datu avota kārtulām, un tāpēc, ka **Nodokļa kods** ir iestatīts kā lauka **Virkne** datu veids, katra kārtula tiks novērtēta izpildlaikā, salīdzinot nodokļa kodu, kas tiek nodots datu avotam, ar nodokļu kodu, kas definēts šajā datu avota ierakstā.</span><span class="sxs-lookup"><span data-stu-id="e06a3-235">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="e06a3-236">Kad tiek atrasta kārtula, kas atbilst konfigurētajam nosacījumam, šis datu avots atgriež kārtulas uzmeklēšanas vērtību, kas definēta laukā **Uzmeklēšanas rezultāts**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-236">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="e06a3-237">Ja kārtula netiek atrasta, tiek izmests izņēmums, lai paziņotu lietotājam, ka pašreizējais datu avots nevar atgriezt pareizu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e06a3-237">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="e06a3-238">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-238">Select **Save**.</span></span>
14. <span data-ttu-id="e06a3-239">Aizveriet lapu **Uzmeklēšanas veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-239">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="e06a3-240">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-240">Select **OK**.</span></span>

    <span data-ttu-id="e06a3-241">Ņemiet vērā, ka jūs pievienojāt jaunu datu avotu, kas atgriezīs nodokļu līmeni kā formāta uzskaitījuma **Nodokļu līmeņu saraksts** vērtību jebkuram nodokļu kodam, kas tiek nodots datu avotam kā datu veida **Virkne** parametra **Kods** arguments.</span><span class="sxs-lookup"><span data-stu-id="e06a3-241">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![ER operācijas veidotāja lapa](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="e06a3-243">Ņemiet vērā, ka konfigurēto kārtulu novērtējums ir atkarīgs no to lauku datu veida, kas atlasīti, lai definētu šo kārtulu nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="e06a3-243">Note that the evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="e06a3-244">Kad tiek atlasīts lauks, kas ir konfigurēts kā datu veida **Skaitlisks** vai **Datums** lauks, kritēriji atšķirsies no tiem kritērijiem, kas iepriekš tika aprakstīti datu veidam **Virkne**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-244">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="e06a3-245">Laukiem **Skaitlisks** un **Datums** kārtulai jābūt norādītai kā vērtību diapazonam.</span><span class="sxs-lookup"><span data-stu-id="e06a3-245">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="e06a3-246">Pēc tam kārtulas nosacījums tiks uzskatīts par izpildītu, ja datu avotam nodotā vērtība būs konfigurētajā diapazonā.</span><span class="sxs-lookup"><span data-stu-id="e06a3-246">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="e06a3-247">Nākamajā attēlā ir parādīts šāda iestatījuma veida piemērs.</span><span class="sxs-lookup"><span data-stu-id="e06a3-247">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="e06a3-248">Papildus datu veida **Virkne** laukam **Modelis.Dati.Nodoklis.Kods** datu veida **Faktisks** lauks **Modelis.Nodoklis.Kopsavilkums.Bāze** tiek izmantots, lai norādītu nosacījumus datu avota uzmeklēšanai.</span><span class="sxs-lookup"><span data-stu-id="e06a3-248">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![ER operācijas veidotāja lapa](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="e06a3-250">Tā kā šim uzmeklēšanas datu avotam ir atlasīti lauki **Modelis.Dati.Nodoklis.Kods** un **Modelis.Nodoklis.Kopsavilkums.Bāze** katra šī datu avota kārtula tiks konfigurēta tālāk norādītajā veidā.</span><span class="sxs-lookup"><span data-stu-id="e06a3-250">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="e06a3-251">Piedāvātajā sarakstā formāta uzskaitījuma **Nodokļu līmeņu saraksts** vērtība ir jāatlasa kā atgrieztā vērtība.</span><span class="sxs-lookup"><span data-stu-id="e06a3-251">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="e06a3-252">Nodokļa kods jāievada kā šīs kārtulas nosacījums.</span><span class="sxs-lookup"><span data-stu-id="e06a3-252">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="e06a3-253">Piemērojami ir tikai tie nodokļu kodi, kurus sniedzis datu avots **Modelis.Dati.Nodoklis**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-253">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="e06a3-254">Minimālās un maksimālās nodokļu bāzes summas vērtības ir jāievada kā šīs kārtulas nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="e06a3-254">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="e06a3-255">Lūk, kā katra šī datu avota kārtula tiks novērtēta izpildlaikā:</span><span class="sxs-lookup"><span data-stu-id="e06a3-255">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="e06a3-256">Vai datu veida **Virkne** kods, kas tika nodots šim datu avotam, ir vienāds ar kārtulas nodokļu kodu?</span><span class="sxs-lookup"><span data-stu-id="e06a3-256">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="e06a3-257">Vai datu veida **Faktiskais** vērtība, kas tika nodota šim datu avotam, atbilst noteiktajām minimālajām un maksimālajām vērtībām?</span><span class="sxs-lookup"><span data-stu-id="e06a3-257">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="e06a3-258">Kārtula tiks uzskatīta par piemērojamu, ja abi nosacījumi būs izpildīti.</span><span class="sxs-lookup"><span data-stu-id="e06a3-258">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="e06a3-259">Tulkot pievienotā uzmeklēšanas datu avota etiķeti</span><span class="sxs-lookup"><span data-stu-id="e06a3-259">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="e06a3-260">Tā kā uzņēmuma lietotāji var izmantot dažādas valodas, lai norādītu no juridiskās personas atkarīgās nodokļu kodu kopas, mēs iesakām pārtulkot etiķeti katram uzmeklēšanas datu avotam, ko esat pievienojis, lai atbilstošajā lapā tā tiktu parādīta katra lietotāja vēlamajā valodā.</span><span class="sxs-lookup"><span data-stu-id="e06a3-260">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="e06a3-261">Atlasiet datu avotu **Modelis.Dati.Atlasītājs**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-261">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="e06a3-262">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-262">Select **Edit**.</span></span>
3.  <span data-ttu-id="e06a3-263">Noklikšķiniet laukā **Etiķete**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-263">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="e06a3-264">Atlasiet **Tulkot**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-264">Select **Translate**.</span></span>
5.  <span data-ttu-id="e06a3-265">Rūts **Teksta tulkošana** laukā **Etiķetes ID** ievadiet **LBL_SELECTOR_DS**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-265">In the **Text translation** pane, in the **Label Id** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="e06a3-266">Laukā **Teksts noklusētajā valodā** ievadiet **Atlasīt nodokļa līmeni pēc nodokļu koda**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-266">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="e06a3-267">Laukā **Valoda** atlasiet **DE**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-267">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="e06a3-268">Laukā **Tulkotais teksts** ievadiet **Steuerebene für Steuerkennzeichen auswählen**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-268">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="e06a3-269">Atlasiet **Tulkot**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-269">Select **Translate**.</span></span>
10. <span data-ttu-id="e06a3-270">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-270">Select **OK**.</span></span>

    ![ER operācijas veidotāja lapa](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="e06a3-272">Pievienojiet jaunu lauku, lai izmantotu konfigurēto uzmeklēšanu</span><span class="sxs-lookup"><span data-stu-id="e06a3-272">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="e06a3-273">Izvērsiet vienumu **Modelis.Dati**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-273">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="e06a3-274">Atlasiet vienumu **Modelis.Dati.Kopsavilkums**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-274">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="e06a3-275">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-275">Select **Add**.</span></span>
4.  <span data-ttu-id="e06a3-276">Atlasiet **Funkcijas/Aprēķinātais lauks**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-276">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="e06a3-277">Laukā **Nosaukums** ievadiet **LevelByLookup**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-277">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="e06a3-278">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-278">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="e06a3-279">Laukā **Formulas lauks** ievadiet **Modelis.Atlasītājs(Modelis.Dati.Kopsavilkums.Kods)**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-279">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="e06a3-280">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-280">Select **Save**.</span></span>

    ![ER operācijas veidotāja lapa](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="e06a3-282">Aizveriet lapu **Formulas redaktors**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-282">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="e06a3-283">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-283">Select **OK**.</span></span>

    ![ER operācijas veidotāja lapa](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="e06a3-285">Ņemiet vērā, ka aprēķinātais lauks **LevelByLookup**, kuru pievienojāt, atgriezīs nodokļa līmeni kā formāta uzskaitījuma **Nodokļu līmeņu saraksts** vērtību katram apkopotajam nodokļa transakciju ierakstam.</span><span class="sxs-lookup"><span data-stu-id="e06a3-285">Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id="e06a3-286">Ieraksta nodokļa kods tiks nodots uzmeklēšanas datu avotam **Modelis.Atlasītājs** un kārtulu kopums šim datu avotam tiks izmantots, lai atlasītu pareizo nodokļa piemērošanas līmeni.</span><span class="sxs-lookup"><span data-stu-id="e06a3-286">The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name="add-a-new-format-enumeration-based-data-source"></a><span data-ttu-id="e06a3-287">Pievienot jaunu uz formātu uzskaitījuma pamatotu datu avotu</span><span class="sxs-lookup"><span data-stu-id="e06a3-287">Add a new format enumeration-based data source</span></span>

<span data-ttu-id="e06a3-288">Pēc tam jūs pievienosit jaunu datu avotu, kas attiecas uz iepriekš pievienoto formāta uzskaitījumu.</span><span class="sxs-lookup"><span data-stu-id="e06a3-288">Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id="e06a3-289">Vēlāk šī datu avota vērtības tiks izmantotas ER formāta izteiksmē.</span><span class="sxs-lookup"><span data-stu-id="e06a3-289">Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id="e06a3-290">Atlasiet **Pievienot sakni**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-290">Select **Add root**.</span></span>
2.  <span data-ttu-id="e06a3-291">Atlasiet **Formātu uzskaitījumi\Uzskaitījums**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-291">Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id="e06a3-292">Laukā **Nosaukums** ievadiet **Nodokļu līmenis**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-292">In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id="e06a3-293">Laukā **Formātu uzskaitījums** atlasiet **Nodokļu līmeņu saraksts**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-293">In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id="e06a3-294">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-294">Select **Save**.</span></span>

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a><span data-ttu-id="e06a3-295">Modificējiet esošu lauku, lai sāktu izmantot uzmeklēšanu</span><span class="sxs-lookup"><span data-stu-id="e06a3-295">Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id="e06a3-296">Pēc tam modificējiet esošo aprēķināto lauku, lai tas izmantotu konfigurēto uzmeklēšanas datu avotu, lai atgrieztu pareizo nodokļa piemērošanas līmeņa vērtību atkarībā no nodokļa koda.</span><span class="sxs-lookup"><span data-stu-id="e06a3-296">Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id="e06a3-297">Atlasiet vienumu **Modelis.Dati.Kopsavilkums.Līmenis**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-297">Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id="e06a3-298">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-298">Select **Edit**.</span></span>
3.  <span data-ttu-id="e06a3-299">Atlasiet **Rediģēt formulu**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-299">Select **Edit formula**.</span></span>

    <span data-ttu-id="e06a3-300">Ievērojiet, ka pašreizējā lauka **Modelis.Dati.Kopsavilkums.Līmenis** izteiksme ietver tālāk minētos stingri kodētos nodokļu kodus.</span><span class="sxs-lookup"><span data-stu-id="e06a3-300">Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id="e06a3-301">GADĪJUMS (@.Code, "VAT19", "Parasts", "InVAT19", "Parasts", "VAT7", "Samazināts", "InVAT7", "Samazināts", "TREŠAIS", "Nav", "InVAT0", "Nav", "Cits")</span><span class="sxs-lookup"><span data-stu-id="e06a3-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="e06a3-302">Laukā **Formula** ievadiet **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Parasts", TaxationLevel.'Reduced taxation', "Samazināts", TaxationLevel.'No taxation', "Nav", "Cits")**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-302">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![ER operācijas veidotāja lapa](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="e06a3-304">Ņemiet vērā, ka lauka **Modelis.Dati.Kopsavilkums.Līmenis** izteiksme tagad atgriezīs nodokļa līmeni, pamatojoties uz pašreizējā ieraksta nodokļa kodu, un kārtulu kopumu, ko uzņēmuma lietotājs konfigurē uzmeklēšanas datu avotā **Modelis.Dati.Atlasītājs**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-304">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="e06a3-305">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-305">Select **Save**.</span></span>
6.  <span data-ttu-id="e06a3-306">Aizveriet lapu **Formāta veidotājs**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-306">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="e06a3-307">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-307">Select **OK**.</span></span>
8.  <span data-ttu-id="e06a3-308">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-308">Select **Save**.</span></span>
9.  <span data-ttu-id="e06a3-309">Aizveriet lapu **Formāta noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-309">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="e06a3-310">Pabeigta atvasinātā formāta melnraksta versija</span><span class="sxs-lookup"><span data-stu-id="e06a3-310">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="e06a3-311">Kopsavilkuma cilnē **Versijas** atlasiet **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-311">On the **Versions** fast tab, select **Change status**.</span></span>
2.  <span data-ttu-id="e06a3-312">Atlasiet **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-312">Select **Complete**.</span></span>
3.  <span data-ttu-id="e06a3-313">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-313">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="e06a3-314">Eksportēt modificētā formāta pabeigtu versiju</span><span class="sxs-lookup"><span data-stu-id="e06a3-314">Export completed version of modified format</span></span>

1.  <span data-ttu-id="e06a3-315">Konfigurācijas kokā atlasiet vienumu **Formatēt, lai uzzinātu, kā uzmeklēt Le datus**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-315">In the configuration tree, select the **Format to learn how to lookup LE data** item.</span></span>
2.  <span data-ttu-id="e06a3-316">Kopsavilkuma cilnē **Versijas** atlasiet ierakstu, kura statuss ir **Pabeigts**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-316">On the **Versions** fast tab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="e06a3-317">Atlasiet **Maiņa**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-317">Select **Exchange**.</span></span>
4.  <span data-ttu-id="e06a3-318">Atlasiet **Eksportēt kā XML failu**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-318">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="e06a3-319">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-319">Select **OK**.</span></span>
6.  <span data-ttu-id="e06a3-320">Tīmekļa pārlūks lejupielādē failu **Formatēt, lai uzzinātu, kā uzmeklēt LE datus. XML**.</span><span class="sxs-lookup"><span data-stu-id="e06a3-320">The web browser downloads a **Format to learn how to lookup LE data.xml** file.</span></span> <span data-ttu-id="e06a3-321">Saglabājiet šo failu lokāli.</span><span class="sxs-lookup"><span data-stu-id="e06a3-321">Store this file locally.</span></span>

<span data-ttu-id="e06a3-322">Atkārtojiet šajā sadaļā norādītās darbības formāta **Formatēt, lai uzzinātu, kā uzmeklēt LE datus** vecākelementiem, un saglabājiet lokāli tālāk norādītos failus.</span><span class="sxs-lookup"><span data-stu-id="e06a3-322">Repeat steps in this section for parent items of the **Format to learn how to lookup LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="e06a3-323">Formatēt, lai uzzinātu parametru izsaukumus.xml</span><span class="sxs-lookup"><span data-stu-id="e06a3-323">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="e06a3-324">Kartēšana, lai uzzinātu parametru izsaukumus.xml</span><span class="sxs-lookup"><span data-stu-id="e06a3-324">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="e06a3-325">Modelēt, lai uzzinātu parametru izsaukumus.xml</span><span class="sxs-lookup"><span data-stu-id="e06a3-325">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="e06a3-326">Lai uzzinātu, kā izmantot konfigurēto ER formātu **Formatēt, lai uzzinātu, kā uzmeklēt LE datus**, lai iestatītu no juridiskas personas atkarīgās nodokļu kodu kopas, lai filtrētu nodokļu transakcijas pēc dažādiem nodokļu līmeņiem, veiciet darbības, kas norādītas tēmā [Iestatīt ER formāta parametrus juridiskai personai](er-app-specific-parameters-set-up.md).</span><span class="sxs-lookup"><span data-stu-id="e06a3-326">To learn how to use the configured **Format to learn how to lookup LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e06a3-327">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e06a3-327">Additional resources</span></span>

[<span data-ttu-id="e06a3-328">Formulu veidotājs elektronisko atskaišu veidošanā</span><span class="sxs-lookup"><span data-stu-id="e06a3-328">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="e06a3-329">Iestatīt ER formāta parametrus juridiskai personai</span><span class="sxs-lookup"><span data-stu-id="e06a3-329">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)
