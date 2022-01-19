---
title: Konfigurācijas noformēšana dokumentu ģenerēšanai Excel formātā
description: Šī tēma sniedz informāciju par to, kā veidot elektronisko pārskatu (ER) formātu, lai aizpildītu Excel veidni un pēc tam ģenerētu izejošos Excel formāta dokumentus.
author: NickSelin
ms.date: 01/05/2022
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
ms.openlocfilehash: 9b1c83894d93789a270ed4521ba7f80da70285ac
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952656"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Konfigurācijas noformēšana dokumentu ģenerēšanai Excel formātā

[!include[banner](../includes/banner.md)]

Varat veidot elektronisko pārskatu (ER) formāta konfigurāciju, kam ir ER formāta komponents, ko varat konfigurēt, lai ģenerētu izejošo [dokumentu](general-electronic-reporting.md) darbgrāmatas Microsoft Excel formātā. Šim nolūkam jāizmanto īpaši ER formāta komponenti.

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

### <a name="replication"></a>Replicēšana

**Replicēšanas virziena** rekvizīts norāda, vai un kā diapazons tiks atkārtots ģenerētajā dokumentā:

- Ja **Replicēšanas virziena** rekvizīts ir iestatīts uz **Bez replikācijas**, atbilstošais Excel diapazons netiks atkārtots ģenerētajā dokumentā.
- Ja **Replicēšanas virziena** rekvizīts ir iestatīts uz **Vertikāls**, atbilstošais Excel diapazons tiks atkārtots ģenerētajā dokumentā. Katrs replicētais diapazons tiek ievietots zem sākotnējā diapazona Excel veidnē. Atkārtojumu skaits tiek noteikts pēc ierakstu skaita **Ierakstu saraksta** tipa datu avotā, kas ir saistīts ar šo ER komponentu.
- Ja **Replicēšanas virziena** rekvizīts ir iestatīts uz **Horizontāls**, atbilstošais Excel diapazons tiks atkārtots ģenerētajā dokumentā. Katrs replicētais diapazons tiek ievietots pa labi no sākotnējā diapazona Excel veidnē. Atkārtojumu skaits tiek noteikts pēc ierakstu skaita **Ierakstu saraksta** tipa datu avotā, kas ir saistīts ar šo ER komponentu.

Lai iegūtu vairāk informācijas par horizontālo replicēšanu, sekojiet soļiem sadaļā [Izmantot horizontāli paplašināmus diapazonus, lai dinamiski pievienotu kolonnas Excel pārskatos](tasks/er-horizontal-1.md).

### <a name="nested-components"></a>Ligzdotie komponenti

**Diapazona** komponentā var būt citi ligzdotie ER komponenti, kas tiek izmantoti, lai ievadītu vērtības atbilstošajos Excel nosauktajos diapazonos.

- Ja kāds **Teksta** grupas komponents tiek izmantots vērtību ievadīšanai, vērtība tiek ievadīta Excel diapazonā kā teksta vērtība.

    > [!NOTE]
    > Izmantojiet šo modeli, lai formatētu ievadītās vērtības, pamatojoties uz lietojumprogrammā definēto lokalizāciju.

- Ja **Excel** grupas **Šūnas** komponents tiek izmantots vērtību ievadīšanai, šī vērtība tiek ievadīta Excel diapazonā kā datu tipa vērtība, kas tiek definēta, saistot šo **Šūnas** komponentu (piemēram, **Virkne**, **Reāls** vai **Vesels skaitlis**).

    > [!NOTE]
    > Izmantojiet šo modeli, lai iespējotu Excel programmu, lai formatētu ievadītās vērtības, pamatojoties uz vietējā datora lokalizāciju, kas atver izejošo dokumentu.

### <a name="enabling"></a>Iespējo

ER operācijas veidotāja cilnē **Kartēšana** varat konfigurēt **Iespējoto** rekvizītu **Diapazona** komponentam, lai norādītu, vai komponents ir jāievieto ģenerētajā dokumentā:

- Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Patiess** izpildlaikā, vai arī, ja neviena izteiksme nav konfigurēta vispār, izveidotajā dokumentā tiks aizpildīts diapazons.
- Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Aplams** izpildlaikā, un, ja šis diapazons nepārstāv visas rindas un kolonnas, izveidotajā dokumentā diapazons netiks aizpildīts.
- Ja **Iespējotā** rekvizīta izteiksme ir konfigurēta, lai atgrieztu opciju **Aplams** izpildlaikā, un šis diapazons pārstāv visas rindas un kolonnas, izveidotajā dokumentā šīs rindas un kolonnas būs slēptas rindas un kolonnas.

