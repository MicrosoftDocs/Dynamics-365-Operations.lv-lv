---
title: E-pasta ziņojuma ER adresāta tips
description: Šajā tēmā sniegta informācija par to, kā konfigurēt arhīva mērķi katrai MAPEI vai FAILA komponentam elektronisko pārskatu (ER) formātā.
author: NickSelin
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 4ee1ae4d8a106e467640a8cbcf5986e770395431
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343864"
---
# <a name="email-er-destination-type"></a>E-pasta ziņojuma ER adresāta tips

[!include [banner](../includes/banner.md)]

Kad elektroniskās ziņošanas (ER) formāts tiek palaists, var izveidot vienu vai vairākus izejošos dokumentus. Formāta komponenti **Mape** vai **Fails** tiek izmantoti FR formātos, lai norādītu izejošo dokumentu struktūru. Varat konfigurēt e-pasta galamērķi šiem komponentu tipiem, lai nosūtītu izejošos dokumentus kā e-pasta pielikumus.

Jūs varat konfigurēt e-pasta galamērķi katram ER formāta komponentam **Mape** vai **Fails**. Šādā gadījumā **katrs nosūtāmais dokuments tiek nosūtīts atsevišķi pa e-pastu**. Pamatojoties uz šo galamērķa iestatījumu, ģenerētais dokuments tiek piegādāts kā e-pasta pielikums. 

> [!NOTE]
> Ja dokuments netiek ģenerēts, jo izteiksme **Iespējots** atbilstošajam komponentam **Fails** ir konfigurēta, lai atgrieztu **False** Būla vērtību, netiek sūtīts e-pasta ziņojums, pat ja komponentam ir konfigurēts un iespējots e-pasta ziņojuma galamērķis.

