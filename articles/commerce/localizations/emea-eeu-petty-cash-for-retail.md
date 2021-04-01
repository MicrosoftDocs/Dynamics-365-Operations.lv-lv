---
title: Mazo kases posteņu pārvaldība programmai Commerce Austrumeiropā
description: Šajā tēmā ir aprakstīts, kā iestatīt un izmantot kases pārvaldības līdzekļus programmā Commerce Austrumeiropā.
author: epopov
manager: annbe
ms.date: 10/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 8807fbf3be7d5a69fb66efed0635c8813674da51
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225714"
---
# <a name="petty-cash-management-for-commerce-for-eastern-europe"></a>Mazo kases posteņu pārvaldība programmai Commerce Austrumeiropā

[!include [banner](../includes/banner.md)]

Šajā rakstā ir informācija par komercnozarei raksturīgo Austrumeiropas lokalizāciju.

Atbilstoši Austrumeiropas valstu grāmatvedības prasībām ir iespējams iestatīt operācijas skaidras naudas kontiem, lai automatizētu procesus ieņēmumiem, skaidras naudas dokumentiem un skaidras naudas pārskatiem. Plašāku informāciju skatiet šeit: [(EEUR) Parametru iestatīšana kases pārvaldībai](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management).

Mazumtirgotāji var pieņemt dažāda veida maksājumus apmaiņā pret pārdotajām precēm un pakalpojumiem. Kaut gan skaidra nauda ir visizplatītākais maksājumu veids, mazumtirgotāji var arī saņemt maksājumus čeku, karšu vai dokumentu formā. Mazumtirdzniecības punktā (POS), skaidra nauda, kredītkaršu kvītis un citi maksājumi tiek apstrādāti, izmantojot kasi.

To var izdarīt, programmā Commerce izmantojot līdzekli Kases pārvaldība.

- Izveidojiet kases kontu katra veikala atlasītajai maksāšanas metodei.
- Lai grāmatotu skaidras naudas transakcijas un debitoru maksājumus, kas tiek saņemti mazumtirdzniecības POS, izmantojiet kases žurnālus.
- Kad grāmatojat pārskatu, apkopojiet transakcijas pārskata rindā. Varat apkopot noguldījumus seifā, noguldījumus bankā, dokumentu transakcijas, noņemt norēķinu darījumus, mainīgo ierakstu transakcijas, ienākumu transakcijas, izdevumu transakcijas, debitoru maksājumus, pārdošanas transakcijas un atgriešanas transakcijas.

Visas transakcijas, kas notiek POS tiek grāmatotas, izmantojot Virsgrāmatas žurnālu. Pārskatu izveidei un grāmatošanai var izmantot skaidras naudas maksājumu žurnālus, debitoru maksājumu žurnālus un Virsgrāmatas žurnālus. Plašāku informāciju skatiet šeit: [Mazumtirdzniecības veikala izrakstu izveidošana, aprēķināšana un grāmatošana](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).

Lapā **Grāmatotie izraksti**, darbību rūtī varat izpildīt tālāk aprakstītās darbības.

- Dodieties uz **Uzziņas \> Žurnāls maksājumiem skaidrā naudā**, lai piekļūtu ar šo izrakstu saistītajiem skaidras naudas maksājumu žurnāliem.
- Dodieties uz **Uzziņas \> Virsgrāmatas žurnāls**, lai piekļūtu ar šo izrakstu saistītajiem virsgrāmatas žurnāliem, kas nav debitoru maksājumu un skaidras naudas maksājumu žurnāli.

## <a name="set-up-for-cash-management-for-pos"></a>POS kases pārvaldības iestatīšana

Pirms kases pārvaldības izmantošanas ir jāveic tālāk aprakstītā iestatīšanas procedūra.

