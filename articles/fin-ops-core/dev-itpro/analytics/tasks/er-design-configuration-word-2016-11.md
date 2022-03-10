---
title: ER konfigurāciju ar Excel veidnēm atkārtota izmantošana, lai veidotu pārskatus Word formātā
description: Šajā tēmā ir aprakstīts, kā pārskatu formātus, kas tika veidoti, lai ģenerētu pārskatus kā Excel darbgrāmatas, var konfigurēt, lai ģenerētu pārskatus kā Word dokumentus.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: de8286c7612cd588b28cf4667340374906962dde
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2022
ms.locfileid: "8324066"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a>ER konfigurāciju ar Excel veidnēm atkārtota izmantošana, lai veidotu pārskatus Word formātā

[!include [banner](../../includes/banner.md)]

Lai izveidotu pārskatus kā Microsoft Word dokumentus, varat [konfigurēt](../er-design-configuration-word.md) jaunu elektronisko [pārskatu (ER)](../general-electronic-reporting.md) formātu. Vai arī varat atkārtoti izmantot ER formātu, kas oriģināli tika izveidots, lai ģenerētu pārskatus kā Excel darbgrāmatas. Šajā gadījumā Excel veidne ir jāaizstāj ar Word veidni.

Šīs procedūras parāda, kā lietotājs vai nu sistēmas administratora lomā, vai Elektronisko pārskatu izstrādātāja loma var konfigurēt ER formātu, lai ģenerētu pārskatus kā Word failus, atkārtoti izmantojot ER formātu, kas projektēja, lai ģenerētu pārskatus kā Excel failus.

Visas šīs procedūras var veikt uzņēmumā GBSI.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai veiktu šīs procedūras darbības, jums vispirms ir jāizpilda procedūra [Noformēt konfigurāciju pārskatu ģenerēšanai formātā OPENXML”](er-design-reports-openxml-2016-11.md) uzdevuma ceļvedī.

Turklāt jums ir nepieciešams šim pašam pārskatam lejupielādēt un lokāli saglabāt šādas veidnes:

