---
title: Kreditoru maksājumu atcelšana
description: Šajā rakstā aprakstītas maksājuma atcelšanas, dzēšanas, anulēšanas un noraidīšanas atšķirības. Papildus šeit ir aprakstītas divas kreditora čeka atcelšanas metodes.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankChequeTable, LedgerJournalTransBankChequeReversal, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14361
ms.assetid: 9f0a1883-cbe0-4cc7-b9f3-dd12fb85ebe8
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2303bf5908137a72b53c7d1aab6343e98a4dad0bb7d315c52611f1356e46c5df
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762191"
---
# <a name="reverse-a-vendor-payment"></a>Kreditoru maksājumu atcelšana

[!include [banner](../includes/banner.md)]

Šajā rakstā aprakstītas maksājuma atcelšanas, dzēšanas, anulēšanas un noraidīšanas atšķirības. Papildus šeit ir aprakstītas divas kreditora čeka atcelšanas metodes. 

Dažkārt pēc maksājuma piegādātājam iegrāmatošanas maksājums ir jāatsauc. Atcelšana atšķiras no maksājuma dzēšanas, anulēšanas vai noraidīšanas. Maksājumu var dzēst tikai tad, ja tā statuss ir **Izveidots**. Šis statuss norāda, ka maksājums ir izveidots, taču vēl nav ģenerēts. Šis ierobežojums ir spēkā vienmēr neatkarīgi no maksāšanas metodes. Varat anulēt negrāmatotus čekus pēc tam, kad ies ir ģenerēti, taču pirms tie ir grāmatoti. Ja ģenerēts maksājums tiek veikts, izmantojot elektronisko līdzekļu pārskaitījumu (EFT), varat noraidīt maksājumu pirms tā grāmatošanas. Lai noraidītu maksājumu, mainiet lauka **Maksājuma statuss** vērtību. Anulētu vai noraidītu maksājumu var atkārtoti ģenerēt pēc tam, kad lauka **Maksājuma statuss** vērtība ir nomainīta atpakaļ uz **Nav**. 

Pēc maksājuma grāmatošanas tiek izmantota atcelšana. Elektroniski veiktos maksājumus nevar atcelt pēc to grāmatošanas. Tā vietā ir jāizveido jauna transakcija par maksājuma summu, lai pasīvu atgrieztu piegādātāja kontā. Ir pieejamas divas iegrāmatoto čeku atcelšanas metodes. Izmantojot vienu no metodēm, atgriešana tiek nekavējoties grāmatota, nospiežot **Maksājuma atcelšana** lapā **Pārbaudīt**. Otrajā metodē, noklikšķinot uz pogas **Maksājuma atcelšana** lapā **Pārbaudīt**, atcelšana vispirms tiek nosūtīta uz čeku anulēšanas žurnālu skaidrā naudā un bankas vadībai, kur pārskatītājs var grāmatot vai noraidīt atcelšanu. 

Lai uzzinātu, kādu metodi izmanto jūsu uzņēmums, skatiet lapu **Skaidras naudas un bankas pārvaldības parametri**. Ja opcija **Maksājumu atgriešanai izmantot pārskatīšanas procesu** ir iestatīta uz **Jā**, atcelšanas tiek sūtītas uz čeku anulēšanas žurnālu pārskatīšanai. Tālāk esošajā tabulā ir aprakstīts, kā čeka atgriešanas metodes atšķiras.

| Ja jūsu organizācija nepārskata čeku atgriešanas gadījumus pirms grāmatošanas                                                                                                                                  | Ja jūsu organizācija pārskata čeku atgriešanas gadījumus pirms grāmatošanas                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Čeks tiek nekavējoties anulēti, noklikšķinot uz **Labi** lapā **Pārbaudīt**.                                                                                                                      | Čeks netiek nekavējoties atgriezts. Tiek izveidots čeku atgriešanas žurnāls pārskatīšanai. Ja čeku atgriešanas žurnāls tiek dzēsts, čeku var vēlreiz atgriezt.                                                                                                                                                                                                                                                                |
| Tiek atgriezti sākotnējā čeka uzskaites ieraksti.                                                                                                                                         | Virsgrāmatas konts no sākotnējā čeku uzskaites ieraksta var netikt iegrāmatots. Finanšu dimensijas no sākotnējā čeka žurnāla tiek lietotas kā noklusējuma finanšu dimensijas čeku atgriešanas žurnālā. Šīs noklusējuma vērtības varat mainīt. Iegrāmatojot čeku atgriešanas žurnālu, galvenie kreditoru konti tiek ievadīti automātiski no iegrāmatošanas profiliem, kas var būt mainīti. |
| Uzskaites struktūras, kas tika izmantotas, kad tika grāmatots sākotnējais čeks, tiek lietotas čeka atgriešanai, pat ja konta struktūra ir mainīta. Kontu kombinācija nav validēta. | Ja konta struktūra tika mainīta pēc tam, kad tika iegrāmatots sākotnējais čeks, jauna finanšu dimensija var būt nepieciešama čeka atgriešanai. Šī finanšu dimensija var netikt ievadīta automātiski no sākotnējā maksājumu žurnāla. Kontu kombinācija tiek validēta, kad ir iegrāmatota čeka atgriešana.                                                                                                        |
| Fiksētas dimensijas nelieto atsaukšanai, palīdzot nodrošināt, ka tiek atsaukti tie paši virsgrāmatas konti.                                                                                      | Fiksētas dimensijas tiek lietotas čeku atgriešanas žurnālam grāmatošanas laikā. Finanšu dimensijas vērtība var nepastāvēt sākotnējā čeka uzskaites ierakstā atkarībā no tā, kad tika definēta fiksētā dimensija.                                                                                                                                                                                                     |

