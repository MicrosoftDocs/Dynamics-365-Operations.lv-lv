---
title: Svītrkodu attēlu ģenerēšanai izmantot svītrkodu datu avotus
description: Šajā tēmā skaidrots, kā izmantot svītrkodu datu avotus, lai ģenerētu svītrkoda attēlus.
author: NickSelin
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: bf71caf2ff14fb815999e63d6b7ee91afccbdd1b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563683"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a>Svītrkodu attēlu ģenerēšanai izmantot svītrkodu datu avotus

[!include[banner](../includes/banner.md)]

Varat izmantot [elektronisko pārskatu (ER)](general-electronic-reporting.md) struktūru, lai veidotu [ER formāta komponentus](general-electronic-reporting.md#FormatComponentOutbound), ko varat palaist, lai izveidotu nepieciešamos elektroniskus un drukājamus izejošos dokumentus. Lai ģenerētu izejošo dokumentu Microsoft Office formātā, ir jānorāda pārskata izkārtojums, izmantojot vai nu Microsoft Excel dokumentu, vai Microsoft Word dokumentu kā pārskata veidni. [ER operāciju veidotājs](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) ļauj jums pievienot Excel vai Word dokumentu kā veidni ER formātam. Pievienotajā veidnē sekojošie, nosauktie elementi ir saistīti ar konfigurētā formāta komponenta elementiem:

- Satura kontrole programmā Word
- Programmā Excel nosauktās lapas, diapazoni, šūnas, formas un attēli

Šie nosauktie elementi tiek izmantoti kā vietturi datiem, kas ir ievadīti ģenerētajā dokumentā, kad tiek palaists ER formāts. ER formāta elementi ir saistīti ar datu avotiem. Šie datu avoti norāda datus, kas tiks ievadīti ģenerētajos dokumentos izpildlaikā. Vairāk informācijas skatiet rakstā [Iegulstiet attēlus un formas jūsu ģenerētajos dokumentos, izmantojot ER](electronic-reporting-embed-images-shapes.md)

Tagad ER atbalsta **Svītrkoda** datu avota tipu. Tādējādi tagad varat ģenerēt attēlu, kas attēlo norādītā teksta svītrkodu. Konfigurējot ER formātu, varat norādīt **Svītrkoda** tipa datu avotus, lai ģenerētu svītrkoda attēlus. Pēc tam šos attēlus var pievienot ģenerētajiem biznesa dokumentiem, piemēram, pasūtījumiem, rēķiniem, pavadzīmēm un apliecinājumiem. Varat arī tās pievienot dažādām etiķetēm, piemēram, preču un plauktu etiķetēm, iepakojuma un piegādes etiķetēm.

Šos vietturus var izmantot pārskata veidnēs, lai ievadītu svītrkoda attēlus:

- [Attēla](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) satura kontrole programmai Word
- [Attēla](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344) objekts programmā Excel

Izmantojot **Svītrkoda** tipa datu avotu, varat ģenerēt svītrkodus šādos formātos:

- Viendimensijas svītrkodi:

    - Codabar
    - Code 39
    - Code 93
    - Code 128
    - EAN-8
    - EAN-13
    - ITF-14
    - Inteliģentais pasts
    - MSI
    - Plessey
    - PDF417
    - UPC-A
    - UPC-E

- Divdimensiju svītrkodi:

    - Aztec
    - Datu matrica
    - QR kods

Konfigurējot **Svītrkoda** datu avotu, varat definēt konkrētus atveidošanas parametrus, kas tiek izmantoti attēla ģenerēšanai:

- **Platums** - norāda svītrkoda platumu pikseļos. Vērtība **0** (nulle) norāda, ka tiek lietots noklusētais platums. Nozīme var atšķirties dažādiem formātiem.
- **Augstums** - norāda svītrkoda augstumu pikseļos. Vērtība **0** (nulle) norāda, ka tiek lietots noklusētais augstums. Nozīme var atšķirties dažādiem formātiem.
- **Piemale** - norāda svītru koda piemales lielumu pikseļos. Piemale ir apgabals katrā svītrkoda pusē, kas jātur tukšs (klusā zona). Vērtība **0** (nulle) norāda, ka tiek lietota noklusētā piemale. Nozīme var atšķirties dažādiem formātiem.
- **Izvades saturs** - iestatiet vērtību **Jā**, lai ģenerētu svītrkoda attēlu, kas satur kodētu informāciju kā tekstu. Noklusējuma vērtība ir **Nē**.
- **Kodējums** - norāda rakstzīmju tipu, kas ir kodēts ģenerētajā svītrkoda attēlā. Pēc noklusējuma tiek izmantots **UTF-8** kodējums.

> [!IMPORTANT]
> Kad pievienojat jaunu **Svītrkoda** datu avotu, tas ir jāievieto citā vienumā (konteinerā) kā ligzdots elements.
>
> Kad tiek saistīts **Svītrkoda** datu avots ar šūnas elementu formātā un šūnas elements ir vai nu Word satura vadīkla, vai Excel attēls, datu avots ir norādīts kā funkcija, kam ir viens **Virknes** tipa parametrs. Šis parametrs jāizmanto, lai norādītu tekstu, kas ir jāpārveido par svītrkoda attēlu, un jālasa, kad tiek skenēts ģenerētais svītrkods.

Papildinformācijai par šo līdzekli, aizpildiet šajā tēmā sniegtos piemērus.

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a>Piemērs: ģenerēt maksājuma čeku, kas satur svītrkodu, kas kodē maksājamo summu

Šis piemērs parāda, kā lietotājs **Sistēmas administratora** vai **Elektroniskās ziņošanas funkcionālās konsultanta** lomā var konfigurēt ER formātu, kas satur izmantoto veidni, lai ģenerētu izejošo dokumentu Excel formātā, kas satur svītrkodu. Piedāvājam apskatu par iesaistītajām darbībām.

1. [Pabeigt priekšnosacījumus](#ExamplePrerequisites).
2. [Aktivizēt konfigurāciju nodrošinātāju](#ExampleProvider).
3. [Importēt sniegto ER risinājumu](#ExampleImportSolution).
4. [Ģenerēt maksājuma čeku](#ExampleGenerateCheque).
5. [Pārskatīt ģenerēto maksājumu čeku](#ExampleReviewGeneratedCheque).
6. [Pārveidot sniegtā ER risinājuma formātu](#ExampleModifyFormat).

    1. [Pielietot jaunu pārbaudes veidni](#ExampleModifyFormatApplyTemplate).
    2. [Pievienot jaunu Svītrkoda datu avotu](#ExampleModifyFormatAddDataSource).
    3. [Saistīt jaunu formāta elementu](#ExampleModifyFormatBindFormatElement).
    4. [Padarīt modificēto versiju pieejamu pārbaudēm](#ExampleModifyFormatMakeVersionAvailable).

        1. [Pabeigt modificēto formāta versiju](#CompleteToRun).
        2. [Padarīt melnraksta versiju pieejamu lietošanai](#MarkToRun).

7. [Ģenerēt maksājuma čeku](#ExampleGenerateCheque2).
8. [Konvertēt ģenerēto čeku uz PDF](#ExampleConvertToPDF).

Šajā piemērā tiks izmantots norādītais ER risinājums, kas ir konfigurēts maksājumu pārbaužu ģenerēšanai. Šis risinājums ģenerē maksājuma čekus, kuros maksājamā summa ir rakstīta gan kā skaitlis, gan kā teksts. Jūs mainīsit šo ER risinājumu, lai čeks iekļautu arī ģenerēto svītrkodu, kur maksājamā summa ir kodēta, un to var nolasīt, izmantojot svītrkodu skeneri.

Darbības var pabeigt uzņēmumā **USMF** programmā Microsoft Dynamics 365 Finance.

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a>Pabeigt priekšnosacījumus

Lai izpildītu šo piemēru, jums programmas Finance uzņēmumā USMF jābūt piekļuvei vienai no tālak norādītajām lomām:

- Elektronisko pārskatu veidošanas funkcionālais konsultants
- Sistēmas administrators

Ja vēl neesat izpildījis piemēru tēmā [Iegult attēlus un formas dokumentos, kurus ģenerējat, izmantojot ER](electronic-reporting-embed-images-shapes.md), lejupielādējiet tālāk norādītās parauga ER risinājumu konfigurācijas.

| Satura apraksts         | Faila nosaukums                   |
|-----------------------------|-----------------------------|
| ER datu modeļa konfigurācija | cheques.xml modelis       |
| ER formāta konfigurācija     | Čeku drukāšanas formāts.xml |

Turklāt lejupielādējiet šo Excel failu, kas satur modificēto veidni sniegtajam ER risinājumam.

| Satura apraksts | Faila nosaukums                 |
|---------------------|---------------------------|
| Pārskata veidne     | Pārbaudīt veidni Excel.xlsx |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a>Konfigurāciju nodrošinātāja aktivizēšana

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas nodrošinātāji** pārliecinieties, vai ir uzskaitīts [konfigurācijas nodrošinātājs](general-electronic-reporting.md#Provider) parauga uzņēmumam **Litware, Inc.** un vai tas ir atzīmēts kā aktīvs. Ja tas nav uzskaitīts vai tas nav atzīmēts kā aktīvs, izpildiet darbības, kas aprakstītas tēmā [Konfigurācijas nodrošinātāja izveide un atzīmēšana par aktīvu](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![Parauga uzņēmuma iestatīšana uz aktīvu lokalizācijas konfigurāciju lapā](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a>Importēt sniegto ER risinājumu

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas** atlasiet elementu **Pārskatu veidošanas konfigurācijas**.
3. Ja lapā **Konfigurācijas** konfigurāciju kokā nav pieejama konfigurācija **Čeku modelis**, sekojiet šiem soļiem, lai importētu ER datu modeļa konfigurāciju:

    1. Darbību rūtī atlasiet **Mainīt** \> **Ielādēt no XML faila**.
    2. Dialoglodziņā atlasiet **Pārlūkot**, atrodiet un atlasiet failu **Čeku modelis.xml** un pēc tam atlasiet **Labi**.

4. Ja **Čeku izdrukas formāta** konfigurācija konfigurāciju kokā nav pieejama, sekojiet šiem soļiem, lai importētu ER formāta konfigurāciju:

    1. Darbību rūtī atlasiet **Mainīt** \> **Ielādēt no XML faila**.
    2. Dialoglodziņā atlasiet **Pārlūkot**, atrodiet un atlasiet failu **Čeku izdrukas formāts.xml** un pēc tam atlasiet **Labi**.

5. Konfigurāciju kokā izvērsiet **Čeku modelis**.
6. Konfigurāciju kokā pārskatiet importējamo ER konfigurāciju sarakstu.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a>Ģenerēt maksājuma čeku

1. Atveriet sadaļu **Kases un bankas vadība** \> **Banku konti** \> **Banku konti**.
2. Lapā **Bankas konti** atlasiet **USMF OPER** kontu.
3. Bankas kontu detaļu lapā, darbību rūtī, cilnē **Iestatīšana**, grupā **Izkārtojums** atlasiet **Čeks**.
4. Lapā **Čeka izkārtojums** atlasiet **Rediģēt**.
5. Kopsavilkuma cilnē **Vispārīgi** iestatiet opciju **Vispārīgs elektroniskās eksportēšanas formāts** uz **Jā**.
6. Laukā **Eksporta formāta konfigurācija** atlasiet **Čeku izdrukas formāta** ER formātu, ko importējāt iepriekš.
7. Darbību rūtī atlasiet **Drukāt testu**.
8. Dialoglodziņā iestatiet **Apgrozāma čeka formāta** opciju uz **Jā** un pēc tam atlasiet **Labi**.

    ![Čeka izkārtojums - drukāt testa dialoglodziņu](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a>Pārskatīt ģenerēto maksājumu čeku

- Atveriet ģenerēto čeku programmā Excel.
2. Pārskatiet ģenerēto XML čeku.

    ![Ģenerētais maksājums programmā Excel](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a>Pārveidot sniegtā ER risinājuma formātu

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a>Pielietot jaunu čeka veidni

Varat izmantot Excel darbvirsmas programmu, lai atvērtu **Čeka veidnes Excel.xlsx** failu, ko importējāt iepriekš. Ievērojiet, ka šī veidne atšķiras no veidnes, ko izmantojāt, lai ģenerētu maksājuma čeku sniegtajā ER risinājumā. Turklāt tajā ir ietverts **AmountBarcode** elements svītru koda attēlam.

![AmountBarcode elements Excel veidnē](./media/er-barcode-data-source-cheque2.png)

Tagad jums ir jāmodificē ER risinājums un pēc tam [atkārtoti jāpiemēro](modify-electronic-reporting-format-reapply-excel-template.md) modificētā veidne.

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas** atlasiet **Pārskatu veidošanas konfigurācijas**.
3. Lapā **Konfigurācijas**, konfigurācijas kokā izvērsiet **Čeku modeli** un atlasiet **Čeku izdrukas formātu**.
4. Darbību rūtī atlasiet **Noformētājs**.
5. ER operāciju veidotājā atlasiet cilni **Kartēšana** lapas labajā pusē, pēc tam kreisajā pusē esošajā formāta koka rūtī atlasiet **Izvērst/sakļaut**.
6. Ievērojiet, ka visi šūnas formāta elementi ir saistīti ar atbilstošajiem datu avotiem.

    ![Šūnas formāta elementu saistījums ar datu avotiem ER operāciju veidotājā](./media/er-barcode-data-source-cells-bound.png)

7. Atlasiet cilni **Formāts** lapas labajā pusē.
8. Darbības rūtī atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Importēt**.
9. Grupā **Importēt** atlasiet **Atjaunināt no Excel** un pēc tam atlasiet **Atjaunināt veidni**.
10. Dialoglodziņā atrodiet **Čeka veidnes Excel.xlsx** failu, kas tiek saglabāts jūsu datorā, atlasiet to un pēc tam atlasiet **Labi**, lai apstiprinātu, ka atlasītā veidne ir jālieto.
11. Atlasiet cilni **Kartēšana** lapas labajā pusē, pēc tam kreisajā pusē esošajā formāta koka rūtī atlasiet **Izvērst/sakļaut**.
12. Ievērojiet, ka **AmountBarcode** šūnas elements ir pievienots formātam. Šis elements ir saistīts ar **AmountBarcode** elementu, kas ir pievienots modificētajai Excel veidnei kā svītrkoda attēla vietturis.

    ![AmountBarcode šūnas elements, kas pievienots formātam ER operāciju noformētājā](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a>Pievienot jaunu Svītrkoda datu avotu

Pēc tam ir jāpievieno jauns **Svītrkoda** tipa datu avots.

1. ER operāciju noformētājā cilnē **Kartēšana** lapas labajā pusē atlasiet **drukāt** datu avotu.
2. Atlasiet **Pievienot** un pēc tam grupā **Funkcijas** atlasiet **Svītrkoda** datu avota tipu.

    ![Svītrkoda datu avota tipa atlasīšana](./media/er-barcode-data-source-add.png)

3. Dialoglodziņa laukā **Nosaukums** ievadiet **svītrkodu**.
4. Sadaļā **Svītrkoda formāts** atlasiet **Kods 128**.
5. Laukā **Platums** ievadiet **500**.
6. Atlasiet **Labi**.

    ![Dialoglodziņš Datu avota rekvizīti](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a>Saistīt jaunu formāta elementu

Pēc tam jaunajam formāta elementam ir jāpiesaista tikko pievienotais datu avots.

1. ER operāciju noformētājā cilnē **Kartēšana** lapas labajā pusē atlasiet **drukāt\\svītrkodu** datu avotu.
2. Formāta koka rūtī kreisajā pusē atlasiet **AmountBarcode** šūnas elementu un pēc tam atlasiet **Saistīt**.
3. Darbību rūtī atlasiet **Rādīt detaļas**.
4. Ņemiet vērā, ka, tā kā **Svītrkoda** datu avots ir attēlots kā funkcija, kas ietver vienu parametru, saistītā formāta elementa nosaukums ir automātiski pieņemts kā šī parametra arguments.

    ![Detalizēta informācija par Svītrkoda datu avotu ER operāciju noformētājā](./media/er-barcode-data-source-bind1.png)

5. Atlasiet **Rediģēt formulu**, lai koriģētu saistījumu.

    Jūs nevēlaties atgriezt šūnas elementa nosaukumu. Tāpēc ir jākonfigurē izteiksme, kas atgriež tekstu, kas ietver pašreizējo čeka maksājamo summu. Tāpēc, ka pamata **ChequeLines** diapazons ir piesaistīts **model.cheques** datu avotam, pašreizējā čeka maksājamā summa ir pieejama datu tipa **Īsts** laukā **model.cheques.attributes.amount**.

6. Laukā **Formula** ievadiet **print.barcode(NUMBERFORMAT(@.attributes.amount, "F2"))**.
7. Atlasiet **Saglabāt** un pēc tam aizveriet [ER formulu noformētāju](general-electronic-reporting-formula-designer.md).
8. Ievērojiet, ka saistījums ir pielāgots.

    ![Pielāgots saistījums ER operāciju noformētājā](./media/er-barcode-data-source-bind2.png)

9. Atlasiet **Saglabāt** un pēc tam aizveriet ER operāciju noformētāju.

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a>Padarīt modificēto versiju pieejamu pārbaudēm

Pēc noklusējuma vienīgās versijas, kuru statuss ir **Pabeigts** un **Koplietojamas**, tiek izmantotas, palaižot ER formātu.

Ja ir pabeigtas izmaiņas, varat pabeigt darbu ar pašreizējo melnraksta versiju un padarīt jūsu izmaiņas pieejamas lietošanai. Instrukcijas skatiet sekojošajā sadaļā [Pabeigt modificēto formāta versiju](#CompleteToRun).

Ja vēlaties turpināt darbu ar pašreizējo melnraksta versiju, bet tā ir jāizmanto, lai izveidotu čekus, ir viennozīmīgi jānorāda, ka vēlaties izmantot formāta melnraksta versiju. Instrukcijas skatiet sadaļā [Padarīt melnraksta versiju pieejamu izmantošanai](#MarkToRun).

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a>Pabeigt modificēto formāta versiju

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas** atlasiet **Pārskatu veidošanas konfigurācijas**.
3. Lapā **Konfigurācijas**, konfigurācijas kokā izvērsiet **Čeku modeli** un atlasiet **Čeku izdrukas formātu**.
4. Kopsavilkuma cilnē **Versijas** atlasiet ierakstu, kura statuss ir **Melnraksts**.
5. Atlasiet **Mainīt statusu** un pēc tam atlasiet **Pabeigt**.
6. Dialoglodziņā atlasiet **Labi**.

Pašreizējās versijas statuss tiek mainīts no **Melnraksts** uz **Pabeigts**, un tiek izveidota jauna versija ar statusu **Melnraksts**. Varat izmantot šo jauno melnraksta versiju, lai piemērotu papildu izmaiņas.

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a>Padarīt melnraksta versiju pieejamu lietošanai

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas** atlasiet **Pārskatu veidošanas konfigurācijas**.
3. Lapas **Konfigurācijas** darbību rūtī, cilnē **Konfigurācijas**, grupā **Papildu iestatījumi** atlasiet vienumu **Lietotāja parametri**.
4. Dialoglodziņā iestatiet **Palaist iestatījumu** opciju uz **Jā** un pēc tam atlasiet **Labi**.
5. Konfigurācijas kokā izvērsiet **Čeku modeli** un atlasiet **Čeku izdrukas formātu**.
6. Iestatiet opciju **Palaist melnrakstu** uz **Jā**.
7. Atlasiet **Saglabāt**.

Atlasītā formāta melnraksta versija ir atzīmēta kā pieejama, kad tiek palaists atlasītais formāts.

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a>Ģenerēt maksājuma čeku

1. Atveriet sadaļu **Kases un bankas vadība** \> **Banku konti** \> **Banku konti**.
2. Lapā **Bankas konti** atlasiet **USMF OPER** kontu.
3. Bankas kontu detaļu lapā, darbību rūtī, cilnē **Iestatīšana**, grupā **Izkārtojums** atlasiet **Čeks**.
4. **Čeka izkārtojuma** lapā, Darbības rūtī atlasiet **Drukāt testu**.
5. Dialoglodziņā iestatiet **Apgrozāma čeka formāta** opciju uz **Jā**.
6. Atlasiet **Labi**.
7. Pārskatiet ģenerēto XML čeku. Ievērojiet, ka svītrkods ir ģenerēts, lai kodētu čeka izmaksājamo summu.

    ![Ģenerētais maksājuma čeks ar svītrkodu programmā Excel](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> Izņēmums tiek izmests, ja **Svītrkoda** datu avota arguments neatbilst atbilstošajām prasībām, kas ir raksturīgas svītrkoda formātam. Piemēram, kad **Svītrkoda** datu avots ir izsaukts, lai ģenerētu [EAN-8](https://wikipedia.org/wiki/EAN-8) svītrkodu norādītajam tekstam, izņēmums tiek izmests, ja teksta garums pārsniedz septiņas rakstzīmes.

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a>Konvertēt ģenerēto čeku uz PDF

Kā aprakstīts tēmā [Ģenerēt drukājamas FTI formas](er-generate-printable-fti-forms.md#finland), var izmantot speciālu fontu, lai izveidotu svītrkodus ģenerētajā dokumentā. Šādā gadījumā ģenerētā dokumenta papildu transformācijas var būt atkarīgas no šī fonta pieejamības transformācijas vidē. Piemēram, ja mēģināt pārvērst dokumentu PDF formātā vai priekšskatīt to vidē, kur trūkst fontu, svītrkodi netiks atveidoti pareizi.

Tomēr, izmantojot **Svītrkoda** datu avotu, lai izveidotu svītrkodus, šo svītrkodu atveidošana nav atkarīga no fonta. Tāpēc varat viegli pārveidot dokumentus, kas satur svītrkodus, uz PDF formātu. Sekojošajā attēlā redzams ģenerētā maksājuma čeka priekšskatījums, kas tika [konvertēts](electronic-reporting-destinations.md#OutputConversionToPDF) PDF failā, pamatojoties uz konfigurētā ER [adresāta](electronic-reporting-destinations.md)  iestatījumu.

![Maksājuma čeka PDF priekšskatījums](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a>Ierobežojumi

> [!NOTE]
> Atsevišķiem svītrkodu tipiem, kas tiek ģenerēti, ir fiksēts aspekta koeficients. Šai uzvedībai ir nozīme, ja esat ieslēdzis līdzekli **Iespējot EPPlus bibliotēkas izmantošanu elektronisko pārskatu struktūru**, lai strādātu ar Excel dokumentiem ER formātā. Šādā gadījumā attēls tiek ievadīts vietturī, kam ir fiksētas proporcijas. Tādēļ, kad viettura izmēri veidnē atbilst ievadītā attēla koeficientam, var tikt mainīts reālais attēls ģenerētajā dokumentā, lai uzturētu nepieciešamo proporciju. Lai izvairītos no attēla izmēru maiņas, izmantojiet vietturi, kam ir paredzētais malu koeficients.

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)
- [Elektroniskā pārskatu veidošanas adresāti](electronic-reporting-destinations.md)
- [Elektronisko atskaišu veidošanas formulas valoda](er-formula-language.md)
- [NUMBERFORMAT funkcija](er-functions-text-numberformat.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]