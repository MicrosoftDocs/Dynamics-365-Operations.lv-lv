---
title: Sava vietējā kontu plāna plānošana
description: Šajā tēmā sniegta informācija, kas palīdzēs jums plānot kontu plānu, kad jūsu organizācijai ir prasības pret likumā noteiktajām/lokālajām prasībām.
author: VeselinaE
ms.date: 10/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts, LedgerConsolidateAccountGroup, MainAccountConsolidateAccount, DimensionDetails, MainAccountDetails
ROBOTS: ''
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.tgt_pltfrm: ''
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.search.industry: ''
ms.author: veneva
ms.search.validFrom: 10/07/2021
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e224a2e24b4ba293c953c6c883307038128e2f04
ms.sourcegitcommit: ba10ba2cd4fb4267afb5aacae4f6a52aa2456e7e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2021
ms.locfileid: "7798300"
---
# <a name="plan-your-local-chart-of-accounts"></a>Sava vietējā kontu plāna plānošana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija, kas palīdzēs jums plānot kontu plānu, kad jūsu organizācija ietver juridiskas personas, kam jāatbilst noteiktu vietējo vietu prasībām, kur tās veic uzņēmējdarbību. Šajā tēmā lietoti šādi termini, lai aprakstītu kontu plānus:

- **Globāls** – kontu plāns, ko organizācija izmanto globālā mērogā. Vairākumā gadījumu jūs konsolidēsiet uz šo kontu plānu.
- **Lokāls** – kontu plāns, ko lieto juridiskas personas noteiktā valstī vai reģionā.
- **Koplietots** - kontu plāns, ko var izmantot vairāk nekā viena juridiska persona. Var koplietot gan globālo kontu plānu, gan lokālos kontu grafikus.

Jūs varat izveidot un koplietot vairākus kontu plānus. Koplietotu kontu plānu var izmantot vairāk nekā viena juridiska persona, bet katrai juridiskajai personai var piešķirt tikai vienu kontu plānu. Kontu plāns, ko izmanto juridiskā persona, tiek definēts lapā **Virsgrāmata**.

Izprojektējot kontu plānu, daudzu organizāciju mērķis ir globāls kontu plāns. Koplietota kontu plāna iespēja ļauj izveidot globālo kontu plānu. Ir atvieglojumi atsevišķa kontu plāna izveidošanai un lietošanai. Piemēram, vadība un kontrole, uzturēšana un pārskatu veidošana ir vieglāka.

Lielākā daļa organizāciju dod priekšroku globālam kontu plānam, un tas ir visvieglākais veids, ko ieviest. Tomēr dažām juridiskajām personām nepieciešams vietējais kontu plāns šādu iemeslu dēļ:

- Vietējās likumā noteiktās prasības
- Vietējo uzskaites standartu prasības
- Nozares prasības
- Uzņēmumam specifiskas pārskata un analīzes prasības

Ja jūsu organizācijai nepieciešams, lai juridiska persona izmantotu vietējo kontu plānu, tā īstenošanai ir pieejamas divas opcijas:

- Piešķiriet globālo kontu plānu un nosakiet citus līdzekļus vietējo prasību izpildei.
- Piešķiriet vietējo kontu plānu juridiskajai personai un definējiet attiecības ar globālo kontu plānu.

Organizācijas struktūra un pārskata struktūra nosaka izmantoto opciju.

[![ Diagramma, kas parāda, kā organizācijas struktūra nosaka, vai izmantot globālo vai lokālo kontu plānu](./media/local-chart-of-accounts-diagram.png)](./media/local-chart-of-accounts-diagram.png)

Ja juridiskajai personai ir piešķirts globālais kontu plāns, lai nodrošinātu vietējo pārskatu sniegšanas prasību izpildi, ir pieejamas šādas opcijas:

- Veikt lokālu konsolidēšanu.
- Lietojiet finanšu dimensiju, lai sekotu līdzi vietējam kontu plānam.
- Izveidojiet vietējos galvenos kontus globālajā kontu plānā.
- Veikt ārējo kartēšanu uz vietējo kontu plānu.

Ja juridiskajai personai ir piešķirts lokālais kontu plāns, lai nodrošinātu vietējo pārskatu sniegšanas prasību izpildi, patlaban ir pieejama tikai globālās konsolidēšanas opcija.

## <a name="global-chart-of-accounts-assigned-to-a-legal-entity"></a>Globālais kontu plāns, kas piešķirts juridiskajai personai

