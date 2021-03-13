---
title: Kolonnu definīcijas finanšu pārskatos
description: Šajā rakstā ir sniegta informācija par kolonnu definīcijām. Kolonnas definīcija ir pārskata komponents jeb veidošanas bloks, kas nosaka katras kolonnas saturu pārskatā.
author: ShylaThompson
manager: AnnBe
ms.date: 10/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 106601
ms.assetid: 66e72a48-edab-4e9d-815f-596a1623c258
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 820604fac96f5c86be3f7206ca88b3eb1fc6c32a
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093113"
---
# <a name="column-definitions-in-financial-reports"></a>Kolonnu definīcijas finanšu pārskatos

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par kolonnu definīcijām. Kolonnas definīcija ir pārskata komponents jeb veidošanas bloks, kas nosaka katras kolonnas saturu pārskatā. Tāpat kā rindas definīcijas pamata kolonnu definīcijas var izmantot vairākos pārskatos.

## <a name="create-and-modify-a-column-definition"></a>Izveidot un modificēt kolonnas definīciju

Kolonnas definīcija var saturēt divas līdz 255 kolonnas.

### <a name="create-a-column-definition"></a>Kolonnas definīcijas izveidošana

1. Pārskata veidotājā, navigācijas rūtī noklikšķiniet uz **Kolonnas definīcijas**.
2. Izvēlnē **Fails** noklikšķiniet uz **Jauns** un pēc tam uz **Kolonnas definīcija**.
3. Pievienojiet kolonnas definīcijas saturu.

### <a name="open-a-column-definition"></a>Kolonnas definīcijas atvēršana

1. Pārskata veidotājā, navigācijas rūtī noklikšķiniet uz **Kolonnas definīcijas**.
2. Veiciet dubultklikšķi uz kolonnas definīcijas, lai to atvērtu.

### <a name="add-a-column-to-a-column-definition"></a>Kolonnas pievienošana kolonnas definīcijai

1. Pārskatu veidotājā noklikšķiniet uz **Kolonnas definīcijas** un atveriet modificējamo kolonnas definīciju.
2. Atlasiet kolonnu, kur ir jāievieto jauna kolonna.
3. Izvēlnē **Rediģēt** noklikšķiniet uz **Ievietot kolonnu**. Jaunā kolonna tiek parādīta pa kreisi no jūsu atlasītās kolonnas.

### <a name="delete-a-column-from-a-column-definition"></a>Kolonnas dzēšana no kolonnas definīcijas

1. Pārskatu veidotājā noklikšķiniet uz **Kolonnu definīcijas** un pēc tam atveriet modificējamo kolonnas definīciju.
2. Atlasiet dzēšamo kolonnu.
3. Izvēlnē **Rediģēt** noklikšķiniet uz **Dzēst kolonnu**.

## <a name="contents-of-a-column-definition"></a>Kolonnas definīcijas saturs
Kolonnas definīcijā ietilpst tālāk uzskaitīta informācija.

- Rindas definīcijas aprakstu kolonna
- Summu kolonnas, kurās ir redzami dati no finanšu datiem vai aprēķiniem, kuru pamatā ir citi dati kolonnas definīcijā
- Formatēšanas kolonnas
- Atribūtu kolonnas

Šī informācija tiek rādīta tālāk norādītajās kolonnas definīcijas sadaļās.

- Kolonnas definīcijas galveņu apgabalā ir galvenes teksts un pārskatā redzamais formatējums. Galveni var attiekties uz vienu datu kolonnu, var aptvert vairākas kolonnas vai var attiekties uz kolonnām pēc nosacījuma. Kolonnas definīcijā var būt tik kolonnu galveņu rindu, cik nepieciešams.

    > [!NOTE]
    > Kolonnu galvenes attiecas uz katru pārskata datu kolonnu. Pārskatu galvenes attiecas uz visu pārskatu. Jūs varat definēt pārskata galvenes pārskata definīcijas cilnē **Galvenes un kājenes**.

- Kolonnu detalizētās informācijas rindas kolonnas definīcijā ir rindas zem galveņu rindām. Kolonnu detalizētās informācijas rindas nosaka pārskatā ietverto informāciju. Nākamajā tabulā ir uzskaitītas un aprakstītas kolonnu detalizētās informācijas rindas.

    | Kolonnas detalizētās informācijas rindas nosaukums                                                | Apraksts                                                                                            |
    |-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
    | Kolonnas tips                                                           | (Obligāts) Norādiet šajā kolonnā esošo datu tipu.                                                     |
    | Uzskaites kods/atribūtu kategorija                                          | Norādiet finanšu datu informāciju **FD** un **ATTR** tipu kolonnās.                       |
    | Finanšu gads Periods Ietvertie periodi                                    | Norādiet finanšu datu informāciju **FD** tipa kolonnām.                                     |
    | Formula                                                               | Norādiet aprēķina formulu **CALC** tipa kolonnām.                                        |
    | Kolonnas platuma Papildu atstarpes pirms kolonnas Formāta ignorēšana Drukas vadība | Norādiet īpašas formāta opcijas.                                                                        |
    | Kolonnas ierobežojumi                                                   | Ierobežojiet datus.                                                                                         |
    | Pārskatu vienība                                                        | Ierobežojiet kolonnu, lai tā rādītu datus tikai norādītajai pārskatu vienībai.                      |
    | Valūtas attēlojums Valūtas filtrs                                      | Formatējiet valūtu.                                                                                       |
    | Dimensiju filtrs                                                      | Norādiet filtru, ar ko datus ierobežot, izmantojot noteiktas finanšu datu pārskatu vienības.                           |
    | Atribūtu filtrs                                                      | Norādiet filtru, ar ko ierobežot finanšu datus.                                                       |
    | Sākuma datums Beigu datums                                                   | Ierobežojiet finanšu datus, izmantojot konkrētus datumus.                                                         |
    | Pamatojums                                                         | Līdziniet rindas definīcijā norādīto apraksta tekstu pa kreisi, pa vidu vai pa labi. |

## <a name="column-restrictions-in-a-column-definition"></a>Kolonnas ierobežojumi kolonnas definīcijā
Kolonnas ierobežojumus var izmantot, lai norādītu, kā kolonnas definīcijā ir jāizmanto dati un jāaprēķina vērtības. Turklāt varat ierobežot pārskata kolonnu, izmantojot konkrētu vienību vai konkrētus datus.

> [!NOTE]
> Izmantojot kodu **Kolonnas ierobežojums**, tiek ignorēti visi konfliktējošie iestatījumi, kas tika piešķirti rindas definīcijai.

### <a name="column-restrictions-cell"></a>Kolonnas ierobežojumu šūna

Šūna **Kolonnas ierobežojumi** var ietvert kodus, kas ierobežo vai likvidē informāciju, piemēram, šīs kolonnas rindu formatējums, detaļas un summas.

#### <a name="add-a-column-restriction-in-a-column-definition"></a>Pievienot kolonnas ierobežojumu kolonnas definīcijai

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Veiciet dubultklikšķi uz kolonnas šūnas **Kolonnas ierobežojumi**, lai ierobežotu.
3. Dialoglodziņā **Kolonnas ierobežojumi**, atlasiet vienu vai vairākus kodus no saraksta, un pēc tam noklikšķiniet uz **Labi**.

### <a name="column-restriction-codes"></a>Kolonnas ierobežojumu kodi

Tālāk redzamajā tabulā ir sniegts kolonnas ierobežojumu kodu apraksts.

