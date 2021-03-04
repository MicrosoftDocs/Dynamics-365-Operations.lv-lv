---
title: Ieņēmumu atzīšanas komplekti
description: Šajā tēmā aprakstīta komplektu funkcionalitāte, kas iekļauta debitoru parādu ieņēmumu atzīšanas iespējā. Komplekts sastāv no pamatelementa un vairākiem komponentu krājumiem.
author: kweekley
manager: aolson
ms.date: 01/04/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: cf4d03c1a697259899c419ce084b35f4eddf13fe
ms.sourcegitcommit: bd53794cb94f8c1ce29a7d6102119a0975f155e3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/09/2021
ms.locfileid: "5142303"
---
# <a name="revenue-recognition-bundles"></a>Ieņēmumu atzīšanas komplekti

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīta komplektu funkcionalitāte, kas iekļauta debitoru parādu ieņēmumu atzīšanas iespējā. Komplekts sastāv no pamatelementa un vairākiem komponentu krājumiem. Pamatelements tiek ievadīts pārdošanas pasūtījumā, lai pasūtījuma ievade būtu efektīvāka. Tomēr tas pēc tam tiek izvērsts komponentu krājumos. Iekšējie dokumenti, piemēram, pavadzīme, uzskaita komponentu krājumus. Tomēr ārējos dokumentos tiek rādīts tikai pamatelements.

> [!NOTE]
> Microsoft Dynamics 365 Commerce kanāli, piemēram, tiešsaistes kanāli, pārdošanas punkti (POS) un zvanu centri, neatbalsta ieņēmumu atzīšanu (tostarp komplekta funkcionalitāti). Tas ietver arī risinājumu No potenciālā klienta līdz skaidrai naudai pakalpojumam Dynamics 365 Supply Chain Management un Dynamics 365 Sales. Krājumi, kas ir konfigurēti ieņēmumu atzīšanai, nav jāpievieno pasūtījumiem vai transakcijām, kas izveidotas Commerce kanālos vai risinājumā No potenciālā klienta līdz skaidrai naudai.

Lai iestatītu komplektus, jāievada konfigurācijas atslēgas ieņēmumu atzīšanai. Tomēr komplektus var izmantot arī tad, ja ieņēmumu atzīšana nav iestatīta. Tāpat komplektus var izmantot arī tad, ja nav iestatīti komplekti. Ja ir iestatīta ieņēmumu atzīšana, komponentu krājumi nosaka ieņēmumu cenu un ieņēmumu grafiku, kas tiek izmantots ieņēmumu atzīšanai vai atliktajiem maksājumiem, kad pārdošanas pasūtījums tiek iekļauts rēķinā.

Komplektu iestatījums izmanto materiālu komplekta (MK) funkcionalitāti. Informāciju par to, kā iestatīt komplekta krājumu, skatiet rakstā [Ieņēmumu atpazīšanas iestatīšana](revenue-recognition-setup.md). Ja pamatelements ir atzīmēts kā komplekts, tas tiek apstrādāts atšķirīgi no citiem MK krājumiem. Šeit ir saraksts ar atšķirībām:

- Komplekti ir jāizvērš, izmantojot pārdošanas pasūtījuma apstiprinājumu, pārdošanas pasūtījuma lapas darbību rūts cilnē **Pārdošana** atlasot **Apstiprināt pārdošanas pasūtījumu**. Komplekta krājumus nekad nedrīkst izvērst, kopsavilkuma cilnes **Pārdošanas pasūtījuma rindas** izvēlnē **Pārdošanas pasūtījuma rinda** atlasot sadaļas **Izvērst** vienumu **MK rinda**. Pretējā gadījumā krājums tiks apstrādāts kā MK, nevis komplekts.
- Pirms pavadzīmes vai rēķina izveidošanas jāapstiprina pārdošanas pasūtījums, kas ietver komplekta krājumu.
- Kad komplekts ir izvērsts, izmantojot pārdošanas pasūtījuma apstiprinājumu, pamatelements tiek atcelts, un tā vienības cena un atlaides tiek piešķirtas komplekta komponentu krājumiem.
- Komponentu krājumu summai vienmēr jābūt vienādai ar pamatelementa cenu. Tāpēc laukiem, kurus var atjaunināt vai mainīt komponentu krājumiem, pastāv ierobežojumi. Piemēram, vienības cenu nevar manuāli mainīt. To arī nevar netieši mainīt, ja stājas spēkā jauns cenu līgums. Lai novērstu jaunu cenu līgumu, komponentu krājumiem nevar mainīt krājumu dimensijas.
- Kad tiek drukāts ārējs dokuments, piemēram, pārdošanas pasūtījuma apstiprinājums vai rēķins, tiek drukāts pamatelements, nevis komponentu krājumi.

