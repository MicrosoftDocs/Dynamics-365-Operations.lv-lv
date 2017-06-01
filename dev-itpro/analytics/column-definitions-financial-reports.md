---
title: "Kolonnu definīcijas finanšu pārskatos"
description: "Šajā rakstā ir sniegta informācija par kolonnu definīcijām. Kolonnas definīcija ir pārskata komponents jeb veidošanas bloks, kas nosaka katras kolonnas saturu pārskatā. Tāpat kā rindas definīcijas pamata kolonnu definīcijas var izmantot vairākos pārskatos."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter, Core
ms.custom: 106601
ms.assetid: 66e72a48-edab-4e9d-815f-596a1623c258
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ca82d24f591aaeb0d675716857cf94a4696785ad
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="column-definitions-in-financial-reports"></a>Kolonnu definīcijas finanšu pārskatos

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par kolonnu definīcijām. Kolonnas definīcija ir pārskata komponents jeb veidošanas bloks, kas nosaka katras kolonnas saturu pārskatā. Tāpat kā rindas definīcijas pamata kolonnu definīcijas var izmantot vairākos pārskatos.

<a name="create-and-modify-a-column-definition"></a>Izveidot un modificēt kolonnas definīciju
-------------------------------------

Kolonnas definīcija var saturēt divas līdz 255 kolonnas.

### <a name="create-a-column-definition"></a>Izveidojiet kolonnas definīciju

1.  Pārskata veidotājā, navigācijas rūtī noklikšķiniet uz **Kolonnas definīcijas**.
2.  Izvēlnē **Fails** noklikšķiniet uz **Jauns** un pēc tam uz **Kolonnas definīcija**.
3.  Pievienojiet kolonnas definīcijas saturu.

### <a name="open-a-column-definition"></a>Atveriet kolonas definīciju

1.  Pārskata veidotājā, navigācijas rūtī noklikšķiniet uz **Kolonnas definīcijas**.
2.  Veiciet dubultklikšķi uz kolonnas definīcijas, lai to atvērtu.

### <a name="add-a-column-to-a-column-definition"></a>Pievienojiet kolonnu kolonnas definīcijai

1.  Pārskatu veidotājā noklikšķiniet uz **Kolonnas definīcijas** un atveriet modificējamo kolonnas definīciju.
2.  Atlasiet kolonnu, kur jāievieto jauno kolonnu.
3.  Izvēlnē **Rediģēt** noklikšķiniet uz **Ievietot kolonnu**. Jaunā kolonna parādās pa kreisi no kolonnas, kuru atlasījāt.

### <a name="delete-a-column-from-a-column-definition"></a>Dzēsiet kolonnu no kolonnas definīcijas

1.  Pārskatu veidotājā noklikšķiniet uz **Kolonnas definīcijas** un atveriet modificējamo kolonnas definīciju.
2.  Atlasiet dzēšamo kolonnu.
3.  Izvēlnē **Rediģēt** noklikšķiniet uz **Dzēst kolonnu**.

## <a name="contents-of-a-column-definition"></a>Kolonnas definīcijas saturs
Kolonnas definīcija satur sekojošo informāciju:

-   Rindas definīcijas aprakstu kolonna
-   Summu kolonnas, kas parāda datus no finanšu datiem, Microsoft Excel darblapas vai aprēķiniem, kas ir balstīti uz citiem datiem kolonnas definīcijā
-   Kolonnu formatēšana
-   Kolonnu attiecināšana

Šī informācija tiek rādīta šādos kolonnas definīcijas apgabalos:

-   Kolonnas definīcijas galvenes apgabals satur virsraksta tekstu un formatējumu, kas parādās pārskatā. Galvene var attiekties uz vienu datu kolonnu, var ietvert vairākas kolonnas vai var tikt piemērota kolonnām uz nosacījuma pamata. Kolonnas definīcija var saturēt tik daudz kolonnas galvenes rindu, cik nepieciešams. **Piezīme:** Kolonnu galvenes attiecas uz katru datu kolonnu pārskatā. Pārskata galvenes attiecas uz visu pārskatu. Jūs varat definēt pārskata galvenes pārskata definīcijas cilnē **Galvenes un kājenes**.
-   Kolonnas detaļu rindas ir rindas zem galvenes rindas kolonnas definīcijā. Kolonnas detaļu rindas definē informāciju, kas tiek iekļauta pārskatā. Šajā tabulā ir uzskaitītas un aprakstītas kolonnas detaļu rindas.

    | Kolonnas detaļu rindas nosaukums                                                | Apraksts                                                                                            |
    |-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
    | Kolonnas tips                                                           | (Obligāts) Norādiet kolonnas datu tipu.                                                     |
    | Grāmatas kods/Kategorijas atribūts                                          | Norādiet finanšu datu informāciju **FD** un **ATTR** tipu kolonnās.                       |
    | Finanšu gada iekļautie periodi                                    | Norādiet finanšu datu informāciju **FD** tipa kolonnām.                                     |
    | Formula                                                               | Norādiet aprēķina formulu **CALC** tipa kolonnām.                                        |
    | Kolonnas platums Papildu atstarpes pirms kolonnas Formāta ignorēšana Drukāšanas vadība | Norādiet īpašas formāta opcijas.                                                                        |
    | Kolonnas ierobežojumi                                                   | Ierobežot datus.                                                                                         |
    | Pārskata vienība                                                        | Ierobežojiet kolonnu, lai tā rādītu tikai norādītās pārskata vienības datus.                      |
    | Valūtas displeja valūtas filtrs                                      | Formatēt valūtu.                                                                                       |
    | Dimensiju filtrs                                                      | Norādiet filtru, lai ierobežotu datus uz konkrētām finanšu datu pārskata vienībām.                           |
    | Atribūtu filtrs                                                      | Norādiet filtru, lai ierobežotu finanšu datus.                                                       |
    | Sākuma datums Beigu datums                                                   | Ierobežojiet finanšu datus noteiktos datumos.                                                         |
    | Pamatojums                                                         | Līdzināt no kreisās puses, līdzināt no centra vai līdzināt no labās puses apraksta tekstu, kas ir norādīts rindas definīcijā. |

## <a name="column-restrictions-in-a-column-definition"></a>Kolonnu ierobežojumi kolonnas definīcijā
Kolonnas ierobežojumus var izmantot, lai norādītu kā kolonnas definīcija izmanto datus vai aprēķina informāciju. Pārskata kolonnu var ierobežot arī noteiktai vienībai vai konkrētiem datumiem. **Piezīme:** Kods **Kolonnas ierobežojums** ignorē konfliktējošu iestatījumu, kas tiek piešķirts rindas definīcijā.

### <a name="column-restrictions-cell"></a>Kolonnas ierobežojumu šūna

Šūna **Kolonnas ierobežojumi** var ietvert kodus, kas ierobežo vai likvidē informāciju, piemēram, šīs kolonnas rindu formatējums, detaļas un summas.

#### <a name="add-a-column-restriction-in-a-column-definition"></a>Pievienot kolonnas ierobežojumu kolonnas definīcijai

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Veiciet dubultklikšķi uz kolonnas šūnas **Kolonnas ierobežojumi**, lai ierobežotu.
3.  Dialoglodziņā **Kolonnas ierobežojumi**, atlasiet vienu vai vairākus kodus no saraksta, un pēc tam noklikšķiniet uz **Labi**.

### <a name="column-restriction-codes"></a>Kolonnas ierobežojumu kodi

Tabulā ir aprakstīti kolonnas ierobežojumu kodi.