| Kolonnas ierobežojuma kods | Apraksts |
|-------------------------|-------------|
| NP                      | Likvidēt pasvītrojumu kolonnai, kur rindas definīcijā ir ievadīta pasvītrojuma komanda (**---**) vai dubultā pasvītrojuma komanda (**===**). Piemēram, iespējams, jūs nevēlēsities pasvītrot summas, kas ir procentuāla aprēķina rezultāts. |
| NK                      | Tiek izlaistas kopsummas, lai kolonnā tiktu parādīta tikai detalizēta informācija (piemēram, statistikas kolonna). |
| ND                      | Likvidēt detaļas, tā, lai tikai kolonnā tiktu parādītas tikai **TOT** un **CAL** rindas (no rindas definīcijas). |
| DE                      | Ierobežot summas kolonnā **FD** līdz debeta summām. |
| KR                      | Ierobežot summas kolonnā **FD** līdz kredīta summām. |
| KOR                     | Kolonnā ietvertās summas tiek ierobežotas tā, lai netiktu rādītas perioda labojuma summas, ja šīs summas ir pieejamas. |
| IZK                     | Kolonnā ietvertās summas tiek ierobežotas tā, lai tiktu izlaistas perioda labojuma summas. |
| GD                      | Kolonnā ietvertās summas tiek ierobežotas tā, lai tiktu iekļauti tikai grāmatotie darījumi, ja šadi darījumi ir pieejami. |
| NGD                     | Ierobežot summas kolonnā, lai tiktu iekļautas tikai negrāmatotās darbības, ja šīs darbības ir pieejamas.<p><strong>Piezīme:</strong> Ne visi datu pakalpojumu sniedzēji atbalsta negrāmatotās darbības. </p> |

### <a name="restrict-a-column-to-a-reporting-unit"></a>Ierobežojuma definēšana kolonnai attiecībā uz noteiktu pārskatu vienību

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Veiciet dubultklikšķi uz kolonnas šūnas **Pārskata vienība**, lai ierobežotu.
3. Atlasiet pārskata koku dialoglodziņa **Pārskata vienību atlase** sarakstā **Pārskata koks**.
4. Izvērsiet vai sakļaujiet vienību sarakstu, atlasiet pārskata vienību un pēc tam noklikšķiniet uz **Labi**.

## <a name="format-column-headers"></a>Kolonnu galveņu formatēšana
Varat pievienot, modificēt un dzēst pārskata galvenes, kas tiek rādītas kolonnu augšdaļā. Jūs varat arī konfigurēt kolonnas nosacījuma laidenes galvenes, pamatojoties uz lauku **Periods** kolonnas definīcijā, un lauku **Bāzes periods** pārskata definīcijās. Pamata perioda līdzeklis palīdz ietaupīt laiku, veidojot apkopojumu prognožu pārskatus.

### <a name="create-and-manage-column-headers"></a>Kolonnu galveņu izveide un pārvaldība

Jūs varat izmantot dialoglodziņu **Kolonnas galvene**, lai pievienotu, modificētu un dzēstu galvenes, kas tiek rādītas pārskatā, kolonnu augšpusē. Tabulā ir aprakstīti dialoglodziņa **Kolonnas galvenes** lauki.

| Lauks                 | Apraksts |
|-----------------------|-------------|
| Kolonnas galvenes teksts    | Šis teksts tiek rādīts kolonnas galvenē. Ievadiet tekstu tieši šajā laukā, vai noklikšķiniet uz **Iespraust automātisko tekstu**, lai atlasītu opciju, kas atjaunina kolonnas galveni katru reizi, kad tiek izveidots pārskats. Lai iekļautu vairākus automātiskā teksta kodus, vēlreiz noklikšķiniet uz **Iespraust automātisko tekstu**, un pēc tam sarakstā noklikšķiniet uz citu kodu. |
| Formatēšanas opcijas        | Izmantojiet formatēšanu kolonnas galvenei, piemēram, rāmi vai pasvītrošanu. |
| Sadalīt no Sadalīt līdz | Izmantojiet opciju, lai definētu kolonnu vai kolonnas, kurās ir jālieto galvenes teksts. |
| Pamatojums         | Norādiet, kā jāizlīdzina kolonnas virsraksta teksts kolonnā vai kolonnas diapazonā, kas ir norādīts laukos **Sadalīt no** un **Sadalīt uz**. |

### <a name="create-a-column-header"></a>Kolonnas galvenes izveide

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Veiciet dubultklikšķi uz galvenes šūnas.
3. Dialoglodziņā **Kolonnas galvene**, ievadiet kolonnas galvenes tekstu. Varat arī noklikšķināt uz **Iespraust automātisko tekstu**, un atlasiet opciju.
4. Laukā **Formatēšanas opcijas**, atlasiet formātu galvenei.
5. Laukā **Sadalīt no**, ievadiet kolonnas burtu, kurā nepieciešams atsākt kolonnas galveni. Laukā **Sadalīt uz**, ievadiet kolonnas burtu, kurā nepieciešams pabeigt kolonnas galveni.
6. Sadaļā **Līdzināšana**, atlasiet, vai kolonnas galvenes tekstam ir jābūt līdzinājumam pa kreisi, uz centru vai pa labi.
7. Noklikšķiniet uz **OK**.

### <a name="add-a-column-header-row"></a>Kolonnas galvenes rindas pievienošana

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Galvenes rindā atlasiet šūnu.
3. Izvēlnē **Rediģēt** noklikšķiniet uz **Ievietot rindu**. Jaunā rinda tiek ievietota virs rindas, ko atlasījāt 2. darbībā.

> [!NOTE]
> Ja pārskatam ir četras vai vairāk pārskata galveņu rindas, galvenes pārklāsies, eksportējot pārskatu uz Excel darblapu. Lai pārskatā skatītu visas galvenes, pārskata definīcijā palieliniet augšējo piemali.

### <a name="delete-a-column-header-row"></a>Kolonnas galvenes rindas dzēšana

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Galvenes rindā atlasiet dzēšanai paredzēto šūnu.
3. Izvēlnē **Rediģēt** noklikšķiniet uz **Dzēst rindu**.

### <a name="create-an-automatically-generated-header"></a>Izveidot automātiski ģenerētu galveni

Pārskata veidotājs var automātiski ģenerēt kolonnas galvenes, pamatojoties uz automātiskā teksta kodiem. Automātiskā teksta kodi ir mainīgās vērtības, kas tiek atjauninātas katru reizi, kad tiek ģenerēts pārskats. Šos kodus var ietvert jebkurā kolonnas virsrakstā, lai norādītu pārskata informāciju, kas var atsķirties, piemēram, datumus vai periodu numurus. Tādējādi vienu kolonnas definīciju varat izmantot vairākām pārskatu definīcijām, laika periodiem un pārskatu kokiem. Tā kā automātiskā teksta kodi balstās uz kalendāra informāciju no kolonnas definīcijas detaļu rindām, tie tiek atbalstīti tikai kolonnām **CALC** un **FD**. Pārskatā redzamās informācijas izskats ir atkarīgs no tā, kā automātiskais teksts tiek parādīts kolonnas virsraksta šūnā. Dialoglodziņā **Kolonnas galvene**, automātiskā teksta kodi parādās dažādu reģistru burtos. Tādēļ teksts pārskatā tiks attēlots tādā pašā izskatā. Piemēram, parastajā kalendārajā gadā **\@CalMonthLong** **7.** mēnesis ir **Jūlijs**. Ja mēneša nosaukumam jābūt rakstītam ar lielajiem burtiem (piemēram, **JŪLIJS**), laukā **Kolonnas galvenes teksts** automātiskā teksta kodu ierakstiet ar lielajiem burtiem. Piemēram, ievadiet **\@CALMONTHLONG**. Kodus un tekstu var kombinēt. Piemēram, jūs ievadāt šādu galvenes tekstu: **Periods \@FinanšuPeriods-\@FinanšuGads no \@SākumaDatums līdz \@BeiguDatums**. Pārskata galvene, kas tiek izveidota līdzinās šādam tekstam: **Periods 1-02 no 01/01/02 līdz 31/01/02**.

> [!NOTE]
> Dažu tekstu formāts, piemēram, pilnais datuma formāts ir atkarīgs no jūsu servera reģionālajiem iestatījumiem. Lai mainītu šos iestatījumus, noklikšķiniet uz pogas **Sākums**, noklikšķiniet uz **Vadības panelis**, un pēc tam noklikšķiniet uz **Reģions un valoda**. Tālāk redzamajā tabulā ir aprakstītas kolonnu virsrakstiem pieejamās automātiskā teksta opcijas.


