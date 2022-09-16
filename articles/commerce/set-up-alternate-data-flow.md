---
title: Alternatīvās datu plūsmas iestatīšana rekomendācijām
description: Šajā rakstā ir aprakstīts, kā konfigurēt vidi, izmantojot alternatīvu datu darbplūsmu, lai sniegtu datus rekomendāciju pakalpojumam.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460105"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>Alternatīvās datu plūsmas iestatīšana rekomendācijām

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā konfigurēt vidi, izmantojot alternatīvu datu darbplūsmu, lai sniegtu datus rekomendāciju pakalpojumam.

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>Lodziņa datu darbplūsmas un alternatīvās datu darbplūsmas salīdzinājums

Šajā attēlā ir attēlota ārpus kastes esošu datu darbplūsma vidē.

![Ārpus lodziņiem aizpildīta datu darbplūsma vidē](media/reco-out-of-the-box-dataflow-2.png)

Šajā ilustrācijā attēlota alternatīvā datu darbplūsma, kur elementa krātuves sinhronizācijas pakešuzdevums tiek aizstāts ar alternatīviem datu darbplūsmas soļiem.

![Alternatīvā datu darbplūsma vidē](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>Pieņēmumi

- Šajā rakstā tiek pieņemts, ka rekomendācijas jūsu videi jau ir iespējotas. Papildinformāciju skatiet Sadaļā Iespējot [preces ieteikumus](enable-product-recommendations.md).
- Kad strādājat ar failiem un mapēm datu Microsoft Azure pārsūtīšanas kontā:

    - Varat izmantot vai nu Azure tīmekļa portāla interfeisu, vai arī Azure Storage Explorer programmu.
    - Sākuma punkti darbam **ar failiem un mapēm ir dynamics365 finanšu dokumentu konteinerā, kas atrodas mapē, kuras nosaukums ir saskaņots** ar jūsu vides VIETRĀDI URL.
    - Ja jūsu kases vides nosaukums ir **MyUAT**, vides bāzes vietrādis URL būs `myuat.sandbox.operations.dynamics.com`.
    - Ja vienam glabāšanas kontam ir piesaistīta vairāk nekā viena vide, katrai videi būs sava saknes mape.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu ieviest alternatīvu datu darbplūsmas pieeju, ir jāizpilda šādi priekšnosacījumi.

### <a name="set-up-microsoft-power-platform"></a>Iestatīt Microsoft Power Platform

Lai iestatītu Microsoft Power Platform, izpildiet Aktivizēt integrāciju [sniegtās Microsoft Power Platform instrukcijas](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

### <a name="install-the-export-to-data-lake-add-in"></a>Uzstādīt Eksportēšanu uz datu Nei7 pievienojumprogrammu

Lai instalētu pievienojumprogrammu Eksportēt uz datu Abonements, [izpildiet norādījumus, kas sniegti sadaļāS Install Export to Azure DataInstalēšanu add-in](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

> [!NOTE]
> Atzīmējiet konfigurācijas vērtības, jo tās būs nepieciešamas dažiem soļiem, kas seko.

### <a name="configure-tables-to-export-in-dynamics-365"></a>Tabulu konfigurēšana eksportēšanai sistēmā Dynamics 365

Tabulu sinhronizācija no Dynamics 365 uz Azure Data Lake Storage tiek pārvaldīta **lapā Eksportēt uz datu summu**. Tā kā lapai pašlaik nav izvēlnes elementa, to var atvērt tikai **sistēmas administratora** drošības lomas lietotāji.

Lai konfigurētu tabulas eksportēšanai sistēmā Dynamics 365, veiciet šīs darbības.

1. Lai atvērtu lapu **Eksportēt uz datureizi,**`?mi=DataFeedsDefinitionWorkspace` pievienojiet virkni vides pamata vietrādim URL, kā parādīts šajā piemērā:

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. Lapā Eksportēt **uz datu Kolonnas** un nokopējiet tabulas, [kas uzskaitītas šī raksta sadaļā RetailSales](#list-of-retailsales-cube-tables) kubu tabulas.
1. Sistēmas nosaukuma **kolonnā** izvērsiet filtra opciju sarakstu.
1. Filtra veidam atlasiet vienu **no tiem**. Pēc tam teksta lodziņā novietojiet kursoru un ielīmējiet to tabulu sarakstu, kuras pārkopējat no **lapas Eksportēt uz datu atvilkšanu**.
1. Filtra opciju saraksta apakšdaļā atlasiet **Lietot**.
1. Atlasiet visas rindas režģī un pēc tam atlasiet **Aktivizēt**.

> [!NOTE]
> Pirms pāriet uz nākamo soli, visām rindām jābūt atjauninātām uz statusu **Notiek**. Pēc vajadzības novērsiet un novērsiet visas kļūdas.

### <a name="create-a-synapse-workspace"></a>Darbalauku izveidošana Darbalaukums

Lai izveidotu Siaapse darbvietu, ja jums vēl nav darbalauku, [izpildiet Quickstart norādītās instrukcijas: Izveidojiet Pirkšanas darbalauku](/azure/synapse-analytics/quickstart-create-workspace).

Lai uzturētu Azure resursu organizētus, ir ieteicams Azure resursu grupā apvienot datu Pārsūtīšanas kontu un Pārsūtīšanas darbvietu. Jūs varat atkārtoti izmantot glabāšanas kontu, ko izveidojāt, kad instalējat pievienojumprogrammu Eksportēt uz datu Nedatiem.

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>Izveidojiet datu bāziKomapse rekomendāciju datu apstrādei

Izmantojiet kopējo datu modeļa utilītas konsoles programmu (CDMUtil_ConsoleApp), lai izveidotu datu bāzi savā Aizpildīšanas darbvietā un aizpildītu to no kopīgās datu modeļu tabulas datu plkst. Ja ir kādi paplašinājumi, ieteicams izstrādes vidē izmantot kopējo datu modeļa utilītu ar datu bāzi.

> [!NOTE]
> Nākamajās darbībās tiek pieņemts, ka RetailSales kubam netiek pievienoti paplašinājuma dati.

Lai izveidotu datu bāzi Nekartē, sekojiet šiem soļiem.

1. Dodieties uz [Dynamics-365-FastTrack-Implementation-Assets GitHub](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app) un sekojiet soļiem, **lai lejupielādētu CDMUtilConsoleApp.zip** failu.
1. Izvelciet pasta indeksu lokālajā mapē.
1. Atveriet failu **CDMUtil_ConsoleApp.dll.config** teksta redaktorā un atjauniniet šādas vērtības:

    1. Iestatiet nomnieka **ID vērtību** (Azure nomnieka ID).
    1. Iestatiet piekļuves **atslēgas** vērtību (piekļuves atslēga kontam Data Plkst).

        1. Azure portālā atveriet glabāšanas kontu.
        1. Izvēlnes lapas kreisajā pusē atlasiet Piekļuves **atslēgas**.
        1. Lapas augšpusē atlasiet Rādīt **atslēgas**.
        1. Atlasiet kopēšanas pogu vienam no diviem atslēgas laukiem un pēc tam ielīmējiet vērtību starp dubultajām pēdiņām konfigurācijas failā.

    1. **Iestatiet ManifestURL vērtību** uz sava tables.manifest.cdm.json **faila** vietrādi URL šeit Azure Data Lake Storage: . Lai iegūtu vietrādi URL, pārlūkojiet failu Azure portālā, atlasiet elipsi (**...**) skata labajā pusē un pēc tam atlasiet **Rekvizīti**. URL ir pirmais rekvizīts, kas tiek rādīts cilnē **Pārskats**.
    1. **Iestatiet TargetDbConnectionString** vērtību savienojuma virknei, kas ir iebūvēta bezservera SQL pūlam jūsu Literapse darbvietā.

        1. Darbalaukē Ierašanās darbvieta izvēlieties cilni **Pārvaldīt**.
        1. Apakšizvēlnē atlasiet **SQL kopas**.
        1. Atlasiet nosaukumu **Iebūvēts,** lai skatītu kopas rekvizītus.
        1. Rekvizītu dialoglodziņā atlasiet datu ADO.NET tipu, kuru vēlaties izmantot. Pēc tam nokopējiet savienojuma virknes vērtību un ielīmējiet to starp dubultajām pēdiņām konfigurācijas failā.

        > [!NOTE]
        > Jums jābūt atļaujai izveidot datu bāzes. Lai vienkāršotu izmantošanu, jūs varētu vēlēties izmantot iebūvēto **SQLAdminUser** administratora kontu.

    1. Atcelt ProcesaE entītiju **mezgla** un iestatīt tā vērtību kā **patiesu** (piemēram`<add key="ProcessEntities" value ="true"/>`).

1. Saglabājiet un aizveriet **CDMUtil_ConsoleApp.dll.config**.
1. Kopējiet **failu EntityList.json** uz **/Manifesta direktoriju**.
1. Komandu uzvednes logā palaidiet cdmutil_consoleapp.exe **·**.

> [!NOTE]
> Pārskatot rezultātu, jābūt 35 elementiem/skatiem, vismaz 75 tabulām un bez kļūdām.

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>Datu gatavošana RetailSales Aggregate Measurements direktorijam

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>Dublējiet pašreizējos RetailSales kuba datus no datu Krātuves

Vienkāršākais veids, kā dublēt pašreizējos RetailSales **kuba datus, ir pārdēvēt RetailSales** direktoriju datu Kolonnu krātuvē **RetailSales-backup** vai citu līdzīgu. Ja problēmu novēršana ir nepieciešama vēlāk, šī metode saglabā esošos datus.

RetailSales **kuba** mape ir atrodama šajā atrašanās vietā:

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>Izveidot jaunu RetailSales mapi un augšupielādēt modeļa failu

Lai izveidotu jaunu **RetailSales** direktoriju un augšupielādēt **model.json** failu datu kat tas ir datu krātuvē, izpildiet šīs darbības.

1. Izveidot jaunu tukšu direktoriju iepriekšējā direktorija līmenī un nosaukt to par **RetailSales**.
1. Augšupielādējiet **failu model.json** jaunajā direktorijā.

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>Izveidot konveijeru, lai kopētu RetailSales kuba datus

Konveijers nolasīs RetailSales kuba skatus un eksportējīs datus uz .csv failiem datu krātuvē.

Lai izveidotu konveijeru RetailSales kuba datu kopēšanai, veiciet šādus soļus.

1. Darbalaukē Summu izveidošana izvēlieties cilni **Integrēt**.
1. Atlasiet plus zīmi ()**+** un pēc tam atlasiet Importēt **no konveijera veidnes**.
1. Lejupielādējiet un pēc tam atlasiet [failu ExportRetailSalesCubeViews.zip](https://aka.ms/reco-alternate-dataflow-files).
1. Atlasiet savu SQL datu bāzes saistīto pakalpojumu.
1. Atlasiet savu glabāšanas konta saistīto pakalpojumu.
1. Atveriet datu **kopēšanas** rīku un mainiet mapes **ceļa rekvizītu** uz **\<environment_name\>/...**.

### <a name="test-execution-of-the-pipeline"></a>Konveijera izpildes pārbaude

Konveijeru ir ieteicams pārbaudīt, izmantojot tikai vienu skatījumu. Skatījums **RetailSales_RetailMediaTemplateView** darbojas labi, jo tas parasti satur mazāk par 10 rindām.

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>Plānot konveijeru, lai to palaistu periodiskajā grafikā

Katru reizi, kad konveijers tiek palaists, rodas Azure patēriņš. Ieteicams ieplānot izpildes ar 48 stundu intervālu vai ilgāk. Konveijeru vienmēr var palaist manuāli, ja dati jāsinhronizē nekavējoties. 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>Tabulu saraksts sinhronizēšanai no Dynamics 365 uz datu e-pasta krātuvi

Tālāk redzamais tabulu saraksts ir visu to tabulu apakškopa, kas nepieciešamas visam RetailSales kubam. Tikai 15 skatījumus RetailSales kubā izmanto rekomendāciju pakalpojums, un nepieciešamo tabulu saraksts tika attiecīgi filtrēts.

### <a name="list-of-retailsales-cube-tables"></a>RetailSales kubu tabulu saraksts

- BICalendarOffsets
- BIDateDimension
- BIDateDimensionValue
- Katalogs
- Kataloga ražošana
- CatalogProductCategory (preču kategorija)
- CustInvoiceJour
- CustInvoiceTrans
- CustTable
- DataArea
- Vērtība DimensionAttributeValueCombination
- Vērtība DimensionAttributeValueSet
- DirPartyTable (tikai DirPartyTable)
- Objekta EcoResCategory kategorija
- Objekta EcoResCategoryHierarchy
- EcoResCategoryHierarchyRole
- EcoResColor (francija)
- Failu ecoResConfiguration
- EcoResProduct (ražošanas)
- Objekta EcoResProductCategory kategorija
- EcoResProductTranslation
- Objekta EcoResSize lielums
- EcoResStyle (Automātiskais)
- HcmWorker
- Inventdim
- InventDimCombination
- Inventitemgroup
- InventItemGroupItem (grupas nosaukums)
- InventItemSetupSupplyType
- InventTable
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionTranslation
- Loģistikas atrašanās vieta
- LogisticsPostalAddress ;
- OMHIERARCHYPURPOSE
- RetailAssortmentLookup
- RetailAssortmentLookupChannelGroup
- RetailChannelProfile (tikai datu fails)
- RetailChannelProfileProperty
- Tabula RetailChannelTable
- RetailChannelTableext
- RetailConnDatabaseProfile
- RetailCustInvoiceJourTable
- RetailCustTable
- RetailMediaTemplate veidne
- RetailOfflineProfile
- RetailPeriodicDiscount
- RetailRecoListConfigurationParameters
- Grupa RetailSalesTaxOverrideGroup
- RetailSharedParameters
- RetailSpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- Tabula RetailTerminalTable
- RetailTmpProductMedia (tikai komisija)
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- Darbība RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- Darbība RetailTransactionSalesTransExt
- RetailTransactionTable
- SalesLine
- SalesTable
- Parametri SystemParameters
- RETAILCATALOGINTERNALORG
- RETAILGROUPMEMBERLINE (TIKAI DATUMOS)
- MAZUMTIRDZNIECĪBASINTERNALORGANIZĀCIJA
- RAŽOŠANA RETAILSPECIALCATEGORYPRODUCT
- KATEGORIJA RETAILPRODUCTCATEGORY
- OBJEKTA ECORESCONFIGURATION
- DIMENSIONATTRIBUTE
- VĒRTĪBA DIMENSIONATTRIBUTEVALUESET
- DIMENSIONHIERARCHY
- DIMENSIONHIERARCHYINTEGRATION
- DIMENSIONHIERARCHYLEVEL
- DIMENSIONPARAMETER
- OMExplodedOrganizationSecurityGraph

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>Skatīt sarakstu ar parametru, kas tiek nodots e-lapas konveijeram E-rādītājs

Tālāk redzamajā ar komatu atdalītajā sarakstā ir RetailSales kuba skati, kuros konveijers izpildīs "izvēlēties" operāciju. Tad rezultāti tiks kopēti uz Data Noliktavu.

RetailSales_RetailAssortmentRulesView,RetailSales_RetailChannelNavigationHierarchiesView,RetailSales_RetailChannelNavigationHierarchyCatalogProductsView,RetailSales_RetailChannelNavigationHierarchyCategoryNodesView,RetailSales_RetailChannelNavigationHierarchyCategoryProductsView,RetailSales_RetailMediaBaseUrlChannelView,RetailSales_RetailMediaRelativeUrlProductView,RetailSales_RetailMediaTemplateView,RetailSales_RetailOptOutCustomersView, RetailSales_RetailProductCategory,RetailSales_RetailProductTransaction,RetailSales_RetailProductVariantDimensionsView,RetailSales_RetailRecoListConfigurationParametersView,RetailSales_RetailRecoListsSharedParametersView,RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> Konveijera parametram ir jābūt skatījuma nosaukumu sarakstam, kas atdalīts ar vienu komatu. Nedrīkst būt atstarpes vai rindu padeve.

## <a name="environment-specific-fixes"></a>Vides raksturīgi labojumi

### <a name="retailchannelview-fix"></a>RETAILCHANNELVIEW labojums

Skatā **RETAILCHANNELVIEW ir** ietverts vesels skaitlis, kodā ir iekļauts "mazumtirdzniecības kanāla" veida organizācija. Tipa faktiskā vērtība var mainīties no vides uz vidi vai no nomnieka uz nomnieku.

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

Lai atjauninātu veselo skaitļu zīmi, veiciet šādus soļus.

1. Sistēmā Dynamics 365 atrodiet kanāla **ID** vērtību savam tiešsaistes kanālam.
1. SQL Server Management Studio (SSMS) instancē, kas ir pievienota Datubāzei Papildmaksas, palaidiet šādu vaicājumu.

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. Kopējiet vērtību no pirmās kolonnas (**INSTANCERELATIONTYPE**) un ielīmējiet to skatījuma definīcijā.

## <a name="troubleshooting"></a>Problēmu novēršana

### <a name="pipeline-task-fails"></a>Konveijera uzdevums neizdodas

Uzdevumam CopyData **jābūt 15 konveijera** uzdevuma izpildei. Ja kāda izpilde neizdodas, jāpārbauda, vai eksistē visi atkarīgās SQL objekti un vai vaicājumi darbojas. Visvieglākais veids, kā piekļūt visām atkarībām, ir izmantot SSMS, lai izveidotu savienojumu ar datu bāzi. Pēc tam varat atlasīt un aizturēt (vai noklikšķināt ar peles labo pogu) skatu un atlasīt **izveidot izveidot jaunu logu**.

Kļūdas ziņojumā var būt iekļauts šāds teksts:

- Kļūda: līdzās "Avots" radās kļūda
- Apstrādājot ārējo failu, radās kļūda: 'Maksimālais kļūdu skaits'.
- /RetailPārdošanas/RetailSales_xxxxxx

#### <a name="example-scenario"></a>Piemērs

Šajā piemērā darba RetailSales_RetailProductCategory **neizdodas**, un tiek saņemts kļūdas ziņojums "Maksimālais kļūdu skaits".

Lai atkļūdotu kļūdu, sekojiet šiem soļiem.

1. Atveriet failu **EntityList.json** teksta redaktorā (piemēram, Visual Studio kods).
1. Atrodiet perioda skatījuma **RetailSales_RetailProductCategory**.

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. Šis skats ir atkarīgs tikai no cita skata: **RetailProductCategoryView** _. Atrast skatījuma definīciju šeit: _*RetailProductCategoryView**.

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. Šis skats ir atkarīgs no trim citiem skatiem: RETAILPRODUCTCATEGORY **,** ECORESPRODUCTTRANSLATIONS **un** RETAILCATEGORYEXPANDED **·**. Atrodiet katra skata definīciju un uzrādiniet to atkarības. Turpiniet, līdz atrod visus apgādājamā skatījumus.

    Šeit ir viss saraksts atkarības koka secībā. Ir jāpārbauda trīspadsmit skati.

    - RetailSales_RetailProductCategory

        - Skats RetailProductCategoryView

            - KATEGORIJA RETAILPRODUCTCATEGORY

                - OBJEKTA ECORESPRODUCTCATEGORY FUNKCIJA
                - ECORESCATEGORYHIERARCHYROLE
                - RAŽOŠANA RETAILSPECIALCATEGORYPRODUCT

                    - ECORESPRODUCT (RAŽOŠANASPRECE)
                    - RETAILGROUPMEMBERLINE (TIKAI DATUMOS)
                    - RETAILSPECIALCATEGORYMEMBER

            - ECORESPRODUCTTRANSLATIONS (FRANCIJA)

                - ECORESPRODUCT (RAŽOŠANASPRECE)
                - ECORESPRODUCTTRANSLATION
                - PARAMETRS SYSTEMPARAMETERS

            - RETAILCATEGORYEXPANDED

                - OBJEKTA ECORESCATEGORY KATEGORIJA
                - ECORESCATEGORYHIERARCHYROLE

1. Programmā Excel izveidojiet šādus 13 priekšrakstus **: skaits(\*\<view_name\>**). Izpildiet šos pārskatus SSMS un nosūtiet rezultātus uz tekstu. Pēc tam ritināt rezultātus, lai redzētu, vai kāds no skatiem neizdevās. Sākotnējā kļūda iesaka, ka vismaz viens no skatiem neizdosies.

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. Viens no veidiem, kā pārbaudīt, ko meklējat, ir izveidot ar sakni atkarīgu skatu, lai izveidotu skatījuma definīciju SSMS. Pēc tam pārbaudiet, vai ir Azure datu pārsūtīšanas faila kolonna, kas ir nosaukta **r.filepath**. Šīs kolonnas klātbūtne nozīmēs, ka skatījums, kurš tiek pārbaudīts, lasa datus no Datu Kolonnu glabāšanas.

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Iespējojiet Azure Data Lake Storage vidē Dynamics 365 Commerce .](enable-adls-environment.md)

[Personalizētu ieteikumu iespējošana](personalized-recommendations.md)

[Iespējot "veikala līdzīgie izskati" rekomendācijas](shop-similar-looks.md)

[Atteikšanās no personalizētiem ieteikumiem](personalization-gdpr.md)

[Pievienot preču ieteikumus punktā POS](product.md)

[Ieteikumu pievienošana transakciju ekrānam](add-recommendations-control-pos-screen.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Manuāli izveidot pārraudzītus ieteikumus](create-editorial-recommendation-lists.md)

[Izveidot ieteikumus ar demonstrācijas datiem](product-recommendations-demo-data.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
