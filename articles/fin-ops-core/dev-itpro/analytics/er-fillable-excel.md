---
title: Konfigurācijas noformēšana dokumentu ģenerēšanai Excel formātā
description: Šī tēma sniedz informāciju par to, kā veidot elektronisko pārskatu (ER) formātu, lai aizpildītu Excel veidni un pēc tam ģenerētu izejošos Excel formāta dokumentus.
author: NickSelin
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 96e1575e2237cab481c368083da1e60fec612087
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359033"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Konfigurācijas noformēšana dokumentu ģenerēšanai Excel formātā

[!include[banner](../includes/banner.md)]

Varat izveidot [elektroniskās ziņošanas (ER)](general-electronic-reporting.md) formāta konfigurāciju, kurai ir ER [formāta komponents](general-electronic-reporting.md#FormatComponentOutbound), ko varat konfigurēt, lai izveidotu izejošo dokumentu Microsoft Excel darbgrāmatas formātā. Šim nolūkam jāizmanto īpaši ER formāta komponenti.

Lai uzzinātu vairāk par šo līdzekli, sekojiet norādījumiem tēmā [Noformēt konfigurāciju, lai veidotu pārskatus OPENXML formātā](tasks/er-design-reports-openxml-2016-11.md).

## <a name="add-a-new-er-format"></a>Jauna ER formāta pievienošana

Kad pievienojat jaunu ER formāta konfigurāciju, lai ģenerētu izejošo dokumentu Excel darbgrāmatas formātā, ir vai nu jāatlasa **Excel** vērtība **Formāta veida** atribūtam, vai nu jāatstāj **formāta veida** atribūtu tukšu.

- Ja atlasāt **Excel**, jūs varat konfigurēt formātu, lai ģenerētu izejošo dokumentu tikai Excel formātā.
- Ja atstājat atribūtu tukšu, varat konfigurēt formātu, lai ģenerētu izejošo dokumentu jebkurā formātā, ko atbalsta ER struktūra.

Lai konfigurētu konfigurācijas ER formāta komponentu, darbību rūtī atlasiet **Veidotājs** un atveriet ER formāta komponentu rediģēšanai ER operāciju veidotājā.

![Lapa Konfigurācijas.](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Excel faila komponents

### <a name="manual-entry"></a>Manuāla ievade

Jums ir jāpievieno **Excel\\Fails** komponents konfigurētajam ER formātam, lai ģenerētu izejošo dokumentu Excel formātā.

![Excel\Faila komponents.](./media/er-excel-format-add-file-component.png)

Lai norādītu izejošā dokumenta izkārtojumu, pievienojiet Excel darbgrāmatu, kam ir paplašinājums .xlsx, **Excel\\Faila** komponentam kā veidni izejošajiem dokumentiem.

> [!NOTE]
> Manuāli pievienojot veidni, jāizmanto [dokumenta veids](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types), kas ir konfigurēts šim nolūkam [ER parametros](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Pielikuma pievienošana Excel\Faila komponentam.](./media/er-excel-format-add-file-component2.png)

Lai norādītu, kā pievienotā veidne tiks aizpildīta, palaižot konfigurēto ER formātu, ir jāpievieno ligzdotas **Lapas**, **Diapazona** un **Šūnas** komponenti **Excel\\Faila** komponentam. Katram ligzdotajam komponentam ir jābūt saistītam ar Excel nosaukto krājumu.

### <a name="template-import"></a>Veidnes importēšana

Varat atlasīt **Importēt no Excel** darbību rūts cilnē **Importēt**, lai importētu jaunu veidni tukšā ER formātā. Šajā piemērā **Excel\\Faila** komponents tiks izveidots automātiski, un importētā veidne tiks tai pievienota. Visi vajadzīgie ER komponenti arī tiks izveidoti automātiski, balstoties uz Excel nosaukto vienumu sarakstu.

![Opcijas Importēt no Excel atlasīšana.](./media/er-excel-format-import-template.png)

> [!NOTE]
> Ja vēlaties izveidot izvēles **Lapas** elementu rediģējamajā ER formātā, iestatiet opciju **Izveidot Excel lapas formāta elementu** uz **Jā**.

## <a name="sheet-component"></a>Lapas komponents

**Lapas** komponents norāda pievienotās Excel darbgrāmatas darblapu, kas ir jāaizpilda. Darblapas nosaukums Excel veidnē ir definēts šī komponenta **Lapas** rekvizītā.

> [!NOTE]
> Šis komponents nav obligāts Excel darbgrāmatām, kurās ir ietverta viena darblapa.

ER operācijas veidotāja cilnē **Kartēšana** varat konfigurēt **Iespējoto** rekvizītu **Lapas** komponentam, lai norādītu, vai komponents ir jāievieto ģenerētajā dokumentā:

- Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Patiess** izpildlaikā, vai arī, ja neviena izteiksme nav konfigurēta vispār, izveidotajā dokumentā tiks ievietota atbilstoša darblapa.
- Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Aplams** izpildlaikā, ģenerētajā dokumentā netiks ietverta darblapa.

![Lapas komponenta piemērs.](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Diapazona komponents

**Diapazona** komponents norāda Excel diapazons, kas ir jākontrolē šim ER komponentam. Diapazona nosaukums ir definēts šī komponenta **Excel diapazona** rekvizītā.

**Replicēšanas virziena** rekvizīts norāda, vai un kā diapazons tiks atkārtots ģenerētajā dokumentā:

- Ja **Replicēšanas virziena** rekvizīts ir iestatīts uz **Bez replikācijas**, atbilstošais Excel diapazons netiks atkārtots ģenerētajā dokumentā.
- Ja **Replicēšanas virziena** rekvizīts ir iestatīts uz **Vertikāls**, atbilstošais Excel diapazons tiks atkārtots ģenerētajā dokumentā. Katrs replicētais diapazons tiek ievietots zem sākotnējā diapazona Excel veidnē. Atkārtojumu skaits tiek noteikts pēc ierakstu skaita **Ierakstu saraksta** tipa datu avotā, kas ir saistīts ar šo ER komponentu.
- Ja **Replicēšanas virziena** rekvizīts ir iestatīts uz **Horizontāls**, atbilstošais Excel diapazons tiks atkārtots ģenerētajā dokumentā. Katrs replicētais diapazons tiek ievietots pa labi no sākotnējā diapazona Excel veidnē. Atkārtojumu skaits tiek noteikts pēc ierakstu skaita **Ierakstu saraksta** tipa datu avotā, kas ir saistīts ar šo ER komponentu.

Lai iegūtu vairāk informācijas par horizontālo replicēšanu, sekojiet soļiem sadaļā [Izmantot horizontāli paplašināmus diapazonus, lai dinamiski pievienotu kolonnas Excel pārskatos](tasks/er-horizontal-1.md).

**Diapazona** komponentā var būt citi ligzdotie ER komponenti, kas tiek izmantoti, lai ievadītu vērtības atbilstošajos Excel nosauktajos diapazonos.

- Ja kāds **Teksta** grupas komponents tiek izmantots vērtību ievadīšanai, vērtība tiek ievadīta Excel diapazonā kā teksta vērtība.

    > [!NOTE]
    > Izmantojiet šo modeli, lai formatētu ievadītās vērtības, pamatojoties uz lietojumprogrammā definēto lokalizāciju.

- Ja **Excel** grupas **Šūnas** komponents tiek izmantots vērtību ievadīšanai, šī vērtība tiek ievadīta Excel diapazonā kā datu tipa vērtība, kas tiek definēta, saistot šo **Šūnas** komponentu (piemēram, **Virkne**, **Reāls** vai **Vesels skaitlis**).

    > [!NOTE]
    > Izmantojiet šo modeli, lai iespējotu Excel programmu, lai formatētu ievadītās vērtības, pamatojoties uz vietējā datora lokalizāciju, kas atver izejošo dokumentu.

ER operācijas veidotāja cilnē **Kartēšana** varat konfigurēt **Iespējoto** rekvizītu **Diapazona** komponentam, lai norādītu, vai komponents ir jāievieto ģenerētajā dokumentā:

- Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Patiess** izpildlaikā, vai arī, ja neviena izteiksme nav konfigurēta vispār, izveidotajā dokumentā tiks aizpildīts diapazons.
- Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Aplams** izpildlaikā, un, ja šis diapazons nepārstāv visas rindas un kolonnas, izveidotajā dokumentā diapazons netiks aizpildīts.
- Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Aplams** izpildlaikā, un šis diapazons pārstāv visas rindas un kolonnas, izveidotajā dokumentā šīs rindas un kolonnas būs slēptas rindas un kolonnas.

## <a name="cell-component"></a>Šūnas komponents

**Šūnas** komponents tiek izmantots, lai aizpildītu Excel nosauktās šūnas, formas un attēlus. Lai norādītu Excel nosaukto objektu, kas jāaizpilda ar **Šūnas** ER komponentu, jums ir jānorāda šī objekta nosaukums **Šūnas** komponenta **Excel diapazona** rekvizītā.

ER operācijas veidotāja cilnē **Kartēšana** varat konfigurēt **Iespējoto** rekvizītu **Šūnas** komponentam, lai norādītu, vai objekts ir jāaizpilda ģenerētajā dokumentā:

- Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Patiess** izpildlaikā, vai arī, ja neviena izteiksme nav konfigurēta vispār, izveidotajā dokumentā tiks aizpildīts objekts. Šīs **Šūnas** komponenta saistījums norāda vērtību, kas tiek ievietota atbilstošajā objektā.
- Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Aplams** izpildlaikā, ģenerētajā dokumentā netiks aizpildīts atbilstošais objekts.

Ja **Šūnas** komponents ir konfigurēts, lai ievadītu vērtību šūnā, tas var būt saistīts ar datu avotu, kas atgriež primitīva datu veida vērtību (piemēram, **Virkne**, **Reāls** vai **Vesels skaitlis**). Šādā gadījumā vērtība tiek ievadīta šūnā kā tā paša datu veida vērtība.

Ja **Šūnas** komponents ir konfigurēts, lai ievadītu vērtību Excel formā, tas var būt saistīts ar datu avotu, kas atgriež primitīva datu veida vērtību (piemēram, **Virkne**, **Reāls** vai **Vesels skaitlis**). Šādā gadījumā vērtība tiek ievadīta Excel formā kā tā pašas formas teksts. Datu veidu vērtībām, kas nav **Virkne**, konvertēšana uz tekstu tiek veikta automātiski.

> [!NOTE]
> Jūs varat konfigurēt **Šūnas** komponentu, lai aizpildītu formu tikai gadījumos, kad tiek atbalstīts formas teksta rekvizīts.

Ja **Šūnas** komponents ir konfigurēts, lai ievadītu vērtību Excel attēlā, tas var būt saistīts ar datu avotu, kas **Konteinera** datu veida vērtību, kas pārstāv attēlu binārā formātā. Šādā gadījumā vērtība tiek ievadīta Excel attēlā kā attēls.

> [!NOTE]
> Katrs Excel attēls un forma tiek uzskatīta par noenkurotu pie tā augšējā kreisā stūra uz noteiktu Excel šūnu vai diapazonu. Ja vēlaties replicēt Excel attēlu vai formu, ir jākonfigurē šūna vai diapazons, kas tiek noenkurots kā replicēta šūna vai diapazons.

Papildinformāciju par attēlu un formu iegulšanu skatiet sadaļā [Attēlu un formu iegulšana dokumentos, kas tiek ģenerēti, izmantojot ER](electronic-reporting-embed-images-shapes.md).

## <a name="page-break-component"></a>Lappuses pārtraukuma komponents

**Lappuses pārtraukuma** komponents liek programmai Excel sākt jaunu lapu. Šis komponents nav nepieciešams, ja vēlaties izmantot programmas Excel noklusējuma lapošanu, bet to vajadzētu izmantot, ja vēlaties, lai Excel seko savam ER formātam struktūras lapošanai.

## <a name="footer-component"></a>Kājenes komponents

Komponents **Kājene** tiek izmantots, lai aizpildītu kājenes Excel darbgrāmatas ģenerētās darblapas apakšdaļā.

> [!NOTE]
> Varat pievienot šo komponentu katram komponentam **Lapa**, lai norādītu dažādas kājenes dažādām darblapām ģenerētajā Excel darbgrāmatā.

Konfigurējot atsevišķu komponentu **Kājene**, var lietot rekvizītu **Virsraksta/kājenes izskats**, lai norādītu lapas, kurām komponents tiek izmantots. Ir pieejamas šādas vērtības:

- **Jebkurš** — palaist konfigurēto komponentu **Kājene** jebkurai vecākelementa Excel darblapas lapai.
- **Pirmais** — palaist konfigurēto komponentu **Kājene** tikai pirmajai vecākelementa Excel darblapas lapai.
- **Pāra** — palaist konfigurēto komponentu **Kājene** tikai vecākelementa Excel darblapas pāra lapām.
- **Nepāra** — palaist konfigurēto komponentu **Kājene** tikai vecākelementa Excel darblapas nepāra lapām.

Vienam komponentam **Lapa** var pievienot vairākus komponentus **Kājene**, no kuriem katram ir atšķirīga vērtība rekvizītam **Galvenes/kājenes izskats**. Šādā veidā Excel darblapā var izveidot dažādas kājenes dažādiem lapu veidiem.

> [!NOTE]
> Pārliecinieties, ka katram komponentam **Kājene**, ko pievienojat vienam komponentam **Lapa**, ir atšķirīga vērtība rekvizītam **Galvenes/kājenes izskats**. Pretējā gadījumā rodas [validācijas kļūda](er-components-inspections.md#i16). Saņemtajā kļūdas ziņojumā ir informācija par nekonsekvenci.

Zem pievienotā komponenta **Kājene** pievienojiet nepieciešamos **Teksts\\Virkne**, **Teksts\\DateTime** vai cita veida ligzdotos komponentus. Konfigurējiet šo komponentu saistījumus, lai norādītu, kā tiek aizpildīta lapas kājene.

Lai pareizi formatētu ģenerētās kājenes saturu, varat izmantot arī īpašus [formatēšanas kodus](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers). Lai uzzinātu, kā izmantot šo pieeju, izpildiet darbības [1. piemērā](#example-1) tālāk šajā tēmā.

> [!NOTE]
> Konfigurējot ER formātus, noteikti apsveriet Excel [ierobežojumu](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) un maksimālo rakstzīmju skaitu vienai galvenei vai kājenei.

## <a name="header-component"></a>Galvenes komponents

Komponents **Galvene** tiek izmantots, lai aizpildītu galvenes Excel darbgrāmatas ģenerētās darblapas augšdaļā. Tas tiek izmantots līdzīgi komponentam **Kājene**.

## <a name="edit-an-added-er-format"></a>Rediģēt pievienoto ER formātu

### <a name="update-a-template"></a>Veidnes atjaunināšana

Varat atlasīt **Atjaunināt no Excel** darbību rūts cilnē **Importēt**, lai importētu atjauninātu veidni rediģējamā ER formātā. Šī procesa laikā atlasītā **Excel\\Faila** komponenta veidne tiks aizstāta ar jaunu veidni. Rediģējamā ER formāta saturs tiks sinhronizēts ar atjauninātās ER veidnes saturu.

- Jauns ER formāta komponents tiks automātiski izveidots katram Excel nosaukumam, ja ER formāta komponents nav atrasts rediģējamā formātā.
- Katrs ER formāta komponents tiks dzēsts no rediģējamā ER formāta, ja tam nav atrasts atbilstošais Excel nosaukums.

> [!NOTE]
> Ja vēlaties izveidot izvēles **Lapas** elementu rediģējamajā ER formātā, iestatiet opciju **Izveidot Excel lapas formāta elementu** uz **Jā**.
>
> Ja rediģējamais ER formāts sākotnēji ietvēra **Lapas** elementus, ieteicams iestatīt opciju **Izveidot Excel lapas formāta elementu** uz **Jā**, importējot atjauninātu veidni. Pretējā gadījumā visi oriģinālās **Lapas** elementa ligzdotie elementi tiks izveidoti no nulles. Tāpēc atjauninātajā ER formātā tiks zaudēti visi atkārtoti izveidoto formāta elementu saistījumi.

![Izveidot Excel lapas formāta elementa opciju dialoglodziņā Atjaunināt no Excel.](./media/er-excel-format-update-template.png)

Lai uzzinātu vairāk par šo līdzekli, sekojiet soļiem sadaļā [Modificēt elektronisko pārskatu formātus, atkārtoti pielietojot Excel veidnes](modify-electronic-reporting-format-reapply-excel-template.md).

## <a name="validate-an-er-format"></a>Pārbaudīt ER formātu

Pārbaudot ER formātu, ko var rediģēt, tiek veikta konsekvences pārbaude, lai pārliecinātos, ka Excel nosaukums ir pašlaik izmantotajā Excel veidnē. Jūs tiksiet informēts par jebkādām neatbilstībām. Dažām neatbilstībām tiks piedāvāta opcija automātiski labot problēmas.

![Pārbaudes kļūdu ziņojums.](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Excel formulu aprēķinu kontrolēšana

Kad tiek ģenerēts izejošais dokuments Microsoft Excel darbgrāmatas formātā, dažas šī dokumenta šūnas var saturēt Excel formulas. Kad ir iespējots līdzeklis **EPPlus bibliotēkas izmantošanas iespējošana elektronisko pārskatu struktūrā**, varat kontrolēt, kad formulas tiek aprēķinātas, mainot **Aprēķina opciju** [parametra](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) vērtību Excel veidnē, kas tiek izmantota:

- Atlasiet **Automātisks**, lai pārrēķinātu visas pakārtotās formulas ik reizi, kad ģenerētais dokuments tiek pievienots, izmantojot jaunus diapazonus, šūnas utt.
    >[!NOTE]
    > Tas var radīt veiktspējas problēmu Excel veidnēm, kas ietver vairākas saistītas formulas.
- Atlasiet **Manuāls**, lai izvairītos no formulas pārrēķina, kad tiek ģenerēts dokuments.
    >[!NOTE]
    > Formulas pārrēķins tiek manuāli izpildīts piespiedu kārtā, kad izveidotais dokuments tiek atvērts priekšskatījumam, izmantojot Excel.
    > Neizmantojiet šo opciju, ja konfigurējat ER galamērķi, kas pieņem izveidotā dokumenta izmantošanu bez tā priekšskatījuma programmā Excel (PDF pārvēršana, nosūtīšana e-pasta utt.), jo izveidotajā dokumentā var nebūt vērtības šūnās, kas satur formulas.

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>1. piemērs: formāta kājenes saturs

1. Izmantojiet nodrošinātās ER konfigurācijas, lai [ģenerētu](er-generate-printable-fti-forms.md) drukājamu brīvā teksta rēķina (FTI) dokumentu.
2. Pārskatiet ģenerētā dokumenta kājeni. Ievērojiet, ka tā satur informāciju par pašreizējās lapas numuru un kopējo lapu skaitu dokumentā.

    ![Ģenerētā dokumenta kājenes pārskatīšana Excel formātā.](./media/er-fillable-excel-footer-1.gif)

3. ER formāta veidotājā [atveriet](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) parauga ER formātu pārskatīšanai.

    Darblapas **Rēķins** kājene tiek ģenerēta, pamatojoties uz divu to komponentu **Virkne** iestatījumiem, kas atrodas zem komponenta **Kājene**:

    - Pirmais komponents **Virkne** aizpilda šādus īpašus formatēšanas kodus, lai programma Excel piemērotu specifisku formatēšanu:

        - **&C** — izlīdzināt kājenes tekstu centrā.
        - **&"Segoe UI,Regular"&8** — rāda kājenes tekstu "Segoe UI Regular" fontā 8 punktu lielumā.

    - Otrais komponents **Virkne** aizpilda tekstu, kas satur pašreizējo lapas numuru un kopējo lapu skaitu pašreizējā dokumentā.

    ![Kājenes ER formāta komponenta pārskatīšana lapā Formāta veidotājs.](./media/er-fillable-excel-footer-2.png)

4. Pielāgojiet parauga ER formātu, lai modificētu pašreizējās lapas kājeni:

    1. [Izveidojiet](er-quick-start2-customize-report.md#DeriveProvidedFormat) atvasinātu **Brīvā teksta rēķina (Excel) pielāgoto** ER formātu, kas ir pamatots uz parauga ER formātu.
    2. Pievienojiet pirmo jauno komponentu **Virkne** pāri **Rēķina** darblapas komponentam **Kājene**:

        1. Pievienojiet komponentu **Virkne**, kas izlīdzina uzņēmuma nosaukumu kreisajā pusē un parāda to 8 punktu "Segoe UI Regular" fontā (**"&L&"Segoe UI,Regular"&8"**).
        2. Pievienojiet komponentu **Virkne**, kas aizpilda uzņēmuma nosaukumu (**model.InvoiceBase.CompanyInfo.Name**).

    3. Pievienojiet otro jauno komponentu **Virkne** pāri **Rēķina** darblapas komponentam **Kājene**:

        1. Pievienojiet komponentu **Virkne**, kas izlīdzina apstrādes datumu labajā pusē un parāda to 8 punktu "Segoe UI Regular" fontā (**"&R&"Segoe UI,Regular"&8"**).
        2. Pievienojiet komponentu **Virkne**, kas aizpilda apstrādes datumu pielāgotā formātā (**"&nbsp;"&DATEFORMAT(SESSIONTODAY(), "yyyy-MM-dd")**).

        ![Kājenes ER formāta komponenta pārskatīšana lapā Formāta veidotājs.](./media/er-fillable-excel-footer-3.png)

    4. [Aizpildiet](er-quick-start2-customize-report.md#CompleteDerivedFormat) atvasinātā **Brīvā teksta rēķina (Excel) pielāgotā** ER formāta melnraksta versiju.

5. [Konfigurējiet](er-generate-printable-fti-forms.md#configure-print-management) drukas pārvaldību, lai izmantotu atvasināto **Brīvā teksta rēķina (Excel) pielāgoto** ER formātu, nevis ER parauga formātu.
6. Ģenerējiet drukājamu FTI dokumentu un pārskatiet ģenerētā dokumenta kājeni.

    ![Ģenerētā dokumenta kājenes pārskatīšana Excel formātā.](./media/er-fillable-excel-footer-4.gif)

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[Konfigurācijas noformēšana pārskatu ģenerēšanai formātā OPENXML](tasks\er-design-reports-openxml-2016-11.md)

[Elektronisko pārskatu veidošanas formātu modificēšana, atkārtoti lietojot Excel veidnes](modify-electronic-reporting-format-reapply-excel-template.md)

[Izmantot horizontāli paplašināmus diapazonus, lai dinamiski pievienotu kolonnas programmas Excel pārskatos](tasks/er-horizontal-1.md)

[Iegulstiet attēlus un formas jūsu ģenerētajos dokumentos, izmantojot ER](electronic-reporting-embed-images-shapes.md)

[Elektronisko pārskatu (EP) izveides konfigurēšana, lai pārsūtītu datu uz pakalpojumu Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]