- Lapā **Maksāšanas metodes** iestatiet maksāšanas metodi katram mazumtirgotāja akceptētajam maksājuma tipam. Transakciju grāmatošanai programmā POS varat izmantot dažādas maksāšanas metodes. Plašāku informāciju par maksāšanas metodēm skatiet [Maksāšanas metodes](https://docs.microsoft.com/dynamics365/unified-operations/retail/payment-methods).
- Iestatiet parametrus skaidras naudas operācijām.
- Iestatiet maksāšanas metodi maksājumiem veikalā skaidrā naudā.

### <a name="set-up-parameters-for-cash-operations"></a>Iestatiet parametrus skaidras naudas operācijām

Varat iestatīt parametrus, lai programmā Commerce izveidotu un grāmatotu skaidras naudas darījumus. Varat izmantot skaidras naudas maksājumu žurnālus, debitoru maksājumu žurnālus vai vispārīgus žurnālus, lai programmā POS grāmatotu pārdošanas darījumus un maksājumu darījumus. Kad grāmatojat pārskatu, varat apkopot darījumus, kuriem ir vienādi rekvizīti.

1. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri \> Komercijas parametri**. Kreisajā rūtī noklikšķiniet uz **Grāmatošana**.
2. Apgabalā **Grāmatošana**, kopsavilkuma cilnē **Apkopojums** vienumu **Norēķinu noņemšana/mainīšana** iestatiet uz **Jā**, lai apkopotu norēķinu noņemšanas vai maiņas transakcijas, kuras izraksta grāmatošanas laikā ir saistītas ar izraksta rindu. Norēķinu darījuma noņemšana tiek izveidota, kad no POS naudas kastes izņemat skaidru naudu. Mainīgo ierakstu darījums tiek izveidots, kad POS naudas kastē ieliekat skaidru naudu.
3. Aktivizējiet tālāk uzskaitītos atsevišķos parametrus, lai apkopotu transakcijas, kuras izraksta grāmatošanas laikā ir saistītas ar izraksta rindu.

    - **Noguldījums bankā** — apkopot bankas transakcijas.
    - **Noguldījums seifā** — apkopot seifa transakcijas.
    - **Ieņēmumu/izdevumu transakcijas** — apkopot ienākumu transakcijas vai izdevumu transakcijas.
    - **Dokumentu transakcijas** — apkopot dokumentu transakcijas.
    - **Debitoru maksājumi** — apkopot debitoru maksājumus.
    - **Pārdošana un ieņēmumi** — apkopot pārdošanas un ieņēmumu transakcijas.

4. Kopsavilkuma cilnē **Maksājumi** atlasiet noklusējuma žurnāla nosaukumu tālāk norādītajām opcijām.

    - **Debitoru maksājumu žurnāls** — šis žurnāls tiek izmantots debitoru maksājumu grāmatošanai.
    - **Žurnāls maksājumiem skaidrā naudā** — šis žurnāls tiek izmantots skaidras naudas maksājumu grāmatošanai.
    - **Vispārējs žurnāls** — šis žurnāls tiek izmantots, lai grāmatotu transakcijas, kas nav maksājumi skaidrā naudā un nav debitoru maksājumi.

### <a name="set-up-a-payment-method-for-cash-payments-in-a-store"></a>Maksāšanas metodes iestatīšana maksājumiem veikalā skaidrā naudā

Izmantojiet šādu procedūru, lai iestatītu maksājuma metodi maksājumiem veikalā skaidrā naudā.

1. Parejiet uz **Mazumtirdzniecība un komercija \> Kanāli \> Veikali \> Visi veikali**.
2. Sarakstu lapā **Visi veikali** atlasiet veikalu, kam iestatīt maksāšanas metodi.
3. Darbību rūts cilnes **Iestatīt** grupā **Iestatīt** noklikšķiniet uz **Maksāšanas metodes**.
4. Lapā **Maksāšanas metode** izveidojiet vai atlasiet kādu maksāšanas metodi.
5. Kopsavilkuma cilnes **Grāmatošana** lauku grupā **Konts**, laukā **Konta tips** atlasiet **Kases konts**.

    > [!NOTE]
    > Vienumu **Kases konts** laukā **Konta tips** varat atlasīt tikai tad, ja laukā **Funkcija** ir atlasīta vērtība **Parasts** vai **Norēķinu noņemšana/mainīšana**.

6. Laukā **Konta numurs** atlasiet kādu kases konta numuru šai maksāšanas metodei.
7. Lauku grupas **Norēķinu noņemšana/mainīšana** laukā **Korespondējošais konts** atlasiet korespondējošo kontu, kur grāmatot norēķinu noņemšanas vai mainīšanas transakcijas šai maksāšanas metodei.

> [!NOTE]
> Korespondējošie konti veikalam ir jāiestata gan kases norēķinu maksāšanas metodei, gan norēķinu noņemšanas vai mainīšanas ierakstu maksāšanas metodei. Šādi norēķinu noņemšanas vai mainīšanas ierakstu transakcijām tiek izveidoti līdzsvaroti virsgrāmatas ieraksti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]