| Automātiskā teksta opcija un kods                | Apraksts |
|-----------------------------------------|-------------|
| Mēneša nosaukums (@CalMonthLong)              | Kolonnas virsrakstā tiek drukāts pašreizējā mēneša nosaukums. Ja pārskata summas vēlaties noapaļot līdz tūkstošiem, miljoniem vai miljardiem, vai arī iestatītā pārskata kolonnas platuma dēļ kolonnā ietilpst ne vairāk par deviņām rakstzīmēm, mēneša nosaukums tiek saīsināts, parādot tikai pirmās trīs rakstzīmes. |
| Mēneša nosaukuma saīsinājums (@CalMonthShort) | Atlasītajam finanšu periodam tiek drukāts saīsināts mēneša nosaukums. |
| Perioda numurs (@FiscalPeriod)           | Šajā kolonnā norādītais finanšu periods tiek drukāts ciparu formātā. Ja kolonnā ir ietverti vairāki periodi, tiek drukāts pēdējais diapazona periods. |
| Perioda apraksts (@FiscalPeriodName)  | Tiek drukāts finanšu datos norādītais finanšu perioda apraksts. |
| Finanšu gads (@FiscalYear)               | Šajā kolonnā norādītais finanšu gads tiek drukāts ciparu formātā. |
| Kalendārais gads (@CalYear)                | Šajā kolonnā norādītais kalendārais gads tiek drukāts ciparu formātā. |
| Sākuma datums (@StartDate)                 | Tiek drukāts kolonnas sākuma datums. |
| Beigu datums (@EndDate)                     | Tiek drukāts kolonnas beigu datums. |
| Vienības nosaukums no koka (@UnitName)         | Ja kolonnai ir noteikts ierobežojums attiecībā uz konkrētu pārskatu koka vienību, kolonnas virsrakstā tiek drukāts vienības nosaukums. |
| Vienības apraksts (@UnitDesc)            | Ja kolonnai ir noteikts ierobežojums attiecībā uz konkrētu pārskatu koka vienību, kolonnas virsrakstā tiek drukāts vienības apraksts. |
| Uzskaites kods (@BookCode)                   | Tiek drukāts kolonnā norādītais uzskaites kods. |
| Tukša līnija (@Blank)                     | Kolonnas virsrakstā tiek ievietota tukša līnija. |

### <a name="create-a-conditional-spanning-header"></a>Nosacījuma savienošanas galvenes izveide

Nosacījuma savienošanas galvenēs var apvienot vairākas kolonnas, ņemot vērā konkrēta perioda datus. Piemēram, ja skatāt finanšu gada budžeta pārskatu un vēlaties skatīt iepriekšējo mēnešu faktiskos budžetus, kā arī nākamo mēnešu plānotos budžetus, varat izmantot nosacījuma savienošanas galveni, lai automātiski atjauninātu pārskata galveni. Veidojot nosacījuma savienošanas galveni, ņemiet vērā tālāk norādīto:

- Jebkurš apturēšanas nosacījums (lauks **Sadalīt uz**), kas ir noteikts pirms sākuma nosacījuma (lauks **Sadalīt no**) tiek ignorēts. Piemēram, kolonnai B sadalīšanas nosacījums ir definēts kā PAMATA+1 līdz PAMATA un vienums PAMATA ir norādīts kolonnā C, bet vienums PAMATA+1 — kolonnā D. Šādā gadījumā apturēšanas nosacījums kolonnā C tiek ignorēts, un galveņu drukāšana tiek sākta kolonnā D.
- Ja norādītās kolonnu galvenes pārklājas, to pārklājums būs redzams, drukājot pārskatu. Pārskats tiek ģenerēts, bet laukā **Pārskata rindas statuss** tiek parādīts šāds brīdinājums: “Kolonnas galvenes, kas izmanto pamatu, pārklājas ar citām kolonnu galvenēm, un var izraisīt teksta pārklāšanos.” Piemēram, kolonnas B galvenes definīcija ir B līdz PAMATA+1, un kolonnas D galvenes definīcija ir PAMATA+1 līdz F. Šajā gadījumā galvenes tiek drukātas viena uz otras un nav salasāmas. Ikreiz, kad definīcijā **Sadalīt no/Sadalīt uz** tiek izmantota vērtība PAMATA, noteikti skatiet ģenerēto pārskatu, lai redzētu, vai galvenes nepārklājas.
- Ja sadales definīcijā norādāt PAMATA, tad kolonnā bez drukāšanas (**NP**) tas tiek ignorēts, neskatoties uz to, kas ir norādīts kolonnas definīcijā. Būtībā, šis scenārijs ir tāds pats kā kolonnas galvenes definīcijas neizveidošana.
- Nosacījuma drukāšanas kolonnām (**P&lt;B**, **P&gt;=B**) nosacījuma laiduma galvenes darbojas kā jebkura parasta kolonnas galvenes definīcija. Piemēram, ja nosacījums ir aplams, drukāšana tiek sākta no jebkādas secīgas kolonnas, kas atbilst sadalījuma nosacījumam.

#### <a name="create-a-conditional-spanning-header"></a>Nosacījuma savienošanas galvenes izveide

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Veiciet dubultklikšķi uz galvenes šūnas.
3. Dialoglodziņā **Kolonnas galvene**, ievadiet kolonnas galvenes tekstu. Varat arī noklikšķināt uz **Iespraust automātisko tekstu**, un atlasiet opciju.
4. Laukā **Formatēšanas opcijas**, atlasiet formatējuma stilu galvenei.
5. Norādiet periodu, kas ir saistīts ar pamata periodu, ko noteicāt pārskata izveides laikā. Laukos **Sadalīt no** un **Sadalīt uz**, ievadiet vienu no šīm vērtībām: **PAMATA**, **PAMATA-X** vai **PAMATA+X**, kur X ir periodu skaits no pamata periodu skaita. Piemēram, ja ievadāt **PAMATA**, laukā **Sadalīt no**, kolonnas nosacījuma laidenes galvenes teksts sākas kolonnas galvenē, kur pārskata definīcijas vērtība **Pamata periods** ir vienāda ar kolonnas definīcijas vērtību **Periods**. Tas beidzas kolonnā, kas ir norādīta laukā **Sadalīt uz**. Tādēļ, ja sadale ir pamats līdz M, un pārskata definīcijas vērtība **Pamata periods** ir **4**, galvene sākas kolonnā, kur periods ir iestatīts uz **4** un beidzas kolonnā M. Galvenes tiek pārtrauktas, un sākas tikai drukāšanas kolonnās.
6. Sadaļā **Līdzināšana**, atlasiet, vai kolonnas galvenes tekstam ir jābūt līdzinājumam pa kreisi, uz centru vai pa labi.
7. Noklikšķiniet uz **Labi**.

#### <a name="example-of-a-conditional-spanning-header"></a>Nosacījuma savienošanas galvenes piemērs

Lietotājs veido pārskatu ar sešu mēnešu dinamisko prognozi. Lietotājs vēlas, lai pāri kolonnām ar faktiskiem datiem būtu drukāts vārds "Faktiskie dati", bet pāri kolonnām ar budžeta prognozēm — vārds "Budžets". Katru mēnesi, veidojot pārskatu, tajā tiek ietverta viena papildu kolonna ar faktiskiem datiem un tiek dzēsta viena kolonna ar budžeta datiem. Lai gan lietotājs var manuāli modificēt kolonnas definīciju ikreiz, kad veido pārskatu, tādējādi pielāgojot galvenes, taču, lai ietaupītu laiku, lietotājs izveido nosacījuma savienošanas galvenes, kas automātiski izveido galvenes attiecīgajās kolonnās ikreiz, kad pārskats tiek palaists. Lietotājs atver Pārskatu veidotāju, navigācijas rūtī noklikšķina uz **Kolonnas definīcija**, un atver pārskata kolonnas definīciju. Pēc tam lietotājs ievada tālāk norādīto informāciju. Pārskata definīcijā norādītais pamata periods ir 4.