| Kolonnas ierobežojumu kods | Apraksts                                                                                                                                                                                                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SU                      | Likvidēt pasvītrojumu kolonnai, kur rindas definīcijā ir ievadīta pasvītrojuma komanda (**---**) vai dubultā pasvītrojuma komanda (**===**). Piemēram, iespējams, jūs nevēlēsities pasvītrot summas, kas ir procentuāla aprēķina rezultāts.                                                                        |
| ST                      | Likvidēt kopsummas, lai kolonnā tiktu parādītas tikai detaļas (piemēram, statistikas kolonna).                                                                                                                                                                                                                                      |
| SD                      | Likvidēt detaļas, tā, lai tikai kolonnā tiktu parādītas tikai **TOT** un **CAL** rindas (no rindas definīcijas).                                                                                                                                                                                                                              |
| DR                      | Ierobežot summas kolonnā **FD** līdz debeta summām.                                                                                                                                                                                                                                                                              |
| CR                      | Ierobežot summas kolonnā **FD** līdz kredīta summām.                                                                                                                                                                                                                                                                             |
| ADJ                     | Ierobežot summas kolonnā līdz perioda korekcijas summām, ja šīs summas ir pieejamas.                                                                                                                                                                                                                                        |
| XAD                     | Ierobežot summas kolonnā, lai perioda korekcijas summas tiktu izslēgtas.                                                                                                                                                                                                                                                     |
| PP                      | Ierobežot summas kolonnā, lai tiktu iekļautas tikai grāmatotās darbības, ja šīs darbības ir pieejamas.                                                                                                                                                                                                                 |
| UPT                     | Ierobežot summas kolonnā, lai tiktu iekļautas tikai negrāmatotās darbības, ja šīs darbības ir pieejamas. **Piezīme:** Ne visi datu pakalpojumu sniedzēji atbalsta negrāmatotās darbības. Plašāku informāciju skatiet [datu integrācijas rokasgrāmatā](http://go.microsoft.com/fwlink/?LinkID=162565) jūsu Microsoft Dynamics ERP sistēmai. |

### <a name="restrict-a-column-to-a-reporting-unit"></a>Ierobežot kolonnu līdz pārskata vienībai

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Veiciet dubultklikšķi uz kolonnas šūnas **Pārskata vienība**, lai ierobežotu.
3.  Atlasiet pārskata koku dialoglodziņa **Pārskata vienību atlase** sarakstā **Pārskata koks**.
4.  Izvērsiet vai sakļaujiet vienību sarakstu, atlasiet pārskata vienību un pēc tam noklikšķiniet uz **Labi**.

## <a name="format-column-headers"></a>Kolonnu galveņu formatēšana
Jūs varat pievienot, modificēt un dzēst galvenes, kas tiek rādītas pārskatā, kolonnu augšpusē. Jūs varat arī konfigurēt kolonnas nosacījuma laidenes galvenes, pamatojoties uz lauku **Periods** kolonnas definīcijā, un lauku **Bāzes periods** pārskata definīcijās. Bāzes periodā līdzeklis palīdz jums ietaupīt laiku, kad veidojat slīdošās prognozes pārskatus.

### <a name="create-and-manage-column-headers"></a>Kolonnu galveņu izveide un pārvaldīšana

Jūs varat izmantot dialoglodziņu **Kolonnas galvene**, lai pievienotu, modificētu un dzēstu galvenes, kas tiek rādītas pārskatā, kolonnu augšpusē. Tabulā ir aprakstīti dialoglodziņa **Kolonnas galvenes** lauki.

| Lauks                 | Apraksts                                                                                                                                                                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kolonnas galvenes teksts    | Šis teksts parādās kolonnas galvenē. Ievadiet tekstu tieši šajā laukā, vai noklikšķiniet uz **Iespraust automātisko tekstu**, lai atlasītu opciju, kas atjaunina kolonnas galveni katru reizi, kad tiek izveidots pārskats. Lai iekļautu vairākus automātiskā teksta kodus, vēlreiz noklikšķiniet uz **Iespraust automātisko tekstu**, un pēc tam sarakstā noklikšķiniet uz citu kodu. |
| Formatēšanas opcijas        | Pielietot formatēšanu kolonnas galvenei, piemēram, lodziņu vai pasvītrojumu.                                                                                                                                                                                                                                                           |
| Sadalīt no Sadalīt uz | Definējiet kolonnu vai kolonnas, uz kurām attiecas galvenes teksts.                                                                                                                                                                                                                                                            |
| Pamatojums         | Norādiet, kā jāizlīdzina kolonnas virsraksta teksts kolonnā vai kolonnas diapazonā, kas ir norādīts laukos **Sadalīt no** un **Sadalīt uz**.                                                                                                                                                               |

### <a name="create-a-column-header"></a>Izveidot kolonnas galveni

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Veiciet dubultklikšķi uz galvenes šūnas.
3.  Dialoglodziņā **Kolonnas galvene**, ievadiet kolonnas galvenes tekstu. Varat arī noklikšķināt uz **Iespraust automātisko tekstu**, un atlasiet opciju.
4.  Laukā **Formatēšanas opcijas**, atlasiet formātu galvenei.
5.  Laukā **Sadalīt no**, ievadiet kolonnas burtu, kurā nepieciešams atsākt kolonnas galveni. Laukā **Sadalīt uz**, ievadiet kolonnas burtu, kurā nepieciešams pabeigt kolonnas galveni.
6.  Sadaļā **Līdzināšana**, atlasiet, vai kolonnas galvenes tekstam ir jābūt līdzinājumam pa kreisi, uz centru vai pa labi.
7.  Noklikšķiniet uz **OK**.

### <a name="add-a-column-header-row"></a>Pievienot kolonnas galvenes rindu

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Atlasīt šūnu galvenes rindā.
3.  Izvēlnē **Rediģēt** noklikšķiniet uz **Ievietot rindu**. Jaunā rinda tiek ievietota virs rindas, ko atlasījāt 2. darbībā. **Piezīme.** Ja pārskatam ir četras vai vairāk pārskata galveņu rindas, galvenes pārklāsies, eksportējot pārskatu uz Excel darblapu. Lai skatītu visas galvenes pārskatā, pārskata definīcijā palieliniet augšējo piemali.

### <a name="delete-a-column-header-row"></a>Dzēst kolonnas galvenes rindu

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Galvenes rindā atlasiet šūnu, kuru nepieciešams dzēst.
3.  Izvēlnē **Rediģēt** noklikšķiniet uz **Dzēst rindu**.

### <a name="create-an-automatically-generated-header"></a>Izveidot automātiski ģenerētu galveni

Pārskata veidotājs var automātiski ģenerēt kolonnas galvenes, pamatojoties uz automātiskā teksta kodiem. Automātiskā teksta kodi ir mainīgie, kas tiek atjaunināts katru reizi, kad tiek izveidots pārskats. Kolonnas galvene var saturēt šos kodus, lai norādītu pārskata informāciju, kas var mainīties, piemēram, datumi vai periodu skaits. Tādējādi jūs varat izmantot vienu kolonnas definīciju vairākām pārskata definīcijām, laika periodiem un pārskata veidošanas kokiem. Tā kā automātiskā teksta kodi balstās uz kalendāra informāciju no kolonnas definīcijas detaļu rindām, tie tiek atbalstīti tikai kolonām **CALC**, **FD**, un **WKS**. Veids, kādā automātiskā teksta kods parādās kolonnas galvenes šūnā nosaka to, kā šī informācija parādās pārskatā. Dialoglodziņā **Kolonnas galvene**, automātiskā teksta kodi parādās dažādu reģistru burtos. Tāpēc, pārskatā teksts parādās dažādu reģistru burtos. Piemēram, standarta kalendārajā gadā **@CalMonthLong** mēnesi **7** atrisina uz **Jūlijs**. Ja mēneša nosaukumā ir jābūt lielajiem burtiem (piemēram **JŪLIJS**), tad laukā **Kolonnas galvenes teksts** ievadiet automātiskā teksta kodu ar lielajiem burtiem. Ievadiet, piemēram, **@CALMONTHLONG**. Jūs varat kombinēt kodus un tekstu. Jūs ievadāt, piemēram, šādu galvenes tekstu: **Periods @FiscalPeriod-@FiscalYear no @StartDate līdz @EndDate**. Pārskata galvene, kas tiek izveidota līdzinās šādam tekstam: **Periods 1-02 no 01/01/02 līdz 31/01/02**. **Piezīme.** Dažu tekstu formāts, piemēram, pilnais datuma formāts, ir atkarīgs no jūsu Dynamics 365 for Operations servera reģionālajiem iestatījumiem. Lai mainītu šos iestatījumus, noklikšķiniet uz pogas **Sākums**, noklikšķiniet uz **Vadības panelis**, un pēc tam noklikšķiniet uz **Reģions un valoda**. Šajā tabulā ir uzskaitītas pieejamās automātiskā teksta opcijas kolonnu galvenēm.

| Automātiskā teksta opcija un kods                | Apraksts                                                                                                                                                                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mēneša nosaukums (@CalMonthLong)              | Ievadiet pašreizējā mēneša nosaukumu kolonnas galvenē. Ja jūs nolemjat noapaļot summas pārskatā līdz tūkstošiem, miljoniem vai miljardiem, vai ja iestatāt kolonnas platumu mazāku par deviņām rakstzīmēm, mēneša nosaukums tiks saīsināts līdz pirmajām trim rakstzīmēm. |
| Saīsinātā mēneša nosaukums (@CalMonthShort) | Ievadiet mēneša saīsināto nosaukumu atlasītajam finanšu periodam.                                                                                                                                                                                                                          |
| Perioda numurs (@FiscalPeriod)           | Ievadiet finanšu perioda, kas ir norādīts šai kolonnai, skaitlisko formu. Ja kolonna ir satur vairākus periodus, tiek ievadīts pēdējais diapazona periods.                                                                                                                                   |
| Perioda apraksts (@FiscalPeriodName)  | Ievadiet finanšu perioda aprakstu, kas ir norādīts finanšu datos.                                                                                                                                                                                                                    |
| Finanšu gads (@FiscalYear)               | Ievadiet kolonnā finanšu gadu ciparu formā.                                                                                                                                                                                                                                            |
| Kalendārais gads (@CalYear)                | Ievadiet kolonnā kalendāro gadu ciparu formā.                                                                                                                                                                                                                                          |
| Sākuma datums (@StartDate)                 | Ievadiet kolonnā perioda sākuma datumu.                                                                                                                                                                                                                                                             |
| Beigu datums (@EndDate)                     | Ievadiet kolonnā perioda beigu datumu.                                                                                                                                                                                                                                                               |
| Vienības nosaukums no koka (@UnitName)         | Ja ierobežojat kolonnu līdz noteiktai vienībai no pārskata koka, ievadiet vienības nosaukumu kolonnas galvenē.                                                                                                                                                                                     |
| Vienības apraksts (@UnitDesc)            | Ja ierobežojat kolonnu līdz noteiktai vienībai no pārskata koka, ievadiet vienības aprakstu kolonnas galvenē.                                                                                                                                                                              |
| Grāmatas kods (@BookCode)                   | Ievadiet grāmatas kodu, kas ir norādīts kolonnā.                                                                                                                                                                                                                                             |
| Tukša rinda (@Blank)                     | Ievietot tukšu rindu kolonnas galvenē.                                                                                                                                                                                                                                                       |

### <a name="create-a-conditional-spanning-header"></a>Izveidojiet nosacījuma laidenes galveni

Nosacījuma laidenes galvenes var ietvert vairākas kolonnas, kas balstās uz noteiktiem perioda datiem. Piemēram, ja jums ir budžeta pārskats finanšu gadam un jūs vēlaties rādīt pēdējo mēnešu faktisko budžetu, kā arī turpmāko mēnešu prognozēto budžetu, jūs varat izmantot nosacījuma laidenes galveni, lai automātiski atjauninātu pārskata galveni. Veidojot nosacījuma laidenes galveni, pievērsiet uzmanību šādiem gadījumiem:

-   Jebkurš apturēšanas nosacījums (lauks **Sadalīt uz**), kas ir noteikts pirms sākuma nosacījuma (lauks **Sadalīt no**) tiek ignorēts. Piemēram, kolonnas B izplatības nosacījums ir definēts kā PAMATA+1 līdz PAMATA, PAMATA ir kolonnā C un PAMATA+1 ir kolonnā D. Šajā gadījumā apturēšanas nosacījums kolonnā C tiek ignorēts, un galvenes ievadīšana sākas kolonnā D.
-   Ja norādāt kolonnu galvenes, kas pārklājas, tās pārklāsies, kad tiks ievadītas pārskatā. Pārskats tiek ģenerēts, bet laukā **Pārskata rindas statuss** tiek parādīts šāds brīdinājums: “Kolonnas galvenes, kas izmanto pamatu, pārklājas ar citām kolonnu galvenēm, un var izraisīt teksta pārklāšanos.” Piemēram, kolonnas B galvenes definīcija ir B līdz PAMATA+1, un kolonnas D galvenes definīcija ir PAMATA+1 līdz F. Šajā gadījumā galvenes tiek drukātas viena uz otras un nav salasāmas. Ikreiz, kad definīcijā **Sadalīt no/Sadalīt uz** tiek izmantota vērtība PAMATA, noteikti skatiet ģenerēto pārskatu, lai redzētu, vai galvenes nepārklājas.
-   Ja sadales definīcijā norādāt PAMATA, tad kolonnā bez drukāšanas (**NP**) tas tiek ignorēts, neskatoties uz to, kas ir norādīts kolonnas definīcijā. Būtībā, šis scenārijs ir tāds pats kā kolonnas galvenes definīcijas neizveidošana.
-   Nosacījuma drukāšanas kolonnām (**P&lt;B**, **P&gt;=B**) nosacījuma laiduma galvenes darbojas kā jebkura parasta kolonnas galvenes definīcija. Piemēram, ja nosacījums nav patiess, jebkuras tālākās kolonnas atbilstības noteikšanu izplatības nosacījumam aizsāk galvenes drukāšanu.

#### <a name="create-a-conditional-spanning-header"></a>Izveidojiet nosacījuma laidenes galveni

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Veiciet dubultklikšķi uz galvenes šūnas.
3.  Dialoglodziņā **Kolonnas galvene**, ievadiet kolonnas galvenes tekstu. Varat arī noklikšķināt uz **Iespraust automātisko tekstu**, un atlasiet opciju.
4.   Laukā **Formatēšanas opcijas**, atlasiet formatējuma stilu galvenei.
5.  Norādiet periodu attiecībā pret pamata periodu, kas ir norādīts pārskata izveides brīdī. Laukos **Sadalīt no** un **Sadalīt uz**, ievadiet vienu no šīm vērtībām: **PAMATA**, **PAMATA-X** vai **PAMATA+X**, kur X ir periodu skaits no pamata periodu skaita. Piemēram, ja ievadāt **PAMATA**, laukā **Sadalīt no**, kolonnas nosacījuma laidenes galvenes teksts sākas kolonnas galvenē, kur pārskata definīcijas vērtība **Pamata periods** ir vienāda ar kolonnas definīcijas vērtību **Periods**. Tas beidzas kolonnā, kas ir norādīta laukā **Sadalīt uz**. Tādēļ, ja sadale ir pamats līdz M, un pārskata definīcijas vērtība **Pamata periods** ir **4**, galvene sākas kolonnā, kur periods ir iestatīts uz **4** un beidzas kolonnā M. Galvenes tiek pārtrauktas, un sākas tikai drukāšanas kolonnās.
6.  Sadaļā **Līdzināšana**, atlasiet, vai kolonnas galvenes tekstam ir jābūt līdzinājumam pa kreisi, uz centru vai pa labi.
7.  Noklikšķiniet uz **OK**.

#### <a name="example-of-a-conditional-spanning-header"></a>Nosacījuma laidenes galvenes piemērs

Madara veido pārskatu dinamiskai sešu mēnešu prognozei. Viņa vēlas, lai vārds "Faktiskais" tiktu drukāts virs kolonnām, kas ietver faktiskos datus, un vārds "Budžets" tiktu drukāts virs kolonnām, kas ietver budžeta prognozes. Katru mēnesi, kad tiek izveidots pārskats, kļūst par vienu faktisko kolonnu vairāk, un par vienu budžeta kolonnu mazāk. Lai gan Madara var modificēt kolonnas definīcija manuāli, ikreiz, kad tiek izveidots pārskats, lai pielāgotu galvenes, lai ietaupītu laiku un pūles, viņa nolemj izveidot nosacījuma laidenes galvenes, kas automātiski izveidos galvenes virs atbilstošajām kolonnām katru reizi, kad tiek palaista atskaite. Madara atver Pārskatu veidotāju, navigācijas rūtī noklikšķina uz **Kolonnas definīcija**, un atver pārskata kolonnas definīciju. Tad viņa ievada šādu informāciju. Pārskata definīcijas pamata periods ir 4.

|                     | A    | B             | C             | D             | E             | F             | G             | H             | I             | J             | tūkst.             | L             | P             |
|---------------------|------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Galvene 1            |      | Faktiskais        | Budžets        |               |               |               |               |               |               |               |               |               |               |
| Galvene 2            |      | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong |
| Galvene 3            |      |               |               |               |               |               |               |               |               |               |               |               |               |
| Kolonnas tips         | DESC | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            |
| Grāmatas kods/Atribūts |      | FAKTISKAIS        | BUDŽETS2012    | FAKTISKAIS        | BUDŽETS2012    | FAKTISKAIS        | BUDŽETS2012    | FAKTISKAIS        | BUDŽETS2012    | FAKTISKAIS        | BUDŽETS2012    | FAKTISKAIS        | BUDŽETS2012    |
| Finanšu gads         |      | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          | PAMATA          |
| Periods              |      | 1             | 1             | 2             | 2             | 3             | 3             | 4.             | 4.             | 5.             | 5.             | 6.             | 6.             |
| Iekļautie periodi     |      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      | PERIODISKS      |
| Kolonnas platums        | 30   | 10.            | 10.            | 10.            | 10.            | 10.            | 10.            | 10.            | 10.            | 10.            | 10.            | 10.            | 10.            |
| Drukāšanas vadība       |      | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        |

Madara veic dubultklikšķi uz kolonnas galvenes šūnas, lai atvērtu dialoglodziņu **Kolonnas galvene**, kur viņa ievada šādu informāciju.

| Lauks              | Vērtība                 |
|--------------------|-----------------------|
| Kolonnas galvenes teksts | Faktiskais                |
| Iespraust automātisko tekstu    | Netika veikta atlase. |
| Formatēšanas opcijas     | Lauks                   |
| Pamatojums      | Netika veikta atlase. |
| Sadalīt no        | mljrd.                     |
| Sadalīt uz          | PAMATA                  |
| Budžeta galvene      | PAMATA+1 līdz beigu kolonnai  |

Pēc tam, kad viņa pabeidz informācijas ievadīšanu, Madara noklikšķina **Labi**. Tad viņa veic dubultklikšķi uz kolonnas galvenes šūnas kolonnā C, lai atvērtu dialoglodziņu **Kolonnas galvene**, kur viņa ievada šādu informāciju.

| Lauks              | Vērtība                 |
|--------------------|-----------------------|
| Kolonnas galvenes teksts | Budžets                |
| Iespraust automātisko tekstu    | Netika veikta atlase. |
| Formatēšanas opcijas     | Lauks                   |
| Pamatojums      | Netika veikta atlase. |
| Sadalīt no        | K                     |
| Sadalīt uz          | PAMATA+2                |

Tagad, katru reizi, kad tiks izveidots šis pārskats, vārds "Faktiskais" tiks drukāts virs kolonnām, kas ietver faktiskos datus, un vārds "Budžets" tiks drukāts virs kolonnām, kas ietver budžeta prognozes. Turklāt kolonnu skaits tiks koriģēts katru mēnesi.

## <a name="apply-column-justification"></a>Pielietot kolonnas līdzinājumu
Šūna **Līdzināšana** tiek izmantota, lai pārskatā veiktu apraksta kolonnas līdzinājuma formatējumu. Šī opcija ietekmē tikai kolonnas aprakstus, nevis faktiskās vērtības.

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Veiciet dubultklikšķi uz šūnas **Līdzināšana**.
3.  Atlasiet vienu no uzskaitītajām vērtībām:
    -   **Nav** – nav līdzinājums netiek pielietots.
    -   **Pa kreisi** – kolonnas aprakstu kreisās puses līdzināšana.
    -   **Centrā** – kolonnas aprakstu līdzināšana no centra.
    -   **Pa labi** – kolonnas aprakstu labās puses līdzināšana.

## <a name="add-special-formatting-options"></a>Pievienot īpašas formatēšanas opcijas
Kolonnas definīcijā, formatēšanas kolonnu detaļu rindas atlasītajām kolonnām pielieto īpašu formatējumu. Kaut arī dažas no **Drukāšanas vadība** opcijām un **Kolonnas ierobežojumi** opcijām ir raksturīgas **FD** kolonnām, lielākā daļa opciju tiek piemērotas visiem kolonnu tipiem. Formatējums, kas ir norādīts kolonnas definīcijā ignorē formatējumu, kas ir norādīts pārskata definīcijā. Tomēr formatējums, kas ir norādīts rindas definīcijā ignorē formatējumu, kas ir norādīts kolonnas definīcijā. Šādas rindas tiek uzskatītas par formatēšanas rindām:

-   Kolonnas platums
-   Papildu atstarpes pirms kolonnas
-   Formatēšana/Valūtas ignorēšana
-   Drukāšanas vadība

### <a name="changing-the-column-width"></a>Kolonnas platuma maiņa

Šūna **Kolonnas platums** norāda rakstzīmju skaitu, lai noteiktu kolonnas platumu izveidotajā pārskatā. Kolonnas platums ir svarīgs kolonnām, kas satur summas (**CALC**, **WKS** vai **FD** tipa kolonnas), aprakstus (**DESC** tipa kolonnas), vai aizpildījumu (**FILL** tipa kolonnas). Pēc noklusējuma tiek atlasīta opcija **Automātiskā ietilpināšana**, lai katras kolonnas platums tiktu automātiski koriģēts, lai ietilpinātu saturu.

#### <a name="specify-the-width-of-a-column-on-a-report"></a>Norādiet kolonnas platumu pārskatā

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Šūnā **Kolonnas platums**, ievadiet kolonnas platuma atstarpju skaitu. Katras kolonnas maksimālais platums 255 rakstzīmes (šis skaitlis ietver centus, komatus un iekavas). Vai arī, lai iespējotu pārskatu veidotāju atlasīt atbilstošu kolonnas platumu, pamatojoties uz šūnu saturu, veiciet dubultklikšķi uz šūnas **Kolonnas platums** un pēc tam noklikšķiniet uz **Automātiskā ietilpināšana**.

### <a name="add-space-between-columns"></a>Pievienot atstarpi starp kolonnām

Šūna **Papildu atstarpes pirms kolonnas** norāda atdalītāja platumu starp kolonnu un blakus esošajām kolonnām kolonnas definīcijā. Iestatījums **Papildu atstarpes pirms kolonnas** ietekmē visas kolonnas detaļu rindas, bet neietekmē kolonnas galvenes rindas. Izmantojiet šo opciju atsevišķām kolonnu grupām, vai dažu atstarpju pievienošanai pirms apraksta, lai apraksta kolonnai pārskatā ir virsraksts ar atkāpi no kreisās puses. Noklusējuma atstarpju skaits starp katru kolonnu ir divas atstarpes. Šo iestatījumu var mainīt cilnē **Iestatījumi** pārskata definīcijā.

#### <a name="specify-the-space-between-columns"></a>Norādiet atstarpi starp kolonnām

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Šūnā **Papildu atstarpes pirms kolonnas**, ievadiet atstarpju skaits, ko ievietot starp kolonnām.

### <a name="specify-a-currency"></a>Norādiet valūtu

Šūna **Formatēšana/Valūtas ignorēšana** norāda decimāldaļas, valūtas un procentu formatēšanu kolonnā. Šis formatējums ignorē jebkuru formatējumu, kas norādīts kolonnas definīcijā vai sistēmas noklusējuma iestatījumos.

#### <a name="assign-a-format-currency-override-to-a-report-column"></a>Piešķirt pārskata kolonnai formatēšanu, valūtas ignorēšanu

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Veiciet dubultklikšķi uz šūnas **Formatēšana/Valūtas ignorēšana** summas kolonnā.
3.  Dialoglodziņā **Formāta ignorēšana**, atlasiet formatēšanas opcijas.

### <a name="add-a-print-control-code"></a>Pievienot drukāšanas vadības kodu

Šūna **Drukāšanas vadība** var saturēt kodus, kas pielāgo kolonnas rādījuma vai drukāšanas īpašības. Ir divu veidu drukāšanas vadības kodi: regulāri drukāšanas vadības kodi un nosacījuma drukāšanas vadības kodi.

#### <a name="regular-print-control-codes"></a>Parasti drukāšanas vadības kodi

| Drukāšanas vadības kods | Transformācija                                     | Apraksts                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NP                 | Nedrukāšana                                     | Izslēgt šīs kolonnas summas no pārskata, kurš tiek drukāts, kā arī no aprēķiniem. Lai aprēķinā iekļautu nedrukājamu kolonnu, veidojiet atsauci uz kolonnu tieši aprēķina formulā. Piemēram, nedrukājama kolonna C ir iekļauta šādā aprēķinā: **B+C+D**. Tomēr, nedrukājamā kolonna C nav iekļauta šādā aprēķinā: **B:D**.                                                                                                                                          |
| XCR                | Nomainīt zīmi, ja tipiska rindas bilance ir kredīts | Izveidot budžeta vai salīdzinošo pārskatu, kur jebkura nelabvēlīga novirze (piemēram, ieņēmumu iztrūkums vai izdevumu pārsniegšana) vienmēr ir negatīva. Lietojiet šo kodu, lai kolonnā **CALC** kolonnas summai mainītu zīmi uz pretējo, ja tipiska dotās rindas bilance ir kredīts (saskaņā ar **C**, rindas definīcijas kolonnā **Parastā bilance**). **Piezīme:** **TOT** un **CAL** rindām, kas parasti ietver kredīta bilanci, pārliecinieties, ka esat ievadījis **C**, rindas definīcijas kolonnā **Parastā bilance**. |
| X0                 | Likvidēt kolonnu, ja visas šūnas ir nulle vai tukšas          | Izslēdziet **FD** kolonnu no pārskata, ja visas šūnas kolonnā ir vai nu tukšas vai satur nulles.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SR                 | Likvidēt noapaļošanu                               | Neļaut summu noapaļošanu šajā kolonnā.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| XR                 | Likvidēt apkopojumu                                 | Likvidējiet apkopojumu. Ja pārskatā tiek izmantots pārskata veidošanas koks, summas šajā kolonnā netiek apkopotas turpmākos pamatmezglos.                                                                                                                                                                                                                                                                                                                                                                                                   |
| RP                 | Atkārtot kolonnu katrā lapā                      | Atkārtojiet norādīto kolonnu katrā pārskata lapā. Piemēram, jūs varat izmantot **RP** drukāšanas kontroles kodu, lai iekļautu kolonnu tipā **RINDA**, kas iegūst rindu kodus katrā lappusē.                                                                                                                                                                                                                                                                                                                                           |
| WT                 |  Aplauzt tekstu                                      |  Ja teksts kolonnā ir pārāk garš un neietilpst šūnā, aplauziet tekstu, lai saglabātu visu tekstu kolonnā.                                                                                                                                                                                                                                                                                                                                                                                                                            |

#### <a name="conditional-print-control-codes"></a>Nosacījuma drukāšanas vadības kodi

| Nosacījuma drukāšanas vadības kods | Apraksts                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------|
| (nav)                         | Notīriet nosacījuma drukāšanas atlasi.                                                  |
| P&lt;B                         | Rādīt norādīto kolonnu, tikai tad, ja periods ir mazāks par pamata periodu.             |
| P&gt;B                         | Rādīt norādīto kolonnu, tikai tad, ja periods ir lielāks par pamata periodu.             |
| P=B                            | Rādīt norādīto kolonnu, tikai tad, ja periods ir vienāds ar pamata periodu.              |
| P&lt;=B                        | Rādīt norādīto kolonnu, tikai tad, ja periods ir mazāks vai vienāds ar pamata periodu. |
| P&gt;=B                        | Rādīt norādīto kolonnu, tikai tad, ja periods ir lielāks vai vienāds ar pamata periodu. |

#### <a name="add-print-control-codes-to-a-report-column"></a>Pievienot pārskata kolonnai drukāšanas vadības kodus

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Veiciet dubultklikšķi uz šūnas **Drukāšanas vadība**.
3.  Dialoglodziņā **Drukāšanas vadība**, atlasiet kodu sarakstā **Atlasiet drukāšanas vadības opcijas**. Lai atlasītu vairāk nekā vienu kodu, turiet nospiestu taustiņu Ctrl un atlasiet kodus.
4.  Atlasiet opciju laukā **Nosacījuma drukāšanas opcijas**. Pēc noklusējuma tiek atlasīts **(nav)**. Vienlaicīgi var atlasīt tikai vienu nosacījuma drukāšanas kodu.
5.  Noklikšķiniet uz **Labi**.

> [!TIP]
> Jūs varat arī ievadīt drukāšanas kodus pa tiešo šūnā **Drukāšanas vadība**. Atdaliet ar komatu vairākus drukāšanas vadības kodus.


## <a name="column-types"></a>Kolonnas tipi
Informācijas tips, ko satur katra kolonna pārskatā, tiek norādīts ar vērtību rindā **Kolonnas tipu** kolonnas definīcijā. Katras kolonnas definīcijai jāsatur vismaz vienu apraksta kolonnu (**DESC**) un vienu summas kolonnu (**FD**, **WKS** vai **CALC**). **Piezīme:** kolonnas tipa kodi neattiecas uz visām grāmatvedības sistēmām. Atlasot tipu, kas nav derīgs jūsu grāmatvedības sistēmai, šī kolonna pārskatā ir tukša.

### <a name="specify-a-column-type"></a>Norādīt kolonnas tipu

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Atbilstošajā kolonnā, veiciet dubultklikšķi uz šūnas rindā **Kolonnas tips**.
3.  Atlasiet kolonnas tipu sarakstā. Tabulā ir aprakstīti dažādi kolonnu tipi.
    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Kolonnas tipa kods</th>
    <th>Apraksts</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>FD</td>
    <td>Rādīt finanšu datus vai datus no Excel darblapas, izmantojot kolonnu <strong>Saite uz finanšu dimensijām</strong> vai kolonnu <strong>Saite uz darblapu</strong> rindas definīcijā. Atlasot <strong>FD</strong> kolonnas tipu, noklusējuma iestatījumi tiek automātiski norādīti šādām rindām: <ul>
    <li><strong>Grāmatas kods/Kategorijas atribūts:</strong> FAKTISKAIS</li>
    <li><strong>Grāmatas kods/Kategorijas atribūts:</strong> FAKTISKAIS</li>
    <li><strong>Finanšu gads:</strong> PAMATA</li>
    <li><strong>Periods:</strong> PAMATA</li>
    <li><strong>Iekļautie periodi:</strong> PERIODISKS</li>
    <li><strong>Kolonnas platums:</strong> 14</li>
    </ul>
Šos noklusējuma iestatījumus jūs varat mainīt.</td>
    </tr>
    <tr class="even">
    <td>CALC</td>
    <td>Parāda vienkāršu vai sarežģītu aprēķinu rezultātu, kas ir norādīti šūnā <strong>Formula</strong>. Plašāku informāciju skatiet sadaļā <a href="advanced-formatting-options-financial-reporting.md">Paplašinātas formatēšanas opcijas finanšu pārskatos</a>.</td>
    </tr>
    <tr class="odd">
    <td>DESC</td>
    <td>Rādīt rindu aprakstu no rindas definīcijas. Kaut arī apraksta kolonna bieži vien ir pirmā kolonna pārskatā, tā var būt jebkurā vietā.</td>
    </tr>
    <tr class="even">
    <td>RINDA</td>
    <td>Parāda finanšu rindas atsevišķām kodu rindām kolonnā <strong>Rindas kods</strong> rindas definīcijā. Plašāku informāciju skatiet sadaļā <a href="row-definitions-financial-reporting.md">Finanšu pārskatu rindu definīcijas</a>.</td>
    </tr>
    <tr class="odd">
    <td>ACCT (Kontu kodi)</td>
    <td>Parāda finanšu datu segmentu vērtības vai dimensijas vērtības, kas attiecas uz katru rindu. Kontu un darbības detaļu pārskatiem tiek drukāts pilnībā derīgs konts (piemēram, <strong>110140-070-0101</strong>). Ja diapazoni ir norādīti kolonnā <strong>Saite uz finanšu dimensijām</strong>, saistītā rindas definīcijā, diapazons ir ietverts kvadrātiekavās un tiek uzskatīts par vienu vērtību (piemēram, <strong>[110140:110700]-070-[0101:0200]</strong>). Finanšu pārskatiem un augsta līmeņa pārskatiem, kas ir vairāku kontu kombinācija, finanšu datu saite tiek drukāta no rindas definīcijas (piemēram, <strong>1100:1200</strong>).</td>
    </tr>
    <tr class="even">
    <td>FILL</td>
    <td>Aizpildīt šūnu ar rakstzīmi, kas ir iekļauta vienpēdiņās. Ja jūs neievadāt rakstzīmi, kolonna ir tukša. Piemēram, lai aizpildītu kolonnu ar daudzpunkti (...), ievadiet <strong>FILL</strong> <strong>'.'</strong>.</td>
    </tr>
    <tr class="odd">
    <td>PAGE</td>
    <td>Iespraust pārskatā vertikālu lappušu pārtraukumu. Kolonnas, kas atrodas pa labi no kolonnas <strong>PAGE</strong>, parādās citā lappusē.</td>
    </tr>
    <tr class="even">
    <td>WKS</td>
    <td>Parāda datus, kas ir izgūti no Excel darblapas. Atlasot <strong>WKS</strong> kolonnas tipu, noklusējuma iestatījumi tiek automātiski norādīti šādām rindām: <ul>
    <li><strong>Finanšu gads:</strong> PERIODISKS</li>
    <li><strong>Periods:</strong> PAMATA</li>
    </ul>
Šos noklusējuma iestatījumus jūs varat mainīt.</td>
    </tr>
    <tr class="odd">
    <td>ATTR</td>
    <td>Ja jūsu grāmatvedības sistēma atbalsta atribūtus, kolonnā parādiet konta vai darījuma atribūtu. Atribūts, kuram jābūt piemērotam vienam pilnam kontam, izgūst pamata kontu vai darbības informāciju no finanšu datiem. Konta līmeņa atribūti attēlo datus no konta, un transakcijas līmeņa atribūti attēlo datus, kas radās transakcijas grāmatošanas laikā. Ja kā kolonnas tipu atlasāt <strong>ATTR</strong>, norādiet atribūta kategoriju kolonnas definīcijas detalizētas informācijas rindā <strong>Grāmatas kods/atribūta kategorija</strong>.</td>
    </tr>
    </tbody>
    </table>

### <a name="financial-dimensions-column"></a>Finanšu dimensijas kolonna

Rindas definīcijas **Kolonnas definīcija** tiek piemērotas kolonnām, kuru kolonnas tips ir **FD** (summas no finanšu dimensijām).

#### <a name="book-codeattribute-category-cell"></a>Šūna Grāmatas kods/Kategorijas atribūts

Šūna **Grāmatas kods/atribūtu kategorijas** identificē grāmatas kodu **FD** kolonnas datiem. Kolonnas definīcija var ietvert vairākas faktiskās, budžeta un statistikas kolonnas. Kolonnas definīcija var parādīt dažādus periodus, piemēram, pašreizējais vai no gada sākuma, un dažādas summas. Grāmatas kodu saraksts atspoguļo faktiskās, budžeta un statistikas (nefinanšu) opcijas, kas ir izveidotas jūsu finanšu datos.

#### <a name="fiscal-year-cell"></a>Šūna finanšu gads

Šūna **Finanšu gads** identificē finanšu gadu, kuram jābūt iekļautam kolonnā. Gads var attiecībā pret pamata gadu, kas ir norādīts pārskata izveides brīdī. Pieejamas šādas opcijas.

| Opcija  | Apraksts                                                                                                                  |
|---------|------------------------------------------------------------------------------------------------------------------------------|
| PAMATA    | Izmantojiet pamata gadu, kas ir norādīts pārskata laikā.                                                                          |
| PAMATA+\# | Izmantojiet gadu, kas ir \# gadus pēc pamata gada. Piemēram, lai izmantotu trešo gadu pēc pamata gada, ievadiet **PAMATA+3**. |
| PAMATA-\# | Izmantojiet gadu, kas ir \# gadus pirms pamata gada. Piemēram, lai izmantotu iepriekšējo gadu, ievadiet **PAMATA-1**.                 |
| \#      | Ievadiet faktisko finanšu gadu.                                                                                                |

#### <a name="period-cell"></a>Perioda šūna

Šūna **Periods** identificē finanšu periodu, kuram jābūt iekļautam kolonnā. Periods var būt attiecībā pret pamata periodu, kas ir norādīts pārskata izveides brīdī. Pieejamas šādas opcijas.

| Opcija          | Apraksts                                                                                                                                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PAMATA            | Izmantojiet pamata periodu.                                                                                                                                                                                                                 |
| PAMATA+\#         | Izmantojiet periodu, kas ir \# periodus pēc pamata perioda. Piemēram, lai izmantotu trešo periodu pēc pamata perioda, ievadiet **PAMATA+3**.                                                                                               |
| PAMATA-\#         | Izmantojiet periodu, kas ir \# periodus pirms pamata perioda. Piemēram, lai izmantotu iepriekšējo periodu, ievadiet **PAMATA-1**.                                                                                                                 |
| PAMATA-\#:PAMATA    | Izmantojiet vairākus periodus, no vairākiem periodiem pirms pamata perioda līdz pamata periodam. Piemēram, lai izmantotu trīs iepriekšējos periodus un pamata periodu, ievadiet **PAMATA-3:PAMATA**.                                                |
| PAMATA:PAMATA+\#    | Izmantojiet vairākus periodus, no pamata perioda līdz vairākiem periodiem pēc pamata perioda. Piemēram, lai izmantotu pamata periodu un trīs sekojošus periodus, ievadiet **PAMATA:PAMATA+2**.                                                  |
| PAMATA-\#:PAMATA+\# | Izmantojiet vairākus periodus, no vairākiem periodiem pirms pamata perioda līdz vairākiem periodiem pēc pamata perioda. Piemēram, lai izmantotu trīs iepriekšējos periodus, pamata periodu un divus sekojošus periodus, ievadiet **PAMATA-3:PAMATA+2**. |
| 1:PAMATA          | Izmantot vairākus periodus, no pirmā perioda līdz pamata periodam.                                                                                                                                                                 |
| \#              | Vienmēr izmantojiet noteikta perioda numuru. Nav ieteicams izmantot šo iespēju, jo tā samazina kolonnas definīcijas elastību.                                                                                       |
| \#:\#           | Vienmēr izmantojiet noteiktu periodu diapazonu. Nav ieteicams izmantot šo iespēju, jo tā samazina kolonnas definīcijas elastību.                                                                                    |

Jūs varat pārsniegt finanšu gada robežas jebkurā no perioda specifikācijām, un jūs varat sajaukt gadus periodu diapazonā. Piemēram, jūs periodu norādāt kā **PAMATA-5** (lai apzīmētu pēdējos sešus periodus) un palaižat pārskatu, kura pamata periods ir 2. Tādā gadījumā pārskatā tiek rādīti norādītā finanšu gada pirmo divu periodu dati un iepriekšējā finanšu gada pēdējie četri periodi.

### <a name="specify-the-periods-for-an-fd-column"></a>Norādiet periodus FD kolonnai

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Kolonnā **FD**, veiciet dubultklikšķi uz šūnas rindā **Periods**, un pēc tam sarakstā atlasiet opciju.
3.  Aizpildiet formulu joslā virs navigācijas rūts, vai arī šūnā **Periods**. Aizstājiet jebkuru numura zīmi (\#) ar atbilstošo vērtību.

#### <a name="periods-covered-cell"></a>Šūna Iekļautie periodi

Šūna **Iekļautie periodi** identificē daudzumu, kuram jābūt parādītam kolonnā. Šī summa ir saistīta ar vērtību kolonnas šūnās **Finanšu gads** un **Periods**. Pieejamas šādas opcijas.

| Opcija      | Apraksts                                                                 |
|-------------|-----------------------------------------------------------------------------|
| PERIODIC    | Parāda aktivitātes summu pašreizējam periodam vai periodu diapazonam. |
| PERIODISKS/BB | Parāda sākuma bilanci pašreizējam periodam vai periodu diapazonam.   |
| YTD         | Parāda aktivitātes summu no gada sākuma.                               |
| YTD/BB      | Parāda gada sākuma bilanci.                                 |

### <a name="specify-the-periods-that-are-covered-for-an-fd-column"></a>Norādiet periodus, kas ir iekļauti FD kolonnai

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Kolonnā **FD**, veiciet dubultklikšķi uz šūnas rindā **Iekļautie periodi**, un pēc tam sarakstā atlasiet opciju.

### <a name="attribute-filter-in-a-column-definition"></a>Atribūtu filtrs kolonnas definīcijā

Atribūti ir finanšu datu vērtības, kas definē kontu vai darbību. Konta atribūti ietver **Pamatlīdzeklis**, **Saistības**, **Ieņēmumi** un **Izdevumi**. Darbības atribūti ietver **Darbības apraksts** un **Darbības piemērošanas datums**. Atribūta atbalsts var atšķirties Microsoft Dynamics ERP sistēmās. Šūna **Atribūtu filtrs** ierobežo datus **FD** kolonnās, līdz noteiktām vērtībām vai diapazoniem atribūta kategorijām. Kaut gan šo līdzekli var izmantot kopā ar **ATTR** kolonnu, **ATTR** kolonna nav nepieciešama. Kolonnā **FD** ir ierobežojums kontiem vai darbībām, kurus pārskats iekļaus no atribūta filtra. **Piezīme:** lai noskaidrotu, kurus atribūtus atbalsta jūsu ERP sistēma, skatiet jūsu sistēmas integrācijas rokasgrāmatu.

#### <a name="apply-an-attribute-filter-for-an-fd-column-on-a-report"></a>Pielietojiet atribūtu filtru FD kolonnai pārskatā

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Veiciet dubultklikšķi uz šūnas **Atribūtu filtrs**, kolonnai **FD**.
3.  Dialoglodziņā **Atribūtu filtrs**, veiciet dubultklikšķi uz šūnas kolonnā **Atribūts**, un pēc tam atlasiet filtra tipu.
4.  Lai ierobežotu rezultātus, ievadiet diapazonu kolonnās **No** un **Līdz**. Šūnā **No** jābūt norādītai vērtībai.
5.  Noklikšķiniet uz **Labi**.

#### <a name="example-of-an-attribute-filter"></a>Atribūtu filtra piemērs

Šajā piemērā ir redzama daļa no kolonnas apraksta, kas ir konta atribūts rindā **Grāmatas kods/Kategorijas atribūts**. Atribūtu filtrs šajā kolonnā norāda pārskatā iekļaujamo vērtību diapazonu.

|                              | A    | B                    |
|------------------------------|------|----------------------|
| Kolonnas tips                  | DESC | FD                   |
| Grāmatas kods/Kategorijas atribūts |      | FAKTISKAIS               |
| Finanšu gads                  |      | PAMATA                 |
| Periods                       |      | 1:PAMATA               |
| Iekļautie periodi              |      | PERIODISKS             |
| ...                          |      |                      |
| Kolonnas platums                 | 30   |                      |
| ...                          |      |                      |
| Atribūtu filtrs             |      |  Atsauce=\[01:10\] |

### <a name="dimension-filter-in-a-column-definition"></a>Dimensiju filtrs kolonnas definīcijā

Dimensijas filtrs tiek izmantots, lai ierobežotu kolonnu **FD** līdz noteiktām dimensiju vērtībām. Filtrs var ietvert vienu dimensiju, dimensiju diapazonu vai dimensiju grupu. Filtrs var ietvert arī dimensiju vērtību kopas. Tā kā dimensiju vērtības var mainīties, tad sistēmai, kas ir balstīta uz \finanšu dimensijām\dimensijām, nav jāatbilst precīzam garumam. Neatkarīgi no tā, vai pārskatā ir ietverts pārskata koks, tiek izmantots filtrs. Jebkurā vietā varat izmantot aizstājējzīmes (\* vai ?). Norādot vairākus kontus, starp kontiem ir jāliek komati, kā redzams šajā piemērā: +Konts=\[1200\], +Konts=\[1100\], Nodaļa=\[01?\] Lai saņemtu visas nodaļas noteiktam kontam, jūs varat izslēgt nodaļas dimensiju no dimensiju filtra. Piemēram, abi šo dimensiju filtri tiek apstrādāti tādā pašā veidā:

-   +Konts=\[1100\],Nodaļa
-   +Konts=\[1100\]

Precīzai salīdzināšanai jūs varat arī izmantot jebkuru burtu un ciparu rakstzīmju kombināciju, kā arī jūs varat definēt daļējas dimensijas. Piemēram, **Novietojums = \[10\*\]** ietver visas novietojuma dimensiju vērtības, kas sākas ar 10.

#### <a name="apply-a-dimension-filter-for-a-column-on-a-report"></a>Pielietot kolonnai dimensiju filtru pārskatā

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Veiciet dubultklikšķi uz šūnas **Dimensiju filtrs**, kolonnai **FD**.
3.  Dialoglodziņā **Dimensijas**, ievadiet filtrus pielietošanai.
4.  Noklikšķiniet uz **OK**.

### <a name="format-a-multiple-currency-report-in-a-column-definition"></a>Formatēt daudzvalūtu pārskatu kolonnas definīcijā

Daudzvalūtu pārskatā var parādīt summas nacionālajā (vietējā) valūtā, funkcionālajā (noklusētajā) valūtā vai pārskata valūtā. Uzņēmuma funkcionālā valūta tiek definēta Microsoft Dynamics ERP sistēmā. Nesajauciet šo ERP iestatījumu ar operētājsistēmas reģionālo opciju iestatījumu, kur jūs varat konfigurēt noklusējuma valūtas simbolus, kas tiek izmantoti pārskatos. Šādas ar valūtu saistītas šūnas ir pieejamas kolonnas definīcijā:

-   **Valūtas parādīšana** — norādiet valūtas tipu (nacionālā, funkcionālā vai pārskata), kurā tiek rādītas transakcijas. Šī funkcionalitāte dažreiz tiek saukta par valūtas pārrēķināšanu. Valūtas pārrēķināšana ir spēja izveidot pārskatu par virsgrāmatas summām, valūtā, kas varētu nebūt uzņēmuma funkcionālā valūta, vai valūtā, kas tika ievadīta darbībai.
-   **Valūtas filtrs** – norādiet valūtas filtru. Atskaitē tiek rādītas tikai darbības, kas tika ievadītas atlasītajā valūtā.

> [!NOTE]
> Lai izveidotu pārskatus, kuros tiek izmantotas vairākas valūtās, jums ir jāatlasa izvēles rūtiņa **Iekļaut visas pārskatu veidošanas valūtas** pārskata definīcijas cilnē **Pārskats**. Lai noteiktu uzņēmuma funkcionālo valūta, rīkojieties šādi.

1.  Pārskatu veidotājā, izvēlnē **Uzņēmums**, noklikšķiniet uz **Uzņēmumi**.
2.  Dialoglodziņā **Uzņēmumi**, atlasiet uzņēmumu, un tad noklikšķiniet **Skatīt**.
3.  Dialoglodziņā **Skatīt uzņēmumu**, sadaļā **Reģionālās opcijas**, jūs varat skatīt valūtu, kas ir definēta atlasītajam uzņēmumam.

#### <a name="specify-the-currency-on-a-multiple-currency-report"></a>Norādiet valūtu daudzvalūtu pārskatā

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Veiciet dubultklikšķi uz šūnas **Valūtas parādīšana** atbilstošajā **FD** kolonnā, un pēc tam atlasiet valūtas informācijas parādīšanas opciju: **Nacionālā/izcelsmes valūta**, **Funkcionālā valūta no uzņēmuma informācijas** vai pārskata valūta.
3.  Veiciet dubultklikšķi uz šūnas **Valūtas filtrs** atbilstošajā **FD** kolonnā, un pēc tam sarakstā atlasiet atbilstošu valūtas kodu. Atskaitē tiek rādītas tikai darbības, kas tika ievadītas šajā valūtā.

> [!NOTE]
> Šeit aprakstītās opcijas var atšķirties atkarībā no ERP sistēmas. Papildinformāciju skatiet savā [Microsoft ERP sistēmas dokumentācijā](https://www.microsoft.com/en-us/download/details.aspx?id=5916).

### <a name="example-for-currency-display-and-currency-filter-cells"></a>Piemērs Valūtas parādīšanas un Valūtas filtra šūnām

Madara kolonnas definīcijā veica šādas valūtas atlases:

-   **Valūtas filtrs:** jēna
-   **Valūtas parādīšana:** funkcionālā (ASV dolāri)

Madaras atlasītā valūtas filtra dēļ, pārskats ietver tikai darbības, kas tika ievadītas Japānas jēnās (JPY). Viņas izvēlētās parādīšanas valūtas dēļ, pārskatā tiek parādītas darbības funkcionālajā valūtā, ASV dolāros (USD).

#### <a name="currency-filter-and-currency-display-combinations"></a>Valūtas filtra un Valūtas parādīšanas kombinācijas

Šajā tabulā ir parādīti pārskata rezultāti, kas var rasties dažādām opciju kombinācijām šūnās **Valūtas parādīšana** un **Valūtas filtrs**, Madaras veiktās atlases dēļ. Funkcionālā valūta ir USD.

| Valūtas parādīšanas šūna                        | Valūtas filtra šūna | Pārskata rezultāts                                                                                                                                                                                    |
|----------------------------------------------|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nacionālā/izcelsmes valūta                 | **JĒNA**              | **Y6 000** – rezultāts rāda tikai darbības, kas tika ievadītas JPY.                                                                                                                        |
| Funkcionālā valūta no uzņēmuma informācijas | **JĒNA**              | **$60** – rezultāts rāda tikai darbības, kas tika ievadītas JPY, un attēlo tās darbības USD. **Piezīme:** konvertēšanas maiņas kurss ir aptuveni 100 JPY par vienu USD.                    |
| Funkcionālā valūta no uzņēmuma informācijas | Tukšs                | **$2310\*\*** — rezultāts rāda visus datus funkcionālajā valūtā, kas ir norādīta uzņēmuma informācijā. **Piezīme:** šī summa ir visu darbību summa funkcionālajā valūtā. |
| Nacionālā/izcelsmes valūta                 | Tukšs                | **$2250** – rezultāts rāda visas summas valūtā, kurā tika veikta darbība.                                                                                                 |

### <a name="calculation-column-in-a-column-definition"></a>Aprēķina kolonna kolonnas definīcijā

Kolonnas tips **CALC** kolonnas definīcijā atbalsta sarežģītus aprēķinus šūnā **Formula** un var ietvert operatorus **+**, **-**, **\*** un **/**, kā arī apgalvojumus **IF/THEN/ELSE**. Aprēķina kolonna var arī atsaukties uz jebkuru citu kolonnu, pat nākamajām kolonnām. Turklāt aprēķina kolonna var arī saturēt finanšu gadu un periodu, lai atbalstītu galvenes kolonnas. Aprēķina formula var saturēt ne vairāk kā 1024 burtciparu rakstzīmes. Lai izteiktu aprēķina rezultātu procentos, izmantojiet īpašu formāta ignorēšanu. **Piezīme:** aprēķina formulu rezultāti neiekļauj nedrukāšanas kolonnu diapazonu vērtības. Piemēram, **A:D** drukā **0** (nulle), bet **A+B+C** aprēķina vērtību nedrukāšanas vērtībām.

#### <a name="operators-in-calculation-columns"></a>Operatori aprēķina kolonnās

Lai saskaitītu, atņemtu, reizinātu vai dalītu kolonnas, ievadiet kolonnu burtus aprēķina secībā, un pēc tam izmantojiet atbilstošu operatoru katras kolonnas burta atdalīšanai. Šajā tabulā sniegts pārskats par operatoriem, kurus jūs varat izmantot aprēķina kolonnā.

| Operators | Piemēra aprēķins | Apraksts                                                                                                                                                                                                                                    |
|----------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| +        | A+C                 | Pievienot summu kolonnā A summai kolonnā C.                                                                                                                                                                                          |
| :        | A:C A:C-D           | Pievienot secīgu kolonnu diapazonu. Piemēram, formula **A:C** pievieno kolonnu summas no A līdz C, un formula **A:C-D** saskaita kolonnu A – C summas, un pēc tam atņem summu kolonnā D.                          |
| -        | A-C                 | Atņemt summu kolonnā A no summas kolonnā C. **Piezīme:** jūs varat izmantot arī mīnus zīmi (-), lai mainītu zīmes kolonnā. Piemēram, izmantojiet **-A+B**, lai pievienotu pretēju A kolonnas summu, B kolonnas summai. |
| \*       | A\*C                | Reizināt summu kolonnā A ar summu kolonnā C.                                                                                                                                                                                     |
| /        | A/C                 | Dalīt summu kolonnā A ar summu kolonnā C.                                                                                                                                                                                       |

#### <a name="use-a-calculation-formula-in-a-column-definition"></a>Izmantot aprēķina formulu kolonnas definīcijā

1.  Pārskatu veidotājā atveriet modificējamo kolonnas definīciju.
2.  Atbilstošajā kolonnā **CALC**, ievadiet formulu šūnā **Formula**.

#### <a name="complex-calculations"></a>Sarežģīti aprēķini

Sarežģīti aprēķini var ietvert jebkuru šūnu atsauču kombināciju, operatorus, vērtības un ligzdoto iekavu līmeņus. Piemēram, lai aprēķinātu kolonnu A un B vidējo vērtību, izmantojiet aprēķina formulu **((A+B)/2)**.

#### <a name="specify-report-cells-in-a-column-calculation"></a>Norādiet pārskata šūnas kolonnas aprēķinā

Jūs varat atsaukties uz noteiktu pārskata šūnu, ievadot kolonnas burtu un rindas kodu. Piemēram, **B.100** attiecas uz rindas kodu 100, kolonnā B. Jūs varat dalīt visu kolonnu ar noteiktu pārskatu šūnas summu, kas ir tajā pašā kolonnā. Piemēram, aprēķins **B/B.100** nozīmē, ka summa B kolonnā būtu jādala ar vērtību rindā ar kodu 100, kolonnā B. Ja aprēķins attiecas uz kolonnu, kas ir atkarīga no citas kolonnas, atkarīgā kolonna ir jāatrisina vispirms. Ja jūs kolonnai veidojat atsauci uz citu kolonnu, kurai ir atsauce uz pirmo kolonnu, tiks izveidota riņķveida atsauces kļūda. **Piezīme:** aprēķins varētu būt nepareizs, ja maināt aprēķina prioritāti pārskatam. Jūs varat iestatīt aprēķina prioritāti pārskata definīcijas cilnē **Iestatījumi**.

#### <a name="multiply-or-divide-a-column-by-a-base-row"></a>Reizināt vai dalīt kolonnu ar pamata rindu

Jūs varat izveidot kolonnu, kas rāda visas vērtības noteiktā kolonnā kā procentus no pamata skaitļa. Tādējādi jūs varat parādīt attiecības starp rindām procentos no pārdošanas rindas, vai procentos no kopējo izdevumu rindas. Lai katrā noteiktas kolonnas rindā reizinātu vai dalītu ar pamata rindu, ievadiet kolonnu, kuru izmantot aprēķinā, un pēc tam ievadiet **\*BASEROW** vai **/BASEROW**. Piemēram, ievadiet **C\*BASEROW** vai **C/BASEROW**. **Piezīme.** Lietojot pamata rindas aprēķinu kolonnas definīcijā, pārliecinieties, ka katra rindas definīcija, kas tiek izmantota šajā kolonnas definīcijā, satur vismaz vienu pamata rindu aprēķiniem.

#### <a name="divide-the-amount-in-a-column-by-the-number-of-periods"></a>Summa kolonnā daliet ar periodu skaitu

Jūs varat dalīt summu kolonnā ar norādīto periodu skaitu. Piemēram, formula **B/periodi** izdala vērtību kolonnā B ar periodu skaitu kolonnā B. Ja aprēķins aptver vairākas kolonnas, norādiet periodu skaitu, izmantošanai aprēķinā. Piemēram, formula **(B+C)/periodi** saskaita summas kolonnā B un kolonnā C, un pēc tam dala rezultātu ar perioda vērtību.

<a name="see-also"></a>Skatiet arī
--------

[Rindas definīcijas finanšu pārskatos](row-definitions-financial-reporting.md)

[Papildu formatēšanas opcijas finanšu pārskatos](advanced-formatting-options-financial-reporting.md)




