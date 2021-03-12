---
title: Valūtas pārvērtēšana moduļiem “Kreditori“ un “Debitori”
description: Valūtas maiņas kursu svārstības laikā gaitā izraisa neapmaksāto transakciju teorētiskās vērtības (atlikušās vērtības) ārvalstu valūtās izmaiņas. Šajā rakstā ir sniegta informācija par ārvalstu valūtas pārvērtēšanas procesu, kas tiek veikts, lai atjauninātu kreditoru un debitoru neapmaksāto transakciju vērtību.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustExchRateAdjustment, VendExchRateAdjustment
audience: Application User
ms.reviewer: roschlom
ms.custom: 14211
ms.assetid: defb1ea5-1f3e-4859-87d8-3f9954d3f388
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec17572612da7152ca0737cbd9f327d29dc54f8c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985241"
---
# <a name="currency-revaluation-for-accounts-payable-and-accounts-receivable"></a>Valūtas pārvērtēšana moduļiem “Kreditori“ un “Debitori”

[!include [banner](../includes/banner.md)]

Valūtas maiņas kursu svārstības laikā gaitā izraisa neapmaksāto transakciju teorētiskās vērtības (atlikušās vērtības) ārvalstu valūtās izmaiņas. Šajā rakstā ir sniegta informācija par ārvalstu valūtas pārvērtēšanas procesu, kas tiek veikts, lai atjauninātu kreditoru un debitoru neapmaksāto transakciju vērtību. 

Neapmaksāto transakciju ārvalstu valūtās teorētiskā vai atlikusī vērtība laika gaitā mainās valūtas maiņas kursu svārstību dēļ. Lai atjauninātu kreditoru un debitoru neapmaksāto transakciju vērtību, izpildiet ārvalstu valūtas pārvērtēšanas procesu. Ārvalstu valūtas pārvērtēšanu var veikt gan kreditoru, debitoru parādiem. Procesā tiek izmantots jauns valūtas maiņas kurss, lai pārvērtētu neapmaksātās summas vai nenosegtās summas uz konkrēto datumu. Starpība starp sākotnēji iegrāmatotajām summām un pārvērtētajām summām rada katras neapmaksātās transakcijas nerealizēto peļņu vai zaudējumus. Pēc tam tiek atjauninātas parādu kreditoriem un debitoru parādu apakšgrāmatas, lai reģistrētu nerealizēto peļņu vai zaudējumus, un Virsgrāmatā tiek grāmatots uzskaites ieraksts.

## <a name="simulate-a-foreign-currency-revaluation"></a>Simulēt ārvalstu valūtas pārvērtēšanu
Pirms neapmaksāto transakciju ārvalstu valūtas summu pārvērtēšanas var veikt tās pašas dienas un metodes ārvalstu valūtas pārvērtēšanas simulācijas pārskatu. Lai ģenerētu simulācijas pārskatu, lapā **Ārvalstu valūtas pārvērtēšana** noklikšķiniet uz pogas **Simulācija**. Atkarībā no definētajiem simulācijas parametriem pārskats nodrošina nerealizētās peļņas vai zuduma summas priekšskatu.

## <a name="process-a-foreign-currency-revaluation"></a>Ārvalstu valūtas pārvērtēšanas apstrāde
Izmantojiet lapu **Ārvalstu valūtas pārvērtēšana** sadaļā **Periodiskie uzdevumi**, lai pārvērtētu atvērtās transakcijas. Varat palaist procesu reāllaikā vai ieplānot tā palaišanu, izmantojot pakešuzdevumu. Norādot pārvērtēšanas procesa iestatījumus, noteikti norādiet, vai vēlaties drukāt rezultātu pārskatu. Pārvērtēšanas pārskatu nevar atkārtoti drukāt pēc procesa pabeigšanas. Ja tiek ģenerēts ārvalstu valūtas pārvērtēšanas pārskats, tajā ir redzami dažādi atlikumi debitora/kreditora un valūtas līmenī:

-   debitoru vai kreditoru, kam ir pārvērtētas transakcijas ārvalstu valūtā, atlikumi. Ir redzami tālāk norādītie atlikumi.
    -   Kopējais sākotnējais atlikums ārvalstu valūtā.
    -   Kopējā ārvalstu valūtas summa uzskaites valūtā pēc iepriekšējās pārvērtēšanas datiem.
    -   Kopējā ārvalstu valūtas summa uzskaites valūtā pēc pašreizējās pārvērtēšanas datiem.
    -   Iepriekšējās un pašreizējās pārvērtēšanas starpība. Šī starpība ir papildu nerealizētā peļņa vai zudums.
-   Kopējā nerealizētā peļņa vai zudums visās valūtās.