Ja globālais kontu plāns jāpiešķir juridiskajai personai, sistēmas konfigurēšanai ir pieejamas četras opcijas, kā aprakstīts iepriekš. Visām četrām opcijām ir konfigurēts viens kontu plāns, kas ir saistīts ar katru juridisko personu **Virsgrāmatas** lapā. Katra opcija tad izmanto atšķirīgu pieeju, lai atbilstu lokalizācijas prasībām. Tālāk norādītās sadaļas ieskicē augsta līmeņa darbības, lai konfigurētu sistēmu lokalizācijas prasībām. Tajos ir aprakstīts arī katras opcijas priekšrocības un trūkumi.

### <a name="do-local-consolidation"></a>Veikt lokālu konsolidēšanu

Lokālā konsolidācija ir ieteicama pieeja vietējo kontu plāna prasību izpildi un sistēmas funkcionalitātes priekšrocības, kas veidotas šim nolūkam.

#### <a name="set-up-consolidation-for-a-local-chart-of-accounts"></a>Iestatīt konsolidāciju lokālam kontu plānam

1. Izveidojiet vienu globālo kontu plānu, kas ietver visus nepieciešamos galvenos kontus.
2. Katrai juridiskajai personai **Virsgrāmatas** lapā piešķiriet globālo kontu plānu.
3. Izveidojiet konsolidācijas juridisko personu katrai pieprasītai lokalizācijai.
4. Izpildiet kādu no šīm darbībām:

    - Ja nepieciešama tikai viena lokalizācija, konfigurējiet konsolidācijas kontu **Galvenā konta** lapā vai izmantojiet **Konsolidācijas grupas** un **Papildu konsolidācijas kontu** lapas.
    - Ja nepieciešama vairāk nekā viena lokalizācija vai arī tad, ja nepieciešams tulkojums gan konta numuram, gan konta nosaukumam, izmantojiet **Konsolidācijas grupas** un **Papildu konsolidācijas kontu** lapas, lai atspoguļotu lokalizācijas prasības.

5. Palaidiet konsolidācijas procesu, lai pārveidotu vērtību no izcelsmes juridiskas personas, kas izmanto globālo kontu plānu, uz konsolidācijas uzņēmumu, kas izmanto vietējo kontu plānu.

#### <a name="advantages"></a>Priekšrocības

- Šī pieeja nodrošina konsekventu darbības veidu organizācijā.
- Ir veikts viens vietējās pozīcijas tulkojums.
- Šī pieeja atbalsta tulkojumu gan galvenā konta ID, gan katra galvenā konta nosaukumam.
- Tas atbalsta vairākas lokalizācijas.

#### <a name="disadvantages"></a>Trūkumi

- Tiek izveidots papildu konsolidācijas uzņēmums.
- Ir pabeigts papildu konsolidācijas process.
- Šī pieeja var ziņot par lokalizēto diagrammu tikai pēc konsolidācijas procesa pabeigšanas.

### <a name="use-a-financial-dimension-to-track-the-local-chart-of-accounts"></a>Lietojiet finanšu dimensiju, lai sekotu līdzi vietējam kontu plānam

Šī pieeja izmanto finanšu dimensiju, kur finanšu dimensijas vērtības parāda vietējos galvenos kontus, kas nepieciešami lokalizācijai. Tā darbojas labi, ja nepieciešama tikai viena lokalizācija. Tomēr tas kļūst mazāk lietojams, pievienojot vairāk lokalizāciju un finanšu dimensiju.

#### <a name="set-up-a-financial-dimension-for-a-local-chart-of-accounts"></a>Iestatiet finanšu dimensiju, lai sekotu līdzi lokālajam kontu plānam

1. Izveidojiet vienu globālo kontu plānu, kas ietver visus nepieciešamos galvenos kontus.
2. Katrai juridiskajai personai **Virsgrāmatas** lapā piešķiriet globālo kontu plānu.
3. Izveidojiet finanšu dimensiju, kas ataino vietējo kontu plānu.
4. Izveidojiet finanšu dimensiju vērtības, kas ataino vietējo kontu plānu galvenos kontus.
5. Atjauniniet konta struktūru tā, lai tā ietver finanšu dimensiju "vietējo kontu plānu".
6. Nodrošiniet, lai finanšu dimensijai "vietējais kontu plāns" vienmēr būtu vērtība un lai tā neatļauj tukšu vērtību. Apsveriet iespēju izmantot atvasinātās dimensijas vai fiksētas dimensijas.
7. Izveidojiet finanšu dimensiju kopu, kur "vietējais kontu plāns" finanšu dimensija ir pirmā atlasītā finanšu dimensija. Finanšu dimensiju kopu var izmantot, kad tiek ģenerēta apgrozījuma bilance.

