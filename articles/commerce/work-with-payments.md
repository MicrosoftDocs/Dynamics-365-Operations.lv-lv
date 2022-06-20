---
title: Maksāšanas metodes zvanu centros
description: Šajā rakstā ir aprakstītas dažādas maksājumu metodes, kuras var lietot zvanu centrā Dynamics 365 Commerce.
author: josaw1
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRSalesTableOrderHistory, MCRCCAuthManagement
audience: Application User
ms.reviewer: josaw
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7f47b6865f408a1dc833dcf15fc254ef8b802bcc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902715"
---
# <a name="payment-methods-in-call-centers"></a>Maksāšanas metodes zvanu centros

[!include [banner](includes/banner.md)]

Programmatūrā Dynamics 365 Commerce zvanu centra kanāla konfigurācijā ietilpst iestatījums ar nosaukumu **Iespējot pasūtījuma pabeigšanu**. Šis iestatījums palīdz garantēt, ka visi pasūtījumi, ko kanāla lietotāji izveido, tiek izlaisti uz pasūtījuma apstrādi tikai tad, ja tiem ir priekšapmaksa vai iepriekš apstiprināts maksājums, kas ietilpst apstiprināto pielaižu robežās. Ja iestatījums **Iespējot pasūtījuma pabeigšanu** ir ieslēgts, zvanu centra lietotāji var ievadīt maksājumus attiecībā uz debitoru pārdošanas pasūtījumiem, izmantojot zvanu centra maksājumu apstrādes līdzekļus. Ja šis iestatījums ir izslēgts, zvanu centra lietotāji nevar izmantot zvanu centra maksājumu apstrādes līdzekļus, bet viņi joprojām var lietot priekšapmaksas attiecībā uz pārdošanas pasūtījumiem, izmantojot standarta funkcionalitāti Debitoru parādi.

Kā daļa no kanāla konfigurēšanas uzņēmumiem ir iespēja definēt maksājuma metodes, kas ir atļautas zvanu centra kanālam. Zvanu centra kanāls izmanto tādas pašas maksāšanas metodes, kādas ir definētas veikalu kanāliem.

Lai konfigurētu maksāšanas metodes zvanu centra kanālam, dodieties uz **Mazumtirdzniecība un komercija** \> **Kanāli** \> **Zvanu centri** \> **Visi zvanu centri** un pēc tam izvēlnē **Iestatīt** atlasiet opciju **Maksāšanas metodes**.

Kad veidojat maksāšanas metodi, piešķiršanai ir pieejamas piecas maksāšanas metodes funkcijas.

