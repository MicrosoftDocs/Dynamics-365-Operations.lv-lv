---
title: "Ārvalstu valūtas pārvērtēšana Virsgrāmatai"
description: "Šajā tēmā ir sniegts pārskats par šīm darbībām Virsgrāmatā ārvalstu valūtas pārvērtēšanas process - uzstādīšana, running procesu, aprēķinu procesā un kā atsaukt pārvērtēšanas darbību, vajadzības."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5d6d13fe44eef7766b4dcaf274c3522bce3da816
ms.lasthandoff: 03/31/2017


---

# <a name="foreign-currency-revaluation-for-general-ledger"></a>Ārvalstu valūtas pārvērtēšana Virsgrāmatai

Šajā tēmā ir sniegts pārskats par šīm darbībām Virsgrāmatā ārvalstu valūtas pārvērtēšanas process - uzstādīšana, running procesu, aprēķinu procesā un kā atsaukt pārvērtēšanas darbību, vajadzības. 

Kā daļu no perioda beigām grāmatvedības metodes nosaka, ka virsgrāmatas kontu bilances, kas ir ārvalstu valūtās, ir nepieciešams pārvērtēt, izmantojot dažādus valūtas maiņas kursa tipus (pašreizējo, vēsturisko, vidējo un citus). Piemēram, viena grāmatvedības metode pieprasa, lai aktīvi un pasīvi tiktu pārvērtēti pēc pašreizējā valūtas maiņas kursa, pamatlīdzekļi — pēc vēsturiskā maiņas kursa, un peļņas un zaudējumu konti — pēc mēneša vidējā kursa. Virsgrāmatas ārvalstu valūtas pārvērtēšanu var izmantot, lai pārvērtētu bilances un peļņas un zaudējumu kontus. 

> [!NOTE]
> Ārvalstu valūtas pārvērtēšanas pieejama arī kreditoru (kreditoru) un realizācijas (AR). Ja jūs izmantojat šos moduļus, izcilu darījumiem jāpārvērtē ārvalstu valūtas pārvērtēšanu, izmantojot šajos moduļos. AR un AP ārvalstu valūtas pārvērtēšana izveidos grāmatvedības ierakstu virsgrāmatā, lai atspoguļotu nerealizēto peļņu vai zaudējumus, tādējādi nodrošinot, ka apakšgrāmatas un virsgrāmatu var saskaņot. Tā kā AR un AP ārvalstu valūtas pārvērtēšana izveido grāmatvedības ierakstus virsgrāmatā, tad galvenie konti moduļos Debitoru parādi un Parādi kreditoriem ir jāizslēdz no virsgrāmatas ārvalstu valūtas pārvērtēšanas. 

Kad palaižat pārvērtēšanas procesu, tiek pārvērtēta bilance katrā galvenajā kontā, kurš ir grāmatots ārvalstu valūtā. Nerealizētās peļņas vai zaudējumu transakcijas, kas tiek izveidotas pārvērtēšanas procesā, ģenerē sistēma. Divas darbības iespējams veidot, viena norēķinu valūtu un otro par pārskata valūtā, ja nepieciešams. Nerealizētā peļņa vai zaudējumi un galveno kontu, tiek pārvērtēti katru grāmatvedības ierakstu post.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Sagatavot ārvalstu valūtas pārvērtēšanas palaišanu
Pirms palaižat pārvērtēšanas procesa, ir nepieciešami tālāk aprakstītie iestatījumi.

-   Lapā **Galvenais konts**:
-   Ja galvenais konts ir jāpārvērtē virsgrāmatā, atzīmējiet vienumu **Ārvalstu valūtas pārvērtēšana**. Ja galvenajam kontam nav jāveic pārvērtēšana (piemēram, attiecībā uz AR un AP, ja pārvērtēšana notiek apakšgrāmatās), notīriet šīs opcijas atzīmi.
-   Ja galvenais konts ir atzīmēts pārvērtēšanai, norādiet vērtību vienumam **Maiņas kursa tips**. Šis maiņas kursa tips tiks izmantots galvenā konta pārvērtēšanai. Finanšu pārskatu veidošanai ir pieejams atsevišķs lauks — **Finanšu pārskatu maiņas kursa tips**. Šie abi lauki netiek sinhronizēti, tādējādi ļaujot pārvērtēšanai un finanšu pārskatu veidošanai izmantot dažādus maiņas kursa tipus.

-   Lapā **Virsgrāmata**:
-   Norādiet vērtību vienumam **Maiņas kursa tips**. Ja galvenajā kontā nav definēts maiņas kursa tips, tad ārvalstu valūtas pārvērtēšanas laikā tiks izmantots šis maiņas kursa tips.
-   Norādiet realizētās peļņas, realizēto zaudējumu, nerealizētās peļņas un nerealizēto zaudējumu kontus valūtas pārvērtēšanai. Realizētās peļņas un realizēto zaudējumu konti tiek izmantoti, kad tiek nokārtotas AR un AP transakcijas, bet nerealizētās peļņas un nerealizēto zaudējumu konti tiek izmantoti atvērto transakciju un virsgrāmatas galveno kontu pārvērtēšanai.