## <a name="reverse-posted-checks-without-reviewing-them"></a>Grāmatoto čeku atgriešana, tos nepārskatot
Ja jūsu organizācija vēlas grāmatot čeku atgriešanas gadījumus uzreiz pēc noklikšķināšanas uz **Maksājuma atcelšana** lapā **Pārbaudīt**. Lapā **Skaidras naudas un bankas pārvaldības parametri** iestatiet opciju **Maksājumu atgriešanai izmantot pārskatīšanas procesu** uz **Nē**. Lapā **Pārbaudīt** varat atzīmēt šo izvēles rūtiņu, lai atceltu, un atlasiet **Maksājuma atcelšana**. Varat tad ievadīt atcelšanas datumu un atlasīt atcelšanas iemeslu.

## <a name="reverse-posted-checks-after-they-are-reviewed-in-the-check-reversal-journal"></a>Grāmatoto čeku atgriešana pēc to pārskatīšanas čeku atgriešanas žurnālā
Ja jūsu organizācija vēlas pārbaudīt čeku atcelšanas pirms to iegrāmatošanas, izveidojiet čeku atcelšanas žurnālu un lapā **Skaidras naudas un bankas pārvaldības parametri** iestatiet opciju **Maksājumu atgriešanai izmantot pārskatīšanas procesu** uz **Jā**. Lapā **Pārbaudīt** varat atzīmēt šo izvēles rūtiņu, lai atceltu; atlasiet **Maksājuma atcelšana**. Varat tad ievadīt atcelšanas datumu un atlasīt atcelšanas iemeslu. Finanšu pamatojums ir jāiestata gan bankas, gan kreditoru tipiem. Lai čeku anulēšanas žurnālā izveidotu žurnālu, ir jāatlasa žurnāla nosaukums.

### <a name="review-a-reversal"></a>Pārlūkot atcelšanu

Ja esat lietotājs, kuram jāpārskata atcelšanas, varat apstiprināt un grāmatot žurnālu vai noraidīt atcelšanu, dzēšot žurnālu. Lapā **Čeku atcelšanas žurnāls** varat izvēlēties atcelšanas žurnālu pārlūkošanai un pēc tam noklikšķināt uz **Rindas**. Varat pārlūkot atcelto čeku un tad atlasīt kādu no šādām apstiprināšanas opcijām:

-   Lai apstiprinātu un grāmatotu atcelšanas žurnālu, noklikšķiniet uz **Grāmatot** vai **Grāmatot un pārsūtīt**.
-   Lai noraidītu atcelšanu, izdzēsiet čeku anulēšanas žurnālu.

> [!NOTE]
> Ja dzēšat žurnālu, atcelšana tiek noņemta no sistēmas, taču sākotnējais čeks joprojām ir norādīts lapā **Čeks**. Čeka statuss vairs nav **Gaidoša atcelšana**.

## <a name="results-of-posting-a-reversal"></a>Atcelšanas grāmatošanas rezultāti
Grāmatojot čeka atcelšanu, notiek šādi notikumi:

-   Čeka status tiek atjaunināts uz **Atcelšana**.
-   Ja atcelšanas laikā anulēšanas lapā tika atlasīta opcija **Saskaņot**, čeks tiek saskaņots (ir atlasīta opcija **Saskaņots** ) un nav redzams lapā **Kontu saskaņošana**.
-   Lai palielinātu bankas konta bilanci, atcelšanas dokuments ir iegrāmatots attiecībā pret bankas kontu, no kura tika izsniegts čeks.
-   Dokuments tiek iegrāmatots virsgrāmatā.
-   Modifikāciju informācija tiek atjaunināta lauka grupā **Vēsture** lapā **Pārbaudīt**.

> [!NOTE] 
> Kad atgriežat čeku, kas tika izsniegts starpuzņēmumu tirdzniecības transakcijai, korespondējošie ieraksti tiek ņemti no starpuzņēmumu tirdzniecības uzskaites iestatījumiem, nevis no sākotnējās transakcijas. Ja atceltais čeks tika izsniegts par kreditora maksājumu, notiek šāds notikums:

-   Oriģinālais maksājums par rēķinu, attiecībā pret kuru maksājums nokārtots, nav piemērots (nokārtošana ir atcelta).
-   Transakcija tiek grāmatota attiecībā pret maksājuma atgriešanas kreditora kontu, un atgrieztais maksājums tiek nosegts attiecībā pret sākotnējo maksājumu. Lauks **Pēdējais nosegšanas dokuments** lapā **Kreditora darbības** sākotnējai kreditoru rēķinu apmaksai tiek atjaunināts, lai parādītu atceltās darbības dokumenta numuru.

Ja atceltais čeks tika izsniegts debitora kompensācijas izmaksai, notiek šādi notikumi:

-   Transakcija tiek grāmatota attiecībā pret maksājuma atgriešanas debitora kontu, un norēķināšanās starp sākotnējo maksājumu un dokumentu, par kuru sākotnēji tika veikts norēķins, ir atgriezta (tiek izveidots negatīvs maksājums).
-   Maksājuma atcelšana tiek piemērota oriģinālajam maksājumam. Lauks **Pēdējais nosegšanas dokuments** lapā **Debitora darbības** sākotnējam debitora maksājumam tiek atjaunināts, lai parādītu atceltās darbības dokumenta numuru.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]