|      Formāts         |  A   | mljrd.             | K             | D             | E             | F             | G             | H             | I             | J             | tūkst.             | L             | P             |
|---------------------|------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| 1. galvene            |      | Faktiskais        | Budžets        |               |               |               |               |               |               |               |               |               |               |
| 2. galvene            |      | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong |
| 3. galvene            |      |               |               |               |               |               |               |               |               |               |               |               |               |
| Kolonnas tips         | APR | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            |
| Uzskaites kods/atribūts |      | FAKTISKAIS        | BUDŽETS2012    | FAKTISKAIS        | BUDŽETS2012    | FAKTISKAIS        | BUDŽETS2012    | FAKTISKAIS        | BUDŽETS2012    | FAKTISKAIS        | BUDŽETS2012    | FAKTISKAIS        | BUDŽETS2012    |
| Finanšu gads         |      | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          |
| Periods              |      | 1             | 1             | 2             | 2             | 3             | 3             | 4.             | 4.             | 5.             | 5.             | 6.             | 6.             |
| Ietvertie periodi     |      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      |
| Kolonnas platums        | 30   | 10.            | 10.            | 10.            | 10.            | 10.            | 10.            | 10.            | 10.            | 10.            | 10.            | 10.            | 10.            |
| Drukas vadība       |      | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        |

Tad lietotājs veic dubultklikšķi uz kolonnas galvenes šūnas kolonnā C, lai atvērtu dialoglodziņu **Kolonnas galvene** un ievada tālāk norādīto informāciju.

| Lauks              | Vērtība                 |
|--------------------|-----------------------|
| Kolonnas galvenes teksts | Faktiskais                |
| Ievietot automātisko tekstu    | Netiek veikta atlase. |
| Formatēšanas opcijas     | Rūtiņa                   |
| Līdzināšana      | Netiek veikta atlase. |
| Sadalīt no        | mljrd.                     |
| Sadalīt līdz          | PAMATA                  |

Pēc informācijas ievadīšanas lietotājs noklikšķina uz **Labi**. Tad lietotājs veic dubultklikšķi uz kolonnas galvenes šūnas kolonnā C, lai atvērtu dialoglodziņu **Kolonnas galvene** un ievada tālāk norādīto informāciju.

| Lauks              | Vērtība                 |
|--------------------|-----------------------|
| Kolonnas galvenes teksts | Budžets                |
| Ievietot automātisko tekstu    | Netiek veikta atlase. |
| Formatēšanas opcijas     | Rūtiņa                   |
| Līdzināšana      | Netiek veikta atlase. |
| Sadalīt no        | BASE+1                |
| Sadalīt līdz          | P                     |

Tagad katru reizi, kad tiks izveidots šis pārskats, pāri kolonnām ar faktiskiem datiem būtu drukāts vārds Faktiski dati, bet pāri kolonnām ar budžeta prognozēm — vārds Budžets. Turklāt katru mēnesi tiks koriģets kolonnu skaits.

## <a name="apply-column-justification"></a>Kolonnas līdzināšanas lietošana
Šūna **Līdzināšana** tiek izmantota, lai pārskatā veiktu apraksta kolonnas līdzinājuma formatējumu. Šī opcija attiecas tikai uz kolonnas aprakstiem, nevis uz faktiskām vērtībām.

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Veiciet dubultklikšķi uz šūnas **Līdzināšana**.
3. Sarakstā atlasiet vienu no šādām vērtībām.

    - **Nav** – nav līdzinājums netiek pielietots.
    - **Pa kreisi** – kolonnas aprakstu kreisās puses līdzināšana.
    - **Centrā** – kolonnas aprakstu līdzināšana no centra.
    - **Pa labi** – kolonnas aprakstu labās puses līdzināšana.

## <a name="add-special-formatting-options"></a>Pievienot īpašā formatējuma opcijas
Kad norādāt kolonnas definīciju, formatēšanas kolonnas detalizētās rindas tiek lietotas, lai atlasītajās kolonnās ieviestu īpašu formatējumu. Kaut arī dažas no **Drukāšanas vadība** opcijām un **Kolonnas ierobežojumi** opcijām ir raksturīgas **FD** kolonnām, lielākā daļa opciju tiek piemērotas visiem kolonnu tipiem. Kolonnas definīcijā norādītais formatējums ignorē pārskata definīcijā norādīto formatējumu. Tomēr rindas definīcijā norādītais formatējums ignorē kolonnas definīcijā norādīto formatējumu. Tālāk redzamās rindas tiek uzskatītas par formatēšanas rindām.

- Kolonnas platums
- Papildu atstarpes pirms kolonnas
- Formāta/valūtas ignorēšana
- Drukas vadība

### <a name="changing-the-column-width"></a>Kolonnu platuma maiņa

Šūna **Kolonnas platums** norāda rakstzīmju skaitu, lai noteiktu kolonnas platumu izveidotajā pārskatā. Kolonnas platums ir svarīgs kolonnām, kas satur summas (**CALC**, **WKS** vai **FD** tipa kolonnas), aprakstus (**DESC** tipa kolonnas), vai aizpildījumu (**FILL** tipa kolonnas). Pēc noklusējuma tiek atlasīta opcija **Automātiskā ietilpināšana**, lai katras kolonnas platums tiktu automātiski koriģēts, lai ietilpinātu saturu.

#### <a name="specify-the-width-of-a-column-on-a-report"></a>Kolonnas platuma norādīšana pārskatā

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Šūnā **Kolonnas platums**, ievadiet kolonnas platuma atstarpju skaitu. Katras kolonnas maksimālais platums 255 rakstzīmes (šis skaitlis ietver centus, komatus un iekavas). Vai arī, lai iespējotu pārskatu veidotāju atlasīt atbilstošu kolonnas platumu, pamatojoties uz šūnu saturu, veiciet dubultklikšķi uz šūnas **Kolonnas platums** un pēc tam noklikšķiniet uz **Automātiskā ietilpināšana**.

### <a name="add-space-between-columns"></a>Atstarpes starp kolonnām pievienošana

Šūna **Papildu atstarpes pirms kolonnas** norāda atdalītāja platumu starp kolonnu un blakus esošajām kolonnām kolonnas definīcijā. Iestatījums **Papildu atstarpes pirms kolonnas** ietekmē visas kolonnas detaļu rindas, bet neietekmē kolonnas galvenes rindas. Izmantojiet šo opciju, lai atdalītu kolonnu grupas vai pievienotu dažas atstarpes pirms apraksta, tādējādi atdalot apraksta kolonnu no kreisajā pusē līdzinātajiem pārskata virsrakstiem. Pēc noklusējuma starp kolonnām tiek ievietotas divas atstarpes. Šo iestatījumu var mainīt cilnē **Iestatījumi** pārskata definīcijā.

#### <a name="specify-the-space-between-columns"></a>Starp kolonnām esošās atstarpes norādīšana

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Šūnā **Papildu atstarpes pirms kolonnas**, ievadiet atstarpju skaits, ko ievietot starp kolonnām.

### <a name="specify-a-format-currency-override"></a>Formāta vai valūtas ignorēšanas norādīšana

Šūna **Formatēšana/Valūtas ignorēšana** norāda decimāldaļas, valūtas un procentu formatēšanu kolonnā. Šis formatējums aizstāj formatējumu, kas ir norādīts pārskata definīcijā vai sistēmas noklusējuma iestatījumos.

#### <a name="assign-a-format-currency-override-to-a-report-column"></a>Formāta vai valūtas ignorēšanas iestatīšana pārskata kolonnā

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Veiciet dubultklikšķi uz summas kolonnas šūnas **Formāta/valūtas ignorēšana**.
3. Dialoglodziņā **Formāta ignorēšana**, atlasiet formatēšanas opcijas.

### <a name="add-a-print-control-code"></a>Drukas vadības koda pievienošana

Šūna **Drukāšanas vadība** var saturēt kodus, kas pielāgo kolonnas rādījuma vai drukāšanas īpašības. Ir divu veidu drukas vadības kodi: parastie drukas vadības kodi un nosacījuma drukas vadības kodi.

#### <a name="regular-print-control-codes"></a>Parastie drukas vadības kodi

