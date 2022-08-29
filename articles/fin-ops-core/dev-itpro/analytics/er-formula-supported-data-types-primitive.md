---
title: Elektronisko pārskatu veidotāja atbalstītie primitīvie datu tipi
description: Šajā rakstā ir sniegta informācija par primitīviem datu veidiem, kas tiek atbalstīti Elektronisko pārskatu (ER) formulās.
author: kfend
ms.date: 06/02/2021
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 26c166744e1705baa9dcce6b93c76f110524b7d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284580"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a>Elektronisko pārskatu veidotāja atbalstītie primitīvie datu tipi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par primitīviem datu veidiem, kas tiek atbalstīti [Elektronisko pārskatu (ER)](general-electronic-reporting.md) izteiksmēs. Tālāk ir sniegta tabula ar primitīvo datu tipiem:

- [boolean](#boolean)
- [date](#date)
- [datetime](#datetime)
- [enumeration](#enumeration)
- [guid](#guid)
- [integer](#integer)
- [int64](#int64)
- [real](#real)
- [string](#string)

## <a name="boolean"></a><a name="boolean"></a>Būla

Primitīvais datu tips *boolean* ietver vērtību, kas tiek novērtēta kā *true* vai *false*. Varat izmantot rezervētos literāļa atslēgvārdus **Patiess** un **Aplams**, vietās, kur tiek sagaidīta *boolean* izteiksme. Noklusējuma vērtība ir *false*.

Datu tipa *boolean* iekšējais attēlojums ir *integer*. Datu tipa *integer* vērtība 0 (nulle) tiek novērtēta kā *false* un visas pārējās *integer* vērtības tiek novērtētas kā *true*. Kad [validējat](general-electronic-reporting-formula-designer.md#TestFormula) konfigurētu izteiksmi, kas atgriež *boolean* datu tipu [ER formulas veidotājā](er-advanced-formula-editor.md), testa rezultātu rūts parāda *0* (nulli), ja tiek atgriezta izteiksme *false*. Pretējā gadījumā testa rezultātu rūts būs *1*.

Datu tipam *boolean* nav netiešas konvertēšanas. Tomēr varat izmantot funkciju [TEXT](er-functions-text-text.md), lai *boolean* tieši konvertētu uz *string*:

- Vērtība *false* tiek konvertēta teksta virknē **Aplams**.
- Vērtība *true* tiek konvertēta teksta virknē **Patiess**.

> [!NOTE]
> Šī pārveidošana nav atkarīga no sniegtās valodas un kultūras [konteksta](er-design-multilingual-reports.md).

Salīdzināšanas [operatori](er-formula-language.md#Operators) ir vienīgais operatora veids, ko var izmantot ar *boolean* datu tipu. Tālāk norādītos operatorus var izmantot, lai salīdzinātu divas *boolean* vērtības: \<\> un =.

## <a name="date"></a><a name="date"></a>Datums

Primitīvais datu tips *date* ietver dienu, mēnesi un gadu. Datumus var iniciēt, izmantojot šādas funkcijas:

- [DATEVALUE](er-functions-datetime-datevalue.md)
- [NULLDATE](er-functions-datetime-nulldate.md)
- [SESSIONTODAY](er-functions-datetime-sessiontoday.md)
- [TODAY](er-functions-datetime-today.md)

Datu tips *date* var būt no 1900. gada 1. janvāra un līdz 2154. gada 31. decembrim. Noklusējuma vērtība ir **null** un iekšējais attēlojums ir datums no 1900. gada 1. janvāra.

Datu tipam *date* nav netiešas konvertēšanas. Tomēr varat izmantot tieši formulētas konvertēšanas funkcijas:

- [DATEFORMAT](er-functions-datetime-dateformat.md)
- [DATETODATETIME](er-functions-datetime-datetodatetime.md)
- [TEXT](er-functions-text-text.md)

Funkcija [ADDDAYS](er-functions-datetime-adddays.md) ļauj pievienot un atņemt dienas no datumiem. Šādā veidā datumu var mainīt noteiktu dienu skaitu uz priekšu un atpakaļ. Funkcija [DAYS](er-functions-datetime-days.md) ļauj atņemt datumus vienu no otra, aprēķinot starpību skaitu dienās. Papildinformāciju par *date* vērtību pārvēršanu skatiet sadaļā [ER funkciju saraksts datuma un laika kategorijā](er-functions-category-datetime.md).

Salīdzināšanas [operatori](er-formula-language.md#Operators) ir vienīgais operatora veids, ko var izmantot ar *date* datu tipu. Tālāk norādītos operatorus var izmantot, lai salīdzinātu divas *date* vērtības: \<\>, \<, \<=, =, \>, un \>=.

## <a name="datetime"></a><a name="datetime"></a>Datetime

Primitīvais datu tips *datetime* apvieno *date* tipu un vērtību, kas atspoguļo laiku, kas pagājis kopš pusnakts. Laiks tiek izteikts stundās, minūtēs, sekundēs un daļskaitļos. Vērtībā *datetime* ir ietverta arī laika zonas informācija.

Datu tips *datetime* var būt no 1900. gada 1. janvāra (1900-01-01T00:00:00.0000000+00:00 aprites [formātā](/dotnet/standard/base-types/standard-date-and-time-format-strings)) un līdz 2154. gada 31. decembrim (2154/12/31T11:59:59.9999999+00:00 aprites formātā). Mazākā laika vienība datu tipam *datetime* ir viena desmit miljonā daļa no sekundes.

> [!NOTE]
> Ja **hh** [apzīmētājs](/dotnet/standard/base-types/standard-date-and-time-format-strings) tiek izmantots stundām, laika vērtības virs 12:59:59:9999999 nevar interpretēt kā derīgus laikus.
>
> Ja **HH** apzīmētājs tiek izmantots stundām, laika vērtības virs 23:59:59:9999999 nevar interpretēt kā derīgus laikus.

Noklusējuma vērtība ir **null** un iekšējais attēlojums ir datums no 1900. gada 1. janvāra (1900-01-01T00:00:00.0000000+00:00 aprites formātā).

Datumus un laikus var iniciēt, izmantojot šādas funkcijas:

- [DATETIMEVALUE](er-functions-datetime-datetimevalue.md)
- [NULNULLDATETIMELDATE](er-functions-datetime-nulldatetime.md)
- [SESSIONNOW](er-functions-datetime-sessionnow.md)
- [NOW](er-functions-datetime-now.md)

Datu tipam *datetime* nav netiešas konvertēšanas. Tomēr varat izmantot tieši formulētas konvertēšanas funkcijas:

- [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md)
- [TEXT](er-functions-text-text.md)

Papildinformāciju par *datetime* vērtību pārvēršanu skatiet sadaļā [ER funkciju saraksts datuma un laika kategorijā](er-functions-category-datetime.md).

Salīdzināšanas [operatori](er-formula-language.md#Operators) ir vienīgais operatora veids, ko var izmantot ar *datetime* datu tipu. Tālāk norādītos operatorus var izmantot, lai salīdzinātu divas *datetime* vērtības: \<\>, \<, \<=, =, \>, un \>=.

## <a name="enumeration"></a><a name="enumeration"></a>Uzskaitījums

Primitīvais datu tips *enumeration* ir literāļu saraksts. Varat izmantot uzskaitījumus, kas ir definēti programmas [avota kodā](../dev-ref/xpp-data-primitive.md#enum). Kā arī varat ieviest savus uzskaitījumus ER datu modeļa un ER formāta komponentos.

Programmas datu tipu *enumeration* var izmantot jebkurās ER modeļa kartēšanas un ER formāta izteiksmēs.

Attēlā parādīts, kā rediģējamam ER datu modelim varat pievienot **CustVendCorrectiveReasonCode** modeļa uzskaitījumu.

[![Modeļa uzskaitījuma konfigurēšana ER datu modeļu veidotājā.](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)

Modeļa *enumeration* var izmantot jebkurās ER modeļa kartēšanas un ER formāta izteiksmēs, kas izveidotas datu modelī, kurā ir ieviests datu tips *enumeration*.

Attēlā parādīts, kā rediģējamam ER formātam var pievienot **Sarakstu ar Natura apgrieztās maksāšanas apakškategoriju** formāta uzskaitījumu.

[![Formāta uzskaitījuma konfigurēšana ER formāta veidotājā.](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)

Formāta *enumeration* var izmantot tikai ER formāta izteiksmēs, kurās ir ieviests datu tips *enumeration*.

Izmantojiet atbilstošu ER datu avotu tipu, lai ieviestu noteiktu uzskaitījumu konfigurētajā ER komponentā kā konstanti vai kā vērtību, ko izmanto lietotājs, kurš izpildlaikā palaidis dialoglodziņā definēto ER risinājumu.

- Programmas uzskaitījumiem var piekļūt, izmantojot **Dynamics 365 for Operations \ Uzskaitījums** un **Vispārīgi \ Lietotāja ievades parametri** datu avotos. Attēlā parādīts, kā rediģējamam ER formātam var pievienot **appenumNoYes** un **uipNoYes** datu avotus, kas attiecas uz **NoYes** programmu uzskaitījumu.

    [![Programmas uzskaitījuma datu avotu pievienošana ER formāta veidotājā.](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)

- Datu modeļa uzskaitījumiem var piekļūt, izmantojot **Datu modelis \ Uzskaitījums** un **Datu modelis \ Uzskaitījums lietotāja ievades parametriem** datu avotos. Attēlā parādīts, kā rediģējamam ER formātam var pievienot **CustVendCorrectiveReasonCode** datu avotu, kas attiecas uz **CustVendCorrectiveReasonCode** datu modeļa uzskaitījumu.

    [![Modeļa uzskaitījuma datu avotu pievienošana ER formāta veidotājā.](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)

- Formāta uzskaitījumiem var piekļūt, izmantojot **Formāts \ Uzskaitījums** un **Formāts \ Uzskaitījums lietotāja ievades parametriem** datu avotos. Attēlā parādīts, kā rediģējamam ER formātam var pievienot **NaturaReverseCharge** datu avotu, kas attiecas uz **Natura apgrieztās maksāšanas apakškategoriju** formāta uzskaitījumu.

    [![Formāta uzskaitījuma datu avotu pievienošana ER formāta veidotājā.](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)

Datu tipam *enumeration* nav netiešas konvertēšanas. Tomēr varat izmantot konvertēšanas funkciju [TEXT](er-functions-text-text.md), lai konvertētu *enumeration* uz teksta virkni. Šī konvertēšana nav pakārtota valodai. Lai uzzinātu, kā *enumeration* vērtību var saistīt ar atbilstošajām valodas etiķetēm, skatiet [LISTOFFIELDS](er-functions-list-listoffields.md) un [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md) funkciju lietojuma piemērus.

Salīdzināšanas [operatori](er-formula-language.md#Operators) ir vienīgais operatora veids, ko var izmantot ar *enumeration* datu tipu. Tālāk norādītos operatorus var izmantot, lai salīdzinātu divas *enumeration* vērtības: \<\> un =.

## <a name="guid"></a><a name="guid"></a>Guid

Primitīvais datu tips *guid* ietver vispārējā unikālā identifikatora (GUID) vērtību. GUID ir vērtība, ko var izmantot visos datoros un tīklos, kur nepieciešams unikāls identifikators. Maz ticams, ka numurs varētu atkārtoties. Derīgs GUID atbilst visām tālāk norādītajām specifikācijām:

- Jābūt 32 heksadecimāliem cipariem.
- Turklāt ir jābūt četrām domuzīmes rakstzīmēm, kas iegultas šādās vietās: 8-4-4-4-12.
- Turklāt neobligātās figūriekavas \{\} var tikt pievienotas virknes sākumā un beigās. Piemēram, gan **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}**, gan **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** ir derīgas GUID virknes.
- Tomēr kopsummā ir jābūt 36 vai 38 rakstzīmēm atkarībā no tā, vai ir pievienotas figūriekavas.
- Burti, kas tiek lietoti kā heksadecimālie cipari, var būt lielie burti (A–F), mazie burti (a–f) vai jaukti burti.

Var tikt izmantotas tieši formulētas konvertēšanas funkcijas:

- [GUIDVALUE](er-functions-text-guidvalue.md)
- [TEXT](er-functions-text-text.md)

Salīdzināšanas [operatori](er-formula-language.md#Operators) ir vienīgais operatora veids, ko var izmantot ar *guid* datu tipu. Tālāk norādītos operatorus var izmantot, lai salīdzinātu divas *guid* vērtības: \<\> un =.

## <a name="integer"></a><a name="integer"></a>Vesels skaitlis

Primitīvais datu tips *integer* apzīmē skaitli, kuram nav decimāldaļu. Veseli skaitļi tiek izmantoti kā kontroles mainīgie atkārtotos pārskatos vai kā indeksi ierakstu sarakstos.

Datu tipa *integer* literālis ir vesels skaitlis, kas ievadīts tieši ER [izteiksmē](general-electronic-reporting-formula-designer.md#formula-designer-overview) (formulā), piemēram, **12345**. Datu tips *integer* ir 32 bitus garš. Noklusējuma vērtība ir **0** un iekšējais attēlojums ir garš numurs. Datu tips *integer* tiek automātiski konvertēts uz *real*.

Turklāt var tikt izmantotas tieši formulētas konvertēšanas funkcijas:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Diapazons datu tipam *integer* ir \[-2,147,483,647 : 2,147,483,647\]. Visus šī diapazona veselos skaitļus var izmantot kā literāļus.

Visus salīdzināšanas un matemātiskos [operatorus](er-formula-language.md#Operators) var izmantot ar *integer* datu tipu.

## <a name="int64"></a><a name="int64"></a>Int64

Primitīvais datu tips *int64* apzīmē skaitli, kuram nav decimāldaļu. *Int64* vērtības tiek izmantotas kā kontroles mainīgie atkārtotos pārskatos vai ierakstu identifikatoros.

Datu tips *int64* ir 64 bitus garš. Noklusējuma vērtība ir **0** un iekšējais attēlojums ir garš numurs. Datu tips *int64* tiek automātiski konvertēts uz *real*.

Turklāt var tikt izmantotas tieši formulētas konvertēšanas funkcijas:

- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Diapazons datu tipam *int64* ir \[-9,223,372,036,854,775,807 : 9,223,372,036,854,775,807\].

Visus salīdzināšanas un matemātiskos [operatorus](er-formula-language.md#Operators) var izmantot ar *int64* datu tipu.

## <a name="real"></a><a name="real"></a>Reāls

Primitīvo datu tips *real* var saturēt decimālskaitļu vērtības papildus veseliem skaitļiem. Decimālus literāļus var izmantot jebkur, kur ir paredzēts *real*. Decimālā literāļa vērtība ir decimāldaļa, kas ievadīta tieši kodā, piemēram, **2,19**.

> [!NOTE]
> ER izteiksmēs punkts (.) vienmēr tiek izmantots kā decimāldaļu atdalītājs.

Reālus var izmantot visās izteiksmēs, un tos var lietot gan ar salīdzināšanas, gan aritmētiskajiem operatoriem. Datu tipam *real* ir ievērojama 16 ciparu precizitāte. Noklusējuma vērtība datu tipam *real* ir **0.0** un iekšējais attēlojums ir bināri kodēts ciparu (BCD) numurs. BCD kodējums ļauj precīzi attēlot vērtības, kas dalās ar 0,1. Diapazons datu tipam *real* ir no -(10)<sup>127</sup> līdz (10)<sup>127</sup>. Visus reālus šajā diapazonā var izmantot kā literāļus ER izteiksmēs.

Datu tipam *real* nav netiešas konvertēšanas. Tomēr varat izmantot tālāk norādītās funkcijas, lai *real* tieši konvērtētu uz citiem datu tipiem un citus datu tipus konvertētu uz *real*:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)
- [VALUE](er-functions-conversion-value.md)

Visus salīdzināšanas un matemātiskos [operatorus](er-formula-language.md#Operators) var izmantot ar *real* datu tipu.

## <a name="string"></a><a name="string"></a>Virkne

Primitīvais datu tips *string* apzīmē rakstzīmju secību, kas tiek izmantota tekstos, kontu numuros, adresēs un tālruņu numuros.

*String* literāļi ir rakstzīmes, kas ietvertas pēdiņās (""). *String* literāļus var izmantot vietās, kur ER izteiksmēs ir sagaidāmas *string* vērtības. Virknes var tikt izmantotas loģiskās izteiksmēs, piemēram, salīdzinājumos. Var arī savienot *string* vērtības, izmantojot **\&** operatorus vai [CONCATENATE](er-functions-text-concatenate.md) funkciju.

> [!NOTE]
> Ja savienojat divas *string* vērtības un vēlaties, lai iegūtā *string* ietvertu vairāk nekā vienu rindu, izmantojiet rindas pārtraukuma atdalītāju starp vērtībām. TEXT izvadei šis atdalītājs var būt rakstzīme, kas tiek ģenerēta, izmantojot izteiksmi [CHAR](er-functions-text-char.md)(10) vai CHAR(13). HTML formātam tas var būt **\<br\>** tags.

Noklusējuma vērtība datu tipam *string* ir tukša teksta virkne, kam nav rakstzīmju un iekšējais attēlojums ir rakstzīmju saraksts.

Virknēm nav iespējama automātiska konvertēšana. Tomēr var tikt izmantotas tieši formulētas konvertēšanas funkcijas:

- [CHAR](er-functions-text-char.md)
- [FORMAT](er-functions-text-format.md)
- [LEFT](er-functions-text-left.md)
- [LEN](er-functions-text-len.md)
- [MID](er-functions-text-mid.md)
- [PADLEFT](er-functions-text-padleft.md)
- [REPLACE](er-functions-text-replace.md)
- [RIGHT](er-functions-text-right.md)
- [TEXT](er-functions-text-text.md)
- [TRANSLATE](er-functions-text-translate.md)
- [TRIM](er-functions-text-trim.md)
- [UPPER](er-functions-text-upper.md)

Papildinformāciju par *string* vērtību pārvēršanu skatiet sadaļā [ER funkciju saraksts teksta kategorijām](er-functions-category-text.md).

Datu tips *string* var saturēt nenoteiktu rakstzīmju skaitu.

Visus salīdzināšanas [operatorus](er-formula-language.md#Operators) var izmantot ar *string* datu tipu.

## <a name="additional-resources"></a>Papildu resursi

- [Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)
- [Elektronisko pārskatu veidošanas formulu valoda](er-formula-language.md)
- [Atbalstītie saliktie datu tipi](er-formula-supported-data-types-composite.md)
