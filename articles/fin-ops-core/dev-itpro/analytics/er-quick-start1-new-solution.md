---
title: Izveidot jaunu ER risinājumu, lai izdrukātu pielāgotu pārskatu
description: Šajā tēmā skaidrots, kā noformēt elektronisko pārskatu (ER) risinājumu, lai izdrukātu pielāgotu pārskatu.
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "220314"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af610ae86e751ec4425f4c555cdf59c042fabcdb46e6a3a018b0d94a8926d92e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770072"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a>Izveidot jaunu ER risinājumu, lai izdrukātu pielāgotu pārskatu

[!include[banner](../includes/banner.md)]

Tālāk aprakstītajās darbībās izskaidrots, kā lietotājs sistēmas administratora, elektroniskā pārskatu izstrādātāja vai elektroniskās ziņošanas funkcionālās konsultanta lomā var konfigurēt ER struktūras parametrus, veidot jaunā ER risinājuma nepieciešamās ER konfigurācijas, lai piekļūtu konkrētā biznesa domēna datiem un izstrādātu pielāgotu pārskatu Microsoft Office formātā. Šīs darbības var veikt uzņēmumā **USMF**.

- [ER struktūras konfigurēšana](#ConfigureFramework)

    - [Konfigurējiet ER parametrus](#ConfigureParameters)
    - [ER konfigurācijas nodrošinātāja aktivizēšana](#ActivateProvider)

        - [ER konfigurācijas nodrošinātāju saraksta pārskatīšana](#ReviewProvidersList)
        - [Jauna ER konfigurācijas nodrošinātāja pievienošana](#AddProvider)
        - [ER konfigurācijas nodrošinātāja aktivizēšana](#ActivateAddedProvider)

- [Domēnam specifiska datu modeļa izveide](#DesignModel)

    - [Importēt jaunu datu modeļa konfigurāciju](#ImportDataModel)
    - [Jaunas datu modeļa konfigurācijas izveide](#DesignDataModel)

        - [Datu modeļa nosaukšana](#NameDataModel)
        - [Datu modeļa lauku pievienošana](#FieldsEntry)
        - [Datu modeļa noformējuma pabeigšana](#CompleteDataModel)

- [Konfigurētā datu modeļa kartēšanas izveidošana](#DesignMapping)

    - [Jaunas modeļa kartēšanas konfigurācijas importēšana](#ImportModelMapping)
    - [Jauna modeļa kartēšanas konfigurācijas izveidošana](#CreateModelMapping)

        - [Jaunu modeļa kartēšanas komponentu izveidošana](#DesignMappingComponent)
        - [Datu avotu pievienošana piekļuves pieteikumu tabulām](#AddMmDataSource1)
        - [Datu avotu pievienošana piekļuves pieteikumu uzskaitījumiem](#AddMmDataSource2)
        - [ER etiķešu pievienošana, lai ģenerētu pārskatu noteiktā valodā](#AddMmLabels)
        - [Datu avotu pievienošana, lai pārveidotu uzskaitījuma vērtību salīdzināšanas rezultātus teksta vērtībā](#AddMmDataSource3)
        - [Datu avotu saistīšana uz datu modeļa laukiem](#AddMmBindings1)
        - [Modeļa kartēšanas noformējuma pabeigšana](#CompleteModelMapping)

- [Veidnes izveide pielāgotam pārskatam](#DesignReportTemplate)
- [Formāta veidošana](#DesignFormat)

    - [Izstrādātā formāta konfigurācijas importēšana](#FormatImport)
    - [Jaunas formāta konfigurācijas izveide](#FormatCreate)

        - [Pārskata veidnes importēšana](#ImportReportTemplate)
        - [Formāta konfigurēšana](#ConfigureFormat)
        - [Pārskata nosaukuma datu saistījumu definēšana](#DefineFormatBindings)
        - [Modeļa datu avota pārskatīšana](#ReviewModelDataSource)
        - [Formāta elementu saistīšana ar datu avotu laukiem](#BindFormatElements)

    - [Izveidoto formātu palaišana no ER](#RunFormatFromER)

- [Izveidotā formāta noskaņošana](#TuneFormat)

    - [Formātu modificēšana, lai mainītu ģenerētā dokumenta nosaukumu](#ModifyToChangeName)
    - [Formātu modificēšana, lai mainītu jautājumu secību](#ModifyToOrder)
    - [Modificēto formātu palaišana no ER](#RunFormatFromER2)
    - [Formāta noformējuma pabeigšana](#CompleteFormat)

- [Pieteikumu artefaktu izstrādāšana, lai izsauktu paredzēto pārskatu](#DevelopCustomCode)

    - [Pirmkoda modificēšana](#ModifySourceCode)

        - [Datu līguma klases pievienošana](#DataContractClass)
        - [UI veidotāja klases pievienošana](#UIBuilderClass)
        - [Datu nodrošinātāja klases pievienošana](#DataProviderClass)
        - [Etiķešu faila pievienošana](#LabelsFile)
        - [Pārskata pakalpojumu klases pievienošana](#ServiceClass)
        - [Pārskata kontrolētāja klases pievienošana](#ControllerClass)
        - [Izvēlnes elementa pievienošana](#MenuItem)
        - [Izvēlnes krājuma pievienošana izvēlnei](#Menu)
        - [Izveidot Visual Studio projektu](#BuildVSProject)

    - [Formāta palaišana no programmas](#RunFormatFromApp)

- [Izstrādāta ER risinājuma noregulēšana](#TuneSolution)

    - [Modeļa kartējuma modificēšana](#ModifyModelMapping)

        - [Datu avotu pievienošana piekļuves datu līguma objektam](#AddDataSource1)
        - [Datu avota pievienošana, lai piekļūtu ER formāta kartēšanas ierakstiem](#AddDataSource2)
        - [Datu avota pievienošana, lai piekļūtu tekošā ER formāta kartēšanas ierakstam](#AddDataSource3)
        - [Tekošā ER formāta nosaukuma ievadīšana datu modelī](#AddBinding)
        - [Modeļa kartēšanas noformējuma pabeigšana](#CompleteModelMapping2)

    - [Formāta modificēšana](#ModifyFormat)

        - [Jauna formāta elementa pievienošana](#AddFormatElement)
        - [Pievienotā formāta elementa saistīšana](#BindAddedFormatElement)
        - [Formāta noformējuma pabeigšana](#CompleteFormat2)

    - [Formāta palaišana no programmas](#RunFormatFromApp2)
    - [Formāta palaišana no ER](#RunFormatFromER3)
    - [Formāta mērķa konfigurēšana ekrānā redzamajā priekšskatījumā](#ConfigureDestination)
    - [Formāta palaišana no programmas, lai to priekšskatītu kā PDF dokumentu](#RunFormatFromApp3)

- [Papildu resursi](#References)

Šajā piemērā tiks izveidots jauns ER risinājums [Anketas](../../../human-resources/hr-learning-questionnaires.md) modulim. Šis jaunais ER risinājums sniedz iespēju izveidot pārskatu, izmantojot Microsoft Excel darblapu kā veidni. Pēc tam varat izveidot **Anketu** pārskatu Excel vai PDF formātā papildus esošo SQL Server pārskatu izveides pakalpojumu (SSRS) pārskata ģenerēšanai. Jauno pārskatu var arī modificēt vēlāk pēc pieprasījuma. Kodēšana nav nepieciešama.

1. Lai palaistu esošo pārskatu, dodieties uz **Anketa** \> **Dizains** \> **Anketas pārskats**.

    ![Atlasot Anketu pārskata izvēlnes krājumu Anketas modulī, lai palaistu esošo SSRS pārskatu.](./media/er-quick-start1-application-menu-origin.png)

2. Dialoglodziņā **Anketu pārskats** norādiet atlases kritērijus. Lietojiet filtru, lai pārskats iekļautu tikai **SBCCrsExam** anketu.

    ![Dialoglodziņā Anketu pārskats norādiet atlases kritērijus.](./media/er-quick-start1-ssrs-report-dialog.png)

Sekojošajā attēlā parādīta SSRS pārskata ģenerētā versija **SBCCrsExam** anketai.

![Ģenerētais SSRS pārskats.](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a>ER struktūras konfigurēšana

Kā lietotājam Elektronisko pārskatu attīstības lomā, jums ir jākonfigurē minimāls ER parametru kopums, pirms varat sākt izmantot ER struktūru, lai veidotu jaunu ER risinājumu.

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a>Konfigurējiet ER parametrus

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Darbvietā **Elektronisko pārskatu veidošana** atlasiet saiti **Elektronisko pārskatu veidošanas parametri**.
3. Lapas **Elektronisko pārskatu veidošanas parametri** cilnē **Vispārīgi** iestatiet opciju **Iespējot noformēšanas režīmu** uz **Jā**.
4. Cilnē **Pielikumi** iestatiet šādus parametrus:

    - Iestatiet lauku **Konfigurācijas** uz **Fails** uzņēmumam **USMF**.
    - Iestatiet **Darbu arhīvs**, **Pagaidu**, **Bāzlīnija** un **Citi** laukus uz **Fails**.

Papildinformāciju par ER parametriem skatiet sadaļā [ER struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a>ER konfigurācijas nodrošinātāja aktivizēšana

Katra ER konfigurācija tiek atzīmēta kā piederoša ER konfigurācijas nodrošinātājam. Tāpēc, pirms sākat pievienot vai rediģēt ER konfigurācijas, jums ir jāaktivizē ER konfigurācijas nodrošinātājs **Elektroniskie pārskati** jebkurā darbvietā.

> [!NOTE]
> Tikai ER konfigurācijas īpašnieks var to rediģēt. Tāpēc, pirms ER konfigurācija var tikt rediģēta, darbvietā **Elektroniskie pārskati** ir jāaktivizē atbilstošais ER konfigurācijas nodrošinātājs.

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a>ER konfigurācijas nodrošinātāju saraksta pārskatīšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Darbvietas **Elektronisko pārskatu veidošana** sadaļā **Saistītās saites** atlasiet **Konfigurācijas nodrošinātāji**.
3. Lapā **Konfigurācijas nodrošinātāji** katrai konfigurācijai ir unikāls nosaukums un URL. Pārskatiet šīs lapas saturu. Ja ieraksts **Litware, Inc.** (`https://www.litware.com`) jau pastāv, izlaidiet nākamo procedūru, [Jauna ER konfigurācijas nodrošinātāja pievienošana](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a>Jauna ER konfigurācijas nodrošinātāja pievienošana

1. Lapā **Konfigurācijas nodrošinātāji** atlasiet **Jauns**.
2. Laukā **Nosaukums** ievadiet **Litware, Inc.**
3. Laukā **Interneta adrese** ievadiet `https://www.litware.com`.
4. Atlasiet **Saglabāt**.

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a>ER konfigurācijas nodrošinātāja aktivizēšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. **Elektroniskā pārskata** darbvietā atlasiet **Litware, Inc.** jūsu konfigurācijas nodrošinātājam.
3. Atlasiet **Iestatīt kā aktīvu**.

Papildinformāciju par ER konfigurācijas nodrošinātājiem skatiet sadaļā [Konfigurācijas nodrošinātāju izveide un atzīmēšana par aktīviem](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a>Domēnam specifiska datu modeļa izveide

Ir jāizveido jauna ER konfigurācija, kas satur [datu modeļa](general-electronic-reporting.md#data-model-and-model-mapping-components) komponentu **Anketas** biznesa domēnam. Šis datu modelis vēlāk tiks izmantots kā datu avots, noformējot ER formātu, lai ģenerētu **Anketas** pārskatu.

Veicot darbības, kas norādītas sadaļā [Importēt jaunu datu modeļa konfigurāciju](#ImportDataModel), jūs varat importēt nepieciešamo datu modeli no norādītā XML faila. Vai arī varat veikt darbības, kas aprakstītas sadaļā [Izveidot jaunu datu modeļa konfigurāciju](#DesignDataModel), lai izveidotu šo datu modeli no jauna.

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a>Importēt jaunu datu modeļa konfigurāciju

1. Lejupielādējiet [Anketu model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) failu un saglabājiet to lokālajā datorā.
2. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
3. Darbvietā **Elektroniskie pārskati** atlasiet **Pārskatu veidošanas konfigurācijas**.
4. Darbību rūtī atlasiet **Mainīt** \> **Ielādēt no XML faila**.
5. Atlasiet **Pārlūkot** un pēc tam atrodiet un atlasiet **Anketu model.version.1.xml** failu.
6. Atlasiet **Labi**, lai importētu konfigurāciju.

Lai turpinātu, izlaidiet nākamo procedūru [Izveidot jaunu datu modeļa konfigurāciju](#DesignDataModel).

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a>Jaunas datu modeļa konfigurācijas izveide

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Darbvietā **Elektroniskie pārskati** atlasiet **Pārskatu veidošanas konfigurācijas**.
3. Atlasiet **Izveidot konfigurāciju**.
4. Nolaižamā dialoglodziņa laukā **Nosaukums** ievadiet **Anketas modelis**.
5. Atlasiet **Izveidot konfigurāciju**, lai izveidotu konfigurāciju.

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a>Datu modeļa nosaukšana

1. Lapā **Konfigurācijas** konfigurācijas kokā atlasiet **Anketas modelis**.
2. Atlasiet **Noformētājs**.
3. Lapas **Datu modeļa veidotājs**, kopsavilkuma cilnē **Vispārēji**, laukā **Nosaukums** ievadiet <a name="DataModeName"></a>**Anketas**.

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a>Jaunu datu modeļa lauku pievienošana

1. Lapā **Datu modeļa noformētājs** atlasiet **Jauns**.
2. Nolaižamajā dialoglodziņā datu modeļa zara pievienošanai veiciet šādas darbības:

    1. Atlasiet **Modeļa sakni** kā jaunā zara tipu.
    2. Laikā **Nosaukums** ievadiet <a name="RootDefinitionName"></a>**Sakne**.
    3. Atlasiet **Pievienot**, lai pievienotu jaunu zaru.

    Šis saknes deskriptors tiks izmantots, lai sniegtu datus **Anketas** pārskatam. Vienam datu modelim var būt vairāki deskriptori. Katru deskriptoru var norādīt vienam ER formātam, lai identificētu datus, kas ir nepieciešami pārskata ģenerēšanai.

3. Vēlreiz atlasiet **Jauns** nolaižamajā dialoglodziņā datu modeļa mezgla pievienošanai veiciet šādas darbības:

    1. Atlasiet **Aktīvā mezgla atvasi** kā jaunā zara tipu.
    2. Laukā **Nosaukums** ievadiet **CompanyName**.
    3. Laukā **Vienuma veids** atlasiet **Virkne**.
    4. Atlasiet **Pievienot**, lai pievienotu jaunu lauku.

    Šis lauks ir nepieciešams, lai nodotu dotā uzņēmuma nosaukumu ER pārskatam, kas patērē šo datu modeli kā datu avotu.

4. Vēlreiz atlasiet **Jauns** nolaižamajā dialoglodziņā datu modeļa mezgla pievienošanai veiciet šādas darbības:

    1. Atlasiet **Aktīvā mezgla atvasi** kā jaunā zara tipu.
    2. Laukā **Nosaukums** ievadiet **Anketa**.
    3. Laukā **Vienuma veids** atlasiet **Ierakstu saraksts**.
    4. Atlasiet **Pievienot**, lai pievienotu jaunu lauku.

    Šis lauks tiks izmantots, lai nodotu anketu sarakstu ER pārskatam, kas patērē šo datu modeli kā datu avotu.

5. Atlasiet **Anketas** mezglu.
6. Turpiniet pievienot vajadzīgos rediģējamo datu modeļa laukus tādā pašā veidā, līdz tiek pabeigta šāda datu modeļa struktūra.

    | Lauka ceļš                                                    | Datu tips   | Lauka apzīmējums/atgrieztā vērtība |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | Sakne                                                          |             | Atsauces punkts, lai pieprasītu anketas datus. |
    | Root\\CompanyName                                             | Virkne      | Pašreizējā uzņēmuma nosaukums. |
    | Root\\ExecutionContext                                        | Reģistrēt      | Formāta izpildes detalizēta informācija. |
    | Root\\ExecutionContext\\FormatName                            | Virkne      | Palaistā ER formāta nosaukums. |
    | Root\\Questionnaire                                           | Ierakstu saraksts | Anketu saraksts |
    | Root\\Questionnaire\\Active                                   | Virkne      | Pašreizējais anketas statuss. |
    | Root\\Questionnaire\\Code                                     | Virkne      | Pašreizējais anketas kods. |
    | Root\\Questionnaire\\Description                              | Virkne      | Pašreizējais anketas apraksts. |
    | Root\\Questionnaire\\QuestionnaireType                        | Virkne      | Pašreizējais anketas tips. |
    | Root\\Questionnaire\\QuestionOrder                            | Virkne      | Pašreizējais anketas skaitliskā kārtība. |
    | Root\\Questionnaire\\ResultsGroup                             | Reģistrēt      | Pašreizējie anketas rezultātu parametri. |
    | Root\\Questionnaire\\ResultsGroup\\Code                       | Virkne      | Pašreizējās rezultātu grupas identifikācijas kods. |
    | Root\\Questionnaire\\ResultsGroup\\Description                | Virkne      | Pašreizējais rezultātu grupas apraksts. |
    | Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints          | Reāls        | Maksimālais punktu skaits, ko varētu nopelnīt. |
    | Root\\Questionnaire\\Question                                 | Ierakstu saraksts | Pašreizējās anketas jautājumu saraksts. |
    | Root\\Questionnaire\\Question\\CollectionSequenceNumber       | Vesels skaitlis     | Pašreizējās atbilžu kolekcijas sērijas numurs. |
    | Root\\Questionnaire\\Question\\Id                             | Virkne      | Pašreizējā jautājuma identifikācijas kods. |
    | Root\\Questionnaire\\Question\\MustBeCompleted                | Virkne      | Karodziņš, kas norāda, vai ir jāatbild uz pašreizējo jautājumu. |
    | Root\\Questionnaire\\Question\\PrimaryQuestion                | Virkne      | Karodziņš, kas norāda, vai ir jāatbild uz pašreizējo jautājumu, ir primārs. |
    | Root\\Questionnaire\\Question\\SequenceNumber                 | Vesels skaitlis     | Pašreizējā jautājuma sērijas numurs. |
    | Root\\Questionnaire\\Question\\Text                           | Virkne      | Pašreizējā jautājuma teksts. |
    | Root\\Questionnaire\\Question\\Answer                         | Ierakstu saraksts | Pašreizējā jautājuma atbilžu saraksts. |
    | Root\\Questionnaire\\Question\\Answer\\CorrectAnswer          | Virkne      | Karodziņš, kas norāda, vai pašreizējā atbilde ir pareiza. |
    | Root\\Questionnaire\\Question\\Answer\\Points                 | Reāls        | Punkti, kas ir iegūti, kad ir atlasīta pašreizējā atbilde. |
    | Root\\Questionnaire\\Question\\Answer\\SequenceNumber         | Vesels skaitlis     | Pašreizējās atbildes sērijas numurs. |
    | Root\\Questionnaire\\Question\\Answer\\Text                   | Virkne      | Pašreizējās atbildes teksts. |

    Sekojošajā attēlā ir parādīts pabeigts rediģējamais datu modelis lapā **Datu modeļu noformētājs**.

    ![Konfigurētais datu modelis ER datu modeļu noformētājā.](./media/er-quick-start1-model2.png)

7. Saglabājiet izmaiņas.
8. Aizveriet lapu **Datu modeļa noformētājs**.

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a>Datu modeļa noformējuma pabeigšana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas** konfigurācijas kokā atlasiet **Anketas modelis**.
3. Kopsavilkuma cilnē **Versijas** atlasiet konfigurēto versiju, kuras statuss ir **Melnraksts**.
4. Atlasiet **Mainīt statusu** \> **Pabeigts**.

Šīs konfigurācijas 1. versijas statuss tiek mainīts no **Melnraksta** uz **Pabeigtu**. 1. versiju vairs nevar mainīt. Šī versija satur konfigurēto datu modeli, un to var izmantot kā pamatu citām ER konfigurācijām. Šīs konfigurācijas 2. versija ir izveidota un tās statuss ir **Melnraksts**. Varat rediģēt šo versiju, lai koriģētu **Anketas** datu modeli.

![Rediģējamās konfigurācijas versijas Konfigurāciju lapā.](./media/er-quick-start1-model-configuration.png)

Lai iegūtu vairāk informācijas par versiju izveidi ER konfigurācijām, skatiet [Elektronisko pārskatu (ER) apskatu](general-electronic-reporting.md#component-versioning).

> [!NOTE]
> Konfigurētais datu modelis ir jūsu abstrakta **Anketas** biznesa domēna pārstāvība, un tas neuztur attiecības ar artefaktiem, kas ir raksturīgi Microsoft Dynamics 365 Finance.

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a>Konfigurētā datu modeļa kartēšanas izveidošana

Kā lietotājam Elektroniskajā pārskata izstrādātāja lomā, ir jāizveido jauna ER konfigurācija, kas ietver [modeļa kartēšanas](general-electronic-reporting.md#data-model-and-model-mapping-components) komponentu **Anketas** datu modelim. Tā kā šis komponents implementē konfigurēto datu modeli Finance, tas ir saistīts ar Finance. Ir jākonfigurē modeļa kartēšanas komponents, lai norādītu programmas objektus, kas jāizmanto, lai aizpildītu konfigurēto datu modeli ar programmas datiem izpildlaikā. Lai izpildītu šo uzdevumu, jums jāzina par biznesa domēna **Anketa** datu struktūras ieviešanas detaļām programmā Finance.

Veicot darbības, kas norādītas sekojošajā sadaļā [Importēt jaunu modeļa kartēšanas konfigurāciju](#ImportModelMapping), jūs varat importēt nepieciešamā modeļa kartēšanas konfigurāciju no norādītā XML faila. Vai arī varat veikt darbības, kas aprakstītas sadaļā [Izveidot jaunu modeļa kartēšanas konfigurāciju](#CreateModelMapping), lai izveidotu šo modeļa kartēšanu no jauna.

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a>Jaunas modeļa kartēšanas konfigurācijas importēšana

1. Lejupielādējiet [Anketu mapping.version.1.1.xm](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) failu un saglabājiet to lokālajā datorā.
2. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
3. Darbvietā **Elektroniskie pārskati** atlasiet **Pārskatu veidošanas konfigurācijas**.
4. Darbību rūtī atlasiet **Mainīt** \> **Ielādēt no XML faila**.
5. Atlasiet **Pārlūkot** un pēc tam atrodiet un atlasiet **Anketu mapping.version.1.1.xm** failu.
6. Atlasiet **Labi**, lai importētu konfigurāciju.

Lai turpinātu, izlaidiet nākamo procedūru [Izveidot jaunu modeļa kartēšanas konfigurāciju](#CreateModelMapping).

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a>Jauna modeļa kartēšanas konfigurācijas izveidošana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas** konfigurācijas kokā atlasiet **Anketas modelis**.
3. Atlasiet **Izveidot konfigurāciju**.
4. Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības.

    1. Laukā **Jauns** atlasiet **Uz datu modeļa anketām balstīts modeļa kartējums**.
    2. Laukā **Nosaukums** ievadiet **Anketu kartēšana**.
    3. Laukā **Datu modeļa definīcija** atlasiet **Saknes** definīciju.
    4. Atlasiet **Izveidot konfigurāciju**, lai izveidotu konfigurāciju.

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a>Jaunu modeļa kartēšanas komponentu izveidošana

1. Lapā **Konfigurācijas** konfigurācijas kokā atlasiet **Anketas kartēšana**.
2. Atlasiet **Noformētājs**, lai atvērtu kartējumu sarakstu.
3. Atlasiet **Anketu kartēšanas** kartēšanu, kas tika automātiski pievienota **Saknes** definīcijai
4. Atlasiet **Noformētājs**, lai sāktu konfigurēt atlasīto kartējumu.

**Saknes** definīcijai automātiski tiek pievienota jauna kartēšana. Šim kartējumam ir **Uz modeli** virziens. Tāpēc šo kartējumu var izmantot, lai aizpildītu datu modeli ar nepieciešamajiem datiem.

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a>Datu avotu pievienošana piekļuves pieteikumu tabulām

Datu avoti ir jākonfigurē, lai piekļūtu programmas tabulām, kas ietver informāciju par anketu.

1. Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avotu tipi** atlasiet **Dynamics 365 for Operations\\Tabulas ieraksti**.
2. Pievienojiet jaunu datu avotu, kas tiks izmantots, lai piekļūtu tabulai KMCollection, kur katrs ieraksts pārstāv vienu anketu:

    1. Atlasiet **Pievienot sakni** rūtī **Datu avoti**.
    2. Dialoglodziņa laukā **Nosaukums** ievadiet **Anketa**.
    3. Laukā **Tabula** ievadiet **KMCollection**.
    4. Iestatiet opciju **Jautāt anketu** uz **Jā**. Tad varēsiet norādīt [filtrēšanas](../../fin-ops/get-started/advanced-filtering-query-options.md) opcijas šai tabulai sistēmas vaicājuma dialoglodziņā izpildlaikā.
    5. Atlasiet **Labi**, lai pievienotu jaunu datu avotu.

3. Rūtī **Datu avota tipi** atlasiet **Dynamics 365 for Operations\\Tabulas ieraksti**.
4. Pievienojiet jaunu datu avotu, kas tiks izmantots, lai piekļūtu tabulai KMQuestion, kur katrs ieraksts pārstāv vienu jautājumu anketā:

    1. Atlasiet **Pievienot sakni** rūtī **Datu avoti**.
    2. Dialoglodziņa laukā **Nosaukums** ievadiet **Jautājumu**.
    3. Laukā **Tabula** ievadiet **KMQuestion**.
    4. Atlasiet **Labi**, lai pievienotu jaunu datu avotu.

5. Rūtī **Datu avota tipi** atlasiet **Dynamics 365 for Operations\\Tabulas ieraksti**.
6. Pievienojiet jaunu datu avota mēģinājumu, kas tiks izmantots, lai piekļūtu tabulai KMAnswer, kur katrs ieraksts pārstāv vienu atbildi uz jautājumu anketā:

    1. Atlasiet **Pievienot sakni** rūtī **Datu avoti**.
    2. Laikā **Nosaukums** ievadiet **Atbilde**.
    3. Laukā **Tabula** ievadiet **KMAnswer**.
    4. Atlasiet **Labi**, lai pievienotu jaunu datu avotu.

7. Rūtī **Datu avota tipi** atlasiet **Funkcijas\\Aprēķinātais lauks**.
8. Pievienojiet jaunu aprēķināto lauku, kas tiks izmantots, lai piekļūtu KMQuestionResultGroup tabulas ierakstam no katra pamata KMCollection tabulas ieraksta:

    1. Atlasiet **Pievienot sakni** rūtī **Anketa**.
    2. Atlasiet **Pievienot**.
    3. Dialoglodziņa laukā **Nosaukums** ievadiet **\$ResultGroup**.
    4. Atlasiet **Rediģēt formulu**.
    5. [ER formulas redaktorā](general-electronic-reporting-formula-designer.md), laukā **Formula** ievadiet **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)**, lai tiktu izmantots [ceļš](er-formula-language.md#Paths) no vienas uz daudzām attiecībām starp KMCollection un KMQuestionResultGroup tabulām.
    6. Atlasiet **Saglabāt** un aizveriet formulas redaktoru.
    7. Atlasiet **Labi**, lai pievienotu jaunu aprēķināto lauku.

9. Rūtī **Datu avota tipi** atlasiet **Funkcijas\\Aprēķinātais lauks**.
10. Pievienojiet jaunu aprēķināto lauku, kas tiks izmantots, lai piekļūtu KMQuestion jautājuma ierakstiem no katra pamata KMCollectionQuestion tabulas ieraksta:

    1. Atlasiet **Pievienot sakni** rūtī **Anketa**.
    2. Izvērsiet **\<Relāciju** mezglu, kas satur KMCollection tabulas relāciju viens pret daudziem.
    3. Atlasiet saistīto **KMCollectionQuestion** tabulu un pēc tam atlasiet **Pievienot**.
    4. Dialoglodziņa laukā **Nosaukums** ievadiet **\$Jautājumu**.
    5. Atlasiet **Rediģēt formulu**.
    6. Formulas redaktorā laukā **Formula** ievadiet **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))**, lai atgrieztu attiecīgos jautājumu ierakstus no KMQuestion tabulas.
    7. Atlasiet **Saglabāt** un aizveriet formulas redaktoru.
    8. Atlasiet **Labi**, lai pievienotu jaunu aprēķināto lauku.

11. Rūtī **Datu avota tipi** atlasiet **Funkcijas\\Aprēķinātais lauks**.
12. Pievienojiet jaunu aprēķināto lauku, kas tiks izmantots, lai piekļūtu KMAnswer tabulas atbilžu ierakstiem no katra pamata KMQuestion tabulas ieraksta:

    1. Rūtī **Datu avoti** atlasiet **Questionnaire.\<Relations.KMCollectionQuestion.\$Question** un pēc tam atlasiet **Pievienot**.
    2. Dialoglodziņa laukā **Nosaukums** ievadiet **\$Answer**.
    3. Atlasiet **Rediģēt formulu**.
    4. Formulas redaktorā laukā **Formula** ievadiet **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)**, lai atgrieztu attiecīgos jautājumu ierakstus no KMAnswer tabulas.
    5. Atlasiet **Saglabāt** un aizveriet formulas redaktoru.
    6. Atlasiet **Labi**, lai pievienotu jaunu aprēķināto lauku.

13. Rūtī **Datu avota tipi** atlasiet **Dynamics 365 for Operations\\Tabula**.
14. Pievienojiet jaunu datu avotu, kas tiks izmantots, lai piekļūtu CompanyInfo tabulas metodēm. Ievērojiet, ka šīs tabulas **meklēšanas()** metode atgriež ierakstu, kas pārstāv pašreizējās Finance instances uzņēmumu, ar kuru šī kartēšana tiek izsaukta kontekstā.

    1. Atlasiet **Pievienot sakni** rūtī **Datu avoti**.
    2. Dialoglodziņa laukā **Nosaukums** ievadiet **CompanyInfo**.
    3. Laukā **Tabula** ievadiet **CompanyInfo**.
    4. Atlasiet **Labi**, lai pievienotu jaunu datu avotu.

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a>Datu avotu pievienošana piekļuves pieteikumu uzskaitījumiem

Datu avoti ir jākonfigurē, lai piekļūtu pieteikumu uzskaitījumiem un salīdzinātu to vērtības ar **Numerācijas** tipa lauku vērtībām. Lai aizpildītu attiecīgos datu modeļa laukus, ir jāizmanto salīdzinājuma rezultāts.

1. Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avotu tipi** atlasiet **Dynamics 365 for Operations\\Uzskaitījums**.
2. Pievienojiet jaunu datu avotu, kas tiks izmantots, lai piekļūtu **EnumAppNoYes** uzskaitījuma vērtībām:

    1. Atlasiet **Pievienot sakni** rūtī **Datu avoti**.
    2. Dialoglodziņa laukā **Nosaukums** ievadiet **EnumAppNoYes**.
    3. **Uzskaitījuma** laukā ievadiet **NoYes**.
    4. Atlasiet **Labi**, lai pievienotu jaunu datu avotu.

3. Rūtī **Datu avota tipi** atlasiet **Dynamics 365 for Operations\\Uzskaitījums**.
4. Pievienojiet jaunu datu avotu, kas tiks izmantots, lai piekļūtu **KMCollectionQuestionMode** uzskaitījuma vērtībām:

    1. Atlasiet **Pievienot sakni** rūtī **Datu avoti**.
    2. Dialoglodziņa laukā **Nosaukums** ievadiet **EnumAppQuestionOrder**.
    3. **Uzskaitījuma** laukā ievadiet **KMCollectionQuestionMode**.
    4. Atlasiet **Labi**, lai pievienotu jaunu datu avotu.

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a>ER etiķešu pievienošana, lai ģenerētu pārskatu noteiktā valodā

Varat pievienot ER etiķetes, lai konfigurētu dažus datu avotus, lai atgrieztu vērtības, kas ir atkarīgas no valodas, kas definēta modeļa kartēšanas izsaukuma kontekstā.

1. Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avoti** atlasiet **Atbilde** un tad atlasiet **Rediģēt**.
2. Aktivizējiet lauku **Etiķete**.
3. Atlasiet **Tulkot**.
4. Dialoglodziņā **Teksta tulkojums** veiciet tālāk norādītās darbības:

    1. Laukā **Etiķetes ID** ievadiet **PositiveAnswer**.
    2. Laukā **Teksts noklusējuma valodā** ievadiet **Jā**.
    3. Atlasiet **Tulkot**.
    4. Laukā **Etiķetes ID** ievadiet **NegativeAnswer**.
    5. Laukā **Teksts noklusējuma valodā** ievadiet **Nē**.
    6. Atlasiet **Tulkot**.

5. Aizveriet dialoglodziņu **Teksta tulkojums**.
6. Atlasiet **Atcelt**.

![Pievienot ER etiķetes rediģējamā modeļa kartēšanai.](./media/er-quick-start1-adding-labels.png)

Jūs esat ievadījis tikai noklusējuma valodas ER etiķetes. Lai iegūtu informāciju par to, kā ER etiķetes var tulkot citās valodās, skatiet rakstu [Vairākvalodu pārskati](er-design-multilingual-reports.md).

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a>Datu avotu pievienošana, lai pārveidotu uzskaitījuma vērtību salīdzināšanas rezultātus teksta vērtībā

Tā kā ir jātransformē salīdzinājuma vērtību un teksta vērtību vairāku reižu pārveidošanas rezultāti ar dažādiem avotiem, ir ieteicams konfigurēt šo loģiku kā vienu datu avotu. Tomēr, lai padarītu šo datu avotu atkārtoti izmantojamu, tas ir jākonfigurē kā parametrizēts datu avots. Papildu informāciju skatiet [Atbalsta Aprēķināto lauka tipa ER datu avotu parametru izsaukumus](er-calculated-field-type.md).

1. Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avotu tipi** atlasiet **Vispārīgi\\Tukšs konteiners**.
2. Pievienot jaunu konteinera datu avotu:

    1. Atlasiet **Pievienot sakni** rūtī **Datu avoti**.
    2. Dialoglodziņa laukā **Nosaukums** ievadiet **Palīgs**.
    3. Atlasiet **Labi**, lai pievienotu jaunu konteinera datu avotu.

3. Rūtī **Datu avota tipi** atlasiet **Funkcijas\\Aprēķinātais lauks**.
4. Pievienot jaunu datu avotu:

    1. Rūtī **Datu avoti** atlasiet **Palīgs**.
    2. Atlasiet **Pievienot**.
    3. Dialoglodziņa laukā **Nosaukums** ievadiet **NoYesEnumToString**.
    4. Atlasiet **Rediģēt formulu**.
    5. Formulas redaktorā atlasiet **Parametri**.
    6. Lai precizētu parametrus konfigurētajai izteiksmei, sekojiet šiem soļiem:

        1. Atlasiet **Jauns**.
        2. Dialoglodziņa laukā **Nosaukums** ievadiet **Arguments**.
        3. Laukā **Tips** atlasiet **Būla** datu tipu.
        4. Atlasiet **Labi**.

    7. Laukā **Formula** ievadiet **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** lai atgrieztu attiecīgās ER etiķetes tekstu atkarībā no izpildes konteksta valodas un norādītā parametra vērtības.
    8. Atlasiet **Saglabāt** un aizveriet formulas redaktoru.
    9. Atlasiet **Labi**, lai pievienotu jaunu datu avotu.

![Konfigurētā modeļa kartēšana ER modeļa kartēšanas noformētājā.](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a>Datu avotu saistīšana uz datu modeļa laukiem

Konfigurētie datu avoti ir jāpiesaista datu modeļa laukiem, lai norādītu, kā datu modelis tiks aizpildīts ar programmas datiem izpildlaikā.

1. Lapā **Modeļa kartējuma noformētājs** rūtī **Datu modelis** atlasiet **CompanyName**.
2. Rūtī **Datu avoti** paplašiniet **CompanyInfo** un pēc tam rīkojieties šādi:

    1. Paplašiniet **CompanyInfo.find()** mezglu, kas apzīmē CompanyInfo tabulas **find()** metodi.
    2. Atlasiet **CompanyInfo.find().Name**.
    3. Atlasiet **Saistīt**, lai aizpildītu uzņēmuma nosaukumu, ko konfigurētā modeļa kartēšana izsauc izpildlaika ietvaros.

3. Atlasiet **Anketa** rūtī **Datu modelis**.
4. Rūtī **Datu avoti** atlasiet **Anketa** un tad atlasiet **Saistīt**, lai aizpildītu anketas ierakstus.
5. Rūtī **Datu modelis** paplašiniet **Anketa** un pēc tam rīkojieties šādi:

    1. Atlasiet **Aktīvs** rūtī **Datu modelis**.
    2. Atlasiet **Rediģēt** rūtī **Datu modelis**.
    3. Laukā **Formula** ievadiet **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** lai aizpildītu no teksta atkarīgu un no valodas atkarīgu rezultātu salīdzinājumā starp uzskaitījuma vērtībām.

6. Turpiniet saistīt datu avotus ar datu modeļa laukiem tādā pašā veidā, līdz tiek sasniegts šāds rezultāts.

    | Lauka ceļš                                              | Datu tips   | Darbība | Saistīšanas izteiksme |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | CompanyName                                             | Virkne      | Saistīt   | CompanyInfo.'find()'.Name |
    | Anketa                                           | Ierakstu saraksts | Saistīt   | Anketa |
    | Questionnaire\\Active                                   | Virkne      | Labot   | Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes) |
    | Questionnaire\\Code                                     | Virkne      | Saistīt   | \@.kmCollectionId |
    | Questionnaire\\Description                              | Virkne      | Saistīt   | \@.Description |
    | Questionnaire\\QuestionnaireType                        | Virkne      | Saistīt   | \@.'&gt;Relations'.kmCollectionTypeId.Description |
    | Questionnaire\\QuestionOrder                            | Virkne      | Labot   | CASE (\@.questionMode,<br>EnumAppQuestionOrder.Conditional, "Conditional",<br>EnumAppQuestionOrder.Random, "Random (procentuāli anketā)",<br>EnumAppQuestionOrder.RandomGroup, "Random (procentuāli rezultāti grupās)",<br>EnumAppQuestionOrder.Sequence, "Sequential",<br>"") |
    | Questionnaire\\ResultsGroup                             | Reģistrēt      |        | |
    | Questionnaire\\ResultsGroup\\Code                       | Virkne      | Saistīt   | \@.'\$ResultGroup'.kmQuestionResultGroupId |
    | Questionnaire\\ResultsGroup\\Description                | Virkne      | Saistīt   | \@.'\$ResultGroup'.description |
    | Questionnaire\\ResultsGroup\\MaxNumberOfPoints          | Reāls        | Saistīt   | \@.'\$ResultGroup'.maxPoint |
    | Questionnaire\\Question                                 | Ierakstu saraksts | Saistīt   | \@.'&lt;Relations'.KMCollectionQuestion |
    | Questionnaire\\Question\\CollectionSequenceNumber       | Vesels skaitlis     | Saistīt   | \@.answerCollectionSequenceNumber |
    | Questionnaire\\Question\\Id                             | Virkne      | Saistīt   | \@.kmQuestionId |
    | Questionnaire\\Question\\MustBeCompleted                | Virkne      | Labot   | Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes) |
    | Questionnaire\\Question\\PrimaryQuestion                | Virkne      | Saistīt   | \@.parentQuestionId |
    | Questionnaire\\Question\\SequenceNumber                 | Vesels skaitlis     | Saistīt   | \@.SequenceNumber |
    | Questionnaire\\Question\\Text                           | Virkne      | Saistīt   | \@.'\$Question'.text |
    | Questionnaire\\Question\\Answer                         | Ierakstu saraksts | Saistīt   | \@.'\$Question'.'\$Answer' |
    | Questionnaire\\Question\\Answer\\CorrectAnswer          | Virkne      | Labot   | Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes) |
    | Questionnaire\\Question\\Answer\\Points                 | Reāls        | Saistīt   | \@.point |
    | Questionnaire\\Question\\Answer\\SequenceNumber         | Vesels skaitlis     | Saistīt   | \@.sequenceNumber |
    | Questionnaire\\Question\\Answer\\Text                   | Virkne      | Saistīt   | \@.text |

    Sekojošajā attēlā redzama konfigurētā modeļa kartēšanas pēdējais stāvoklis **Modeļa kartēšanas veidotāja** lapā.

    ![Pilnībā konfigurētā modeļa kartēšana ER modeļa kartēšanas noformētājā.](./media/er-quick-start1-mapping2.png)

7. Saglabājiet izmaiņas.
8. Aizveriet lapu **Modeļa kartējuma noformētājs**.

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a>Modeļa kartēšanas noformējuma pabeigšana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas** konfigurācijas kokā atlasiet **Anketas kartēšana**.
3. Kopsavilkuma cilnē **Versijas** atlasiet konfigurēto versiju, kuras statuss ir **Melnraksts**.
4. Atlasiet **Mainīt statusu** \> **Pabeigts**.

Šīs konfigurācijas 1.1. versijas statuss tiek mainīts no **Melnraksta** uz **Pabeigtu**. 1.1. versiju vairs nevar mainīt. Šī versija satur konfigurēto modeļa kartēšanu, un to var izmantot kā pamatu citām ER konfigurācijām. Šīs konfigurācijas 1.2. versija ir izveidota un tās statuss ir **Melnraksts**. Varat rediģēt šo versiju, lai koriģētu **Anketas kartēšanas** konfigurāciju.

![Rediģējamās ER konfigurācijas versijas Konfigurāciju lapā.](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> Konfigurētā modeļa kartēšana ir jūsu Finance specifiska abstraktā datu modeļa implementēšana, kas pārstāv **Anketas** biznesa domēnu.

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a>Veidnes izveide pielāgotam pārskatam

EP struktūra izmanto iepriekš definētas veidnes, lai ģenerētu pārskatus Microsoft Office formātos (Excel darbgrāmatas vai Word dokumentus). Kamēr tiek ģenerēts pieprasītais pārskats, veidne tiek aizpildīta ar nepieciešamajiem datiem atbilstoši konfigurētajām darbplūsmas. Tāpēc vispirms ir jāizveido jūsu pielāgotā pārskata veidne. Šī veidne ir jāveido kā Excel darbgrāmata, kuras struktūra ir pielāgota pārskata izkārtojums. Jums jāpiešķir nosaukums katram Excel vienumam, ko plānojat aizpildīt ar nepieciešamajiem datiem.

1. Lejupielādējiet [Anketu report template.xlsx](https://download.microsoft.com/download/3/8/2/382c3cf0-87bb-473f-b7bb-3015b4facb74/Questionnaires_report_template.xlsx) failu un saglabājiet to lokālajā datorā.
2. Atveriet failu programmā Excel un pārskatiet darbgrāmatas struktūru.

Kā redzams sekojošajā attēlā, lejupielādētā veidne ir izstrādāta, lai izdrukātu norādītās anketas, kas sniedz anketas jautājumus kopā ar atbilstošajām atbildēm.

![Excel veidne, lai izdrukātu norādītās anketas.](./media/er-quick-start1-template-layout.png)

Lai aizpildītu anketu detaļas, šai veidnei ir pievienoti Excel nosaukumi. Varat izmantot Nosaukumu pārvaldnieku, lai pārskatītu Excel nosaukumus.

![Izmantot Nosaukumu pārvaldnieku, lai pārskatītu Excel nosaukumus norādītajā Excel veidnē.](./media/er-quick-start1-template-names.png)

Angļu valodas pārskata etiķetes ir pievienotas kā fiksēts teksts. Varat aizstāt pārskata etiķetes ar jaunajiem Excel nosaukumiem, kas aizpilda etiķetes ar no valodas atkarīgu tekstu, izmantojot ER formāta [etiķetes](#AddMmLabels), kā tas tika paveikts valodu pārdomātām izteiksmēm konfigurētajā modeļa kartēšanā. Šajā gadījumā ER etiķetes ir jāpievieno rediģējamā ER formātā.

Kā redzams sekojošajā attēlā, pielāgotas atskaites galvene ir norādīta, lai iespējotu Excel veikt lapošanu.

![Pielāgots pārskata virsraksts norādītajā Excel veidnē.](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a>Formāta veidošana

Kā lietotājs Elektroniskās ziņošanas funkcionālā konsultanta lomā jums ir jāizveido jauna ER konfigurācija, kas ietver [formāta](general-electronic-reporting.md#FormatComponentOutbound) komponentu. Ir jākonfigurē formāta komponents, lai norādītu, kā pārskata veidne tiks aizpildīta ar nepieciešamajiem datiem izpildlaikā.

Veicot darbības, kas norādītas sadaļā [Importēt izveidotā formāta konfigurāciju](#FormatImport), jūs varat importēt nepieciešamo formātu no norādītā XML faila. Vai arī varat veikt darbības, kas aprakstītas sadaļā [Izveidot jaunu formāta konfigurāciju](#FormatCreate), lai izveidotu šo formātu no jauna.

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a>Izstrādātā formāta konfigurācijas importēšana

1. Lejupielādējiet [Anketu format.version.1.1.xm](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) failu un saglabājiet to lokālajā datorā.
2. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
3. Darbvietā **Elektroniskie pārskati** atlasiet **Pārskatu veidošanas konfigurācijas**.
4. Darbību rūtī atlasiet **Mainīt** \> **Ielādēt no XML faila**.
5. Atlasiet **Pārlūkot** un pēc tam atrodiet un atlasiet **Anketu format.version.1.1.xm** failu.
6. Atlasiet **Labi**, lai importētu konfigurāciju.

Lai turpinātu, izlaidiet nākamo procedūru [Izveidot jaunu formāta konfigurāciju](#FormatCreate).

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a>Jaunas formāta konfigurācijas izveide
 
1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas** konfigurācijas kokā atlasiet **Anketas modelis**.
3. Atlasiet **Izveidot konfigurāciju**.
4. Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības.

    1. Laukā **Jauns** atlasiet **Uz datu modeļa anketām balstīts formāts**.
    2. Laukā **Nosaukums** ievadiet **Anketu pārskats**.
    3. Laukā **Datu modeļa versija** atlasiet **1**.

        > [!NOTE]
        > - Ja jūs atlasāt noteiktu pamatdatu modeļa versiju, atbilstošā datu modeļa sistēmas struktūra tiks parādīta kā **Modeļa** datu avota struktūra izveidotajā formātā.
        > - Jūs varat atstāt šo lauku tukšu. Šādā gadījumā datu modeļa **Melnraksta** versijas struktūra tiks attēlota kā **Modeļa** datu avota struktūra izveidotajā formātā. Pēc tam varat koriģēt modeli un uzreiz redzēt šos pielāgojumus jūsu formātā. Šī pieeja varētu uzlabot ER risinājuma dizaina efektivitāti, konfigurējot datu modeli, modeļa kartēšanu un formātu vienlaicīgi.
        > - Ja atlasāt noteiktu pamatdatu modeļa versiju, varat vēlāk pārslēgt to uz **Melnraksta** versiju.

    4. Laukā **Datu modeļa definīcija** atlasiet **Saknes** definīciju.

5. Atlasiet **Izveidot konfigurāciju**, lai izveidotu konfigurāciju.

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a>Pārskata veidnes importēšana

1. Lapā **Konfigurācijas** konfigurācijas kokā atlasiet **Anketas pārskats**.
2. Atlasiet **Noformētājs**, lai sāktu pielāgotā formāta konfigurēšanu.
3. Lapā **Formāta noformētājs**, darbību rūtī atlasiet **Importēt** \> **Importēt no Excel**.
4. NDialoglodziņā veiciet tālāk norādītās darbības:

    1. Atlasiet **Pievienot veidni**.
    2. Meklējiet un atlasiet lokāli saglabāto **Anketu pārskata template.xslx** failu un pēc tam atlasiet **Atvērt**.
    3. Atlasiet **Labi**, lai importētu veidni.

    ![Pārskata veidnes importēšana.](./media/er-quick-start1-template-import.png)

**Excel\\File** formāta elements tiek automātiski pievienots rediģējamam formātam kā saknes elements. Turklāt **Excel\\Range** formāta elements vai **Excel\\Cell** formāta elements tiek automātiski pievienots katram importētās veidnes atpazītajam Excel nosaukumam. **Excel\\Header** formāts, kas ietver ligzdotu **Virknes** elementu, tiek automātiski pievienots, lai atspoguļotu importētās veidnes virsraksta iestatījumus.

![Formatēt struktūru, kas ietver automātiski pievienotos elementus ER operāciju rīkā.](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a>Formāta konfigurēšana

1. Lapā **Formāta veidotājs** formatēšanas kokā atlasiet **Excel** saknes elementu.
2. Cilnē **Formāts**, kas atrodas lapas labajā pusē, laukā **Nosaukums** ievadiet <a name="AddFormatRootElement"></a>**Pārskats**.
3. Laukā **Valodas izvēle** atlasiet **Lietotāja preference**, lai palaistu pārskatu lietotāja vēlamajā valodā.
4. Laukā **Kultūras izvēle** atlasiet **Lietotāja preference**, lai palaistu pārskatu lietotāja vēlamajā kultūrā.

    Informāciju par to, kā noteikt valodas un kultūras kontekstu ER procesam, skatiet šeit: [Vairākvalodu pārskatu noformēšana](er-design-multilingual-reports.md).

    ![Valodas un kultūras iestatījumu konfigurēšana plānotajam pārskatam ER operāciju veidotājā.](./media/er-quick-start1-template-format-structure1.png)

5. Formatēšanas kokā izvērsiet saknes mezglu un pēc tam atlasiet **ResultsGroup**.
6. Cilnē **Formāts** laukā **Replicēšanas virziens** atlasiet **Nav replikācijas**, jo nav paredzēts, ka vienai anketai ir vairākas rezultātu grupas.

    ![Definēt replicēšanas virzienu diapazona formāta elementiem, kas atrodas ER operāciju veidotājā.](./media/er-quick-start1-template-format-structure2.png)

7. Atlasiet **Saglabāt**.

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a>Pārskata nosaukuma datu saistījumu definēšana

Ir jānorāda datu saistījums formāta elementam, kas tiek izmantots, lai aizpildītu ģenerētā pārskata nosaukumu.

1. Lapas **Formāta noformētājs** labās puses cilnē **Kartēšana** atlasiet **Report\\ReportTitle** elementu.
2. Atlasiet **Rediģēt formulu**.
3. Formulas redaktorā atlasiet **Tulkot**.
4. Dialoglodziņā **Teksta tulkojums** veiciet tālāk norādītās darbības:

    1. Laukā **Etiķetes ID** ievadiet **ReportTitle**.
    2. Laukā **Teksts noklusējuma valodā** ievadiet **Aptaujas pārskats**.
    3. Atlasiet **Tulkot** un pēc tam **Saglabāt**.
    4. Atlasiet **Tulkot**, lai aizvērtu **Teksta tulkojuma** dialoglodziņu.

5. Aizveriet formulas redaktoru.

    ![Saistījuma konfigurēšana, lai aizpildītu ģenerētā pārskata nosaukumu.](./media/er-quick-start1-add-report-title-label.png)

Varat izmantot šo metodi, lai visas pārējās pašreizējās veidnes etiķetes būtu atkarīgas no valodas. Lai iegūtu informāciju par to, kā vienas ER konfigurācijas pievienotās etiķetes var tulkot visās atbalstītajās valodās, skatiet rakstu [Daudzvalodu pārskatu izveide](er-design-multilingual-reports.md).

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a>Modeļa datu avota pārskatīšana

1. Lapā **Formāta veidotājs** cilnē **Kartēšana** atlasiet <a name="ModelDSName"></a>**modeļa** datu avotu, kas apzīmē šī ER formāta pamata datu modeli.
2. Atlasiet **Rediģēt**.
3. Pārskatiet informāciju dialoglodziņā **Datu avota rekvizīti**. Šis datu avots pārstāv **Anketu** datu modeļa komponenta 1. versiju, kas atrodas **Anketu modeļa** ER konfigurācijā.

![Rekvizīti par modeļa datu avotu ER operāciju noformētājā.](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a>Formāta elementu saistīšana ar datu avotu laukiem

Lai norādītu, kā tiek aizpildīta veidne izpildlaikā, ir jāpiesaista katrs formāta elements, kas ir saistīts ar atbilstošu Excel nosaukumu atsevišķam šī formāta datu avota laukam.

1. Lapā **Formāta veidotājs** formatēšanas kokā atlasiet **Report\\CompanyName** formāta elementu.
2. Cilnē **Kartēšana** atlasiet **model.CompanyName** **Virknes** tipa datu avota lauku.
3. Atlasiet **Saistīt**, lai ievadītu uzņēmuma nosaukumu veidnē.
4. Formāta kokā atlasiet **Report\\Questionnaire** elementu.
5. Cilnē **Kartēšana** atlasiet **model.Questionnaire** **Ieraksta saraksta** tipa datu avota lauku.
6. Atlasiet **Saistīt**.
7. Atlasiet **Rādīt detaļas**, lai skatītu plašāku informāciju par formāta elementiem.

    **Anketas** diapazona formāta elements ir konfigurēts kā vertikāli replicēts. Kad tas ir piesaistīts datu avotam ar **Ierakstu saraksta** tipu, atbilstošais Excel veidnes **Anketu** diapazons tiek atkārtots katram saistītā datu avota ierakstam.
 
    ![Anketu diapazona formāta elementu saistīšana ar atbilstošajiem Ierakstu saraksta datu avotiem ER operāciju veidotājā.](./media/er-quick-start1-bindings1.png)

    Tā kā Excel veidnes **Anketu** diapazons ir definēts no 5. līdz 14. rindai, šīs rindas tiek atkārtotas katrai pārskatā iekļautajai anketai.

    ![Rindas Excel veidnē, kas tiks atkārtotas ģenerētajā pārskatā katram Ierakstu saraksta datu avotu ierakstam.](./media/er-quick-start1-template-questionnaire-range.png)

8. Konfigurējiet līdzīgus saistījumus atlikušajiem formāta elementiem, kā aprakstīts šajā tabulā.

    > [!NOTE]
    > Šajā tabulā informācija kolonnā "Datu avota ceļš" tiek pieņemts, ka [relatīvā ceļa](relative-path-data-bindings-er-models-format.md) ER funkcija ir ieslēgta.

    | Formatēt elementa ceļu                                      | Datu avota ceļš |
    |----------------------------------------------------------|------------------|
    | Excel\\ReportTitle                                       | **\@"GER\_LABEL:ReportTitle"** |
    | Excel\\CompanyName                                       | **model.CompanyName** |
    | Excel\\Questionnaire                                     | **model.Questionnaire** |
    | Excel\\Questionnaire\\Active                             | **\@.Active**, kur **\@** ir **model.Questionnaire** |
    | Excel\\Questionnaire\\Code                               | **\@.Code** |
    | Excel\\Questionnaire\\Description                        | **\@.Description** |
    | Excel\\Questionnaire\\QuestionnaireType                  | **\@.QuestionnaireType** |
    | Excel\\Questionnaire\\QuestionOrder                      | **\@.QuestionOrder** |
    | Excel\\Questionnaire\\ResultsGroup\\Code\_               | **\@.ResultsGroup.Code** |
    | Excel\\Questionnaire\\ResultsGroup\\Description\_        | **\@.ResultsGroup.Description** |
    | Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints    | **\@.ResultsGroup.MaxNumberOfPoint** |
    | Excel\\Questionnaire\\Question                           | **\@.Question** |
    | Excel\\Questionnaire\\Question\\CollectionSequenceNumber | **\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question** |
    | Excel\\Questionnaire\\Question\\Id                       | **\@.Id** |
    | Excel\\Questionnaire\\Question\\MustBeCompleted          | **\@.MustBeCompleted** |
    | Excel\\Questionnaire\\Question\\PrimaryQuestion          | **\@.PrimaryQuestion** |
    | Excel\\Questionnaire\\Question\\SequenceNumber           | **\@.SequenceNumber** |
    | Excel\\Questionnaire\\Question\\Text                     | **\@.Text** |
    | Excel\\Questionnaire\\Question\\Answer                   | **\@.Answer** |
    | Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer    | **\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer** |
    | Excel\\Questionnaire\\Question\\Answer\\Points           | **\@.Points** |
    | Excel\\Questionnaire\\Question\\Answer\\Text             | **\@.Text** |

9. Pēc pabeigšanas atlasiet **Saglabāt**.

Sekojošajā attēlā redzama konfigurētās datu saistīšanas pēdējais stāvoklis **Formāta veidotāja** lapā.

![Konfigurētie datu saistījumi ER operāciju noformētājā.](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> Visu norādīto datu avotu un saistījumu kolekcija attēlo konfigurētā formāta kartējuma komponentu. Šī formāta kartēšana tiek izsaukta, palaižot konfigurēto formātu pārskata ģenerēšanai.

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a>Izveidoto formātu palaišana no ER

Tagad ir iespējams palaist noformētu formātu testēšanas nolūkiem no **Konfigurāciju** lapas.

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācija**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Aptaujas modelis** un pēc tam atlasiet **Aptaujas pārskats**.
3. Izvēlieties **Noformētāju** formāta versijai ar statusu **Melnraksts**.
4. Lapā **Formāta veidotājs** atlasiet **Palaist**.
5. Dialoglodziņā **ER parametri** kopsavilkuma cilnē **Ierakstus, ko iekļaut** konfigurējiet filtrēšanas opciju, lai tiktu iekļauta tikai **SBCCrsExam** anketa.
6. Lai apstiprinātu filtrēšanas opciju, atlasiet **Labi**.
7. Atlasiet **Labi**, lai palaistu pārskatu.
8. Pārskatiet ģenerēto pārskatu.

Pēc [noklusējuma](electronic-reporting-destinations.md#default-behavior) ģenerētais pārskats tiek piegādāts kā Excel fails, ko var lejupielādēt. Šajā ilustrācijā ir parādītas divas ģenerētā pārskata lapas Excel formātā.

![Ģenerētā pārskata piemērs Excel formātā, 1. lpp.](./media/er-quick-start1-report1a.png)

![Ģenerētā pārskata piemērs Excel formātā, 2. lpp.](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a>Izveidotā formāta noskaņošana

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a>Formātu modificēšana, lai mainītu ģenerētā dokumenta nosaukumu

Pēc noklusējuma ģenerētais dokuments tiek nosaukts, izmantojot pašreizējā lietotāja aizstājvārdu. Modificējot formātu, varat mainīt šo darbību tā, lai ģenerētais dokuments tiktu nosaukts, pamatojoties uz jūsu pielāgoto loģiku. Piemēram, ģenerētā dokumenta nosaukums var pamatoties uz pašreizējo sesijas datumu un laiku, kā arī uz pārskata nosaukumu.

1. Lapā **Formāta veidotājs** atlasiet saknes krājumu **Pārskats**.
2. Cilnē **Kartēšana** atlasiet **Rediģēt faila nosaukumu**.
3. Laukā **Formula** ievadiet **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.
4. Atlasiet **Saglabāt** un aizveriet formulas redaktoru.
5. Atlasiet **Saglabāt**.

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a>Formātu modificēšana, lai mainītu jautājumu secību

Jautājumi nav pareizi sakārtoti ģenerētajā pārskatā. Varat mainīt secību, modificējot formātu.

1. Lapā **Formāta veidotājs** atlasiet saknes krājumu **Pārskats**.
2. Cilnē **Kartēšana** formatēšanas kokā izvērsiet **Pārskats\\Aptauja\\Jautājums**.

    ![Diapazona tipa jautājuma formāta elements ER operāciju veidotājā.](./media/er-quick-start1-bindings3.png)

3. Cilnē **Kartēšana** atlasiet **model.Questionnaire**.
4. Atlasiet **Pievienot** \> **Funkcijas\\Aprēķinātais lauks** un pēc tam laukā **Nosaukums** ievadiet **OrderedQuestions**.
5. Atlasiet **Rediģēt formulu**.
6. Formulas redaktorā laukā **Formula** ievadiet **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)**, lai numurētu pašreizējās anketas jautājumu sarakstu pēc secības pasūtījuma numura.
7. Atlasiet **Saglabāt** un aizveriet formulas redaktoru.
8. Atlasiet **Labi**, lai pabeigtu jauna aprēķinātā lauka ievadi.
9. Cilnē **Kartēšana** atlasiet **model.Questionnaire.OrderedQuestions**.
10. Formatēšanas kokā atlasiet **Excel\\Aptauja\\Jautājums**.
11. Atlasiet **Saistīt** un tad apstipriniet, ka pašreizējais **model.Questionnaire.Questions** ceļš ir aizstāts ar jauno **model.Questionnaire.OrderedQuestions** ceļu visos ligzdoto elementu saistījumos.
12. Atlasiet **Saglabāt**.

![Jautājuma formāta elementu saistīšana ar konfigurēto OrderedQuestions datu avotu, kas atrodas ER operāciju veidotājā.](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a>Modificēto formātu palaišana no ER

Tagad varat izmantot modificēto formātu testēšanas nolūkiem no ER struktūras.

1. Lapā **Formāta veidotājs** atlasiet **Palaist**.
2. Dialoglodziņā **ER parametri** kopsavilkuma cilnē **Ierakstus, ko iekļaut** konfigurējiet filtrēšanas opciju, lai tiktu iekļauta tikai **SBCCrsExam** anketa.
3. Lai apstiprinātu filtrēšanas opciju, atlasiet **Labi**.
4. Atlasiet **Labi**, lai palaistu pārskatu.
5. Pārskatiet ģenerēto pārskatu.

Sekojošajā attēlā redzams ģenerētais pārskats Excel formātā, kur jautājumi ir pareizi sakārtoti.

![Ģenerētais pārskats Excel formātā, kur ir pareizi sakārtoti jautājumi.](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a>Formāta noformējuma pabeigšana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Aptaujas modelis** un pēc tam atlasiet **Aptaujas pārskats**.
3. Kopsavilkuma cilnē **Versijas** atlasiet konfigurēto versiju, kuras statuss ir **Melnraksts**.
4. Atlasiet **Mainīt statusu** \> **Pabeigts**.

Šīs konfigurācijas 1.1. versijas statuss tiek mainīts no **Melnraksta** uz **Pabeigtu**. 1.1. versiju vairs nevar mainīt. Šajā versijā ir konfigurēts formāts, un to var izmantot, lai izdrukātu jūsu pielāgoto pārskatu. Šīs konfigurācijas 1.2. versija ir izveidota un tās statuss ir **Melnraksts**. Varat rediģēt šo versiju, lai koriģētu jūsu **Anketas** pārskata formātu.

![Rediģējamās ER konfigurācijas Konfigurāciju lapā.](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> Konfigurētais formāts ir jūsu **Anketas** pārskata noformējums, un tas nesatur attiecības ar Finance saistītiem artefaktiem.

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a>Pieteikumu artefaktu izstrādāšana, lai izsauktu paredzēto pārskatu

Kā lietotājam lomā Sistēmas administrators, jums ir jāizstrādā jauna loģika, lai konfigurēto ER formātu varētu izsaukt no lietojumprogrammas lietotāja interfeisa (UI), lai ģenerētu pielāgoto pārskatu. Pašlaik ER nepiedāvā nekādu iespēju konfigurēt šāda veida loģiku. Tāpēc ir nepieciešams atsevišķs tehniskais darbs. 

Lai attīstītu jaunu loģiku, jums jāizvieto topoloģija, kas atbalsta pastāvīgu būvēšanu. Papildinformāciju skatiet tēmā [Tādu topoloģiju izvietošana, kuras atbalsta pastāvīgu būvēšanu un testu automatizēšanu](../perf-test/continuous-build-test-automation.md). Jums jābūt arī piekļuvei šīs topoloģijas izstrādes videi. Papildinformāciju par pieejamo ER API skatiet sadaļā [ER struktūras API](er-apis-app73.md).

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a>Pirmkoda modificēšana

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a>Datu līguma klases pievienošana

Pievienojiet jaunu **QuestionnairesErReportContract** klasi savam Microsoft Visual Studio projektam un ierakstiet kodu, kas norāda datu līgumu, kas jāizmanto, lai darbinātu konfigurēto ER formātu.

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a>UI veidotāja klases pievienošana

Pievienojiet jaunu **QuestionnairesErReportUIBuilder** klasi jūsu Visual Studio projektam un ierakstiet kodu, lai ģenerētu izpildlaika dialoglodziņu, kas tiks izmantots, lai uzmeklētu ER formāta kartējuma ID, kas ir jāpalaiž. Norādītais kods meklē tikai ER formātus, kas satur **Datu modeļa** tipa datu avotu, kas attiecas uz **[Anketu](#DataModeName)** datu modeli, izmantojot **[Saknes](#RootDefinitionName)** definīciju.

> [!NOTE]
> Varat arī izmantot ER integrācijas punktus, lai filtrētu ER formātus. Plašāku informāciju skatiet [API, lai parādītu formāta kartēšanas uzmeklēšanu](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a>Datu nodrošinātāja klases pievienošana

Pievienojiet jaunu **QuestionnairesErReportDP** klasi savam Microsoft Visual Studio projektam un ierakstiet kodu, kas iepazīstina datu nodrošinātāju, kas jāizmanto, lai darbinātu konfigurēto ER formātu. Norādītais kods ietver tikai datu līgumu šim datu nodrošinātājam.

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a>Etiķešu faila pievienošana

Pievienojiet jaunajam **QuestionnairesErReportLabels\_en-US** etiķešu failu jūsu Visual Studio projektam un precizējiet sekojošās etiķetes jaunajiem UI resursiem:

- **\@QuestionnairesReport** etiķete jaunajam izvēlnes krājumam, kas satur sekojošo tekstu angļu valodā (en-US): **Aptauju pārskats (darbina ER)**
- **\@QuestionnairesReportBatchJobDescription** etiķete pakešuzdevuma nosaukumam, ja atlasītais ER formāts ir plānots izpildei kā pakešuzdevums

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a>Pārskata pakalpojumu klases pievienošana

Pievienojiet jaunu **QuestionnairesErReportService** klasi jūsu Visual Studio projektam un rakstāt kodu, kas izsauc ER formātu identificē to ar formāta kartēšanas ID un nodrošina datu līgumu kā parametru.

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

Kad jāizmanto ER formāts, kas palaiž programmas datus, ir jākonfigurē **Datu modeļa** tipa datu avots formāta kartēšanā. Šis datu avots attiecas uz specifisku noteikta datu modeļa daļu, izmantojot vienu saknes definīciju. Kad ER formāts ir palaists, to sauc par šo datu avotu, lai piekļūtu atbilstošajai ER modeļa kartēšanai, kas ir konfigurēta dotajam modelim un saknes definīcijai.

Visu informāciju, ko jūs varētu sagatavot pirmkodā un saglabāt kā daļu no datu līguma, var nodot uz palaisto ER formātu, izmantojot šāda veida ER modeļa kartēšanu. ER modeļa kartēšanai ir jākonfigurē **Objekta** tipa datu avots, kas attiecas uz **[QuestionnairesErReportContract](#DataContractClass)** klasi. Lai identificētu modeļa kartēšanu, jānorāda datu avots, kas izsauc šo modeļa kartēšanu. Nodrošinātāja kodā šis datu avots, ko norādījis **ERModelDataSourceName** konstants, kuram ir **[modeļa](#ModelDSName)** vērtība. Lai noteiktu, kurš datu avots tiek izmantots datu līguma atklāšanai modeļa kartēšanā, jānorāda datu avota nosaukums. Nodrošinātāja kodā šis nosaukums, ko norādījis **ParametersDataSourceName** konstants, kuram ir <a name="DataContractDSName"></a>**RunTimeParameters** vērtība.

> [!NOTE]
> Jaunā vidē var būt nepieciešams atsvaidzināt ER metadatus, lai šis klases veids būtu pieejams ER modeļu kartēšanas veidotājā. Papildinformāciju skatiet tēmā [ER struktūras konfigurēšana](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a>Pārskata kontrolētāja klases pievienošana

Pievienojiet projektam jaunu **QuestionnairesErReportController** klasi jūsu Visual Studio projektam un ierakstiet kodu, kas palaiž ER formātu sinhronajā režīmā vai partijas režīmā, kā vēlaties, dialoglodziņā, kas tiek veidots, pamatojoties uz nodrošinātās **QuestionnairesErReportUIBuilder** klasi.

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a>Izvēlnes elementa pievienošana

Pievienojiet jūsu Visual Studio projektam jaunu **QuestionnairesErReport** izvēlnes elementu. **Objekta** rekvizītā šis izvēlnes elements attiecas uz **QuestionnairesErReportController** klasi, un to izmanto, lai norādītu lietotāja atļauju atlasīt un palaist ER formātu. **Etiķetes** rekvizītā šis izvēlnes elements attiecas uz **\@QuestionnairesReport** etiķeti, ko jūs iepriekš izveidojāt, lai pareizais teksts tiktu parādīts programmā UI.

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a>Izvēlnes krājuma pievienošana izvēlnei

Pievienojiet projektam esošu **KM** izvēlni jūsu Visual Studio projektam. Šai izvēlnei ir jāpievieno jauns **Izejošā** tipa **QuestionnairesErReport** krājums izvēlnei. Šim krājumam ir jāattiecas uz **QuestionnairesErReport** izvēlnes elementu, kas aprakstīts iepriekšējā sadaļā.

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a>Izveidot Visual Studio projektu

Izveidojiet savu projektu, lai jaunais izvēlnes elements būtu pieejams lietotājiem.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a>Formāta palaišana no programmas

1. Dodieties uz **Aptauja** \> **Noformējums** \> **Aptauju pārskats (darbina ER)**.

    ![Atlasot Anketu pārskata (darbina ER) izvēlnes krājumu Anketas modulī, lai palaistu konfigurēto ER formātu.](./media/er-quick-start1-application-menu-modified.png)

2. Dialoglodziņā **Formāta kartēšana** atlasiet **Anketu pārskats**.
3. Atlasiet **Labi**.
4. Dialoglodziņā **Elektronisko pārskatu parametri** kopsavilkuma cilnē **Ierakstus, ko iekļaut** konfigurējiet filtrēšanas opciju, lai tiktu iekļauta tikai **SBCCrsExam** anketa.
5. Lai apstiprinātu filtrēšanas opciju, atlasiet **Labi**.
6. Atlasiet **Labi**, lai palaistu pārskatu.

    ![Dialoglodziņā Elektroniskais pārskats norādiet atlases kritērijus.](./media/er-quick-start1-report-run-dialog-page.png)

7. Pārskatiet ģenerēto pārskatu.

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a>Izstrādāta ER risinājuma noregulēšana

Varat modificēt konfigurēto ER risinājumu tā, lai tas izmantotu datu nodrošinātāju klasi, ko izstrādājāt, lai piekļūtu informācijai par darbojošos ER formātu, un tā, lai tā ievadītu šī ER formāta nosaukumu ģenerētajā pārskatā.

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a>Modeļa kartējuma modificēšana

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a>Datu avotu pievienošana piekļuves datu līguma objektam

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Aptaujas modelis** un pēc tam atlasiet **Aptaujas kartēšana**.
3. Atlasiet **Noformētājs**, lai atvērtu **Modelis datu avota kartēšanas** lapu.
4. Atlasiet **Noformētājs**, lai atvērtu atlasīto kartējumu modeļa kartēšanas veidotājā.
5. Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avotu tipi** atlasiet **Dynamics 365 for Operations\\Objekts**.
6. Atlasiet **Pievienot sakni** rūtī **Datu avoti**.
7. Dialoglodziņā **Nosaukums** ievadiet **[RunTimeParameters](#DataContractDSName)**, kā definēts **QuestionnairesErReportService** klases pirmkodā.
8. Laukā **Klase** ievadiet **[QuestionnairesErReportContract](#DataContractClass)**, kas tika iepriekš kodēts.
9. Atlasiet **Labi**.
10. Izvērst **RunTimeParameters**.

Pievienotais datu avots sniedz informāciju par palaisto ER formāta kartēšanas ieraksta ID.

![Pievienots datu avots ER modeļu kartēšanas veidotājā.](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a>Datu avota pievienošana, lai piekļūtu ER formāta kartēšanas ierakstiem

Turpiniet rediģēt atlasīto modeļa kartēšanu, pievienojot datu avotu, lai piekļūtu ER formāta kartēšanas ierakstiem.

1. Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avotu tipi** atlasiet **Dynamics 365 for Operations\\Tabulas ieraksti**.
2. Atlasiet **Pievienot sakni** rūtī **Datu avoti**.
3. Dialoglodziņa laukā **Nosaukums** ievadiet **ER1**.
4. Laukā **Tabula** ievadiet **ERFormatMappingTable**.
5. Atlasiet **Labi**.

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a>Datu avota pievienošana, lai piekļūtu tekošā ER formāta kartēšanas ierakstam

Turpiniet rediģēt atlasīto modeļa kartēšanu, pievienojot datu avotu, lai piekļūtu palaistā ER formāta formāta kartēšanas ierakstam.

1. Lapā **Modeļa kartējuma noformētājs**, rūtī **Datu avotu tipi** atlasiet **Funkcijas\\Aprēķinātais lauks**.
2. Atlasiet **Pievienot sakni** rūtī **Datu avoti**.
3. Dialoglodziņa laukā **Nosaukums** ievadiet **ER2**.
4. Atlasiet **Rediģēt formulu**.
5. Formulu redaktorā laukā **Formula** ievadiet **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.
6. Atlasiet **Saglabāt** un aizveriet formulas redaktoru.
7. Atlasiet **Labi**.

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a>Tekošā ER formāta nosaukuma ievadīšana datu modelī

Turpiniet rediģēt atlasīto modeļa kartēšanu, lai datu modelī tiktu ievadīts palaists ER formāta nosaukums.

1. Lapā **Modeļa kartējuma noformētājs** rūtī **Datu modelis** izvērsiet **ExecutionContext** un tad atlasiet **ExecutionContext\\FormatName**.
2. Rūtī **Datu modelis** atlasiet **Rediģēt**, lai konfigurētu datu saistījumu atlasītajam datu modeļa laukam.
3. Formulas redaktorā laukā **Formula** ievadiet **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.
4. Atlasiet **Saglabāt** un aizveriet formulas redaktoru.

Tā kā jūs izmantojāt lauku **FormatName**, konfigurētā modeļa kartēšana tagad pakļauj ER formāta nosaukumu, kas izsauc šo modeļa kartēšanu izpildes laikā.

![Datu modeļa lauku saistīšana ar pievienoto datu avota metodi ER modeļa kartēšanas veidotājā.](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a>Modeļa kartēšanas noformējuma pabeigšana

1. Lapā **Modeļa kartēšanas noformētājs** atlasiet **Saglabāt**.
2. Aizvērt lapu.
3. Aizveriet modeļa kartējumu lapu.
4. **Konfigurāciju** lapā, konfigurācijas kokā pārliecinieties, vai **Aptaujas kartēšanas** konfigurācija joprojām ir atlasīta. Tad kopsavilkuma cilnē **Versijas** atlasiet konfigurēto versiju, kuras statuss ir **Melnraksts**.
5. Atlasiet **Mainīt statusu** \> **Pabeigts**.

Šīs konfigurācijas 1.2. versijas statuss tiek mainīts no **Melnraksta** uz **Pabeigtu**. 1.2. versiju vairs nevar mainīt. Šī versija satur konfigurēto modeļa kartēšanu, un to var izmantot kā pamatu citām ER konfigurācijām. Šīs konfigurācijas 1.3. versija ir izveidota un tās statuss ir **Melnraksts**. Varat rediģēt šo versiju, lai koriģētu **Anketas** modeļa kartēšanu.

### <a name="modify-a-format"></a><a name="ModifyFormat"></a>Formāta modificēšana

Varat modificēt konfigurēto ER formātu tā, lai tā nosaukums būtu redzams pārskata kājenē, kas tiek ģenerēts, kad tiek palaists ER formāts.

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a>Jauna formāta elementa pievienošana

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Aptaujas modelis** un pēc tam atlasiet **Aptaujas pārskats**.
3. Atlasiet **Noformētājs**.
4. Lapā **Formāta veidotājs** atlasiet saknes krājumu **Pārskats**.
5. Atlasiet **Pievienot**, lai atlasītajam **Pārskata** saknes krājumam pievienotu jaunu ligzdotu formāta elementu.
6. Atlasiet **Excel\\Footer**.
7. Laikā **Nosaukums** ievadiet **Kājene**.
8. Atlasiet **Pārskats/Kājene** un pēc tam atlasiet **Pievienot**.
9. Atlasiet **Teksts\\Virkne**.

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a>Pievienotā formāta elementa saistīšana

1. Lapā **Formāta noformētājs**, cilnē **Kartēšana**, formatēšanas kokā elementā **Kājene\\Virkne** atlasiet **Rediģēt formulu**.
2. Formulas redaktorā laukā **Formula** ievadiet **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.
3. Atlasiet **Saglabāt** un aizveriet formulas redaktoru.
4. Atlasiet **Saglabāt**.

Konfigurētais formāts tagad ir pārveidots tā, lai tā nosaukums tiktu ievadīts ģenerētā pārskata kājenē, izmantojot **Kājenes\\Virknes** elementu.

![Kājenes formāta elementa pievienošana konfigurētajam formātam ER operāciju veidotājā.](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a>Formāta noformējuma pabeigšana

1. Aizveriet lapu **Formāta veidotājs**.
2. **Konfigurāciju** lapā, konfigurācijas kokā pārliecinieties, vai **Aptaujas pārskats** konfigurācija joprojām ir atlasīta. Tad kopsavilkuma cilnē **Versijas** atlasiet konfigurēto versiju, kuras statuss ir **Melnraksts**.
3. Atlasiet **Mainīt statusu** \> **Pabeigts**.

Šīs konfigurācijas 1.2. versijas statuss tiek mainīts no **Melnraksta** uz **Pabeigtu**. 1.2. versiju vairs nevar mainīt. Šī versija satur konfigurēto formātu, un to var izmantot kā pamatu citām ER konfigurācijām. Šīs konfigurācijas 1.3. versija ir izveidota un tās statuss ir **Melnraksts**. Varat rediģēt šo versiju, lai koriģētu **Anketas** pārskatu.

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a>Formāta palaišana no programmas

1. Dodieties uz **Aptauja** \> **Noformējums** \> **Aptauju pārskats (darbina ER)**.
2. Dialoglodziņā **Formāta kartēšana** atlasiet **Anketu pārskats**.
3. Atlasiet **Labi**.
4. Dialoglodziņā **ER parametri** kopsavilkuma cilnē **Ierakstus, ko iekļaut** konfigurējiet filtrēšanas opciju, lai tiktu iekļauta tikai **SBCCrsExam** anketa.
5. Lai apstiprinātu filtrēšanas opciju, atlasiet **Labi**.
6. Atlasiet **Labi**, lai palaistu pārskatu.
7. Pārskatiet ģenerēto failu Excel formātā.

Ievērojiet, ka ģenerētā pārskata kājenē ir norādīts tā ER formāta nosaukums, kas tika izmantots, lai to ģenerētu.

![Ģenerētais fails Excel formātā.](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a>Formāta palaišana no ER

1. Dodieties uz **Organizācijas administrēšana** \> **Elektronisko pārskatu veidošana** \> **Konfigurācijas**.
2. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Aptaujas modelis** un pēc tam atlasiet **Aptaujas pārskats**.
3. Darbību rūtī atlasiet **Palaist**.
4. Dialoglodziņā **Elektronisko pārskatu parametri** kopsavilkuma cilnē **Ierakstus, ko iekļaut** konfigurējiet filtrēšanas opciju, lai tiktu iekļauta tikai **SBCCrsExam** anketa.
5. Lai apstiprinātu filtrēšanas opciju, atlasiet **Labi**.
6. Atlasiet **Labi**, lai palaistu pārskatu.
7. Pārskatiet ģenerēto failu Excel formātā.

Ievērojiet, ka ģenerētā pārskata kājenē nav ER formāta nosaukuma, kas tika izmantots, lai to ģenerētu, jo datu līguma objekts netika nodots darbības modeļa kartēšanai, kad to izsauca ER formāts, kas tika palaists no ER.

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a>Formāta mērķa konfigurēšana ekrānā redzamajā priekšskatījumā

1. Dodieties uz **Organizācijas administrēšana** \> **Elektroniskie pārskati** \> **Elektroniskās pārskatu veidošanas adresāts**.
2. **Elektroniskās ziņošanas mērķa** lapā konfigurētajam **Anketas pārskata** ER formātam pievienojiet mērķa ierakstu.
3. Kopsavilkuma cilnē **Faila mērķis** iestatiet **Ekrāna** [mērķi](er-destination-type-screen.md) **Pārskata** formāta komponentam, kas ir [pievienots](#AddFormatRootElement) kā konfigurētā **Anketas pārskata** ER formāta saknes elements.
4. Kopsavilkuma cilnē **PDF pārvēršanas iestatījumi** konfigurējiet mērķi, lai pārveidotu pārskatu [PDF formātā](electronic-reporting-destinations.md#OutputConversionToPDF), kas izmanto **Ainavas** lapas orientāciju.

![Pielāgota ekrāna mērķa konfigurēšana ER formātam elektroniskās ziņošanas mērķa lapā.](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a>Formāta palaišana no programmas, lai to priekšskatītu kā PDF dokumentu

1. Dodieties uz **Aptauja** \> **Noformējums** \> **Aptauju pārskats (darbina ER)**.
2. Dialoglodziņā **Formāta kartēšana** atlasiet **Anketu pārskats**.
3. Atlasiet **Labi**.
4. Dialoglodziņā **Elektronisko pārskatu parametri** kopsavilkuma cilnē **Ierakstus, ko iekļaut** konfigurējiet filtrēšanas opciju, lai tiktu iekļauta tikai **SBCCrsExam** anketa.
5. Lai apstiprinātu filtrēšanas opciju, atlasiet **Labi**.

    Kopsavilkuma cilnē **Galamērķi** ievērojiet, ka **Izvades** lauks ir iestatīts uz **Ekrāns**. Ja vēlaties mainīt konfigurēto mērķi, atlasiet **Mainīt**.

    ![ER pārskata izpildlaika dialoglodziņš, kur varat mainīt konfigurēto mērķi.](./media/er-quick-start1-run-settings.png)

6. Atlasiet **Labi**, lai palaistu pārskatu.
7. Pārskatiet ģenerēto failu PDF formātā.

    ![Ģenerētā faila ekrāna priekšskatījums PDF formātā.](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)
- [Elektronisko pārskatu veidošanas formulu valoda](er-formula-language.md)
- [Daudzvalodu pārskatu noformēšana](er-design-multilingual-reports.md)
- [Elektronisko pārskatu struktūras API](er-apis-app73.md)
- [CASE funkcija](er-functions-logical-case.md)
- [CONCATENATE funkcija](er-functions-text-concatenate.md)
- [DATETIMEFORMAT funkcija](er-functions-datetime-datetimeformat.md)
- [FILTER funkcija](er-functions-list-filter.md)
- [FIRSTORNULL funkcija](er-functions-list-firstornull.md)
- [FORMAT funkcija](er-functions-text-format.md)
- [IF funkcija](er-functions-logical-if.md)
- [ORDERBY funkcija](er-functions-list-orderby.md)
- [SESSIONNOW funkcija](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