Par katru veikto ārvalstu valūtas pārvērtēšanu tiek veikta uzskate. Lapas **Ārvalstu valūtas pārvērtēšana** ierakstā atlasiet opciju **Transakcijas**, lai skatītu detalizētu to transakciju sarakstu, kas tika izveidotas pārvērtēšanas procesā. Katra dokumenta transakcija atbilst atvērtajai transakcijai, kas tika pārvērtēta. Ja kāda atvērtā transakcija tika pārvērtēta vairākas reizes, ir redzami divi ieraksti, kam ir izmantots viens un tas pats dokuments. Viens ieraksts atbilst iepriekšējās nerealizētās peļņas vai zaudējumu anulēšanai, bet otrs ieraksts atbilst jaunajai nerealizētajai peļņai vai zaudējumiem. Lai izpildītu pārvērtēšanas procesu, noklikšķiniet uz pogas **Ārvalstu valūtas pārvērtēšana**. Definējiet attiecīgos tālāk norādīto parametru iestatījumus.

-   **Metode** — atlasītajā ārvalstu valūtas pārvērtēšanas darbā izmantotā metode.
    -   **Standarts** — ārvalstu valūtas pārvērtēšanas darbi tiek grāmatoti neatkarīgi no tā, vai rezultāts ir peļņa vai zaudējums.
    -   **Minimums** — ārvalstu valūtas pārvērtēšanas darbi tiek grāmatoti tikai tad, ja rezultāts ir zaudējums.
    -   **Rēķina datums** — ārvalstu valūtas pārvērtēšanas darbos tiek izmantots to transakciju sākotnējais maiņas kurss, kuras tiek pārvērtētas to sākotnējā vērtībā uzskaites valūtā. Visa iepriekšējās ārvalstu valūtas pārvērtēšanas ietekme tiek atcelta.
-   **Attiecīgais datums** — datums, kurā atrod visas transakcijas ar nenomaksātām (nenosegtām) summām uz šo datumu. Ārvalstu valūtas summas, kas tiek pārvērtētas, izmantojot valūtas maiņas kursus, kas ir ievadīti lapā **Valūtas maiņas kursi** uz attiecīgo datumu. Ja ārvalstu valūtas summas tiek pārvērtētas attiecīgajā datumā, šis datums kļūst par koriģēto transakciju pēdējās ārvalstu valūtas pārvērtēšanas datumu. Ja ārvalstu valūtas pārvērtēšana attiecīgajā datumā, kas ir pirms pēdējā ārvalstu valūtas pārvērtēšanas datuma, tiek veikta jau koriģētām transakcijām, periodiskā darba izpildes gaitā netiek koriģētas transakcijas, kas nav bijušas apmaksātas uz iepriekšējo attiecīgo datumu, bet uz kurām attiecas jaunāks ārvalstu valūtas pārvērtēšanas datums.
-   **Valūtas kursa datums** — datums, kas nosaka ārvalstu valūtas pārvērtēšanas procesā izmantoto valūtas kursu.
-   **Izmantot grāmatošanas metodi no** — grāmatošanas metode, ko izmanto, lai atvērtu kreditora vai debitora noklusējuma galveno kontu ārvalstu valūtas pārvērtēšanas transakciju uzskaites ierakstiem.
    -   **Grāmatošana** — izmantotā debitora transakciju grāmatošanas metode.
    -   **Atlasīt** — grāmatošanas metodes ievadīšana laukā **Grāmatošanas profils**.
-   **Grāmatošanas metode** — ja laukā **Izmantot grāmatošanas metodi no** ir atlasīta opcija **Atlasīt**, tad šajā laukā ievadītā grāmatošanas metode nosaka ārvalstu valūtas pārvērtēšanas transakciju grāmatošanas metodi.
-   **Finanšu dimensijas** — finanšu dimensijas, kas tiek iegrāmatotas ārvalstu valūtas pārvērtēšanas transakciju uzskaites ierakstos.
    -   **Nav** — netiek iegrāmatota neviena finanšu dimensija. Ja konta struktūrā ir noteikta obligāta finanšu dimensija, pārvērtēšanas process tiek veikts, bet tiek izveidoti uzskaites ieraksti bez finanšu dimensijām. Vispirms tiek parādīts brīdinājuma ziņojums, kas ļauj pārvērtēšanu atcelt.
    -   **Tabula** — ārvalstu valūtas pārvērtēšanas transakcijās tiek iegrāmatotas debitora un kreditora konta finanšu dimensijas.
    -   **Grāmatošana** — ārvalstu valūtas pārvērtēšanas transakcijās tiek iegrāmatotas pārvērtētās transakcijas finanšu dimensijas. Pēc noklusējuma pārvērtēšanas transakcijas AR/AP galvenajam kontam tiek izmantotas sākotnējās transakcijas AR/AP virsgrāmatas konta finanšu dimensijas, bet pārvērtēšanas transakcijas nerealizētās peļņas/zuduma galvenajam kontam tiek izmantotas sākotnējās transakcijas izdevumu/līdzekļu/ieņēmumu virsgrāmatas konta finanšu dimensijas.