| Drukas vadības kods | Atšifrējums                                     | Apraksts |
|--------------------|-------------------------------------------------|-------------|
| NED                 | Nedrukāt                                     | Šajā kolonnā esošās summas netiek iekļautas drukātajā pārskatā un izmantotas aprēķinos. Lai nedrukājamu kolonnu iekļautu aprēķinā, šī kolonna jānorāda tieši aprēķina formulā. Piemēram, nedrukājama kolonna C ir iekļauta šādā aprēķinā: **B+C+D**. Tomēr, nedrukājamā kolonna C nav iekļauta šādā aprēķinā: **B:D**. |
| MZK                | Zīmes maiņa, ja rindas parastā bilance ir kredīts | Tiek izveidots budžets vai salīdzinošs pārskats, kurā nevēlamā novirze (piemēram, ieņēmumu deficīts vai izdevumu pārtēriņš) vienmēr tiek rādīta kā negatīva. Lietojiet šo kodu, lai kolonnā **CALC** kolonnas summai mainītu zīmi uz pretējo, ja tipiska dotās rindas bilance ir kredīts (saskaņā ar **C**, rindas definīcijas kolonnā **Parastā bilance**).<p><strong>Piezīme:</strong> <strong>TOT</strong> un </strong>CAL</strong> rindām, kas parasti ietver kredīta bilanci, pārliecinieties, ka esat ievadījis <strong>C</strong>, rindas definīcijas kolonnā <strong>Parastā bilance</strong>.</p> |
| X0                 | Neietvert kolonnu, ja visas tās vērtības ir vienādas ar nulli vai ir tukšas          | Izslēdziet **FD** kolonnu no pārskata, ja visas šūnas kolonnā ir vai nu tukšas vai satur nulles. |
| NN                 | Nepieļaut noapaļošanu                               | Kolonnā esošās summas netiek noapaļotas. |
| NA                 | Nepieļaut apkopošanu                                 | Nepieļauj apkopošanu. Ja pārskatā izmantojat pārskatu koku, šajā kolonnā esošās summas netiek apkopotas attiecīgajos vecākmezglos. |
| AD                 | Atkārtot kolonnu katrā lapā                      | Norādītā kolonna tiek atkārtota katrā pārskata lapā. Piemēram, jūs varat izmantot **RP** drukāšanas kontroles kodu, lai iekļautu kolonnu tipā **RINDA**, kas iegūst rindu kodus katrā lappusē. |
| AT                 |  Aplauzt tekstu                                      |  Ja kolonnas teksta garums pārsniedz kolonnas platumu, teksts tiek aplauzts, tādējādi paturot visu tekstu attiecīgajā kolonnā. |

#### <a name="conditional-print-control-codes"></a>Nosacījuma drukas vadības kodi

| Nosacījuma drukas vadības kods | Apraksts                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------|
| (nav)                         | Notīriet nosacījuma drukāšanas atlasi.                                                  |
| P&lt;B                         | Rādīt norādīto kolonnu, tikai tad, ja periods ir mazāks par pamata periodu.             |
| P&gt;B                         | Rādīt norādīto kolonnu, tikai tad, ja periods ir lielāks par pamata periodu.             |
| P=B                            | Rādīt norādīto kolonnu, tikai tad, ja periods ir vienāds ar pamata periodu.              |
| P&lt;=B                        | Rādīt norādīto kolonnu, tikai tad, ja periods ir mazāks vai vienāds ar pamata periodu. |
| P&gt;=B                        | Rādīt norādīto kolonnu, tikai tad, ja periods ir lielāks vai vienāds ar pamata periodu. |

#### <a name="add-print-control-codes-to-a-report-column"></a>Drukas vadības kodu pievienošana pārskata kolonnai

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Veiciet dubultklikšķi uz šūnas **Drukas vadība**.
3. Dialoglodziņā **Drukāšanas vadība**, atlasiet kodu sarakstā **Atlasiet drukāšanas vadības opcijas**. Lai atlasītu vairāk nekā vienu kodu, turiet nospiestu taustiņu Ctrl un atlasiet kodus.
4. Atlasiet opciju laukā **Nosacījuma drukāšanas opcijas**. Pēc noklusējuma ir atlasīta opcija **(nav)**. Vienlaicīgi var atlasīt tikai vienu nosacījuma drukāšanas kodu.
5. Noklikšķiniet uz **Labi**.

> [!TIP]
> Jūs varat arī ievadīt drukāšanas kodus pa tiešo šūnā **Drukāšanas vadība**. Vairāku drukas kodu atdalīšanai izmantojiet komatu.

## <a name="column-types"></a>Kolonnas tipi
Informācijas tips, ko satur katra kolonna pārskatā, tiek norādīts ar vērtību rindā **Kolonnas tipu** kolonnas definīcijā. Katrā kolonnas definīcijā ir jāietver vismaz viena apraksta kolonna (**APR**) un viena summas kolonna (**FD**, **DL** vai **APRĒK**).

> [!NOTE]
> Atsevišķās grāmatvedības sistēmās kolonnas tipa kodi, iespējams, nav derīgi. Ja atlasītais tips nav derīgs izmantojamajā grāmatvedības sistēmā, pārskatā attiecīgā kolonna tiek rādīta kā tukša.

### <a name="specify-a-column-type"></a>Kolonnas tipa norādīšana

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Atbilstošajā kolonnā, veiciet dubultklikšķi uz šūnas rindā **Kolonnas tips**.
3. Sarakstā atlasiet kolonnas tipu. Tālāk redzamajā tabulā ir sniegts dažādu kolonnu tipu apraksts.

    <table>
    <thead>
    <tr>
    <th>Kolonnas tipa kods</th>
    <th>Apraksts</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>FD</td>
    <td>Finanšu dati tiek rādīti, kad lietojat kolonnu <strong>Saite uz finanšu dimensijām</strong> rindu definīcijā. Atlasot kolonnas tipu <strong>FD</strong>, tālāk norādītajās rindās tiek automātiski rādīti noklusējuma iestatījumi. <ul>
    <li><strong>Uzskaites kods/atribūtu kategorija:</strong> FAKTISKAIS</li>
    <li><strong>Uzskaites kods/atribūtu kategorija:</strong> FAKTISKAIS</li>
    <li><strong>Finanšu gads:</strong> PAMATA</li>
    <li><strong>Periods:</strong> PAMATA</li>
    <li><strong>Ietvertie periodi:</strong> PERIODISKAIS</li>
    <li><strong>Kolonnas platums:</strong> 14</li>
    </ul>
