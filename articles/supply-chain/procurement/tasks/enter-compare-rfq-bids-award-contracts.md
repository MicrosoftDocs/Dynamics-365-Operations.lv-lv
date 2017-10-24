--- 
title: "PP piedāvājumu ievade un salīdzināšana un līgumu piešķiršana"
description: "Šajā procedūrā ir parādīts, kā ievadīt atbildes uz PP, noteikt punktu skaitu un salīdzināt piedāvājumus, un kā pēc tam piešķirt piedāvājumu vienam no kreditoriem."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5dea9d7bfb1bf7b11f6c49cccaab1b73d4e58d16
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>PP piedāvājumu ievade un salīdzināšana un līgumu piešķiršana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā ievadīt atbildes uz PP, noteikt punktu skaitu un salīdzināt piedāvājumus, un kā pēc tam piešķirt piedāvājumu vienam no kreditoriem. Šo procedūru varat lietot ar demonstrācijas datu uzņēmumu USMF. Pirms sākšanas jums ir nepieciešams PP ar divām rindām, kas ir nosūtīts vismaz diviem kreditoriem. Kā priekšnosacījumu tā izveidošanai varat palaist procedūru “Izveidot piedāvājuma pieprasījumu”. Lai varētu palaist šo procedūru, ir nepieciešams iestatīt punktu skaitīšanas kritērijus.


## <a name="enter-a-reply-from-a-vendor"></a>Ievadīt atbildi no kreditora
1. Dodieties uz Sagāde un avoti > Piedāvājumu pieprasījumi > Visi piedāvājumu pieprasījumi.
2. Atlasiet PP, kura statuss ir Nosūtīts, un noklikšķiniet uz numura Piedāvājuma pieprasījuma gadījums saites.
    * PP ir jāsūta vismaz 2 kreditoriem.  
3. Noklikšķiniet uz Virsraksts, lai dotos uz kreditoru sarakstu.
4. Atlasiet kreditoru, kuram vēlaties ievadīt PP atbildi.
5. Noklikšķiniet uz Ievadīt atbildi.
6. Darbību rūtī noklikšķiniet uz Atbilde.
7. Noklikšķiniet uz Kopēt datus uz atbildēm.
    * Ar šo darbību atlasītie dati, piemēram, daudzums, no PP gadījuma tiks kopēti uz PP atbildi. Alternatīvi šo darbību varat izlaist un visus atbildes laukus aizpildīt manuāli, kad rediģējat atbildi.  
8. Noklikšķiniet uz Rediģēt.
9. Laukā Vienības cena ievadiet kādu skaitli.
10. Izvēlēties otru piedāvājuma rindu.
11. Laukā Vienības cena ievadiet kādu skaitli.

## <a name="score-the-bid"></a>Skaitīt piedāvājuma punktus
1. Noklikšķiniet uz Virsraksts, lai dotos uz piedāvājuma punktu skaitīšanu.
2. Izvērsiet piedāvājuma punktu skaitīšanas sadaļu.
3. Laukā Punktu skaits ievadiet numuru vienam no punktu skaitīšanas kritērijiem.
    * Ja peles kursoru novietojat virs viena no punktu skaitīšanas kritērija, ar rīka padomu tiek parādīts nepieciešamo punktu diapazons. Šajā demonstrācijā jebkuram kritērijam varat pievienot skaitli no 1 līdz 5.  
4. Atlasiet citu punktu skaitīšanas kritēriju.
5. Laukā Punktu skaits ievadiet kādu numuru.
6. Izvērsiet sadaļu Anketas.
    * Ja PP gadījumam ir anketa, kas tika nosūtīta kreditoriem, tad anketas sadaļā varat ievadīt viņu atbildes.  
7. Aizvērt lapu.

## <a name="enter-a-reply-for-another-vendor"></a>Ievadīt atbildi citam kreditoram
1. Atlasiet nākamo kreditoru, noņemot atzīmi tā kreditora izvēles rūtiņai, kuram tikko ievadījāt atbildi, un pēc tam atzīmējot rindu nākamajam kreditoram.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Noklikšķiniet uz Ievadīt atbildi.
4. Noklikšķiniet uz Kopēt datus uz atbildēm.
5. Noklikšķiniet uz Rediģēt.
6. Laukā Vienības cena ievadiet kādu skaitli.
7. Izvēlēties otru piedāvājuma rindu.
8. Laukā Vienības cena ievadiet kādu skaitli.

## <a name="score-the-second-bid"></a>Skaitīt otra piedāvājuma punktus
1. Noklikšķiniet uz Virsraksts, lai dotos uz piedāvājuma punktu skaitīšanu.
2. Laukā Punktu skaits ievadiet kādu numuru.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Laukā Punktu skaits ievadiet kādu numuru.

