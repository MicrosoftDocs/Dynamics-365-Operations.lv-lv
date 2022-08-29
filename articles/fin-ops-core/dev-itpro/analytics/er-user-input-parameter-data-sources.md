---
title: Izmantot LIETOTĀJA IEVADES PARAMETRU datu avotus, lai norādītu pārskata parametrus
description: Šajā rakstā skaidrots, kā izmantot LIETOTĀJA IEVADES PARAMETRU datu avotus, lai norādītu parametrus pārskatiem, ko ģenerējiet.
author: kfend
ms.date: 04/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.27
ms.custom: 220314
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: c6d0f1a0d9c5eb70a9812459a25d5b14407cce7a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278713"
---
# <a name="use-user-input-parameter-data-sources-to-specify-parameters-for-a-report"></a>Izmantot LIETOTĀJA IEVADES PARAMETRU datu avotus, lai norādītu pārskata parametrus

[!include[banner](../includes/banner.md)]

Veidojot elektronisko [pārskatu](general-electronic-reporting.md) (ER) [modeļu](er-overview-components.md#model-mapping-component) kartēšanu un ER [formāta](er-overview-components.md#format-component) komponentus, *varat izmantot LIETOTĀJA IEVADES PARAMETRA* tipa datu avotus, lai iegūtu nepieciešamās vērtības, kuras var norādīt datu ievades laukos dialoglodziņa izpildlaikā, pirms sākas ER formāta izpilde. Šajā rakstā ir aprakstīti pašlaik *atbalstītie* LIETOTĀJA IEVADES PARAMETRU datu avoti.

## <a name="mandatory-properties"></a><a name="mandatory-properties"></a> Obligātie rekvizīti

Katra LIETOTĀJA IEVADĪTĀ PARAMETRA tipa datu avotiem ir jānorāda *šādi* rekvizīti:

- **Laukā** Nosaukums ievadiet datu avota iekšējo nosaukumu. Šo nosaukumu var lietot citās izteiksmēs [un](er-formula-language.md) konfigurētā modeļa kartēšanas vai formāta komponenta saistīšanā.

## <a name="optional-properties"></a><a name="optional-properties"></a> Neobligāti rekvizīti

Lietotāja ievades parametra tipa datu avotiem pēc izvēles var norādīt *šādus rekvizītus*:

- Laukā **Iezīme** norādiet iezīmi, kas izpildlaika dialoglodziņā tiek izmantota saistītam datu ievades laukam. Dažādiem valodu kodiem varat pievienot citu iezīmes tekstu, aktivizējot lauku **Iezīme un pēc tam atlasot Tulkot** **.**
- Ja ir atlasīts rediģējams lietotāja ievades PARAMETRA tipa datu avots, laukā Palīdzība norādiet palīdzības tekstu, **·** **·** **kas** izstrādes laikā tiek rādīts formāta veidotāja lapas vai modeļu kartēšanas veidotāja lapas apakšā.*·* Šis teksts var sniegt papildu informāciju par datu avotu, lai palīdzētu lietotājiem, kad tie konfigurē rediģējamu formātu vai modeļa kartēšanas komponentu. Dažādiem valodu kodiem var pievienot dažādus palīdzības tekstus, atlasot **Tulkot**.

    > [!NOTE]
    > Poga **Tulkot**, kuru var [izmantot](er-design-multilingual-reports.md#format-component), lai pievienotu valodai specifiskas iezīmes un tekstu, kļūst pieejama tikai pēc datu avota pievienošanas, izmaiņu saglabāšanas un pēc tam atkārtoti atvērt datu avotu rediģēšanai.

- Laukā **Tikai lasāms** konfigurējiet izteiksmi, kas atgriež *[Būla](er-formula-supported-data-types-primitive.md#boolean)* vērtību.

    - Ja konfigurētā izteiksme izpildlaikā atgriež vērtību Patiess **, saistītais datu ievades** lauks dialoglodziņā parādās nedarbojas, un tās vērtību nevar mainīt.
    - Ja konfigurētā izteiksme izpildlaikā atgriež vērtību Aplams vai arī nav konfigurēta izteiksme, saistītais datu ievades **lauks** ir pieejams dialoglodziņā, un tās vērtību var mainīt.

- Laukā **Noklusētā** vērtība konfigurējiet izteiksmi, kas atgriež atsauces parametra tipa vērtību. Šo vērtību var izmantot, lai izpildlaikā aizpildītu saistīto datu ievades lauka noklusēto vērtību.

    Izpildot ER formātu, vērtība, ko ievadāt saistītajā datu ievades laukā, izpildlaika dialoglodziņā, tiek saglabāta atmiņā kā iepriekš izmantotā vērtība. Iepriekš izmantotās vērtības tiek saglabātas atsevišķi katram laukam, palaižot ER formātu, pašreizējo lietotāju un pašreizējo organizāciju (uzņēmumu).

    - Iestatiet opciju **Vienmēr atiestatīt noklusējuma vērtību** **uz Jā** **·**, ja noklusējuma vērtības izteiksmes atgrieztā vērtība vienmēr jāizmanto kā noklusējuma vērtība neatkarīgi no iepriekš lietotās vērtības.
    - Iestatiet opciju **Vienmēr atiestatīt** **uz noklusējuma vērtību uz Nē** **·**, ja vērtība, ko atgriezusi noklusējuma vērtības izteiksmes vērtība, ir jāizmanto kā noklusējuma vērtība tikai tad, ja trūkst iepriekš izmantotās vērtības.

    > [!NOTE]
    > Ja opcija Vienmēr atiestatīt **noklusējuma vērtību tiek** iestatīta uz **Jā**, izteiksme ir jākonfigurē laukā **Noklusējuma** vērtība.

- Ja opcija Atļaut vairākas **atlases tiek** iestatīta uz **Jā**, izpildlaikā konfigurētam parametram varat atlasīt vairākas vērtības. Ja iestatāt to uz **Nē**, varat atlasīt tikai vienu vērtību.

    > [!NOTE]
    > Šī opcija nav piemērojama visiem LIETOTĀJU IEVADES *PARAMETRU* tipiem. Dizaina laikā tiek izmetts izņēmums, lai informētu lietotāju, ka konfigurētais lietotāja ievades parametrs neatbalsta vairākas atlases, un ka var atlasīt vai ievadīt tikai vienu vērtību.
    >
    > Iestatot opciju Atļaut **vairākas atlases** **kā** Jā un **laukā** Noklusējuma vērtība norādījāt izteiksmi, šo izteiksmi var izmantot tikai vienas noklusējuma vērtības iestatīšanai.

- Atlasiet opciju **Rediģēt** redzamību, lai norādītu, vai konfigurētais parametrs izpildlaika dialoglodziņā ir jārāda.

    > [!NOTE]
    > LIETOTĀJA IEVADES PARAMETRA tipa datu avotu noklusējuma *redzamība* ir atkarīga no ER komponenta, kas tos ietver.
    >
    > - Ja datu avots ir konfigurēts formāta komponentā, tas ir redzams pēc noklusējuma.
    > - Ja datu avots ir konfigurēts modeļa kartēšanas komponentā, tas ir redzams tikai tad, ja datu avota vērtība ietekmē rezultātu, kad tiek palaists ER komponents. Piemēram, esat pievienojis datu avotu, taču to neizmantoja pašreizējā modeļa kartēšanas komponenta izteiksmēs un saistīšanā. Šajā gadījumā pēc noklusējuma atbilstošais datu ievades lauks izpildlaikā netiks rādīts dialoglodziņā. 

    Formulas **veidotāja** lapā formulas **laukā** konfigurējiet izteiksmi, kas atgriež Būla *vērtību*.

    - Ja konfigurētā izteiksme izpildlaikā atgriež vērtību Patiess **vai arī nav konfigurēta izteiksme, izpildlaikā saistītie datu ievades** lauki ir redzami dialoglodziņā.
    - Ja konfigurētā izteiksme atgriež vērtību **Aplams**, saistītais datu ievades lauks izpildlaika dialoglodziņā ir slēpts. Ja izpildlaikā to izsauc citas izteiksmes, tas atgriež noklusējuma vērtību, iepriekš izmantoto vērtību vai pašreizējā datu tipa vērtības noklusējumu atkarībā no citiem iestatījumiem.

## <a name="type-specific-properties"></a>Tipa specifiskie rekvizīti

### <a name="application-dependent-user-input-parameter"></a>No programmas atkarīga lietotāja ievades parametrs

Izmantojiet vispārējā **lietotāja** \> **·** Microsoft Dynamics ievades parametra tipa datu avotu, lai iegūtu nepieciešamo datu tipa vērtību vai vērtības, kas ir norādītas pašreizējai 365 Finanšu programmas instancei. Kad jūs pievienojiet šī tipa datu avotu ER komponentam, norādiet šādus rekvizītus:

- Laukā **Operāciju datu tipa nosaukums (EDT, uzskaitījums)** atlasiet programmas paplašināto [datu tipu (EDT)](../extensibility/extensible-edts.md) vai programmas uzskaitījumu.

> [!NOTE]
> Mainot operāciju datu tipa nosaukumu (EDT, uzskaitījumu) **·** **atsauci šī LIETOTĀJA IEVADES parametra tipa rediģējamā datu avotā, ieteicams pārskatīt izteiksmes** **·** *·*, kas ir konfigurētas laukos Tikai lasāms un Noklusējuma vērtība.

Šajā attēlā redzami datu avota `$TaxRegNum` rekvizīti, kas tika konfigurēti **Instat XML (DE)** ER formāta konfigurācijā. Šis datu avots ir konfigurēts *izmantot apraksta* EDT **·**, lai izpildlaikā nodokļu reģistrācijas numura datu ievades lauku piedāvātu dialoglodziņā.

![LIETOTĀJA IEVADES PARAMETRA tipa datu avota rekvizīti, kas atrodas formāta veidotāja lapas dialoglodziņā.](./media/er-user-input-parameter-data-sources-01.png)

Šajā attēlā parādīts dialoglodziņš **, kas tiek rādīts izpildlaikā, kad Instat XML (DE)** ER formāta konfigurācija tiek [palaista, lai ģenerētu](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md) Intrastat deklarāciju. Ievērojiet, ka datu **ievadei ir** pieejams konfigurētais nodokļu reģistrācijas numura lauks.

![Intrastat pārskata dialoglodziņš ER formāta veidošanai Intrastat lapā.](./media/er-user-input-parameter-data-sources-02.png)

### <a name="data-model-enumeration-user-input-parameter"></a>Datu modeļa uzskaitījuma lietotāja ievades parametrs

Izmantojiet datu modeļa **uzskaitījuma** \> **lietotāja ievades parametra**[tipa datu avotu, lai iegūtu viena datu modeļa uzskaitījuma nepieciešamo vērtību vai vērtības.](er-formula-supported-data-types-primitive.md#enumeration) Kad jūs pievienojiet šī tipa datu avotu ER komponentam, norādiet šādus rekvizītus:

- Laukā **Modelis** norādiet atsauci uz pamatdatu modeli.
- **Modeļu uzskaitījuma** laukā norādiet atsauci uz atsauces datu modeļa uzskaitījumu.
- Laukā **Versija** atlasiet pārskatījuma numuru ER datu modeļa komponentam, kas satur atsauces modeļa uzskaitījumu.

    > [!TIP]
    > Izstrādes laikā varat atstāt lauku Versija tukšu, lai piekļūtu uzskaitījumu sarakstam atsauces datu modeļa komponentam, **kas** atrodas atbilstošās ER datu modeļa konfigurācijas melnraksta versijā. Šādā veidā var vienlaicīgi rediģēt sava modeļa kartēšanas vai formāta komponenta melnraksta versiju un pamatdatu modeļa komponenta melnraksta versiju.
    >
    > Tomēr ievērojiet, ka **lauku** Versija var atstāt tukšu tikai modeļa kartēšanas vai formāta komponenta melnraksta versijā. Ja maināt **ER** **modeļa** kartēšanas statusu vai formāta konfigurāciju no Melnraksts uz Pabeigtu, šis lauks automātiski tiek aizpildīts ar augstāko modeļa pārskatījuma numuru, kas ir pieejams pašreizējā Finanšu instancē. Ja tiek ieviests jauns uzskaitījums vai jauna uzskaitījuma vērtība pamatdatu modeļa melnraksta versijā un atsaucaties uz to rediģējamā modeļa kartēšanas vai formāta komponentā, pabeidziet šo bāzes datu modeļa konfigurācijas melnraksta versiju pirms ir pabeigta ER modeļa kartēšanas vai formāta konfigurācijas melnraksta versija. Pretējā gadījumā izņēmums "Ceļš nav atrasts" tiks parādīts, ja modeļa kartēšanas vai formāta konfigurācijas statusu mainīsiet no Melnraksts **uz** **Pabeigts**. Ziņojums jūs informēs, ka bāzes datu modelī trūkst atsauces uzskaitījuma vai uzskaitījuma vērtības.

Šajā attēlā redzami datu avota `$ReportDirection` rekvizīti, kas tika konfigurēti **Instat XML (DE) Contoso** ER formāta konfigurācijā. Instat **XML (DE) Contoso** konfigurācija ir atvasināta [no](general-electronic-reporting.md#Configuration) **Instat XML (DE)** konfigurācijas. Šis datu avots ir konfigurēts *ReportDirection modeļa* uzskaitījuma izmantošanai, lai izpildlaikā piedāvātu atbilstošu uzmeklēšanas lauku dialoglodziņā.

![LIETOTĀJA IEVADES PARAMETRA tipa datu avota rekvizīti, kas atrodas formāta veidotāja lapas dialoglodziņā.](./media/er-user-input-parameter-data-sources-03.png)

### <a name="format-enumeration-user-input-parameter"></a>Formāta uzskaitījuma lietotāja ievades parametrs

Izmantojiet formāta uzskaitījuma **uzskaitījuma lietotāja** \> **ievades** parametra tipa datu avotu, lai iegūtu viena formāta uzskaitījuma nepieciešamo vērtību vai vērtības. Kad jūs pievienojiet šī tipa datu avotu ER komponentam, norādiet šādus rekvizītus:

- Laukā **Formāta uzskaitījums** norādiet rediģējamā formāta uzskaitījumu.

> [!NOTE]
> Šī tipa datu avotus var konfigurēt tikai rediģējama formāta komponenta tvērumā.

## <a name="additional-resources"></a>Papildu resursi

[Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)

[USER INPUT PARAMETER veida datu avota vērtību iniciēšana no avota koda](er-initiate-uip-data-source-value-from-source-code.md)