#### <a name="advantages"></a>Priekšrocības

- Darbību līmenī pastāv gan globālie, gan lokālie kontu galvenie konti. Galvenais konts ir globāls, un finanšu dimensijas vērtība ir lokāla.
- Šī pieeja nodrošina reāllaika pārskatus un skatījumus gan no globālā finanšu amata, gan vietējā finanšu pozīcijas.

#### <a name="disadvantages"></a>Trūkumi

- Virsgrāmatas parametros, ja lauka **Summu kontam izmantotās vērtības** ir iestatītas uz **Uzskaites sadale**, finanšu dimensijas, kas apzīmē galveno kontu izdevumiem/aktīviem/ieņēmumiem, tiks nepareizi izmantotas debitoru parādu un kreditoru parādu kopsavilkuma kontam. Ieteicams iestatīt lauku pirmdokumentam, lai nodrošinātu pareizu finanšu dimensiju vērtību lietošanu.
- Ja nepieciešams daudz vietējo kontu plānu un visiem tiek lietota viena finanšu dimensija, izmantoto finanšu dimensiju vērtību saraksts var kļūt garš un ar to var būt grūti strādāt.
- Ja nepieciešams daudz vietējo kontu plānu un katra dimensija tiek izmantota, lai attēlotu katru no tiem, tad, pievienojot finanšu dimensijas un finanšu dimensiju kopas, sistēmas izmantojamību un veiktspēju var ietekmēt.
- Mēs iesakām rūpīgi izvērtēt finanšu dimensiju skaitu, kas nepieciešamas, vērtību skaitu katrā no tām un finanšu dimensiju kopu skaitu, jo visi šie faktori var ietekmēt sistēmas veiktspēju.

### <a name="create-local-main-accounts-in-the-global-chart-of-accounts"></a>Izveidojiet vietējos galvenos kontus globālajā kontu plānā

*Par ko jautāja kopijas redaktors:* Izmantojot šo pieeju, lokālie galvenie konti globālā kontu plānā ietver galvenos kontus vietējā kontu plānā globālajā kontu plānā.

*Sākotnējā versija:* lokālie galvenie konti globālā CoA pieejas ietvaros ir tas, ka lokālie CoA galvenie konti tiek iekļauti globālajā CoA.

*Ja ir šādi:* Šādā gadījumā lokālie galvenie konti vietējā kontu plānā tiek iekļauti globālā kontu plānā.


#### <a name="set-up-local-main-accounts-in-the-global-chart-of-accounts"></a>Iestatiet vietējos galvenos kontus globālajā kontu plānā

1. Izveidojiet vienu kontu plānu, kas ietver galvenos kontus gan globālajam kontu plānam, gan vietējam kontu plānam.
2. Katrai juridiskajai personai **Virsgrāmatas** lapā piešķiriet globālo kontu plānu.
3. Izveidojiet kontu kopsummu kontu plānā, lai summētu galvenos kontus, kas norāda vienu un to pašu nolūku.
4. Izveidojiet juridiskas personas ignorējumus katram vietējam kontam, lai novērstu citu juridisku personu darbības, kurām netika paredzēts lokālais konts.
5. Izveidojiet juridiskas personas ignorējumus katram globālajam kontam, lai novērstu darbības no lokalizācijas juridiskajām personām.

#### <a name="advantages"></a>Priekšrocības

- Reāllaika skatījums gan par globālo finanšu pozīciju, gan vietējo finanšu pozīciju ir pieejams konkrētos pārskatos un īpašos sistēmas skatos, piemēram, bilances finanšu pārskatā. Tai var arī piekļūt, kopsummas kontā izmantojot pogu **Periods**.
- Virsgrāmatas kontā nav papildu segmenta.

#### <a name="disadvantages"></a>Trūkumi

- Kopējā konta izmantošana un redzamība ir ierobežota. Piemēram, kopsummas konti nav redzami **Apgrozījuma bilances** saraksta lapā.
- Apkopei nepieciešams papildu darbs.
- Finanšu pārskatu veidošanai nepieciešams manuāls papildu darbs.

### <a name="do-external-mapping-to-the-local-chart-of-accounts"></a>Veikt ārējo kartēšanu uz vietējo kontu plānu

Globālajā kontu plānā tiek pieņemts, ka pārvaldāt kartēšanu un lokalizācijas ārpus sistēmas. Izmantojot šo pieeju, jūs tikko izveidojat vienu globālo kontu plānu Microsoft Dynamics 365 Finance un apstrādājiet prasības ārpus sistēmas.