### <a name="resizing"></a>Izmēru maiņas

Varat konfigurēt Excel veidni, lai lietotu šūnas, lai uzrādītu teksta datus. Lai nodrošinātu, ka viss teksts šūnā ir redzams ģenerētajā dokumentā, var konfigurēt, lai šūna automātiski ietītu tajā tekstu. Varat konfigurēt arī rindu, kas satur šo šūnu, lai automātiski pielāgotu tās augstumu, ja pievienotais teksts nav pilnībā redzams. Papildinformāciju skatiet sadaļas Satīt tekstu šūnā sadaļā Labot [datus, kas ir izgriezti šūnās](https://support.microsoft.com/office/fix-data-that-is-cut-off-in-cells-e996e213-6514-49d8-b82a-2721cef6144e).

> [!NOTE]
> Zināma Excel ierobežojuma dēļ, pat ja šūnas tiek konfigurētas teksta dzēšanai, un rindas, kurās šīs šūnas ir ietvertas, tiek konfigurētas tā, lai automātiski pielāgotu to augstumus atbilstoši ievietotajam tekstam, iespējams, nevarēsit sapludinātām šūnām un rindām, kurās tās ietvertas, izmantot [līdzekļus](https://support.microsoft.com/topic/you-cannot-use-the-autofit-feature-for-rows-or-columns-that-contain-merged-cells-in-excel-34b54dd7-9bfc-6c8f-5ee3-2715d7db4353)**AutoFit** un Wrappe text **Excel**. 

Attiecībā uz versiju 10.0.23 var likt ER aprēķināt katras rindas augstumu, kas tika konfigurēts, lai automātiski ietilptu ligzdoto šūnu saturam, ja šī rinda satur vismaz vienu sapludinātu šūnu, kas bija konfigurēta teksta saglabāšanai Dynamics 365 Finance tajā. Aprēķinātais augstums tiek izmantots rindas izmēru maiņai, lai nodrošinātu, ka visas šūnas rindā ir redzamas ģenerētajā dokumentā. Lai sāktu izmantot šo funkcionalitāti, kad izpildiet visus ER formātus, kas tika konfigurēti, lai izmantotu Excel veidnes nosūtīšanas dokumentu ģenerēšanai, rīkojieties šādi.

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Saistītās saites** atlasiet **Elektronisko pārskatu veidošanas parametri**.
3. Lapas **Elektronisko pārskatu parametri** cilnē **Izpildlaiks iestatiet opciju Automātiski** **ietilpināt rindu augstumu** **jā**.

Ja vēlaties mainīt šo kārtulu vienam ER formātam, atjauniniet šī formāta melnraksta versiju, veidojot šādas darbības.

1. Dodieties uz **Organizācijas administrēšana** \> **Darbvietas** \> **Elektronisko pārskatu veidošana**.
2. Lapas **Lokalizācijas konfigurācijas** sadaļā **Konfigurācijas** atlasiet **Pārskatu veidošanas konfigurācijas**.
3. Konfigurācijas lapā konfigurācijas koka kreisajā rūtī atlasiet ER konfigurāciju, kas izveidota, lai izmantotu Excel veidni izejošo **dokumentu** ģenerēšanai.
4. Kopsavilkuma cilnē **Versijas** atlasiet konfigurēto versiju, kuras statuss ir **Melnraksts**.
5. Darbību rūtī atlasiet **Noformētājs**.
6. Formāta **veidotāja lapas formāta kokā kreisajā rūtī atlasiet Excel komponentu, kas** ir saistīts ar Excel veidni.
7. Cilnes Formāts laukā Pielāgot rindas augstumu atlasiet vērtību, lai norādītu, vai ER jābūt forsētam izpildlaikā, lai mainītu rindu augstumu izejošā dokumentā, ko ģenerējis **rediģētais** **ER** formāts:

    - **Noklusējums** – izmantojiet vispārējo iestatījumu, kas ir konfigurēts **laukā Automātiskais rindas augstums lapā Elektronisko pārskatu** **parametri**.
    - **Jā** – ignorē vispārējo iestatījumu un mainiet rindas augstumu izpildlaikā.
    - **Nē** - ignorē vispārējo iestatījumu un nemainiet rindas augstumu izpildlaikā.

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

## <a name="page-component"></a><a name="page-component"></a>Lapas komponents

### <a name="overview"></a>Pārskats

Varat lietot komponentu **Lapa**, ja vēlaties, lai Excel ievēro jūsu ER formāta un struktūras sadalījumu pa lapām ģenerētā izvades dokumentā. Kad ER formāts palaiž komponentus, kuri ir zem **Lapas** komponenta, automātiski tiek pievienots vajadzīgais lappuses pārtraukums. Šī procesa laikā ģenerētā satura izmērs, Excel veidnes lappuses iestatījums un Excel veidnē atlasītais papīra izmērs tiek ņemti vērā.

Ģenerētais dokuments ir jāsadala vairākās sadaļās, katra ar atšķirīgu sadalījumu pa lapām, vairākus **Lappuses** komponentus varat konfigurēt katrā [Lapas](er-fillable-excel.md#sheet-component) komponentā.

### <a name="structure"></a><a name="page-component-structure"></a>Struktūra

Pirmais komponents zem komponenta **Lappuse** ir [Diapazons](er-fillable-excel.md#range-component), kurā rekvizīts **Replicēšanas virziens** ir iestatīts uz vērtību **Bez replicēšanas**, šo diapazonu uzskata par lapas galveni sadalījumam pa lapām, kas ir balstīts pašreizējā **Lappuses** komponenta iestatījumos. Excel diapazons, kas tiek saistīts ar šo formāta komponentu, tiek atkārtots katras lappuses augšpusē, kuru ģenerē, izmantojot pašreizējo **Lappuses** komponentu.

> [!NOTE]
> Lai nodrošinātu pareizu sadalījumu pa lapām, ja Excel veidnē tiek konfigurēts diapazons [Rindas, kuras atkārtot augšpusē](https://support.microsoft.com/office/repeat-specific-rows-or-columns-on-every-printed-page-0d6dac43-7ee7-4f34-8b08-ffcc8b022409), šī Excel diapazona adresei ir jābūt vienādai ar tā Excel diapazona adresi, kura tiek saistīta ar iepriekš aprakstīto **Diapazona** komponentu.

Pēdējais komponents zem komponenta **Lappuse** ir **Diapazons**, kurā rekvizīts **Replicēšanas virziens** ir iestatīts uz vērtību **Bez replicēšanas**, šo diapazonu uzskata par lapas kājeni sadalījumam pa lapām, kas ir balstīts pašreizējā **Lappuses** komponenta iestatījumos. Excel diapazons, kas tiek saistīts ar šo formāta komponentu, tiek atkārtots katras lappuses apakšpusē, kuru ģenerē, izmantojot pašreizējo **Lappuses** komponentu.

> [!NOTE]
> Lai nodrošinātu pareizu sadalījumu pa lapām, Excel diapazoniem, kuri ir saistīti ar **Diapazona** komponentiem, palaišanas laikā vajadzētu mainīt izmēru. Neiesakām formatēt šī diapazona šūnas, izmantojot Excel [opcijas](https://support.microsoft.com/office/wrap-text-in-a-cell-2a18cff5-ccc1-4bce-95e4-f0d4f3ff4e84) **Aplauzt tekstu šūnā** un **Automātiski ietilpināt rindas augstumu**.

Varat pievienot vairākus citus **Diapazona** komponentus starp neobligātajiem **Diapazona** komponentiem, lai norādītu, kā tiek aizpildīts ģenerētais dokuments.

Ja ligzdotā **Diapazona** komponentu kopa zem **Lappuses** komponent neatbilst iepriekš aprakstītajai struktūrai, ER formāta noformētāja formēšanas laikā tiek rādīta validācijas [kļūda](er-components-inspections.md#i17). Šis kļūdas ziņojums informē, ka problēma var radīt problēmas palaišanas laikā.

> [!NOTE]
> Lai ģenerētu pareizus izejas datus, nenorādiet saistījumu nevienam no **Diapazona** komponentiem zem **Lappuses** komponenta, ka šī **Diapazona** komponenta rekvizīts **Replicēšanas virziens** ir iestatīts uz vērtību **Bez replicēšanas** un diapazons ir konfigurēts tā, lai tiktu ģenerētas lapu galvenes vai kājenes.

Ja vēlaties ar sadalījumu pa lapām saistītu summēšanu un skaitīšanu, lai aprēķinātu palaistās kopsummas un kopskaitu katrai lapai, iesakām konfigurēt vajadzīgos [Datu kolekcijas](er-data-collection-data-sources.md) datu avotus. Lai uzzinātu, kā lietot **Lappuses** komponentu, lai pa lapām sadalītu ģenerēto Excel dokumentu, izpildiet darbības, kas norādītas sadaļā [Noformēt ER formātu, lai pa lapām sadalītu Excel formātā ģenerētu dokumentu](er-paginate-excel-reports.md).

### <a name="limitations"></a><a name="page-component-limitations"></a>Ierobežojumi

Excel sadalījumam pa lapām lietojot **Lappuses** komponentu, jūs nezināsit lappušu gala skaitu ģenerētajā dokumentā, kamēr nav pabeigts sadalījums pa lapām. Tāpēc jūs nevar aprēķināt kopējo lappušu skaitu, izmantojot ER formulas, un drukāt ģenerētā dokumenta pareizo lappušu skaitu uz jebkuras lappuses pirms pēdējās lappuses.

> [!TIP]
> Lai šo rezultātu panāktu Excel galvenē vai kājenē, ir jālieto īpašs Excel [formatējums](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) galvenēm un kājenēm.

Konfigurētie **Lapas** komponenti netiek ņemti vērā, atjauninot Excel veidni rediģējamā formātā Dynamics 365 Finance 10.0.22. versijā. Šī funkcija tiek ņemta vērā jaunākos Finance laidienos.

Ja konfigurējat Excel veidni, lai lietotu [nosacījuma formatēšanu](/office/dev/add-ins/excel/excel-add-ins-conditional-formatting), tā dažos gadījumos varētu nedarboties, kā paredzēts.

### <a name="applicability"></a>Piemērojamība

**Lappuses** komponents darbojas [Excel faila](er-fillable-excel.md#excel-file-component) formāta komponentam tikai tad, ja šim komponentam ir konfigurēta veidnes lietošana Excel. Ja [aizstājat](tasks/er-design-configuration-word-2016-11.md) Excel veidni ar Word veidni un pēc tam palaižat rediģējamu ER formātu, **Lappuses** komponents tiks ignorēts.

**Lappuses** komponents darbojas tikai tad, ja ir iespējots līdzeklis **Iespējot EPPlus bibliotēkas izmantošanu elektronisko pārskatu struktūrā**. Izpilddlaikā tiek palaists izņēmums, ja ER mēģina apstrādāt **Lappuses** komponentu, kamēr ir atspējots šis līdzeklis.

> [!NOTE]
> Izpildlaikā tiek palaists izņēmums, ja ER formāts apstrādē **Lappuses** komponentu Excel veidnei, kura satur vismaz vienu formulu, kura atsaucas uz nederīgu šūnu. Lai novērstu izpilddlaika kļūdas, veiciet Excel veidnes labojumu, kā aprakstīts sadaļā [Kā labot #REF! kļūdu](https://support.microsoft.com/office/how-to-correct-a-ref-error-822c8e46-e610-4d02-bf29-ec4b8c5ff4be).

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

## <a name="example-2-fixing-the-merged-cells-epplus-issue"></a><a name="example-2"></a> 2. piemērs: sapludināto šūnu EPPlus problēmas labošana

ER formātu varat palaist, lai izveidotu izejošo dokumentu Excel darbgrāmatas formātā. Kad iespējo EPPlus bibliotēkas izmantošanu elektronisko pārskatu veidošanas struktūras līdzeklī, kas ir iespējots Līdzekļu pārvaldības darbvietā, EPPlus bibliotēka tiek izmantota **Excel** **·**[izvades](https://www.nuget.org/packages/epplus/4.5.2.1) veidošanai. Tomēr, tā kā Excel funkcionalitāte ir zināma un EPPlus bibliotēka ir ierobežota, varat saskarties ar šādu [izņēmumu](https://answers.microsoft.com/msoffice/forum/all/deleting-a-range-of-cells-that-includes-merged/8601462c-4e2c-48e0-bd23-848eecb872a9): "Nevar dzēst/pārrakstīt sapludinātās šūnas. Diapazons ir daļēji sapludināts ar citu sapludinātu diapazonu." Lai uzzinātu, kādas Excel veidnes var izraisīt šo izņēmumu un kā var labot šo problēmu, izpildiet šo piemēru.

1. Excel darbvirsmas programmā izveidojiet jaunu Excel darbgrāmatu.
2. Darblapas **lapā1** pievienojiet **ReportTitle** nosaukumu šūnai **A2.**
3. Sapludināt šūnas **A1** un **A2**.

    ![Pārskatiet šūnu A1 un A2 sapludināšanas rezultātus excel darba programmas Excel darbvirsmas programmā.](./media/er-fillable-excel-example2-1.png)

3. Konfigurāciju **lapā pievienojiet** jaunu [ER formātu,](er-fillable-excel.md#add-a-new-er-format) lai izveidotu izejošo dokumentu Excel darbgrāmatas formātā.
4. Formāta **veidotāja** lapā [importējiet izveidoto Excel darbgrāmatu pievienotjā ER formātā kā jaunu veidni](er-fillable-excel.md#template-import) izejošajiem dokumentiem.
5. Cilnē **Kartēšana** konfigurējiet saistījumu **šūnas tipa ReportTitle**[komponentam](er-fillable-excel.md#cell-component).
6. Palaidiet konfigurēto ER formātu. Ievērojiet, ka ir parādīts šāds izņēmums: "Nevar dzēst/pārrakstīt sapludinātās šūnas. Diapazons ir daļēji sapludināts ar citu sapludinātu diapazonu."

    ![Pārskatiet rezultātus, kas rodas, izpildot konfigurēto ER formātu formāta veidotāja lapā.](./media/er-fillable-excel-example2-2.png)

Varat labot šo problēmu vienā no tālāk norādītajiem veidiem:

- **Vieglāka, bet nav ieteicama: Funkciju pārvaldības darbvietā izslēdziet EPPlus bibliotēkas lietošanas** **·** **iespējošanu elektronisko pārskatu veidošanas struktūras** funkcijai. Kaut arī šī pieeja ir vieglāka, jūs variet pieredzi ar citiem jautājumiem, ja jūs to izmantojat, jo dažas ER funkcijas tiek atbalstītas tikai tad, ja EPPlus bibliotēkas enable izmantošana Elektronisko pārskatu veidošanas struktūras **funkcionalitātē** ir aktivizēta.
- **Ieteicams:** veiciet tālāk norādītās darbības.

    1. Excel darbvirsmas programmā modificējiet Excel darbgrāmatu vienā no šiem veidiem:

        - Darblapas **lapā1** atvienojiet šūnas **A1** un **A2**.
        - Mainiet ReportTitle nosaukuma atsauci **no** **=Sheet1!$A$2** uz **=Sheet1!$A$1.**

        ![Pārskatiet rezultātus, kas rodas, mainot atsauci Excel darbvirsmas programmas izveidotai darbgrāmatai.](./media/er-fillable-excel-example2-3.png)

    2. Formāta **veidotāja** lapā [importējiet](er-fillable-excel.md#template-import) modificēto Excel darbgrāmatu rediģējamā ER formātā, lai atjauninātu esošo veidni.
    3. Palaist modificēto ER formātu.

        ![Pārskatiet ģenerēto dokumentu Excel darbvirsmas programmā.](./media/er-fillable-excel-example2-4.png)

## <a name="limitations"></a>Ierobežojumi

### <a name="known-epplus-library-limitations"></a>Zināmās EPPlus bibliotēkas ierobežojumi

#### <a name="external-data-sources"></a>Ārējo datu avoti

Ja kāda no veidnēm ietver PivotTable, kas ir balstīta uz modeli, kas attiecas uz ārējo datu avotu, un ir iespējota EPPlus bibliotēkas iespējošana Elektronisko pārskatu veidošanas struktūras funkcija, izpildot ER formātu, kas izmanto šo veidni izejošā dokumenta ģenerēšanai PowerPivot [Excel](https://support.microsoft.com/office/create-a-pivottable-with-an-external-data-source-db50d01d-2e1c-43bd-bfb5-b76a818a927b)**formātā**: "Kešatmiņas avots nav darblapa." Lai novērstu šo problēmu, jums ir šādas opcijas:

- **Ieteicams:** pārveidot Excel risinājumu, kuru izmantojat:

    1. Izdaliet daļu, kas satur pivots atsevišķā Excel darbgrāmatā (A darbgrāmata). 
    2. Izmantojiet ER, lai no Finanšu programmas ģenerētu otru Excel darbgrāmatu (darbgrāmatu B), kurā ir nepieciešamie dati. 
    3. Atsaucieties uz B darbgrāmatu A, tiklīdz tiek ģenerēta darbgrāmata B.

- Izslēdziet šo līdzekli. Lai izmantotu opciju, kas nav **EPPlus, aktivizējiet** EPPlus bibliotēkas lietošanu elektronisko pārskatu struktūrā. 

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[Konfigurācijas noformēšana pārskatu ģenerēšanai formātā OPENXML](tasks\er-design-reports-openxml-2016-11.md)

[Elektronisko pārskatu veidošanas formātu modificēšana, atkārtoti lietojot Excel veidnes](modify-electronic-reporting-format-reapply-excel-template.md)

[Izmantot horizontāli paplašināmus diapazonus, lai dinamiski pievienotu kolonnas programmas Excel pārskatos](tasks/er-horizontal-1.md)

[Iegulstiet attēlus un formas jūsu ģenerētajos dokumentos, izmantojot ER](electronic-reporting-embed-images-shapes.md)

[Elektronisko pārskatu (EP) izveides konfigurēšana, lai pārsūtītu datu uz pakalpojumu Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
