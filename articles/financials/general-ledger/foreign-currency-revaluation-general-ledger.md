---
title: Ārvalstu valūtas pārvērtēšana Virsgrāmatai
description: 'Šajā tēmā ir sniegts pārskats par šādiem ārvalstu valūtas pārvērtēšanas procesiem Virsgrāmatā: iestatīšana, procesa izpilde, procesa aprēķini un pārvērtēšanas transakciju anulēšana nepieciešamības gadījumā.'
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf61aa839d4d59b2c93eee9931eef0e6c51d4ac
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839309"
---
# <a name="foreign-currency-revaluation-for-general-ledger"></a>Ārvalstu valūtas pārvērtēšana Virsgrāmatai

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts pārskats par šādiem ārvalstu valūtas pārvērtēšanas procesiem Virsgrāmatā: iestatīšana, procesa izpilde, procesa aprēķini un pārvērtēšanas transakciju anulēšana nepieciešamības gadījumā. 

Kā daļu no perioda beigām grāmatvedības metodes nosaka, ka virsgrāmatas kontu bilances, kas ir ārvalstu valūtās, ir nepieciešams pārvērtēt, izmantojot dažādus valūtas maiņas kursa tipus (pašreizējo, vēsturisko, vidējo un citus). Piemēram, viena grāmatvedības metode pieprasa, lai aktīvi un pasīvi tiktu pārvērtēti pēc pašreizējā valūtas maiņas kursa, pamatlīdzekļi — pēc vēsturiskā maiņas kursa, un peļņas un zaudējumu konti — pēc mēneša vidējā kursa. Virsgrāmatas ārvalstu valūtas pārvērtēšanu var izmantot, lai pārvērtētu bilances un peļņas un zaudējumu kontus. 

> [!NOTE]
> Ārvalstu valūtas pārvērtēšana ir pieejama arī moduļos Debitoru parādi un Parādi kreditoriem. Ja izmantojat šos moduļus, nenokārtotās transakcijas ir jāpārvērtē, izmantojot ārvalstu valūtas pārvērtēšanu šajos moduļos. AR un AP ārvalstu valūtas pārvērtēšana izveidos grāmatvedības ierakstu virsgrāmatā, lai atspoguļotu nerealizēto peļņu vai zaudējumus, tādējādi nodrošinot, ka apakšgrāmatas un virsgrāmatu var saskaņot. Tā kā AR un AP ārvalstu valūtas pārvērtēšana izveido grāmatvedības ierakstus virsgrāmatā, tad galvenie konti moduļos Debitoru parādi un Parādi kreditoriem ir jāizslēdz no virsgrāmatas ārvalstu valūtas pārvērtēšanas. 

Kad palaižat pārvērtēšanas procesu, tiek pārvērtēta bilance katrā galvenajā kontā, kurš ir grāmatots ārvalstu valūtā. Nerealizētās peļņas vai zaudējumu transakcijas, kas tiek izveidotas pārvērtēšanas procesā, ģenerē sistēma. Var izveidot divas transakcijas — vienu uzskaites valūtai un otru pārskata valūtai, ja tas ir vajadzīgs. Katrs uzskaites ieraksts tiks grāmatots nerealizētajā peļņā vai zaudējumos, kā arī galvenajā kontā, kam tiek veikta pārvērtēšana.

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

Izmantot Izmantojot lauku **Likmes datums**, varat norādīt noklusējuma maiņas kursa datumu. Piemēram, varat pārvērtēt bilances datumu diapazonā no 1. janvāra līdz 31. janvārim, izmantojot 1. februārim norādīto maiņas kursu. 

Atlasiet, kurus galvenos kontus pārvērtēt: Visi, Bilance vai Peļņa un zaudējumi. Tiek pārvērtēti tikai tie galvenie konti, kas ir atzīmēti pārvērtēšanai (lapā Galvenais konts). Ja vēlaties precizēt galveno kontu diapazonu, norādiet galveno kontu diapazonu vai atsevišķus galvenos kontus cilnē **Iekļaujamie ieraksti**. 

Pārvērtēšanas procesu var izpildīt vienai vai vairākām juridiskajām personām. Uzmeklēšanas sarakstā tiek rādītas tikai tās juridiskās personas, kurām varat piekļūt. Atlasiet juridiskās personas, kurām vēlaties izpildīt pārvērtēšanas procesu. 