-   Lapā **Valūtas pārvērtēšanas konti**:
-   Katrai valūtai un uzņēmumam atlasiet citus valūtas pārvērtēšanas kontus. Ja neviens konts nav definēts, tiek izmantoti konti no lapas **Virsgrāmata**.

## <a name="process-foreign-currency-revaluation"></a>Apstrādāt ārvalstu valūtas pārvērtēšanu
Kad iestatīšana ir pabeigta, izmantojiet lapu **Ārvalstu valūtas pārvērtēšana**, lai pārvērtētu galveno kontu bilances. Varat palaist procesu reāllaikā vai ieplānot tā palaišanu, izmantojot pakešuzdevumu. 

Lapā **Ārvalstu valūtas pārvērtēšana** tiek rādīta katra pārvērtēšanas procesa vēsture, tostarp laiks, kad šis process tika palaists, kādi kritēriji bija definēti, saite uz pārvērtēšanai izveidoto dokumentu, kā arī ieraksts, ja iepriekšējā pārvērtēšana tika anulēta. Lai palaistu pārvērtēšanas procesu, atlasiet pogu **Ārvalstu valūtas pārvērtēšana**. 

Vērtības **No datuma** un **Līdz datumam** definē pārvērtējamās ārvalstu valūtas bilances aprēķina datumu intervālu. Kad veicat pārvērtēšanu peļņas un zaudējumu kontos, tiek pārvērtēta summa no visām transakcijām, kas notikušas šajā datumu intervālā. Kad pārvērtējat bilances kontus, vērtība No datuma tiek ignorēta. Tās vietā pārvērtējamā bilance tiek noteikta, sākot no finanšu gada sākuma līdz vērtībai Līdz datumam. 

**Dienas likme** var izmantot, lai noteiktu datumu, kuram būtu noklusējuma valūtas kursu. Piemēram, var pārvērtēt līdzsvaru starp datumu diapazonā no 1 janvāris janvāris 31, bet izmanto tādu pašu maiņas kursu, kas noteikts 1. februāris. 

Atlasiet, kurus galvenos kontus pārvērtēt: Visi, Bilance vai Peļņa un zaudējumi. Tiks pārvērtēta tikai galvenā uzskaite iezīmēja pārvērtēšanai (lapā galvenais konts). Ja vēlaties vēl vairāk ierobežot diapazonā no galvenā uzskaite, izmantot ierakstus **iekļaut** tab, lai definētu diapazonu galvenā uzskaite, vai individuālie konti galvenajā. 

Pārvērtēšanas process var darbināt vienu vai vairākas juridiskas personas. Pārlūkfunkcija parādīs tikai juridiskas personas, kurām jums ir piekļuve. Atlasiet juridiskām personām, par kuru vēlaties izpildīt pārvērtēšanas process. 

Pārvērtēšanu var palaist vienai vai vairākām ārvalstu valūtām. Uzmeklēšanas ietvers visu valūtu, kas tika grāmatota norādītajā datumu diapazonā atbilst galvenais konts (bilances vai peļņas un zaudējumu), juridiskām personām, kas izvēlēti, lai pārvērtētu tipam. Sarakstā tiks iekļautas norēķinu valūtu, bet nekas pārvērtē, atlasot norēķinu valūtu. 

Iestatiet **Preview pirms grāmatošanas** uz **Jā** ja jūs vēlētos pārbaudīt Virsgrāmatas pārvērtēšanas rezultāts. Preview vispār grāmatas atšķiras no simulācija AR un AP ārvalstu valūtas pārvērtēšana. Simulācija AR un AP atskaites, bet Virsgrāmatā ir priekšskatījums, kuru var iegrāmatot, bez nepieciešamības vēlreiz palaidiet pārvērtēšanas process. Priekšskatījuma rezultātus var eksportēt uz Microsoft Excel, lai uzturētu summu aprēķināšanas vēsturi. Ja vēlaties priekšskatīt pārvērtēšanas rezultātus, nevar izmantot pakešapstrādi. No priekšskatījuma lietotājam ir iespēja grāmatot visu juridisko personu rezultātus, izmantojot pogu **Grāmatot**. Ja kādas juridiskās personas rezultātos pastāv problēma, lietotājam ir arī iespēja grāmatot juridisko personu apakškopu, izmantojot pogu **Atlasīt grāmatojamās juridiskās personas**. 