## <a name="bundles-on-sales-orders"></a>Komplekti pārdošanas pasūtījumos

USMF demonstrācijas uzņēmums ietver šādu komplektu iestatīšanu. Ņemiet vērā, ka visi ieņēmumu atzīšanas iestatījumi, piemēram, ieņēmumu grafiku iestatījumi, ir noņemti no krājumiem, kas tiek ietverti šajā scenārijā.

**Pamatelements:** klēpjdatora komplekts

- **Komponenta krājums:** 1 no krājuma 1000
- **Komponenta krājums:** 1 no krājuma S0021
- **Komponenta krājums:** 1 no krājuma Atbalsts

Komponentu krājumu *pārdošanas pamatcena* ir būtiska komponentu iestatīšanas daļa. Pārdošanas pamatcena ir definēta krājuma kopsavilkuma cilnē **Pārdošana**. To izmanto sadalījuma koeficienta aprēķināšanai, ja pamatelementa cena par vienību ir piešķirta komponentu krājumiem. Tirdzniecības līguma pārdošanas cenas nekad netiek izmantotas šim nolūkam.

Komponentu krājumiem ir definētas šādas pārdošanas pamatcenas:

- **1000:** 1900,00 $
- **S0021:** 150,00 $
- **Atbalsts:** 500,00 $

Pārdošanas pasūtījums tiek ievadīts debitoram US-004, Cave Wholesales. Vienīgā ievadītā rinda ir klēpjdatora komplekta krājumam. Pamatrindā noklusējuma cenu par vienību var paņemt no vairākām vietām, piemēram, tirdzniecības līguma vai pārdošanas pamatcenas. Šajā piemērā 2300 $ ir ievadīts manuāli kā vienības cena.

[![Klēpjdatora komplekta krājums pārdošanas pasūtījumā](./media/bundle-01.png)](./media/bundle-01.png)

Tā kā pārdošanas pasūtījums ietver komplektu, tas ir jāapstiprina. Apstiprinājuma dialoglodziņā parādīti komplekta komponenti.

[![Apstiprināt pārdošanas pasūtījuma dialoglodziņu, kurā ir parādīti komponentu krājumi](./media/bundle-02.png)](./media/bundle-02.png)

Tomēr izdrukātajā apstiprināšanas pārskatā parādīti tikai komplekta pamatelementi, jo šis pārskats ir debitora ārējās dokuments.

[![Apstiprinājuma pārskats, kurā ir parādīts tikai pamatelements](./media/bundle-03.png)](./media/bundle-03.png)

Kad pārdošanas pasūtījums ir apstiprināts, pamatelements joprojām tiek rādīts pārdošanas pasūtījumā, taču tā statuss ir mainīts uz **Atcelts**. Turklāt neto summa tiek izsekota laukā **Komplekta neto summa**. Šī summa ir nepieciešama rēķina drukāšanai, jo rēķins rāda pamatelementu, nevis komponenta krājumus.

Komponentu krājumu summai ir jābūt vienādai ar pamatelementa **komplekta neto summas** vērtību, jo šī vērtība ir summa, kas drukātajā rēķinā tiek uzrādīta debitoram. Lai nodrošinātu, ka rēķins atbilst summām, kas ir iegrāmatotas virsgrāmatā, komponentu krājumu rediģējumi ir ierobežoti. Piemēram, vietu un noliktavu nevar mainīt, jo šīs izmaiņas var izraisīt cenas maiņu, balstoties uz tirdzniecības līgumu.

Pamatelementa rindas vienības cena tiek piešķirta komponentiem šādi:

**Kopējās pārdošanas pamatcenas no komponentiem:** 1900 $ + 500 $ + 150 $ = 2550 $