#### <a name="set-up-external-mapping-to-a-local-chart-of-accounts"></a>Iestatīt ārējo kartēšanu uz vietējo kontu plānu

1. Izveidojiet vienu globālo kontu plānu, kas ietver visus nepieciešamos galvenos kontus.
2. Katrai juridiskajai personai **Virsgrāmatas** lapā piešķiriet globālo kontu plānu.
3. Veikt kartēšanu uz vietējo kontu plānu ārpus Finance.

#### <a name="advantages"></a>Priekšrocības

- Šī pieeja nodrošina konsekventu darbības veidu organizācijā.

#### <a name="disadvantages"></a>Trūkumi

- No sistēmas nav pieejams lokāls pārskats.
- Veidojot finanšu pārskatus, šī pieeja ir kļūdaina.

## <a name="local-chart-of-accounts-assigned-to-legal-entity"></a>Lokālais kontu plāns, kas piešķirts juridiskajai personai

Ja jūsu organizācija izlemj nelietojiet globālo kontu plānu juridiskajām personām, katram unikālajam lokālajam kontu plānam tiek izveidots atsevišķs kontu plāns. Pēc tam katra juridiskā persona ir saistīta ar atbilstošo kontu plānu **Virsgrāmatas** lapā.

### <a name="do-global-consolidation"></a>Veikt globālu konsolidēšanu

Izmantojot šo pieeju, konsolidētais uzņēmums tiek izmantots, lai apkopotu un kombinētu bilances no katra avota lokālā uzņēmuma kombinētajā globālajā kontu plānā konsolidētajā uzņēmumā. Šai pieejai nepieciešams uzturēt katra lokālā kontu plāna kartēšanu uz globālo kontu plānu konsolidētajā uzņēmumā.

#### <a name="set-up-global-consolidation"></a>Iestatīt globālu konsolidēšanu

1. Izveidojiet atsevišķu kontu plānu katrai juridiskajai personai, kam ir atšķirīgs vietējais kontu plāns. Ja kādai juridiskajai personai ir vienāds vietējais kontu plāns, nepieciešams tikai viens lokālais kontu plāns, un to var koplietot.
2. Katrai juridiskajai personai **Virsgrāmatas** lapā piešķiriet globālo kontu plānu.
3. Nav obligāti: izveidojiet kontu plānu katra konsolidācijas uzņēmuma globālajam kontu plānam, kuram ir cits globālais kontu plāns.
4. Izveidojiet konsolidācijas juridisko personu katram pieprasītais konsolidācijas līmenim un piešķiriet atbilstošu kontu plānu **Virsgrāmatas** lapā.
5. Izpildiet kādu no šīm darbībām:

    - Ja nepieciešama tikai viena konsolidācija, konfigurējiet konsolidācijas kontu **Galvenā konta** lapā.
    - Ja nepieciešama vairāk nekā viena lokalizācija vai arī tad, ja nepieciešams tulkojums gan konta numuram, gan konta nosaukumam, izmantojiet **Konsolidācijas grupas** un **Papildu konsolidācijas kontu** lapas, lai atspoguļotu lokalizācijas prasības.

6. Palaidiet konsolidācijas procesu, lai pārsūtītu bilances no lokālām juridiskajām personām uz konsolidēto juridisko personu. Šī konsolidētā juridiskā persona izmanto 5. solī definētos konsolidācijas kontus.

#### <a name="advantages"></a>Priekšrocības

- Vietējo grāmatvedības standartu formāts tiek pielietots vietēji.
- Šī pieeja sniedz vietējai finanšu komandai vieglāku darba veidu.

#### <a name="disadvantages"></a>Trūkumi

- Nav pieejams globālās pozīcijas reāllaika skats.
- Konsolidācijas procesu var palaist daudz bieži.

## <a name="additional-resources"></a>Papildu resursi

- [Sava kontu plāna plānošana](plan-chart-of-accounts.md)
- [Virsgrāmatu konfigurēšana](configure-ledger.md)
- [Finanšu dimensijas un grāmatošana](Default-dimensions.md#balancing-dimension)
- [Finanšu dimensiju kopas](financial-dimension-sets.md)
- [Konsolidēšanas un koriģēšanas pārskats](../budgeting/consolidation-elimination-overview.md)
- [Konsolidācijas kontu grupas un papildu konsolidācijas konti](../budgeting/consolidation-account-groups-consolidation-accounts.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