Pēc ārvalstu valūtas pārvērtēšanas process ir pabeigts, izsekot katras palaišanas vēsture tiks izveidots ieraksts.  Atsevišķu ierakstu tiks izveidota katrai juridiskai personai un Grāmatošanas slānis.

## <a name="calculate-unrealized-gainloss"></a>Aprēķināt nerealizēto peļņu/zaudējumus
Virsgrāmatas pārvērtēšanas un AR un AP pārvērtēšanas procesos nerealizētās peļņas/zaudējumu transakcijas tiek izveidotas atšķirīgi. Moduļos AR un AP iepriekšējā pārvērtēšana tiek pilnīgi anulēta (pieņemot, ka transakcija vēl nav nosegta) un nerealizētajai peļņai/zaudējumiem tiek izveidota jauna pārvērtēšanas transakcija, pamatojoties uz jauno valūtas maiņas kursu. Tas tiek darīts tādēļ, ka moduļos AR un AP mēs pārvērtējam katru atsevišķo transakciju. Virsgrāmatā, iepriekšējo pārvērtēšanas nav mainījusies. Tā vietā, delta starp galveno kontu, ieskaitot iepriekšējo pārvērtēšanas summas, un jaunā vērtība, pamatojoties uz norādīto maiņas kursu dienas likme bilances tiek veidota darbība. 

**Piemērs** šādas bilances pastāv galvenais konts 110110.

|            |                    |                        |                       |
|------------|--------------------|------------------------|-----------------------|
| **Datums**   | **Virsgrāmatas konts** | **Darbības summa** | **Uzskaites summa** |
| 20. janvāris | 110110 (skaidra nauda)      | 500 EUR (debets)        | 1000 USD (debets)      |

Galvenais konts ir pārvērtēta, 31. janvārī.  Nerealizēto peļņu/zaudējumus aprēķina šādi.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Pašreizējā bilance transakcijas valūtā** | **Pašreizējā bilance uzskaites valūtā** | **Valūtas maiņas kurss pie pārvērtēšanas** | **Jaunā uzskaites valūtas summa** | **Nerealizētā peļņa/zaudējumi**    |
| 500 EUR                                     | 1000 USD                                   | 166.6667                         | 833,33 EUR (500 x 1,666667)        | 166,67 zaudējumi (833,33 – 1000) |

Tiks izveidots tālāk norādītais uzskaites ieraksts.

|            |                          |           |            |
|------------|--------------------------|-----------|------------|
| **Datums**   | **Virsgrāmatas konts**       | **Debets** | **Kredīts** |
| 31. janvāris | 110110 (skaidra nauda)            |           | 166.67     |
| 31. janvāris | 801400 (nerealizētie zaudējumi) | 166.67    |            |

Nav jaunu tiek grāmatotas par februāra mēnesi.  28. februārī pārvērtē galvenajā kontā.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Pašreizējā bilance transakcijas valūtā** | **Pašreizējā bilance uzskaites valūtā** | **Valūtas maiņas kurss pie pārvērtēšanas** | **Jaunā uzskaites valūtas summa** | **Nerealizētā peļņa/zaudējumi**    |
| 500 EUR                                     | 833,33 USD (1000 - 166,67)                 | 250.0000                         | 1250 USD (500 x 2,5)               | 416,67 peļņa (1250 – 833,33) |

Tiks izveidots tālāk norādītais uzskaites ieraksts.

|             |                          |           |            |
|-------------|--------------------------|-----------|------------|
| **Datums**    | **Virsgrāmatas konts**       | **Debets** | **Kredīts** |
| 28. februāris | 110110 (skaidra nauda)            | 416.67    |            |
| 28. februāris | 801600 (nerealizētā peļņa) |           | 416.67     |

## <a name="reverse-foreign-currency-revaluation"></a>Anulēt ārvalstu valūtas pārvērtēšanu
Ja ir nepieciešams anulēt pārvērtēšanas transakciju, atlasiet pogu **Anulēt transakciju** lapā **Ārvalstu valūtas pārvērtēšana**. Tiek izveidots jauns ārvalstu valūtas pārvērtēšanas vēsturiskais ieraksts, lai uzturētu vēsturiskos auditācijas pierakstus par to, kad pārvērtēšana notika vai tika anulēta. 

Nav dienas kārtībā pārvērtēšanas rezultātus var atcelt, bet jums var būt nepieciešams arī apgriezt precīzākām pārvērtēšanu, lai nodrošinātu pareizu katras pārvērtētās galveno kontu atlikumus. Maiņas var rasties no dienas kārtībā, jo tur ir veids, kā kontrolēt, kuras galvenā uzskaite tiek pārvērtēta un biežumu, kad tie tiek pārvērtēti. Piemēram, organizācija var pārvērtēt savas naudas galvenā uzskaite pa ceturkšņiem, bet visu pārējo galveno kontu katru mēnesi.