Šos noklusējuma iestatījumus var mainīt.</td>
    </tr>
    <tr>
    <td>APRĒK</td>
    <td>Parāda vienkāršu vai sarežģītu aprēķinu rezultātu, kas ir norādīti šūnā <strong>Formula</strong>. Plašāku informāciju skatiet sadaļā <a href="advanced-formatting-options-financial-reporting.md">Paplašinātas formatēšanas opcijas finanšu pārskatos</a>.</td>
    </tr>
    <tr>
    <td>DESC</td>
    <td>Rādīt rindu aprakstu no rindas definīcijas. Lai gan apraksta kolonna pārskatā bieži tiek izmantota kā pirmā kolonna, to var ievietot jebkurā pozīcijā.</td>
    </tr>
    <tr>
    <td>RINDA</td>
    <td>Parāda finanšu rindas atsevišķām kodu rindām kolonnā <strong>Rindas kods</strong> rindas definīcijā. Plašāku informāciju skatiet sadaļā <a href="row-definitions-financial-reporting.md">Finanšu pārskatu rindu definīcijas</a>.</td>
    </tr>
    <tr>
    <td>ACCT (Kontu kodi)</td>
    <td>Parāda finanšu datu segmentu vērtības vai dimensijas vērtības, kas attiecas uz katru rindu. Detalizētajos konta un darījumu pārskatos tiek drukāts pilns konta numurs (piemēram, <strong>110140-070-0101</strong>). Ja saistītās rindas definīcijas kolonnā <strong>Saite uz finanšu dimensijām</strong> ir norādīti diapazoni, attiecīgais diapazons tiek ietverts kvadrātiekavās un apstrādāts kā viena vērtība (piemēram, <strong>[110140:110700]-070-[0101:0200]</strong>). Finanšu pārskatos un augsta līmeņa pārskatos, kuros ir ietverti vairāki konti, tiek drukāta saite uz finanšu datiem rindas definīcijā (piemēram, <strong>1100:1200</strong>).</td>
    </tr>
    <tr>
    <td>AIZP</td>
    <td>Norādiet šūnā rakstzīmi vienpēdiņās. Ja nav ievadīta neviena rakstzīme, kolonna ir tukša. Piemēram, lai aizpildītu kolonnu ar daudzpunkti (...), ievadiet <strong>FILL</strong> <strong>'.'</strong>.</td>
    </tr>
    <tr>
    <td>LAPA</td>
    <td>Pārskatā tiek ievietots vertikāls lapas pārtraukums. Kolonnas <strong>LAPA</strong> labajā pusē esošās kolonnas tiek rādītas citā lapā.</td>
    </tr>
    <tr>
    <td>ATR</td>
    <td>Ja grāmatvedības sistēmā tiek atbalstīti atribūti, kolonnā tiek parādīts konta vai darījuma atribūts. Atribūts ir jāsaista ar vienu pilnu kontu. Izmantojot atribūtu, no finanšu datiem tiek izgūta informācija par saistītu kontu vai darījumu. Izmantojot konta līmeņa atribūtus, tiek rādīti dati par kontu, savukārt, izmantojot darījuma līmeņa atribūtus, — dati, kas tika izveidoti, grāmatojot darījumu. Ja atlasītais kolonnas tips ir <strong>ATTR</strong>, kolonnas definīcijas detalizētas informācijas rindā <strong>Uzskaites kods/atribūtu kategorija</strong> norādiet atribūtu kategoriju.</td>
    </tr>
    </tbody>
    </table>

### <a name="financial-dimensions-column"></a>Kolonna Finanšu dimensijas

Rindas definīcijas **Kolonnas definīcija** tiek piemērotas kolonnām, kuru kolonnas tips ir **FD** (summas no finanšu dimensijām).

#### <a name="book-codeattribute-category-cell"></a>Šūna Uzskaites kods/atribūtu kategorija

Šūna **Grāmatas kods/atribūtu kategorijas** identificē grāmatas kodu **FD** kolonnas datiem. Kolonnas definīcijā var ietvert vairākas faktisko, budžeta un statistikas vērtību kolonnas. Kolonnas definīcijā var tikt parādīti arī atšķirīgi periodi, piemēram, pašreizējais vai no gada sākuma, kā arī atšķirīgas summas. Grāmatas kodu saraksts atspoguļo faktiskās, budžeta un statistikas (nefinanšu) opcijas, kas ir izveidotas jūsu finanšu datos.

#### <a name="fiscal-year-cell"></a>Šūna Finanšu gads

Šūna **Finanšu gads** identificē finanšu gadu, kuram jābūt iekļautam kolonnā. Gads var būt saistīts ar to pamata gadu, kas tika norādīts pārskata ģenerēšanas laikā. Ir pieejamas tālāk minētās opcijas.

| Opcija  | Apraksts                                                                                                                  |
|---------|------------------------------------------------------------------------------------------------------------------------------|
| PAMATA    | Izmantojiet pamata gadu, kas ir norādīts pārskata laikā.                                                                          |
| PAMATA+\# | Izmantojiet gadu, kas ir \# gadus pēc pamata gada. Piemēram, lai izmantotu trešo gadu pēc pamata gada, ievadiet **PAMATA+3**. |
| PAMATA-\# | Izmantojiet gadu, kas ir \# gadus pirms pamata gada. Piemēram, lai izmantotu iepriekšējo gadu, ievadiet **PAMATA-1**.                 |
| \#      | Ievadiet faktisko finanšu gadu.                                                                                                |

#### <a name="period-cell"></a>Perioda šūna

Šūna **Periods** identificē finanšu periodu, kuram jābūt iekļautam kolonnā. Periods var būt saistīts ar to pamata periodu, kas tika norādīts pārskata ģenerēšanas laikā. Pieejamas šādas opcijas.

| Opcija          | Apraksts |
|-----------------|-------------|
| PAMATA            | Izmantojiet pamata periodu. |
| PAMATA+\#         | Izmantojiet periodu, kas ir \# periodus pēc pamata perioda. Piemēram, lai izmantotu trešo periodu pēc pamata perioda, ievadiet **PAMATA+3**. |
| PAMATA-\#         | Izmantojiet periodu, kas ir \# periodus pirms pamata perioda. Piemēram, lai izmantotu iepriekšējo periodu, ievadiet **PAMATA-1**. |
| PAMATA-\#:PAMATA    | Izmantojiet vairākus periodus, no vairākiem periodiem pirms pamata perioda līdz pamata periodam. Piemēram, lai izmantotu trīs iepriekšējos periodus un pamata periodu, ievadiet **PAMATA-3:PAMATA**. |
| PAMATA:PAMATA+\#    | Izmantojiet vairākus periodus, no pamata perioda līdz vairākiem periodiem pēc pamata perioda. Piemēram, lai izmantotu pamata periodu un trīs sekojošus periodus, ievadiet **PAMATA:PAMATA+2**. |
| PAMATA-\#:PAMATA+\# | Izmantojiet vairākus periodus, no vairākiem periodiem pirms pamata perioda līdz vairākiem periodiem pēc pamata perioda. Piemēram, lai izmantotu trīs iepriekšējos periodus, pamata periodu un divus sekojošus periodus, ievadiet **PAMATA-3:PAMATA+2**. |
| 1:PAMATA          | Izmantot vairākus periodus, no pirmā perioda līdz pamata periodam. |
| \#              | Vienmēr izmantojiet noteikta perioda numuru. Nav ieteicams izmantot šo iespēju, jo tā samazina kolonnas definīcijas elastību. |
| \#:\#           | Vienmēr izmantojiet noteiktu periodu diapazonu. Nav ieteicams izmantot šo iespēju, jo tā samazina kolonnas definīcijas elastību. |

Jebkurā no periodu specifikācijām varat norādīt diapazonu pēc vai pirms finanšu gada, kā arī varat kombinēt gadus noteiktā periodu diapazonā. Piemēram, jūs periodu norādāt kā **PAMATA-5** (lai apzīmētu pēdējos sešus periodus) un palaižat pārskatu, kura pamata periods ir 2. Tādā gadījumā pārskatā tiek rādīti norādītā finanšu gada pirmo divu periodu dati un iepriekšējā finanšu gada pēdējie četri periodi.