Pārvērtēšanu var palaist vienai vai vairākām ārvalstu valūtām. Uzmeklēšanas sarakstā ir iekļautas visas valūtas, kas ir grāmatotas norādītajā datumu diapazonā saistībā ar attiecīgo galvenā konta veidu (Bilance vai Peļņa un zaudējumi) pārvērtēšanai atlasītajām juridiskām personām. Šajā sarakstā ir iekļauta uzskaites valūta, taču, ja tā tiek atlasīta, nekas netiek pārvērtēts. 

Ja vēlaties pārskatīt Virsgrāmatas pārvērtēšanas rezultātu, iestatiet opcijas **Priekšskatīt pirms grāmatošanas** vērtību **Jā**. Virsgrāmatas priekšskatījums atšķiras no ārvalstu valūtas pārvērtēšanas simulācijas modulī Debitoru parādi vai Parādi kreditoriem. Simulācija modulī Debitoru parādi vai Parādi kreditoriem ir pārskats, taču Virsgrāmatas priekšskatījumu var grāmatot, atkārtoti neveicot pārvērtēšanas procesu. Priekšskatījuma rezultātus var eksportēt uz programmu Microsoft Excel, lai saglabātu summu aprēķināšanas vēsturi. Ja vēlaties priekšskatīt pārvērtēšanas rezultātus, nevar izmantot pakešapstrādi. No priekšskatījuma lietotājam ir iespēja grāmatot visu juridisko personu rezultātus, izmantojot pogu **Grāmatot**. Ja kādas juridiskās personas rezultātos pastāv problēma, lietotājam ir arī iespēja grāmatot juridisko personu apakškopu, izmantojot pogu **Atlasīt grāmatojamās juridiskās personas**. 

Pēc ārvalstu valūtas pārvērtēšanas procesa pabeigšanas tiek izveidots ieraksts, kas sniedz iespēju izsekot katras izpildes vēsturi.  Katrai juridiskajai personai un grāmatošanas līmenim tiek izveidots atsevišķs ieraksts.

## <a name="calculate-unrealized-gainloss"></a>Aprēķināt nerealizēto peļņu/zaudējumus
Virsgrāmatas pārvērtēšanas un AR un AP pārvērtēšanas procesos nerealizētās peļņas/zaudējumu transakcijas tiek izveidotas atšķirīgi. Moduļos AR un AP iepriekšējā pārvērtēšana tiek pilnīgi anulēta (pieņemot, ka transakcija vēl nav nosegta) un nerealizētajai peļņai/zaudējumiem tiek izveidota jauna pārvērtēšanas transakcija, pamatojoties uz jauno valūtas maiņas kursu. Tas tiek darīts tādēļ, ka moduļos AR un AP mēs pārvērtējam katru atsevišķo transakciju. Virsgrāmatā netiek anulēta iepriekšējā pārvērtēšana. Tā vietā tiek izveidota transakcija starpībai starp galvenā konta bilanci, tostarp visām iepriekšējām pārvērtēšanas summām, un jauno vērtību, pamatojoties uz valūtas maiņas kursu datumā, kas ir norādīts laukā Likmes datums. 

**Piemērs.** Galvenajam kontam 110110 ir tālāk norādītās bilances.

|            |                    |                        |                       |
|------------|--------------------|------------------------|-----------------------|
| **Datums**   | **Virsgrāmatas konts** | **Darbības summa** | **Uzskaites summa** |
| 20. janvāris | 110110 (skaidra nauda)      | 500 EUR (debets)        | 1000 USD (debets)      |

31. janvārī tiek pārvērtēts galvenais konts.  Nerealizētā peļņa/zaudējumi tiek aprēķināti tālāk norādītajā veidā.

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

Februārī netiek grāmatota neviena jauna transakcija.  28. februārī tiek pārvērtēts galvenais konts.

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

Varat anulēt pārvērtēšanas rezultātus neatkarīgi no datumu secības, taču var būt nepieciešams anulēt arī jaunāku pārvērtēšanu, lai nodrošinātu, ka katra pārvērtētā galvenā konta bilance ir pareiza. Anulēšanu var veikt neatkarīgi no datumu secības, jo nevar kontrolēt to, kuri galvenie konti un cik bieži tiek pārvērtēti. Piemēram, organizācija var izvēlēties pārvērtēt savus skaidras naudas galvenos kontus reizi ceturksnī, taču visus citus galvenos kontus reizi mēnesī.