- [Maksājumu pārskata veidne (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Maksājumu pārskata saistītā veidne (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

Šīs procedūras ir līdzeklim, kas ir pievienots versijā Dynamics 365 for Operations 1611 (2016. gada novembrī).

## <a name="select-the-existing-er-report-configuration"></a>Atlasiet esošo ER pārskatu konfigurāciju

1. Pakalpojumā Dynamics 365 Finance dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Pārliecinieties, ka konfigurācijas nodrošinātājs **Litware, Inc.** ir atlasīts kā **Aktīvs**. Ja tā nav, izpildiet konfigurācijas nodrošinātāju darbības sadaļā [Konfigurācijas nodrošinātāju izveidē un atzīmējiet tos kā](er-configuration-provider-mark-it-active-2016-11.md) aktīvus uzdevumu ceļvedī.
3. Atlasiet **Pārskatu konfigurācijas**. Jūs atkārtoti izmantosim esošo ER konfigurāciju, kas sākotnēji tika veidota tā, lai pārskata izvadi ģenerētu formātā OPENXML.
4. Lapā **Konfigurācijas**, konfigurācijas koka skata kreisajā rūtī izvērsiet **Maksājuma modelis** un pēc tam atlasiet **Parauga darbgrāmatas pārskats**.

    > [!NOTE]
    > Atlasītā ER formāta melnrakstu var rediģēt kopsavilkuma cilnē **Versijas**.

5. Atlasiet **Noformētājs**.
6. **Formāta veidotāja** lapā ievērojiet, ka saknes formāta elementa nosaukums norāda, ka pašlaik tiek izmantota Excel veidne.

![Atlasiet esošo konfigurāciju.](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a>Pārskatīt lejupielādēto Word veidni

1. Word darbvirsmas programmā atveriet **SampleVendPaymDocReport.docx veidnes** failu, kuru lejupielādējāt iepriekš.
2. Ņemiet vērā, ka šī veidne satur tikai dokumenta izkārtojumu, kuru vēlaties ģenerēt kā ER izvadi.

![Pārskata parauga veidnes priekšskatīšana Word darbvirsmas programmā.](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a>Aizstāt Excel veidni ar Word veidni un pievienot pielāgotu XML daļu

Pašlaik Excel dokuments tiek izmantots kā veidne, lai ģenerētu izvadi formātā OPENXML. Esošo Excel veidni aizstājiet ar iepriekš lejupielādēto Word veidni SampleVendPaymDocReport.docx. Paplašiniet Word veidni, pievienojot pielāgotu XML daļu.

1. Pakalpojuma Finance lapas **Formāta veidotājs** cilnē **Formāts** atlasiet **Pielikumi**.
2. Lai noņemtu esošo Excel veidni, lapā **Pielikumi** atlasiet **Dzēst**. Atlasiet **Jā**, lai apstiprinātu izmaiņas.
3. Atlasiet **Jauns** \> **Fails**.

    > [!NOTE]
    > Izmantojiet dokumenta veidu, kas [konfigurēts](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) ER parametros, lai glabātu ER formāta veidnes.

4. Atlasiet **Pārlūkot** un pēc tam pārlūkojiet un atlasiet **SampleVendPaymDocReport.docx** failu, kuru iepriekš lejupielādējāt.
5. Atlasiet **Labi**.
6. Aizveriet lapu **Pielikumi**.
7. **Formāta veidotāja** lapas laukā **Veidne** ievadiet vai atlasiet **SampleVendPaymDocReport.docx** failu, lai izmantotu šo Word veidni iepriekš izmantotās Excel veidnes vietā.
8. Atlasiet **Saglabāt**.

    Papildus konfigurācijas izmaiņu uzglabāšanai darbība **Saglabāt** arī atjaunina pievienoto Word veidni. Izstrādātā formāta struktūra tiek pārnesta uz pievienoto Word dokumentu kā jauna pielāgota XML daļa ar nosaukumu **Pārskats**. Ņemiet vērā, ka pievienotajā Word veidnē ir ne tikai dokumenta izkārtojums, kādā vēlamies ģenerēt ER izvadi, bet tajā ir arī datu struktūra, ar ko ER izpildlaikā aizpildīs šo veidni.

9. Formāta veidotāja lapā ievērojiet, ka saknes formāta elementa nosaukums norāda, ka pašlaik tiek izmantota Excel veidne.

    ![Aizstāt Excel veidni ar Word veidni un pievienot pielāgotu XML daļu.](../media/er-design-configuration-word-2016-11-image03.gif)

10. Cilnē **Formāts** atlasiet **Pielikumi**.

Veiciet elementu kartēšanu no **Pārskata** pielāgotās XML daļas un Word dokumenta satura vadīklām.

Ja pārzināt Word dokumentus, ko var noformēt kā veidlapas, kurās ir [satura vadīklas](/office/client-developer/word/content-controls-in-word), kas ir kartētas ar [pielāgotu XML daļu elementiem](/visualstudio/vsto/custom-xml-parts-overview), pabeidziet visas darbības nākamajā procedūŗā, lai izveidotu dokumentu. Papildinformāciju skatiet rakstā [Veidlapu izveide, kuras lietotāji var aizpildīt un izdrukāt Word formātā](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b). Pretējā gadījumā izlaidiet nākamo darbību.

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a>Iegūt Word dokumentu, kam ir pielāgota XML daļa, un veikt datu kartēšanu

1. Finanšu lapā **Pielikumi** atlasiet **Atvērt**, lai lejupielādētu atlasīto veidni no Finanšu un uzglabātu to lokāli kā Word dokumentu.
3. Word datora programmā atveriet tikko lejupielādēto dokumentu.
4. Cilnē **Izstrādātājs** atlasiet **XML kartēšanas rūts**.

    > [!NOTE]
    > Ja cilne **Izstrādātājs** nav redzama lentē, pielāgojiet lenti tās pievienošanai.

5. **XML kartējuma** rūts laukā **Pielāgotā XML daļa** atlasiet **Pārskata** pielāgoto XML daļu.
6. Veiciet elementu kartēšanu no **Pārskata** pielāgotās XML daļas un Word dokumenta satura vadīklām.
7. Saglabājiet atjaunināto Word dokumentu lokāli kā **SampleVendPaymDocReportBounded.docx**.

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Pārskatīt Word veidni, kur pielāgotā XML daļa ir kartēta uz satura vadīklām

1. Word darbvirsmas programmā atveriet **SampleVendPaymDocReport.docx veidnes** veidnes failu.
2. Ņemiet vērā, ka šī veidne satur tikai dokumenta izkārtojumu, kuru vēlaties ģenerēt kā ER izvadi. Satura vadīklas, kas tiek izmantotas kā vietturi datiem, ko ER ievadīs šajā veidnē izpildlaikā, ir balstītas uz kartējumiem, kas ir konfigurēti starp **Pārskata** pielāgotās XML daļas elementiem un Word dokumenta satura vadīklām.

![Pārskata parauga veidnes priekšskatīšana Word darbvirsmas programmā.](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Pārskatīt Word veidni, kur pielāgotā XML daļa ir kartēta uz satura vadīklām

1. Finanšu dokumentu lapā **Pielikumi** atlasiet **Dzēst**, lai noņemtu Word veidni, kam nav kartējumu starp **Pārskata** pielāgotās XML daļas un satura kontroles elementiem. Atlasiet **Jā**, lai apstiprinātu izmaiņas.
2. Atlasiet **Jauns** \> **Fails**, lai pievienotu jaunu veidnes failu, kas satur kartējumus starp **Pārskata** pielāgotās XML daļas elementiem un satura vadīklām.

    > [!NOTE]
    > Izmantojiet dokumenta veidu, kas [konfigurēts](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) ER parametros, lai glabātu ER formāta veidnes.

3. Atlasiet **Pārlūkot** un pēc tam pārlūkojiet un atlasiet **SampleVendPaymDocReportBounded.docx** failu, kuru lejupielādējat vai sagatavojat, izpildot procedūru sadaļā [Iegūt Word, kam ir pielāgota XML daļa, lai paveiktu datu kartēšanu](#get-word-doc).
4. Atlasiet **Labi**.
5. Aizveriet lapu **Pielikumi**.
6. **Formāta veidotāja** lapas laukā **Veidnes** izvēlieties dokumentu, ko tikko lejupielādējāt.
7. Atlasiet **Saglabāt**.
8. Aizveriet lapu **Formāta veidotājs**.

## <a name="mark-the-configured-format-as-runnable"></a>Atzīmēt konfigurēto formātu kā palaižamu

Lai palaistu rediģējamā formāta melnraksta versiju, tā ir jāpadara [palaižama](../er-quick-start2-customize-report.md#MarkFormatRunnable).

1. Pakalpojuma Finance lapas **Konfigurācijas** darbību rūts cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
2. Dialoglodziņā **Lietotāja parametri** iestatiet opciju **Palaist iestatījumus** uz **Jā** un pēc tam atlasiet **Labi**.
3. Atlasiet **Rediģēt**, lai pašreizējo lapu varētu rediģēt pēc nepieciešamības.
4. Pašlaik atlasītajai **Parauga darblapas pārskata** konfigurācijai iestatiet opciju **Palaist melnrakstu** uz **Jā**.
5. Atlasiet **Saglabāt**.

## <a name="run-the-format-to-create-output-in-word-format"></a>Palaist formātu, lai izveidotu izvadi Word formātā

1. Dodieties uz **Kreditori** \> **Maksājumi** \> **Maksājumu žurnāls**.
2. Iepriekš ievadītajā maksājumu žurnālā atlasiet **Rindas**.
3. Lapā **Kreditoru maksājumi** atlasiet visas režģa rindas.
4. Atlasiet **Maksājuma statusu** \> **Nav**.

    ![Maksājumi apstrāde lapā Kreditora maksājumi.](../media/er-design-configuration-word-2016-11-image05.png)

5. Darbību rūtī atlasiet **Ģenerēt maksājumus**.
6. Nolaižamajā dialoglodziņā veiciet tālāk norādītās darbības:

    1. Laukā **Maksājuma metode** atlasiet **Elektronisks**.
    2. Laukā **Bankas konts** atlasiet **GBSI OPER**.
    3. Atlasiet **Labi**.

7. Dialoglodziņā **Elektroniskā pārskata parametri** atlasiet **Labi**.
8. Izveidotā izvade tiek rādīta formātā Word, un tā ietver detalizētu informāciju par apstrādātajiem maksājumiem. Analizējiet ģenerēto izvadi.

    ![Ģenerētais rezultāts Word formātā.](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a>Papildu resursi

- [Jaunas ER konfigurācijas noformēšana, lai ģenerētu atskaites Word formātā](../er-design-configuration-word.md)
- [Iegulstiet attēlus un formas jūsu ģenerētajos dokumentos, izmantojot ER](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