### <a name="specify-the-periods-for-an-fd-column"></a>Periodu norādīšana kolonnā FD

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Kolonnā **FD**, veiciet dubultklikšķi uz šūnas rindā **Periods**, un pēc tam sarakstā atlasiet opciju.
3. Aizpildiet formulu joslā virs navigācijas rūts, vai arī šūnā **Periods**. Aizstājiet jebkuru numura zīmi (\#) ar atbilstošo vērtību.

#### <a name="periods-covered-cell"></a>Šūna Iekļautie periodi

Šūna **Iekļautie periodi** identificē daudzumu, kuram jābūt parādītam kolonnā. Šī summa ir saistīta ar vērtību kolonnas šūnās **Finanšu gads** un **Periods**. Ir pieejamas tālāk minētās opcijas.

| Opcija      | Apraksts                                                                 |
|-------------|-----------------------------------------------------------------------------|
| PERIODISKS    | Tiek parādīta pašreizējā perioda vai periodu diapazona darbības summa. |
| PERIODISKS/BB | Tiek parādīta pašreizējā perioda vai periodu diapazona sākuma bilance.   |
| ŠG         | Tiek parādīta darbības summa no gada sākuma.                               |
| ŠG/BB      | Tiek parādīta gada sākuma bilance.                                 |

### <a name="specify-the-periods-that-are-covered-for-an-fd-column"></a>Ietverto periodu norādīšana kolonnā FD

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Kolonnā **FD**, veiciet dubultklikšķi uz šūnas rindā **Iekļautie periodi**, un pēc tam sarakstā atlasiet opciju.

### <a name="attribute-filter-in-a-column-definition"></a>Atribūtu filtrs kolonnas definīcijā

Atribūti ir finanšu datu vērtības, ko izmanto konta vai darījuma definēšanai. Konta atribūti ietver **Pamatlīdzeklis**, **Saistības**, **Ieņēmumi** un **Izdevumi**. Darbības atribūti ietver **Darbības apraksts** un **Darbības piemērošanas datums**. Dažādās Microsoft Dynamics ERP sistēmās var tikt atbalstīti atšķirīgi atribūti. Šūna **Atribūtu filtrs** ierobežo datus **FD** kolonnās, līdz noteiktām vērtībām vai diapazoniem atribūta kategorijām. Kaut gan šo līdzekli var izmantot kopā ar **ATTR** kolonnu, **ATTR** kolonna nav nepieciešama. Kolonnā **FD** ir ierobežojums kontiem vai darbībām, kurus pārskats iekļaus no atribūta filtra.

> [!NOTE]
> Informāciju par savā ERP sistēmā atbalstītajiem atribūtiem skatiet sistēmas integrēšanas rokasgrāmatā.

#### <a name="apply-an-attribute-filter-for-an-fd-column-on-a-report"></a>Atribūtu filtra izmantošana pārskata FD kolonnai

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Veiciet dubultklikšķi uz kolonnas **FD** šūnas **Atribūtu filtrs**.
3. Dialoglodziņā **Atribūtu filtrs** veiciet dubultklikšķi uz kolonnā **Atribūts** redzamās šūnas un pēc tam atlasiet filtra tipu.
4. Lai ierobežotu rezultātus, ievadiet diapazonu kolonnās **No** un **Līdz**. Šūnā **No** jābūt norādītai vērtībai.
5. Noklikšķiniet uz **Labi**.

#### <a name="example-of-an-attribute-filter"></a>Atribūtu filtra piemērs

Šajā piemērā ir redzama daļa no kolonnas apraksta, kas ir konta atribūts rindā **Grāmatas kods/Kategorijas atribūts**. Šīs kolonnas atribūtu filtrs norāda vērtību diapazonu, kas jāietver pārskatā.

|      Filtrēt                  | A    | mljrd.                   |
|------------------------------|------|---------------------|
| Kolonnas tips                  | DESC | FD                  |
| Uzskaites kods/atribūtu kategorija |      | FAKTISKAIS              |
| Finanšu gads                  |      | PAMATA                |
| Periods                       |      | 1:PAMATA              |
| Ietvertie periodi              |      | PERIODISKS            |
| ...                          |      |                     |
| Kolonnas platums                 | 30   |                     |
| ...                          |      |                     |
| Atribūtu filtrs             |      | Atsauce=\[01:10\] |

### <a name="dimension-filter-in-a-column-definition"></a>Dimensiju filtrs kolonnas definīcijā

Dimensijas filtrs tiek izmantots, lai ierobežotu kolonnu **FD** līdz noteiktām dimensiju vērtībām. Filtrā var ietvert vienu dimensiju, dimensiju diapazonu vai dimensiju grupu. Turklāt filtrā var ietvert dimensiju vērtību kopas. Tā kā dimensiju vērtības var mainīties, tad sistēmai, kas ir balstīta uz ..\\finanšu dimensijām\\dimensijām, nav jāatbilst precīzam garumam. Neatkarīgi no tā, vai pārskatā ir ietverts pārskata koks, tiek izmantots filtrs. Jebkurā vietā varat izmantot aizstājējzīmes (\* vai ?). Ja norādāt vairākus kontus, atdaliet tos ar komatu kā šajā piemērā: +Konts=\[1200\], +Konts=\[1100\], Nodaļa=\[01?\]. Lai iegūtu visas noteikta konta nodaļas, varat dimensiju filtrā izlaist dimensiju Nodaļa. Piemēram, abi šo dimensiju filtri tiek apstrādāti tādā pašā veidā:

- +Konts=\[1100\],Nodaļa
- +Konts=\[1100\]

Precīzai salīdzināšanai jūs varat arī izmantot jebkuru burtu un ciparu rakstzīmju kombināciju, kā arī jūs varat definēt daļējas dimensijas. Piemēram, **Novietojums = \[10\*\]** ietver visas novietojuma dimensiju vērtības, kas sākas ar 10.

#### <a name="apply-a-dimension-filter-for-a-column-on-a-report"></a>Dimensiju filtra lietošana pārskata kolonnā

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Veiciet dubultklikšķi uz šūnas **Dimensiju filtrs**, kolonnai **FD**.
3. Dialoglodziņā **Dimensijas**, ievadiet filtrus pielietošanai.
4. Noklikšķiniet uz **OK**.

### <a name="format-a-multiple-currency-report-in-a-column-definition"></a>Daudzvalūtu pārskata formatēšana kolonnas definīcijā

Daudzvalūtu pārskatā var parādīt summas virsgrāmatas uzskaites valūtā, virsgrāmatas pārskata valūtā, sākotnējā darījuma valūtā vai pārrēķinātajā pārskata valūtā. Uzņēmuma uzskaites valūta tiek definēta virsgrāmatas iestatījumos. Pievērsiet uzmanību, ka šis iestatījums nav tas pats, kas operētājsistēmas reģionālo opciju iestatījums, kur varat konfigurēt noklusējuma valūtas simbolu, kas ir jāizmanto pārskatos. Kolonnas definīcijā ir pieejamas tālāk norādītas šūnas, kas ir saistītas ar valūtas datiem.

- **Valūtas parādīšana** — norādiet valūtas tipu (uzskaites, pārskata, darījuma vai pārrēķinātā pārskata valūta), kurā tiek rādīti darījumi. Pārrēķināšanas uz pārskata valūtu funkcionalitāte dažreiz tiek dēvēta par valūtas pārrēķināšanu. Valūtas pārrēķināšana nodrošina iespēju pārskatā ietvert virsgrāmatas summas, kas ir norādītas citā valūtā nekā uzņēmuma funkcionālā vai pārskata valūtā vai valūtā, kurā ievadījāt darījumu.
- **Valūtas filtrs** – norādiet valūtas filtru. Atskaitē tiek rādītas tikai darbības, kas tika ievadītas atlasītajā valūtā.

> 
Lai noteiktu uzņēmuma uzskaites valūtu, veiciet šīs darbības.

1. Pārskatu veidotāja izvēlnē **Uzņēmums** noklikšķiniet uz vienuma **Uzņēmumi**.
2. Dialoglodziņā **Uzņēmumi**, atlasiet uzņēmumu, un tad noklikšķiniet **Skatīt**.
3. Dialoglodziņā **Skatīt uzņēmumu**, sadaļā **Reģionālās opcijas**, jūs varat skatīt valūtu, kas ir definēta atlasītajam uzņēmumam.

#### <a name="specify-the-currency-on-a-multiple-currency-report"></a>Valūtas norādīšana daudzvalūtu pārskatā

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Veiciet dubultklikšķi uz šūnas **Valūtas parādīšana** atbilstošajā **FD** kolonnā, un pēc tam atlasiet valūtas informācijas parādīšanas opciju: **Virsgrāmatas uzskaites valūta**, **Virsgrāmatas pārskata**, darījuma valūta, vai atlasiet pārrēķināšanu citā pārskata valūta.
3. Veiciet dubultklikšķi uz šūnas **Valūtas filtrs** atbilstošajā **FD** kolonnā, un pēc tam sarakstā atlasiet atbilstošu valūtas kodu. Atskaitē tiek rādītas tikai darbības, kas tika ievadītas šajā valūtā.


### <a name="example-for-currency-display-and-currency-filter-cells"></a>Šūnu “Valūtas attēlojums” un “Valūtas filtrs” piemērs

Lietotājs atlasīja šādu valūtu kolonnas definīcijā:

- **Valūtas filtrs:** jēna
- **Valūtas parādīšana:** uzskaites valūta no virsgrāmatas (ASV dolāri)

Ņemot vērā atlasīto valūtas filtru, pārskatā ir iekļauti tikai tie darījumi, kas tika ievadīti Japānas jenās (JPY). Ņemot vērā atlasīto valūtas attēlojumu, pārskatā tiek rādīti tikai darījumi uzskaites valūtā — ASV dolāros (USD).

#### <a name="currency-filter-and-currency-display-combinations"></a>Valūtas filtra un valūtas attēlojuma kombinācijas

Šajā tabulā ir parādīti pārskata rezultāti, kas var rasties dažādām opciju kombinācijām šūnās **Valūtas parādīšana** un **Valūtas filtrs**, veiktās atlases dēļ. Funkcionālā valūta ir USD.


| Šūna Valūtas attēlojums                        | Šūna Valūtas filtrs | Pārskata rezultāts |
|----------------------------------------------|----------------------|---------------|
| Darbības valūta                 | **JĒNA**              | **Y6 000** – rezultāts rāda tikai darbības, kas tika ievadītas JPY. |
| Uzskaites valūta no virsgrāmatas | **JĒNA**              |**$60** – rezultāts rāda tikai darbības, kas tika ievadītas JPY, un attēlo tās darbības USD.<p><strong>Piezīme:</strong> konvertēšanas maiņas kurss ir aptuveni 100 JPY par vienu USD.</p> |
| Uzskaites valūta no virsgrāmatas | Tukšs                | **$2310** — rezultāts rāda visus datus uzskaites valūtā, kas ir norādīta virsgrāmatā.<p><strong>Piezīme.</strong> Šī summa ir visu darījumu summa uzskaites valūtā.</p> |
| Darbības valūta                 | Tukšs                | **$2250** – rezultāts rāda visas summas valūtā, kurā tika veikta darbība. Tas nozīmē, ka kopsumma tiek iegūta, saskaitot dažādu valūtu summas. |

### <a name="calculation-column-in-a-column-definition"></a>Kolonna Aprēķins kolonnas definīcijā

Kolonnas veids **CALC** kolonnas definīcijā atbalsta sarežģītus aprēķinus šūnā **Formula** un var ietvert operatorus **+**, **-**, **\**_ un _*/**, kā arī apgalvojumus **IF/THEN/ELSE**. Aprēķina kolonna var arī atsaukties uz jebkuru citu kolonnu, pat nākamajām kolonnām. Turklāt aprēķina kolonnā var būt ietverts arī finanšu gads un periods, lai atbalstītu kolonnas galvenes. Aprēķina formulā var izmantot ne vairāk par 1024 rakstzīmēm. Lai tiktu parādīta aprēķinu rezultātu procentuālā vērtība, izmantojiet īpašo formāta ignorēšanu.

> [!NOTE]
> Aprēķinu formulu rezultātos netiek ietvertas vērtības no nedrukājamo kolonnu diapazoniem. Piemēram, **A:D** drukā **0** (nulle), bet **A+B+C** aprēķina vērtību nedrukāšanas vērtībām.

#### <a name="operators-in-calculation-columns"></a>Aprēķinu kolonnu operatori

Lai saskaitītu, atņemtu, reizinātu vai dalītu kolonnu vērtības, ievadiet kolonnu burtus to aprēķināšanas secībā un pēc tam izmantojiet atbilstošo operatoru, lai atdalītu katru kolonnas burtu. Šajā tabulā sniegts pārskats par operatoriem, kurus jūs varat izmantot aprēķina kolonnā.

| Operators | Piemēra aprēķins | Apraksts |
|----------|---------------------|-------------|
| +        | A+C                 | Pievienot summu kolonnā A summai kolonnā C. |
| :        | A:C A:C-D           | Tiek pievienots secīgu kolonnu diapazons. Piemēram, formula **A:C** pievieno kolonnu summas no A līdz C, un formula **A:C-D** saskaita kolonnu A – C summas, un pēc tam atņem summu kolonnā D. |
| -        | A-C                 | No kolonnas A summas tiek atņemta kolonnas C summa.<p><strong>Piezīme.</strong> Varat izmantot arī mīnus zīmi (-), lai mainītu zīmes kolonnā. Piemēram, izmantojiet <strong>-A+B</strong>, lai pievienotu pretēju A kolonnas summu, B kolonnas summai.</p> |
| \*       | A\*C                | Reizināt summu kolonnā A ar summu kolonnā C. |
| /        | A/C                 | Dalīt summu kolonnā A ar summu kolonnā C. |

#### <a name="use-a-calculation-formula-in-a-column-definition"></a>Izmantot aprēķina formulu kolonnas definīcijā

1. Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2. Atbilstošajā kolonnā **CALC**, ievadiet formulu šūnā **Formula**.

#### <a name="complex-calculations"></a>Sarežģīti aprēķini

Sarežģītos aprēķinos var tikt ietverta jebkura šūnu atsauču, operatoru, vērtību un iekavu līmeņu kombinācija. Piemēram, lai aprēķinātu kolonnu A un B vidējo vērtību, izmantojiet aprēķina formulu **((A+B)/2)**.

#### <a name="specify-report-cells-in-a-column-calculation"></a>Pārskata šūnu norādīšana kolonnas aprēķinā

Varat izmantot atsauci uz konkrētu pārskata šūnu, ievadot kolonnas burtu un rindas kodu. Piemēram, **B.100** attiecas uz rindas kodu 100, kolonnā B. Jūs varat dalīt visu kolonnu ar noteiktu pārskatu šūnas summu, kas ir tajā pašā kolonnā. Piemēram, aprēķins **B/B.100** nozīmē, ka summa B kolonnā būtu jādala ar vērtību rindā ar kodu 100, kolonnā B. Ja aprēķins attiecas uz kolonnu, kas ir atkarīga no citas kolonnas, atkarīgā kolonna ir jāatrisina vispirms. Ja kolonnai tiek izveidota atsauce uz tādu kolonnu, kuras atsauce pēc tam tiek atgriezta uz pirmo kolonnu, radīsies riņķveida atsauces kļūda.

> [!NOTE]
> Ja mainījāt pārskata aprēķina prioritāti, šis aprēķins var nebūt pareizs. Jūs varat iestatīt aprēķina prioritāti pārskata definīcijas cilnē **Iestatījumi**.

#### <a name="multiply-or-divide-a-column-by-a-base-row"></a>Kolonnu vērtību reizināšana vai dalīšana ar pamata rindas vērtību

Varat izveidot kolonnu, kur visas noteiktā kolonnā ietvertās vērtības ir parādītas kā pamata skaitļa procentuālā vērtība. Tādējādi varat parādīt rindu relācijas, piemēram, rindas Pārdošana vai rindas Izdevumu kopsumma procentuālo vērtību. Lai katrā noteiktas kolonnas rindā reizinātu vai dalītu ar pamata rindu, ievadiet kolonnu, kuru izmantot aprēķinā, un pēc tam ievadiet **\*BASEROW** vai **/BASEROW**. Piemēram, ievadiet **C\*BASEROW** vai **C/BASEROW**.

> [!NOTE]
> Ja kolonnas definīcijā izmantojat pamata rindas aprēķinu, katras šajā kolonnas definīcijā lietotās rindas definīcijā noteikti jābūt ietvertai vismaz vienai pamata rindai, ko izmantot aprēķiniem.

#### <a name="divide-the-amount-in-a-column-by-the-number-of-periods"></a>Kolonnas summas dalīšana ar periodu skaitu

Kolonnas summu var dalīt ar noteiktu periodu skaitu. Piemēram, formula **B/periodi** izdala vērtību kolonnā B ar periodu skaitu kolonnā B. Ja aprēķins aptver vairākas kolonnas, norādiet periodu skaitu, izmantošanai aprēķinā. Piemēram, formula **(B+C)/periodi** saskaita summas kolonnā B un kolonnā C, un pēc tam dala rezultātu ar perioda vērtību.

## <a name="additional-resources"></a>Papildu resursi

[Rindas definīcijas finanšu atskaišu veidotājā](row-definitions-financial-reporting.md)

[Papildu formatēšanas opcijas finanšu pārskatos](advanced-formatting-options-financial-reporting.md)