## <a name="compare-the-replies"></a>Salīdzināt atbildes
1. Darbību rūtī noklikšķiniet uz Vispārīgi.
2. Noklikšķiniet uz Salīdzināt atbildes.
3. Laukā Rangs ievadiet kādu numuru.
    * Šajā lapā tiek rādīti piedāvājumi ar virsrakstu un rindām, kā arī kopējo punktu skaitu virsraksta līmenī. Rindas varat salīdzināt, kārtojot režģī, lai salīdzināmās rindas atrastos līdzās. Informācijā ir iekļautas arī tālāk uzskaitītās vērtības. Daudzums: kreditora piedāvātais daudzums. Šis daudzums var nebūt vienāds ar daudzumu, kas norādīts PP.   Neto summa: kreditora piedāvātā cena pēc visu atlaižu atņemšanas rindā norādītajiem krājumiem.   Novirze: dienu skaits, par kādu piedāvājuma virsrakstā vai rindā norādītais piegādes datums atšķiras no PP virsrakstā vai PP rindā pieprasītā piegādes datuma.   Katram piedāvājumam varat ievadīt rangu.  
4. Atlasiet virsraksta rindu otram piedāvājumam, kuram vēlaties noteikt rangu.
5. Laukā Rangs ievadiet kādu numuru.
6. Noklikšķiniet uz Saglabāt.

## <a name="reject-a-bid"></a>Noraidīt piedāvājumu
1. Atlasiet virsraksta rindu piedāvājumam, kuru vēlaties noraidīt.
    * Vienlaicīgi varat pieņemt, noraidīt vai atgriezt tikai vienu piedāvājumu vai viena piedāvājuma rindas.  
2. Atzīmējiet izvēles rūtiņu Atzīmēt.
    * Ja piedāvājuma virsrakstā atzīmējat izvēles rūtiņu Atzīmēt, tad tiek atzīmētas arī visas rindas. Piedāvājumā varat arī atzīmēt rindu apakškopu, lai tās noraidītu vai pieņemtu. Ir iespējams pieņemt viena kreditora piedāvājumu noteiktām PP rindām, un pēc tam pārējās PP rindas piešķirt citam kreditoram, taču tas ir jādara 2 darbībās un vienlaicīgi tikai vienā piedāvājumā. Ja pastāv citas rindas, varat pieņemt tikai sākotnējo piedāvājuma rindu vai tās alternatīvu, bet ne abas.  
3. Noklikšķiniet uz Noraidīt.
4. Noklikšķiniet uz Parametri, lai atvērtu nolaižamo dialogu.
5. Laukā Noraidīšanas pamatojums ievadiet vai atlasiet kādu vērtību.
    * Atteikuma pamatojums tiks saglabāts atbildē.  
6. Noklikšķiniet uz OK.
7. Noklikšķiniet uz OK.
8. Aizvērt lapu.
9. Aizvērt lapu.
10. Atsvaidziniet lapu.

## <a name="accept-a-bid"></a>Pieņemt piedāvājumu
1. Atlasiet piedāvājumu, kuru vēlaties pieņemt, un pēc tam noklikšķiniet uz saites laukā Piedāvājuma pieprasījums.
2. Darbību rūtī noklikšķiniet uz Atbilde.
3. Noklikšķiniet uz Akceptēt.
    * Ja esat atzīmējis vienas rindas, bet ne citas, tad pieņemšanas darbībā tiks iekļautas tikai atzīmētās rindas. Vai vēlaties pieņemt visas piedāvājuma rindas, tad rindas nav jāatzīmē.  
4. Noklikšķiniet uz Parametri, lai atvērtu nolaižamo dialogu.
    * Šādi jūs varat ierakstīt piedāvājuma pieņemšanas pamatojumu. Pamatojums tiks saglabāts piedāvājumā.  
5. Laukā Pieņemšanas pamatojums ievadiet vai atlasiet kādu vērtību.
6. Noklikšķiniet uz OK.
7. Noklikšķiniet uz OK.
    * Kad noklikšķināt uz Labi, ar šo tiek izveidots pirkšanas pasūtījums, pamatojoties uz PP pieņemšanā iekļautajām rindām. Ja pastāv citi piedāvājumi, kas nav apstrādāti (pieņemti, noraidīti vai atgriezti), tad sistēma jums piedāvā noraidīt atlikušos piedāvājumus.  

## <a name="view-the-purchase-order-thats-been-generated"></a>Skatīt ģenerēto pirkšanas pasūtījumu
1. Darbību rūtī noklikšķiniet uz Vispārīgi.
2. Noklikšķiniet uz Pirkšanas pasūtījums.
    * Šeit varat redzēt pirkšanas pasūtījumu, kas tika ģenerēts, kad pieņēmāt piedāvājumu.  
3. Aizvērt lapu.
4. Aizvērt lapu.
5. Aizvērt lapu.
6. Aizvērt lapu.


