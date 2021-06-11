---
title: Dataverse virtuālās tabulas vaicājumu optimizācija
description: Optimizēt Dataverse virtuālās tabulas vaicājumu veiktspēju un novērst ar to saistītas problēmas
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66fb9f2b50079b5eb4eb16da17b8a473d687d354
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054912"
---
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="3c651-103">Dataverse virtuālās tabulas vaicājumu optimizācija</span><span class="sxs-lookup"><span data-stu-id="3c651-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="3c651-104">Izsniegt</span><span class="sxs-lookup"><span data-stu-id="3c651-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="3c651-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="3c651-105">Overview</span></span>

<span data-ttu-id="3c651-106">Izmantojot Dataverse virtuālās tabulas, lai izstrādātu integrācijas un citus datu savienojumus ar Dynamics 365 Human Resources, var rasties veiktspējas problēmas ar virtuālo tabulu vaicājumiem.</span><span class="sxs-lookup"><span data-stu-id="3c651-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="3c651-107">Lēna vaicājuma izpilde var notikt dažādos klientos vai interfeisos.</span><span class="sxs-lookup"><span data-stu-id="3c651-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="3c651-108">Piemēram, var rasties problēma šādos apstākļos:</span><span class="sxs-lookup"><span data-stu-id="3c651-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="3c651-109">Veicot vaicājumu virtuālajā tabulā, izmantojot Dataverse Web API</span><span class="sxs-lookup"><span data-stu-id="3c651-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="3c651-110">Veidojot Power App pret virtuālo tabulu</span><span class="sxs-lookup"><span data-stu-id="3c651-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="3c651-111">Veidojot Power BI pārskatu par virtuālo tabulu</span><span class="sxs-lookup"><span data-stu-id="3c651-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="3c651-112">Visiem šiem interfeisiem ir potenciāls radīt veiktspējas problēmu.</span><span class="sxs-lookup"><span data-stu-id="3c651-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="3c651-113">Viens no iemesliem lēnai darbībai ar Dataverse virtuālām tabulam pakalpojumam Human Resources ir ārējās atslēgas kolonnas virtuālajā tabulā, kas saistīta ar tabulas [navigācijas rekvizītiem](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span><span class="sxs-lookup"><span data-stu-id="3c651-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="3c651-114">Kad navigācijas rekvizīti ir izveidoti virtuālai tabulai, ārējās atslēgas kolonna tiek automātiski pievienota tabulai, lai attēlotu atslēgas vērtību saistītās virtuālās tabulas atslēgas kolonnai.</span><span class="sxs-lookup"><span data-stu-id="3c651-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="3c651-115">Piemēram, kolonna **_mshr_fk_person_id_value** ir pievienota elementam **mshr_hcmworkerbaseentity** ar ārējās atslēgas rekvizītu no elementa **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="3c651-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="3c651-116">Tā kā šo ārējo atslēgu kolonnu vērtības tiek uzturētas tabulā, vērtību iegūšana var negatīvi ietekmēt vaicājuma veiktspēju virtuālajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="3c651-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="3c651-117">Iespējamie simptomi</span><span class="sxs-lookup"><span data-stu-id="3c651-117">Potential symptoms</span></span>

