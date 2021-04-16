---
title: Word satura vadīklu likvidēšana ģenerētajos pārskatos
description: Šajā tēmā paskaidrots, kā konfigurēt elektronisko pārskatu (ER) formātu, lai ģenerētu pārskatus kā Microsoft Word failus, kuros satura vadīklas ir likvidētas.
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 8c99203110cfdc7f8123c30488611d55f48e8f67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753605"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a>Word satura vadīklu likvidēšana ģenerētajos pārskatos

[!include [banner](../includes/banner.md)]

Lai ģenerētu pārskatus kā Microsoft Word dokumentus, ir jāizveido veidne pārskatiem kā Word dokuments. Šajā veidnē jābūt Word satura vadīklām kā vietturiem datiem, kas tiks aizpildīti izpildlaikā. Lai izveidoto Word dokumentu izmantotu kā veidni jūsu pārskatiem, varat [konfigurēt](er-design-configuration-word.md) jaunu [elektronisko pārskatu sniegšanas (ER)](general-electronic-reporting.md) [risinājumu](er-quick-start1-new-solution.md). Risinājumam jāietver ER [konfigurācija](general-electronic-reporting.md#Configuration), kas satur ER [formāta](general-electronic-reporting.md#FormatComponentOutbound) komponentu. Šis ER formāts ir jākonfigurē, lai pārskata ģenerēšanai izmantotu izveidoto veidni.

Programmas Dynamics 365 Finance versijā 10.0.6 un jaunākās versijās varat konfigurēt formulas savā ER formātā, lai likvidētu dažas Word satura vadīklas ģenerētajos dokumentos.

Turpmākās darbības paskaidro veidu, kā lietotājs, kuram ir piešķirta sistēmas administratora vai elektronisko pārskatu funkcionālā konsultanta loma, var konfigurēt ER formātu, kas ģenerē pārskatus kā Word failus un likvidē dažas satura vadīklas ģenerētajā pārskatā, kurš ir konfigurēts, izmantojot Word veidni.

Šīs darbības var veikt uzņēmumā GBSI.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai veiktu šīs darbības, vispirms veiciet darbības tālāk minētajos uzdevumu ceļvežos.

- [Izveidot konfigurāciju atskaišu ģenerēšanai formātā OPENXML](./tasks/er-design-reports-openxml-2016-11.md)
- [ER konfigurāciju atkārtota izmantošana ar Excel veidnēm, lai izveidotu pārskatus Word formātā](./tasks/er-design-configuration-word-2016-11.md)

Pabeidzot šo uzdevumu ceļvežu darbības, ir sagatavoti tālāk minētie vienumi.

- **Parauga darblapas pārskata** ER formāts, kas ir konfigurēts dokumenta ģenerēšanai Word formātā
- [Melnraksta](general-electronic-reporting.md#component-versioning) versija **Parauga darblapas pārskata** ER formātam, kas ir atzīmēta kā **Palaižama**
- **Elektroniska** maksājumu metode, kas ir konfigurēta, lai izmantotu **Parauga darblapas pārskata** ER formātu kreditoru maksājumu apstrādei

Turklāt jums ir nepieciešams šim pašam pārskatam lejupielādēt un saglabāt šādu veidni:

- [Maksājumu pārskata saistītā 2. veidne (SampleVendPaymDocReportBounded2.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a>Pārskatīt lejupielādēto Word veidni

1. Word darbvirsmas programmā atveriet **SampleVendPaymDocReportBounded2.docx veidnes** failu, kuru lejupielādējāt iepriekš.
2. Pārbaudiet, vai veidnes failā ir kopsavilkuma sadaļa, kurā redzamas kopējās maksājumu summas katram valūtas kodam, kas izpildīts apstrādātajos maksājumos.

    - Kopsavilkuma sadaļa atrodas atsevišķā Word dokumenta tabulā.
    - Šīs tabulas pirmajā rindā ir tabulu kolonnu virsraksti kā sadaļas virsraksts.
    - Šīs tabulas otrajā rindā ir atkārtota satura vadīkla kā sadaļas informācija.
    - Šī satura vadīkla ir kartēta uz **Pārskata** pielāgotās XML daļas lauku **SummaryLines**.
    - Pamatojoties uz šo kartēšanu, satura vadīkla ir saistīta ar rediģējamā ER formāta elementu **SummaryLines**.

    > [!NOTE]
    > Atkārtotā satura vadīkla ir atzīmēta ar atslēgu **SummaryLines**, kas atbilst pielāgotās XML daļas laukam, uz kuru tā ir kartēta.

    ![Word veidnes izkārtojums](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a>Atlasiet esošo ER pārskatu konfigurāciju

Tālāk minētajām darbībām jūs atkārtoti izmantosiet esošo ER konfigurāciju, ko konfigurējāt, kad izpildījāt darbības iepriekš minētajos uzdevumu ceļvežos.

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Atlasiet **Pārskatu konfigurācijas**.
3. Lapā **Konfigurācijas**, konfigurācijas koka skatā izvērsiet **Maksājuma modelis** un pēc tam atlasiet **Parauga darbgrāmatas pārskats**.
4. Atlasiet **Veidotājs**, lai rediģētu atlasītā ER formāta melnraksta versiju.

## <a name="replace-the-current-template-with-the-new-template"></a>Pašreizējo veidni nomainiet ar jaunu veidni

Pašlaik SampleVendPaymDocReportBounded.docx fails tiek izmantots kā veidne, lai ģenerētu izvadi Word formātā. Nākamajās darbībās aizstājiet Word veidni ar jauno Word veidni — SampleVendPaymDocReportBounded2.docx —, kuru lejupielādējāt iepriekš.

1. Lapā **Formāta veidotājs** atlasiet **Pielikumi**.
2. Lai noņemtu esošo veidni, lapā **Pielikumi** atlasiet **Dzēst**.
3. Atlasiet **Jā**, lai apstiprinātu dzēšanu.
4. Atlasiet **Jauns** \> **Fails**.
5. Atlasiet **Pārlūkot** un pārlūkojiet un atlasiet **SampleVendPaymDocReportBounded2.docx** failu, kuru iepriekš lejupielādējāt.
6. Atlasiet **Labi**.
7. Aizveriet lapu **Pielikumi**.
8. Lapas **Formāta veidotājs** laukā **Veidne** ievadiet vai atlasiet failu **SampleVendPaymDocReportBounded2.docx**.

## <a name="run-the-format-to-create-word-output"></a>Palaist formātu, lai izveidotu Word izvadi

1. Pārejiet uz sadaļu **Kreditori** \> **Maksājumi** \> **Maksājumu žurnāls**.
2. Lapas **Kreditora maksājumi** cilnē **Saraksts** atlasiet visus maksājumus.
3. Atlasiet **Maksājuma statusu** \> **Nav**.
4. Atlasiet **Ģenerēt maksājumus**.
5. Laukā **Maksājuma metode** atlasiet **Elektronisks**.
6. Laukā **Bankas konts** atlasiet **GBSI OPER**.
7. Atlasiet **Labi**.
8. Dialoglodziņā **Elektroniskā pārskata parametri** atlasiet **Labi** un analizējiet ģenerēto izvadi.

    ![Maksājumi apstrāde lapā Kreditora maksājumi](./media/er-design-configuration-word-suppress-controls-image2.gif)

    Rezultāts ir parādīts Word formātā un satur kopsavilkuma sadaļu.

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a>Konfigurēt rediģējamu formātu, lai likvidētu kopsavilkuma sadaļu

Ja vēlaties likvidēt kopsavilkuma sadaļu ģenerētajā dokumentā, pamatojoties uz lietotāja pieprasījumu, kurš lieto šo ER formātu, jums ir jāmodificē rediģējamais ER formāts.

1. Pārejiet uz sadaļu **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu sniegšana** un atveriet ER formāta melnraksta versiju rediģēšanai.
2. Atlasiet **Pārskatu konfigurācijas**. 
3. Lapā **Konfigurācijas** konfigurācijas koka skatā izvērsiet **Maksājuma modelis** \> **Parauga darblapas pārskats**.
4. Atlasiet **Noformētājs**.
5. Lapā **Formāta veidotājs** izvērsiet **Word** un atlasiet **SummaryLines**.
6. Cilnē **Kartēšana** pievienojiet jaunu datu avotu, lai lietotājam izpildlaikā uzdotu jautājumu, vai kopsavilkuma sadaļa būtu jālikvidē.

    1. Atlasiet **Pievienot sakni**.
    2. Dialoglodziņā **Pievienot datu avotu** atlasiet **Vispārīgo\lietotāja ievades parametru**, lai atvērtu dialoglodziņu **'Lietotāja ievades parametra datu avota rekvizīti**.
    3. Laukā **Nosaukums** ievadiet **uipSuppress**.
    4. Laukā **Etiķete** ievadiet **Likvidēt kopsavilkuma sadaļu**.
    5. Laukā **Operāciju datu veida nosaukums**, atlasiet vai ievadiet **NoYes**.
    6. Atlasiet **Labi**.

7. Pievienojiet jaunu **NoYes** programmas uzskaitījuma veida datu avotu.

    1. Atlasiet **Pievienot sakni**.
    2. Dialoglodziņā **Pievienot datu avotu** atlasiet **Dynamics 365 for Operations\Uzskaitījums**, lai atvērtu dialoglodziņu **Uzskaitījuma datu avota rekvizīti**.
    3. Laukā **Nosaukums** ievadiet **enumNoYes**.
    4. Laukā **Etiķete** ievadiet **Likvidēt opcijas**.
    5. Laukā **Operāciju datu veida nosaukums**, atlasiet vai ievadiet **NoYes**.
    6. Atlasiet **Labi**.

8. Konfigurējiet formulu atlasītajam formāta elementam **SummaryLines**, lai norādītu, kad ar atlasīto formāta elementu saistītā Word satura vadīkla būtu jālikvidē.

    1. Cilnes **Kartēšana** sadaļā **Noņemts** atlasiet **Rediģēt**, lai atvērtu lapu **[Formulas veidotājs](general-electronic-reporting-formula-designer.md)**.
    2. Laukā **Formula** ievadiet formulu `uipSuppress = enumNoYes.Yes`.
    3. Atlasiet **Saglabāt** un aizvēriet lapu **Formulas veidotājs** .

        > [!NOTE]
        > Šī formula tiks lietota ģenerētam dokumentam pēc **visu pārējo formāta elementu izpildes**. Lai lietotu šo formulu, Word satura vadīkla, kas ir atzīmēta kā formāta elements, kam šī formula ir konfigurēta (šajā gadījumā **SummaryLines** ) atrodas ģenerētā dokumentā. Pēc tam šī satura vadīkla tiek pilnībā noņemta kopā ar to rindu Word tabulā, kurā tā atrodas. Kopsavilkuma sadaļas detalizētās informācijas rinda tiek izņemta no ģenerētā dokumenta.
        >
        > Izstrādes laikā varat konfigurēt formulu **Noņemts** formāta elementam, kaut arī Word veidnē, kuru izmantojat, nevienai satura vadīklai, ko izmantojat, nav taga, kas atbilst formāta elementa nosaukumam, kam konfigurēts rekvizīts **Noņemts**. Apstiprinot formātu izstrādes laikā, saņemsit [brīdinājumu](er-components-inspections.md#i14) par šo neatbilstību.
        >
        > Izpildlaikā tiek izmests izņēmums, ja jūsu lietotajā Word veidnē satura vadīklai nav etiķetes, kas atbilst tā formāta elementa nosaukumam, kuram ir konfigurēts rekvizīts **Noņemts**.

    4. Cilnes **Kartēšana** sadaļā **Noņemts** iestatiet opciju **Ar vecāku** uz **Jā**.

        > [!NOTE]
        > Šī opcija ir jāiestata uz **Jā**, lai noņemtu visu Word tabulu kā tās rindas vecākobjektu, kura satur kopsavilkuma sadaļas informāciju. Ja iestatāt šo opciju uz **Nē**, sadaļas galvenes rinda paliek ģenerētajā dokumentā.

9. Atlasiet **Saglabāt**, lai saglabātu rediģējamā formāta izmaiņas.

    ![Ģenerētā izvade Word formātā](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a>Palaist modificēto formātu, lai izveidotu Word izvadi

1. Pārejiet uz sadaļu **Kreditori** \> **Maksājumi** \> **Maksājumu žurnāls**.
2. Atlasiet izveidoto maksājumu žurnālu un pēc tam atlasiet **Rindas**.
3. Lapā **Kreditora maksājumi** atlasiet visas rindas un pēc tam atlasiet **Maksājuma statuss** \> **Nav**.
4. Atlasiet **Ģenerēt maksājumus**.
5. Laukā **Maksājuma metode** atlasiet **Elektronisks**.
6. Laukā **Bankas konts** atlasiet **GBSI OPER**.
7. Atlasiet **Labi**.
8. Dialoglodziņa **Elektroniskā pārskata parametri** laukā **Likvidēt kopsavilkuma sadaļu** atlasiet **Jā**.
9. Atlasiet **Labi** un analizējiet ģenerēto izvades informāciju.

    ![Ģenerētais rezultāts Word formātā](./media/er-design-configuration-word-suppress-controls-image4.gif)

    Ņemiet vērā, ka izvade neietver kopsavilkuma sadaļu, jo tā ir likvidēta.

## <a name="additional-resources"></a>Papildu resursi

- [Izveidot konfigurāciju atskaišu ģenerēšanai formātā OPENXML](./tasks/er-design-reports-openxml-2016-11.md)
- [Jaunas ER konfigurācijas noformēšana, lai ģenerētu atskaites Word formātā](er-design-configuration-word.md)
- [ER konfigurāciju atkārtota izmantošana ar Excel veidnēm, lai izveidotu pārskatus Word formātā](./tasks/er-design-configuration-word-2016-11.md)
- [Konfigurēto ER komponentu pārbaude, lai novērstu izpildlaika problēmas](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]