- **1. komponents:** 2300 $ × (1900 ÷ 2550) = 1713,73 $
- **2. komponents:** 2300 $ × (500 ÷ 2550) = 450,98 $
- **3. komponents:** 2300 $ × (150 ÷ 2550) = 135,29 $

Komponentu summai jābūt vienādai ar 2300 $, un tā arī ir (1713,73 $ + 450,98 $ + 135,29 $ = 2300 $).

Ja izmaiņas ir nepieciešamas visiem komponenta krājumiem, pamatelementu var noņemt. Šajā gadījumā tiek noņemti arī komponenta krājumi. Pēc tam pamatelementu var pievienot vēlreiz un nepieciešamos rediģējumus var veikt pirms pārdošanas pasūtījuma apstiprināšanas.

[![Komplekta krājums, kas ietver komponentu krājumu izmaiņas](./media/bundle-04.png)](./media/bundle-04.png)

Kad pārdošanas pasūtījums ir izdots un iepakots, dokumentos tiks iekļauti tikai komplekta komponenti. Pavadzīmei un rēķinam ir jāietver pilns komplekts. Pretējā gadījumā tos nevar grāmatot. Piemēram, dialoglodziņā ir parādīti trīs komponentu krājumi. Mēģinot dzēst vienu no tiem, tiek parādīts kļūdas ziņojums, ka pirms rēķina izrakstīšanas jānosūta visas komplekta preces.

Komplektam jābūt nosūtītam un iekļautam rēķinā kā pilnīgam komplektam. Piemēram, ja krājuma 1000 daudzums tiek mainīts uz 4, bet citu komponentu krājumu daudzums tiek atstāts kā 5, pavadzīmi un rēķinu nevar iegrāmatot.

Daļēju summu var nosūtīt un iekļaut rēķinā tikai tad, ja daudzums tiek samazināts visiem komplekta komponentiem. Piemēram, pārdošanas pasūtījumā klēpjdatora komplekta krājuma daudzums tiek ievadīts kā 5. Kad pārdošanas pasūtījums ir apstiprināts, trīs komponentu krājumi tiek parādīti pārdošanas pasūtījumā, un katra krājuma daudzums ir 5. Pēc noklusējuma nosūtīšanas un rēķina izrakstīšanas laikā katram komponentam daudzums tiks iestatīts uz 5. Taču visiem trīs komponentu krājumiem daudzumu var pielāgot līdz 3. Šajā gadījumā tiks nosūtīti un izrakstīti rēķini trīs pilniem komplektiem. Atlikušos divus komplektu krājumus (katrā no trim komponentu krājumiem daudzums ir 2) var nosūtīt un iekļaut rēķinā vēlāk.

Pēdējā darbība ir pārdošanas pasūtījuma iekļaušana rēķinā. Rēķina izrakstīšanas laikā rēķina dialoglodziņā tiks rādīti komponentu krājumi.

[![Rēķina izrakstīšanas dialoglodziņš, kurā ir parādīti komponentu krājumi](./media/bundle-06.png)](./media/bundle-06.png)

Tomēr drukātajā rēķinā tiek rādīts tikai pamatelements.
 
[![Drukāts rēķins, kurā ir parādīts tikai pamatelements](./media/bundle-07.png)](./media/bundle-07.png)

Rēķinu žurnāls, kas tiek izveidots pēc grāmatošanas, neietver pamatelementu no komplekta, jo šī krājuma statuss ir **Atcelts**.

[![Rēķinu žurnāls, kurā nav iekļauts pamatelements](./media/bundle-08.png)](./media/bundle-08.png)

Svarīgi, lai rēķinu žurnālā nebūtu iekļauts komplekta pamatelements, jo visi procesi, kas tiek veikti pēc rēķina grāmatošanas, ir balstīti uz šo rēķinu žurnālu. Piemēram, ja izveidojat kredīta notu no darbības rūts cilnes **Pārdošana**, izveidotā kredīta nota ietvers komponenta krājumus, bet ne pamatelementu.

[![Kredītnota, kas parāda komponentu krājumus, bet ne pamatelementu](./media/bundle-09.png)](./media/bundle-09.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]