<span data-ttu-id="3c651-118">Piemērs, kur, iespējams, redzat šo ietekmi, ir vaicājumos pret nodarbināto (**mshr_hcmworkerentity**) vai pamata nodarbināto (**mshr_hcmworkerbaseentity**) elementu.</span><span class="sxs-lookup"><span data-stu-id="3c651-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="3c651-119">Jūs varat redzēt veiktspējas problēmas paradīsies dažos dažādos veidos:</span><span class="sxs-lookup"><span data-stu-id="3c651-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="3c651-120">**Palēnināta vaicājuma izpilde**: vaicājums attiecībā uz virtuālo tabulu var atgriezt paredzamos rezultātus, bet tas var aizņemt vairāk laika, nekā paredzēts vaicājuma izpildes pabeigšanai.</span><span class="sxs-lookup"><span data-stu-id="3c651-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="3c651-121">**Vaicājuma taimauts**: Iespējams, ka vaicājumam iestājas taimauts un tiek atgriezta šāda kļūda: "tika iegūta pilnvara, lai izsauktu Finance and Operations, bet Finance and Operations atgrieza InternalServerError veida kļūdu."</span><span class="sxs-lookup"><span data-stu-id="3c651-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="3c651-122">**Neparedzēta kļūda**: vaicājums var atgriezt 400 veida kļūdas ar šādu ziņojumu: "Radusies negaidīta kļūda."</span><span class="sxs-lookup"><span data-stu-id="3c651-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![Kļūdas veids 400 uz HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="3c651-124">**Ierobežošana**: vaicājums var pārmērīgi izmantot servera resursus un tikt pakļauts ierobežošanai.</span><span class="sxs-lookup"><span data-stu-id="3c651-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="3c651-125">Šajā gadījumā vaicājums atgriež šādu kļūdu: "Marķieris tika iegūts, lai izsauktu Finance and Operations, bet Finance and Operations atgrieza 429 veida kļūdu."</span><span class="sxs-lookup"><span data-stu-id="3c651-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="3c651-126">Papildinformāciju par ierobežošanu pakalpojumā Human Resources skatiet sadaļā [Bieži uzdotie jautājumi par ierobežošanu](./hr-admin-integration-throttling-faq.md).</span><span class="sxs-lookup"><span data-stu-id="3c651-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![Kļūdas veids 429 uz HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="3c651-128">Novēršana</span><span class="sxs-lookup"><span data-stu-id="3c651-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="3c651-129">Ierobežot datu vaicājumā iekļauto kolonnu skaitu</span><span class="sxs-lookup"><span data-stu-id="3c651-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="3c651-130">Izmantojot virtuālās tabulas, viena no metodēm ar vislielāko potenciālu uzlabot vaicājuma veiktspēju ir ierobežot vaicājumā atlasīto kolonnu skaitu.</span><span class="sxs-lookup"><span data-stu-id="3c651-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="3c651-131">Vispārīgie norādījumi vaicājuma veiktspējas optimizēšanai ir ierobežot vaicājumā atgrieztās kolonnas līdz tikai nepieciešamajiem rekvizītiem.</span><span class="sxs-lookup"><span data-stu-id="3c651-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="3c651-132">Īpaši tas attiecas uz ārējo atslēgu kolonnām virtuālajās tabulās.</span><span class="sxs-lookup"><span data-stu-id="3c651-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="3c651-133">Ja jūsu integrācijai vai pārskatam nav nepieciešamas vērtības ārējās atslēgas kolonnās, tad strukturējiet vaicājumu, lai atlasītu tikai tās kolonnas, kuras nepieciešamas, izņemot ārējās atslēgas kolonnas.</span><span class="sxs-lookup"><span data-stu-id="3c651-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="3c651-134">Kolonnu atlase OData vaicājumā</span><span class="sxs-lookup"><span data-stu-id="3c651-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="3c651-135">Veicot vaicājumu virtuālajā tabulā, izmantojot Dataverse Web API, var ierobežot vaicājumā iekļauto kolonnu skaitu, izmantojot **$atlasīt** sistēmas vaicājuma opciju un definēt kolonnas, kurām jāatgriež rezultāti.</span><span class="sxs-lookup"><span data-stu-id="3c651-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="3c651-136">Lai maksimizētu veiktspēju, no vaicājuma izslēdziet ārējās atslēgas (ar **_mshr_FK_** prefiksu).</span><span class="sxs-lookup"><span data-stu-id="3c651-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="3c651-137">Piemēram, nākamajā vaicājumā attiecībā pret elementu **mshr_hcmworkerbaseentity** tiks iekļautas tikai kolonnas, kas iekļautas vaicājuma opciju klauzulā **$atlasīt**, izņemot ārējās atslēgas vērtības.</span><span class="sxs-lookup"><span data-stu-id="3c651-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="3c651-138">Tas nodrošina nozīmīgus veiktspējas uzlabojumus vaicājumā, kas ietver visas tabulas kolonnas.</span><span class="sxs-lookup"><span data-stu-id="3c651-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="3c651-139">Ieteikums ierobežot atlasīto kolonnu skaitu tiek lietots arī tad, ja izmantojat vaicājuma opciju **$paplašināt**, lai izvērstu vaicājumu uz saistītajām virtuālajām tabulām, izmantojot navigācijas rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="3c651-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="3c651-140">Piemēram, šajā vaicājumā ir iekļautas kolonnas no elementa **mshr_hcmworkerbaseentity** ar paplašinātām kolonnām no elementa **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="3c651-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="3c651-141">Ievērojiet, ka vaicājuma opcija **$atlasīt** ir iekļauta arī vaicājuma opcijas klauzulā **$paplašināt**.</span><span class="sxs-lookup"><span data-stu-id="3c651-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="3c651-142">Izmantojot šo datu izgūšanas metodi ar vaicājuma opciju **$atlasīt** vaicājuma opciju klauzulā **$paplašināt**, parasti jūs redzēsiet lielākus veiktspējas uzlabojumus, ja navigācijas rekvizīts starp elementiem ir relācija daudzi pret vienu.</span><span class="sxs-lookup"><span data-stu-id="3c651-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="3c651-143">Izvēršot relāciju “viens pret daudziem”, iespējams, neredzēsit tādu pašu vaicājuma izpildes laika samazinājumu.</span><span class="sxs-lookup"><span data-stu-id="3c651-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="3c651-144">Plašāku informāciju par Dataverse virtuālo tabulu attiecību definīciju skatiet [Tabulu attiecībās](/powerapps/maker/data-platform/create-edit-entity-relationships).</span><span class="sxs-lookup"><span data-stu-id="3c651-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="3c651-145">Papildinformāciju par sistēmas vaicājuma opciju **$atlasīt** un **$paplašināt** izmantošanu Dataverse Web API skatiet sadaļā [Saistīto elementu ierakstu izgūšana ar vaicājumu](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span><span class="sxs-lookup"><span data-stu-id="3c651-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="3c651-146">Kolonnu atlase pakalpojumā Power BI</span><span class="sxs-lookup"><span data-stu-id="3c651-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="3c651-147">Ja, veidojot Power BI pārskatu Dataverse virtuālai tabulai, rodas kāda no iepriekšminētajām pazīmēm par lēnu veiktspēju, veiktspēju var uzlabot, izslēdzot ārējās atslēgas kolonnas no kolonnām, kas atlasītas atskaites tabulā.</span><span class="sxs-lookup"><span data-stu-id="3c651-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="3c651-148">Piemēram, ja lietojat Power BI Desktop, lai izveidotu pārskatu pret elementu **mshr_hcmworkerbaseentity**, var veikt šādas darbības, lai atlasītu kolonnas, kuras vēlaties iekļaut atskaites vaicājumā.</span><span class="sxs-lookup"><span data-stu-id="3c651-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="3c651-149">Pakalpojumā Power BI Desktop atlasiet **Vairāk...** nolaižamajā sarakstā **Iegūt datus** darbību lentē.</span><span class="sxs-lookup"><span data-stu-id="3c651-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="3c651-150">Logā **Iegūt datus** ievadiet **Common Data Service** meklēšanas lodziņā, atlasiet savienotāju **Common Data Service** un atlasiet **Savienot**.</span><span class="sxs-lookup"><span data-stu-id="3c651-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="3c651-151">Laukā **Servera Url**, logā Common Data Service ievadiet uzņēmuma URI jūsu Dataverse videi un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3c651-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![Ievadiet URI jūsu Dataverse videi](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="3c651-153">Logā Navigators izvērsiet zaru **Elementi**.</span><span class="sxs-lookup"><span data-stu-id="3c651-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="3c651-154">Meklēšanas lodziņā ievadiet **mshr_hcmworkerbaseentity** un atlasiet elementu.</span><span class="sxs-lookup"><span data-stu-id="3c651-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="3c651-155">Atlasiet **Datu transformācija**.</span><span class="sxs-lookup"><span data-stu-id="3c651-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="3c651-156">Power Query redaktora logā atlasiet **Paplašinātais redaktors**.</span><span class="sxs-lookup"><span data-stu-id="3c651-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="3c651-157">Logā **Paplašinātais redaktors** atjauniniet vaicājumu, lai tas izskatītos līdzīgi kā turpmāk, pēc nepieciešamības pievienojot vai noņemot kolonnas masīvam.</span><span class="sxs-lookup"><span data-stu-id="3c651-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Atjaunināt vaicājumu Power Query redaktoram Vaicājumu redaktorā](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. <span data-ttu-id="3c651-159">Atlasiet **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="3c651-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="3c651-160">Ja pirms atjaunināšanas jūs iepriekš saņēmāt no vaicājuma 429 vaida kļūdu, var būt nepieciešams gaidīt atkārtoto mēģinājumu periodu pirms vaicājuma atsvaidzināšanas, lai veiksmīgi to pabeigtu.</span><span class="sxs-lookup"><span data-stu-id="3c651-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="3c651-161">Noklikšķiniet uz **Aizvērt &, Lietot** Power Query redaktora darbības lentē.</span><span class="sxs-lookup"><span data-stu-id="3c651-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="3c651-162">Pēc tam Power BI pārskatu ir iespējams izveidot pret kolonnām, kas atlasītas no virtuālās tabulas.</span><span class="sxs-lookup"><span data-stu-id="3c651-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="3c651-163">Kolonnu atlase pakalpojumā Power Apps</span><span class="sxs-lookup"><span data-stu-id="3c651-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="3c651-164">Līdzīgi kā Dataverse Web API vaicājumiem un Power BI varat uzlabot Power Apps vaicājumu veiktspēju, pamatojoties uz Dataverse virtuālajām tabulām, izslēdzot saistīto tabulu kolonnas no programmas.</span><span class="sxs-lookup"><span data-stu-id="3c651-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="3c651-165">Ja kāda kolonna no saistītās tabulas ir ietverta lapā, tad pieprasījuma URL, kas veidots, lai iegūtu datus, iekļaus saistītās tabulas ārējās atslēgas rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="3c651-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="3c651-166">Tas, tāpat kā augstāk minētie piemēri par [Kolonnu atlasīšanu OData vaicājumā](#selecting-columns-in-power-apps), samazina veiktspēju, radot papildu datu meklēšanas.</span><span class="sxs-lookup"><span data-stu-id="3c651-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="3c651-167">Lai to paveiktu, varat pārbaudīt, vai Power App datu veidlapā nav iekļauti datu lauki no saistītām tabulām.</span><span class="sxs-lookup"><span data-stu-id="3c651-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="3c651-168">Koka skata rūtī atlasiet datu veidlapu ekrānam.</span><span class="sxs-lookup"><span data-stu-id="3c651-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="3c651-169">Rūtī **Rekvizīti** atlasiet **Rediģēt** rekvizītā **Lauki**.</span><span class="sxs-lookup"><span data-stu-id="3c651-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="3c651-170">Rūtī **Dati** pārbaudiet, vai neviens no atlasītajiem laukiem nav datu avota virtuālās tabulas lauks.</span><span class="sxs-lookup"><span data-stu-id="3c651-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="3c651-171">Piemēram, ja vienam no datu laukiem, kas ietverti programmas lapā, ir atsauce uz citu tabulu, piemēram, **ThisItem.Worker.Name**, kur **Nodarbinātais** ir saistītā tabula, datu ienesē var samazināt veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="3c651-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="3c651-172">Varat izmantot [Power Apps monitoru](/powerapps/maker/monitor-overview), lai nodrošinātu, ka tikai jums nepieciešamas kolonnas tiek iekļautas vaicājumā, lai iegūtu datus par programmu Power App.</span><span class="sxs-lookup"><span data-stu-id="3c651-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="3c651-173">Varat skatīt URL, kas veidots getRows operācijai, lai nodrošinātu, ka jūsu programmai atlasītās kolonnas būs optimālas datu izgūšanai.</span><span class="sxs-lookup"><span data-stu-id="3c651-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![Izmantojiet Power Apps monitoru, lai analizētu getData operāciju](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="3c651-175">Datu vaicājuma filtrēšana</span><span class="sxs-lookup"><span data-stu-id="3c651-175">Filtering the data query</span></span>

<span data-ttu-id="3c651-176">Cita metode vaicājuma izpildes veiktspējas uzlabošanai ir ierobežot vaicājuma rezultātos atgriezto ierakstu skaitu.</span><span class="sxs-lookup"><span data-stu-id="3c651-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="3c651-177">To var izdarīt, filtrējot rezultātus, lai pārliecinātos, ka saņemat tikai tos ierakstus, kurus nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="3c651-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="3c651-178">Lai iegūtu papildu informāciju par vaicājuma datu filtrēšanu, skatiet [Filtra rezultāti](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results).</span><span class="sxs-lookup"><span data-stu-id="3c651-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="3c651-179">Vaicājuma lapas izmēra ierobežošana</span><span class="sxs-lookup"><span data-stu-id="3c651-179">Limiting the page size of the query</span></span>

<span data-ttu-id="3c651-180">Ja strādājat ar lielām datu kopām, vaicājuma rezultātus var sadalīt vairākās lapās, datu vaicājumiem pievienojot `odata.maxpagesize` preferenču virsrakstu.</span><span class="sxs-lookup"><span data-stu-id="3c651-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="3c651-181">Papildinformāciju par lapošanu skatiet sadaļā [Norādīt elementu skaitu, kas jāatgriež lapā](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span><span class="sxs-lookup"><span data-stu-id="3c651-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="3c651-182">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="3c651-182">See also</span></span>

- [<span data-ttu-id="3c651-183">Pakalpojuma Dataverse virtuālo tabulu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="3c651-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="3c651-184">Bieži uzdotie jautājumi par Human Resources tabulām</span><span class="sxs-lookup"><span data-stu-id="3c651-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="3c651-185">Bieži uzdotie jautājumi par ierobežošanu</span><span class="sxs-lookup"><span data-stu-id="3c651-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]