| Funkcija            | Apraksts |
|---------------------|-------------|
| Parasts              | Savai maksāšanas metodei izmantojiet funkciju **Parasts**, kad definējat tādas maksāšanas metodes kā skaidra nauda vai dokumenti. Kad šāda veida maksājumi tiek lietoti pārdošanas pasūtījumam zvanu centrā, karodziņam **Priekšapmaksa** tiks atlasīts noklusējuma iestatījums **Jā**. Tādējādi, iesniedzot šo pasūtījumu, šis priekšapmaksas dokuments tiks nekavējoties grāmatots debitora kontā. Ja nepieciešams, lietotāji var mainīt karodziņa **Priekšapmaksa** iestatījumu uz **Nē**, lai maksājuma dokuments netiktu izveidots līdz rēķina grāmatošanai. Priekšapmaksas dokuments tiek iegrāmatots debitora transakciju vēsturē, kur tas tiks sistemātiski segts attiecībā pret rēķinu par pārdošanas pasūtījumu. |
| Atzīmēt               | Izmantojiet funkciju **Čeks**, kad kā maksājuma veidu definējat bankas čeka instrumentu. Kad šis maksājuma tips tiek lietots pārdošanas pasūtījumam, kā daļa no maksājumu pieteikumu apstrādes lietotājam ir jāievada debitora čeka numurs. Ja tiek lietoti čeka maksājumi, tie vienmēr tiek uzskatīti par priekšapmaksu, un maksājuma dokumenti tiek izveidoti uzreiz pēc pasūtījuma iesniegšanas. Šie priekšapmaksas dokumenti tiek sistemātiski segti attiecībā pret rēķiniem, kas tiek veidoti šim pasūtījumam. |
| Kartes               | Karšu maksājumu tipi pārstāv jebkura tipa maksājumu, kam ir nepieciešams ievadīt kartes numuru, kurš ir norādīts uz debitora maksājuma kartes. Piemēri tostarp ir kredītkartes un dāvanu kartes. Kad konfigurējat šāda tipa maksājumus, jums ir jāizmanto izvēlne **Kartes iestatīšana**, lai definētu kartes ID, kurš ir saistīts ar šo maksāšanas metodi. Pasūtījuma ievadīšanas laikā lietotāji var norādīt, vai kartes maksājums būs priekšapmaksa, maksājuma ieraksta lapā izmantojot opciju **Priekšapmaksa**. Ja vien biznesam nav nepieciešamas priekšapmaksas, tipiskā patiesas kredītkartes maksājumu darbplūsma sastāv no diviem posmiem, kur autorizācija tiek iegūta pasūtījuma izveides laikā, un pēc tam maksājums tiek segts un iekasēts no debitora kartes rēķina izrakstīšanas laikā. Dāvanu karšu maksājumiem ir ieteicams izmantot priekšapmaksu, jo dāvanu kartes bilance ir jāsamazina nekavējoties, lai debitors to pašu vērtību nevarētu lietot kaut kur citur. |
| Debitors            | Funkcija **Debitors** maksāšanas metodē nozīmē, ka maksājums tiks lietots debitora kredīta limitam vai tiks novietots “starpkontā”. Programmatūrā Commerce debitoram var piešķirt kredīta limitu, kuru var validēt pasūtījuma izveides laikā. Maksājumi, kas tiek veikti, izmantojot maksāšanas metodi, kas ir saistīta ar funkciju **Debitors**, izveido saistības attiecībā pret debitora kontu. Pēc tam, kad tiek izrakstīts rēķins par pārdošanas pasūtījumu, tiek rādīta maksājamā bilance. Šajās situācijās debitori parasti sūta maksājumu saskaņā ar sniegtajiem nosacījumiem. Maksājamās bilances segšanai var izmantot arī iepriekšēju atvērtu kredīta dokumentu debitora kontā. Ņemiet vērā, ka pat tad, ja definējat šo maksāšanas metodi, zvanu centra pasūtījuma izveidē tā netiek rādīta maksājuma atlases opciju sarakstā, ja vien debitoram, ar kuru strādājat, debitora ierakstam nav iestatīts karodziņš **Ļaut starpkontu**. Šis karodziņš atrodas debitora ieraksta cilnē **Maksājuma noklusējuma informācija**. |
| Norēķina noņemšana/mainīšana | Funkcija **Norēķina noņemšana/mainīšana** netiek izmantota zvanu centrā. To var lietot tikai tad, ja definējot maksājuma metodes, kuras pārdošanas punkta (POS) programma izmanto veikala kanālā. |

Definējot maksājuma metodes, tām ir jābūt saistītam ar virsgrāmatu vai bankas kontu. Ja izlaižat šo posmu, lietotāji saņem kļūdas, kad viņi mēģina saglabāt maksājuma tipu.

## <a name="refund-payment-methods"></a>Atmaksas maksāšanas metodes

Atmaksas apstrādāšanas scenārijos zvanu centrs izmanto arī dažas maksāšanas metodes, kas ir definētas modulī Debitoru parādi. Lai konfigurētu šīs maksāšanas metodes, dodieties uz **Retail un Commerce** \> **Kanāla iestatīšana** \> **Zvanu centra iestatīšana** \> **Zvanu centra atmaksas metodes**. Jums ir jāizpilda šī konfigurācija, lai apstrādātu debitoriem paredzētus atmaksas čekus. Piemēram, ja debitors sākotnēji maksāja par pasūtījumu, izmantojot skaidru naudu vai čeku, lietotājs varētu vēlēties nosūtīt debitoram atmaksas čeku, izmantojot moduli Debitoru parādi. Šajā gadījumā zvanu centra skaidras naudas un čeka maksājuma tipiem ir jābūt kartētiem uz pareizo maksāšanas metodi modulī Debitoru parādi, lai palīdzētu nodrošināt pareizu atmaksas apstrādāšanu.

Turklāt, ja lietotājs apstrādā atgriešanas pasūtījumu kā zvanu centra lietotājs programmatūrā Commerce, bet lietotājs nevar šo atgriešanu saistīt ar sākotnējo pārdošanu, tad **Atgriešanas** maksāšanas metode ir jādefinē zvanu centra parametros. Dodieties uz **Retail un Commerce** \> **Kanāla iestatīšana** \> **Zvanu centra iestatīšana** \> **Zvanu centra parametri** un pēc tam cilnē **RMA/Atgriešana**, laukā **Maksāšanas metode** pārliecinieties, ka ir definēta kāda maksāšanas metode. Maksāšanas metode būs tā maksāšanas metode, kas tiek izmantota atmaksām. Parasti tā tiek definēta kā čeka metode vai debitora konta metode.


[!INCLUDE[footer-include](../includes/footer-banner.md)]