Var arī [grupēt](#grouping) vairākus komponentus **Mape** vai **Fails** kopā un pēc tam konfigurējiet e-pasta ziņojuma galamērķi visiem komponentiem grupā. Šādā gadījumā visi izejošie dokumenti, kas tiek ģenerēti pēc grupai piederošiem komponentiem, **tiek sūtīti kā viena e-pasta ziņojuma vairāki pielikumi**. Pamatojoties uz šo galamērķa iestatījumu, katrs ģenerētais dokuments tiek piegādāts kā e-pasta ziņojuma pielikums.

> [!NOTE]
> Ja vismaz viens dokuments ir izveidots ar komponentu **Fails** komponentu grupā, tiek nosūtīts e-pasta ziņojums. Ja dokuments netiek ģenerēts pēc grupētiem komponentiem, jo izteiksme **Iespējots** katram komponentam **Fails** ir konfigurēta, lai atgrieztu **False** Būla vērtību, netiek sūtīts e-pasta ziņojums, pat ja komponentu grupai ir konfigurēts un iespējots e-pasta ziņojuma galamērķis.
>
> **E-pasta** ir vienīgais galamērķis, ko var konfigurēt komponentu grupai. Lai piegādātu dokumentu, kas ir nosūtīts pa e-pastu, pamatojoties uz e-pasta galamērķa iestatījumu grupai, pievienojiet vēl vienu galamērķa ierakstu, atlasiet vēlamo komponentu un pēc tam konfigurējiet citu mērķi šim ierakstam.

Vienai ER formāta konfigurācijai var konfigurēt vairākas komponentu grupas. Šādā veidā varat konfigurēt e-pasta ziņojuma galamērķi katrai komponentu grupai un e-pasta ziņojumu galamērķi katram komponentam.

## <a name="enable-an-email-destination"></a>E-pasta ziņojuma galamērķa iespējošana

Lai nosūtītu vienu vai vairākus izvades failus pa e-pastu, sekojiet šiem soļiem.

1. Lapā **Elektronisko ziņojumu galamērķis**, kopsavilkuma cilnē **Faila galamērķis** atlasiet režgī komponentu vai komponentu grupu.
2. Atlasiet **Iestatījumi**, dialoglodziņā **Galamērķa iestatījumi** cilnē **E-pasta ziņojums** iestatiet opciju **Iespējots** uz **Jā**.

[![Opcijas Iespējots iestatīšana uz Jā e-pasta galamērķim.](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="configure-an-email-destination"></a>E-pasta ziņojuma galamērķa konfigurēšana

### <a name="email-content"></a>E-pasta ziņojuma saturs

Varat rediģēt e-pasta ziņojuma tēmu un pamattekstu.

Laukā **Tēma** ievadiet e-pasta tēmas tekstu, kam ir jāparādās izpildlaikā ģenerētā elektroniskā ziņojuma tēmas laukā. Laukā **Pamatteksts** ievadiet e-pasta pamatteksta tekstu, kam ir jāparādās elektroniskā ziņojuma pamatteksta laukā. E-pasta ziņojuma tēmai un pamattekstam varat iestatīt konstantus tekstus, vai arī varat lietot ER [formulas](er-formula-language.md), lai e-pasta tekstus izveidotu dinamiski izpildlaikā. Konfigurētai formulai ir jāatgriež [virknes](er-formula-supported-data-types-primitive.md#string) veida vērtība.

Atkarībā no e-pasta klienta e-pasta ziņojuma pamatteksts ir TEKSTA vai HTML formātā. Jūs varat izmantot jebkuru izkārtojumu, stilu un zīmolu, ko HTML un iekļautās kaskadētās stila lapas (CSS) atļauj.

> [!NOTE]
> E-pasta klienti nosaka izkārtojuma un stila ierobežojumus, kas varētu prasīt labojumus HTML un CSS, ko izmantojat ziņojuma pamattekstam. Mēs iesakām jums iepazīties ar labāko praksi, lai izveidotu HTML, ko atbalstīs populārākie e-pasta klienti.
>
> Izmantojiet pareizu kodējumu, lai ieviestu rakstatgriezi, atkarībā no pamatteksta formatējuma. Lai iegūtu plašāku informāciju skatiet datu veida [Virkne](er-formula-supported-data-types-primitive.md#string) definīciju.

### <a name="email-addresses"></a>E-pasta adreses

Varat norādīt e-pasta sūtītāju un e-pasta saņēmējus. Pēc noklusējuma e-pasta ziņojums tiek sūtīts pašreizējā lietotāja vārdā. Lai norādītu citu e-pasta sūtītāju, ir jākonfigurē lauks **No**.

> [!NOTE]
> Kad e-pasta adresāts ir konfigurēts, lauks **No** ir redzams tikai lietotājiem, kuriem ir `ERFormatDestinationSenderEmailConfigure` drošības privilēģija, **Konfigurēt sūtītāja e-pasta adresi ER formāta adresātiem**.
>
> Kad e-pasta adresātu piedāvā mainīt [palaišanas laikā](electronic-reporting-destinations.md#security-considerations), lauks **No** ir redzams tikai lietotājiem, kuriem ir `ERFormatDestinationSenderEmailMaintain` drošības privilēģija, **Saglabāt sūtītāja e-pasta adresi ER formāta adresātiem**.
>
> Kad lauks **No** ir konfigurēts izmantot e-pasta adresi, kas nav pašreizējā lietotāja adrese, tiesības **Sūtīt kā** vai **Sūtīt vārdā** ir pareizi [jāiestata](/microsoft-365/solutions/allow-members-to-send-as-or-send-on-behalf-of-group?view=o365-worldwide) iepriekš. Pretējā gadījumā izpildlaikā tiek parādīts šāds izņēmums: "Nevar nosūtīt e-pastu kā \<from email account\> no \<current user account\> konta, lūdzu, pārbaudiet atļaujas Sūtīt kā šim \<from email account\> kontam."

Varat konfigurēt lauku **No**, lai atgrieztu vairāk nekā vienu e-pasta adresi. Šajā gadījumā pirmā saraksta adrese tiek izmantota kā e-pasta sūtītāja adrese.

Lai norādītu e-pasta saņēmējus, ir jākonfigurē lauki **Kam** un **Kopija** (neobligāti).

E-pasta adreses lietošanai ar ER varat konfigurēt divos veidos. Konfigurāciju var pabeigt tādā pašā veidā, kā to pabeidz drukāšanas pārvaldības līdzeklis, vai arī varat atrisināt e-pasta adresi, izmantojot tiešu atsauci uz ER konfigurāciju ar formulas palīdzību.

## <a name="email-address-types"></a>E-pasta adrešu tipi

Ja atlasāt **Rediģēt** blakus laukam **No**, **Kam** vai **Kopija** dialoglodziņā **Galamērķa iestatījumi**, tiek parādīts dialoglodziņš **E-pasta ziņojums no**, **E-pasta ziņojums kam**, **E-pasta ziņojuma kopija**. Tur varat konfigurēt e-pasta sūtītāju un e-pasta saņēmējus. Atlasiet **Pievienot** un pēc tam atlasiet izmantojamās e-pasta adreses tipu. Divi pašlaik atbalstītie tipi: **Drukāt pārvaldības e-pasta ziņojumu** un **Konfigurācijas e-pasta ziņojums**.

[![E-pasta adreses tipa atlasīšana.](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management-email"></a>Drukāt pārvaldības e-pasta ziņojumu

Ja atlasāt **Drukāt pārvaldības e-pasta ziņojumu** kā e-pasta adreses tipu, varat ievadīt fiksētās e-pasta adreses dialoglodziņā **E-pasta ziņojums no**, **E-pasta ziņojums kam** vai **E-pasta ziņojuma kopija**, iestatot šādus laukus:

- Laukā **E-pasta avots** atlasiet **Nav**.
- Laukā **Papildu e-pasta adreses, kas atdalītas ar “;”** ievadiet fiksētās e-pasta adreses.

Varat arī saņemt e-pasta adreses no tās puses kontaktinformācijas, kurai ģenerējat izejošo dokumentu. Lai lietotu e-pasta adreses, kas nav fiksētas, laukā **E-pasta avots** atlasiet puses [lomu](../../fin-ops/organization-administration/overview-global-address-book.md#party-roles) faila galamērķim. Tālāk ir norādītas atbalstītās lomas:

- Debitors
- Kreditors
- Paredzams klients
- Kontaktpersona
- Konkurents
- Darbinieks
- Kandidāts
- Potenciālais piegādātājs
- Neatļauts piegādātājs
- Juridiska persona

Piemēram, lai konfigurētu e-pasta adresātu ER formātam, kas tiek izmantots, lai apstrādātu kreditoru maksājumus, atlasiet lomu **Kreditors**.

Pēc tam, kad ir atlasīta vajadzīgā loma, atlasiet pogu **Saistīt** (ķēdes simbols) blakus laukam **E-pasta avota konts** , lai atvērtu lomu [Formulas veidotājs](general-electronic-reporting-formula-designer.md). Pēc tam varat izmantot šo lapu, lai konfigurētu formulu, kas izpildlaikā atgriezīs puses konta numuru, kas piešķirts konfigurētajai lomai no apstrādātā dokumenta uz e-pasta galamērķi.

> [!NOTE]
> Formulas ir atkarīgas no ER konfigurācijas.

Lapas **Formulas veidotājs** laukā **Formula** ievadiet dokumentam specifisku atsauci uz atbalstītu lomu. Tā vietā, lai rakstītu atsauci, rūtī **Datu avots** meklējiet un atlasiet datu avota zaru, kas attēlo konfigurētās lomas kontu, un pēc tam atlasiet **Pievienot datu avotu**, lai atjauninātu formulu. Piemēram, ja konfigurējat e-pasta adresātu konfigurācijai **ISO 20022 kredīta pārskaitījumu**, kas tiek izmantota kreditoru maksājumu apstrādei, zars, kas norāda kreditora kontu, ir `'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

![E-pasta avota konta konfigurēšana.](./media/er_destinations-emaildefineaddresssource.gif)

Ja konfigurētās lomas kontu numuri ir unikāli visai Microsoft Dynamics 365 Finance instancei, dialoglodziņa **E-pasta ziņojuma adresāts** lauks **E-pasta ziņojuma avota uzņēmums** var palikt tukšs.

Vai arī var būt situācija, kad dažādas puses [globālajā adrešu grāmatā](../../fin-ops/organization-administration/overview-global-address-book.md) ir reģistrētas dažādos uzņēmumos ([juridiskas personas](../../fin-ops/organization-administration/organizations-organizational-hierarchies.md#legal-entities)) tādā veidā, ka tās visas izmanto vienu konta numuru, lai aizpildītu konfigurēto lomu. Šādā gadījumā konfigurētās lomas kontu numuri nav unikāli visai finanšu instancei. Tāpēc, lai skaidri atlasītu pusi, nevar norādīt tikai konta numuru. Jānorāda arī uzņēmums, kam puse reģistrēta, lai aizpildītu konfigurēto lomu. Atlasiet pogu **Saistīt** (ķēdes simbols) blakus dialoglodziņa **E-pasta adresāts** laukam **E-pasta avota uzņēmums**, lai atvērtu lapu [Formulas veidotājs](general-electronic-reporting-formula-designer.md). Pēc tam varat izmantot šo lapu, lai konfigurētu formulu, kas izpildlaikā atgriež tā uzņēmuma kodu, kas ir atrodams vēlamajā avotā.

> [!TIP]
> Ja ir jāizmanto uzņēmuma kods, lai izpildītu ER formātu, bet ER formāts nesniedz datu avotus, no kuriem var iegūt uzņēmuma kodu, konfigurējiet formulu `GetCurrentCompany()`, izmantojot iebūvēto ER funkciju [GETCURRENTCOMPANY](er-functions-other-getcurrentcompany.md).

> [!NOTE]
> Formulas ir atkarīgas no ER konfigurācijas.

Lai norādītu, kāda tipa e-pasta adreses jāizmanto izpildlaikā, dialoglodziņā **E-pasta ziņojuma adresāts** atlasiet **Rediģēt** blakus laukam **Adresāts**, lai atvērtu nolaižamo dialoglodziņu **Piešķirt e-pasta adresi**. Pēc tam iestatiet tālāk minētos laukus.

- Laukā **Nolūks** atlasiet nolūku. Tiks izmantotas tikai atlasīto mērķu e-pasta adreses no atklātās puses kontaktpersonām.
- Iestatiet opciju **Primārā kontaktpersona** uz **Jā**, lai izmantotu e-pasta adresi, kas ir konfigurēta atklātajai pusei kā primārā e-pasta adrese.

> [!NOTE]
> Ja nolūki ir atlasīti laukā **Nolūks** un opcija **Primārā kontaktpersona** ir iestatīta uz **Jā** vienlaikus, katrs e-pastu ziņojums, kas atbilst vismaz vienam konfigurētajam kritērijam, tiks izmantots izpildlaikā.

### <a name="configuration-email"></a>Konfigurācijas e-pasta ziņojums

Atlasiet **Konfigurācijas e-pasta ziņojums** kā e-pasta adreses tipu, ja izmantojamā konfigurācija ir mezgls datu avotos, kas atgriež vienu e-pasta adresi vai vairākas e-pasta adreses, kuras ir atdalītas ar semikoliem (;). Varat izmantot [datu avotus](general-electronic-reporting.md#FormatComponentOutbound) un [funkcijas](er-formula-language.md#Functions) formulas veidotājā, lai iegūtu pareizi formatētu e-pasta adresi vai pareizi formatētas e-pasta adreses, kas atdalītas ar semikoliem. Piemēram, ja izmantojat **ISO 20022 kredīta pārskaitījuma** konfigurāciju, mezgls, kas norāda kreditora primāro e-pasta adresi no kreditora kontaktinformācijas, uz kuru jānosūta pavadvēstule, ir `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![E-pasta adreses avota konfigurēšana.](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="group-format-components"></a><a id="grouping"></a>Formāta komponentu grupēšana

Lai grupētu formāta komponentus, lapas **Elektroniskās ziņošanas galamērķis** kopsavilkuma cilnē **Faila adresāts** atlasiet režģa komponentus un pēc tam atlasiet **Grupa**.

**E-pasts** ir vienīgais iepriekš konfigurētais galamērķis, kas joprojām ir pieejams atlasītajiem komponentiem. Nav pieejami citi iepriekš konfigurēti galamērķi, jo tie tiek uzskatīti par neatbalstītiem komponentu grupai. Jūs tiksiet informēts par šīm izmaiņām pēc nepieciešamības.

Iepriekš pievienotais ieraksts tiek uzskatīts par izveidotās grupas virsrakstu. Šis virsraksta ieraksts ietver grupas e-pasta ziņojumu galamērķa iestatījumus. Citi ieraksti ir grupas dalībnieki, kas izmantos grupas virsraksta ieraksta e-pasta ziņojumu galamērķa iestatījumus.

Lai atgrupētu formāta komponentus, kopsavilkuma cilnē **Faila galamērķis** atlasiet ierakstu, kas pieder grupai, un pēc tam atlasiet **Atgrupēt**.

- Ja atlasāt virsraksta ierakstu, visa grupa tiks atgrupēta.
- Ja tiek atlasīts dalībnieka ieraksts un tas ir pēdējā dalībnieka ieraksts grupā, visa grupa tiks atgrupēta.
- Ja atlasāt dalībnieka ierakstu, kas nav pēdējais dalībnieka ieraksts grupā, šis ieraksts tiks izslēgts no pašreizējās grupas.

Tālāk atrodamajā attēlā redzama ER formāta struktūra, kas tika konfigurēta, lai izveidotu tilpsaspiesto izejošo failu, kas satur atgādinājuma vēstules piezīmi un piemērotus debitoru rēķinus PDF formātā.

[![ER formāta struktūra, kas ģenerē izejošos dokumentus.](./media/ER_Destinations-Email-Grouping1.png)](./media/ER_Destinations-Email-Grouping1.png)

Tālāk atrodamajā attēlā parādīts process (kā aprakstīts šajā tēmā) ar atsevišķu komponentu grupēšanu un jaunas grupas galamērķa **E-pasta ziņojums** iespējošanu, lai atgādinājuma vēstule tiktu nosūtīta kopā ar atbilstošiem debitoru rēķiniem kā e-pasta pielikumi.

[![Atsevišķu komponentu grupēšana un e-pasta ziņojuma galamērķa iespējošana.](./media/ER_Destinations-Email-Grouping2.gif)](./media/ER_Destinations-Email-Grouping2.gif)

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas (ER) apskats](general-electronic-reporting.md)
- [Elektroniskās pārskatu veidošanas (ER) adresāti](electronic-reporting-destinations.md)
- [Formulas veidotājs elektronisko pārskatu veidošanā (ER)](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
