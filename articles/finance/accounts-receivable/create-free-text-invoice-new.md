---
title: Izveidot brīva teksta rēķinu
description: Šajā rakstā skaidrots, kā izveidot brīva teksta rēķinus.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: e8f80aa4cc0a7248506e0725881b8f575a0c7ff4
ms.sourcegitcommit: 29d9a7573bdac004726da88a9d7b2cc9c383e9ca
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788545"
---
# <a name="create-a-free-text-invoice"></a>Izveidot brīva teksta rēķinu

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā izveidot brīva teksta rēķinus. Šai procedūrai izmantojiet demonstrācijas uzņēmuma **USMF** datus.

## <a name="create-a-free-text-invoice"></a>Brīva teksta rēķina izveidošana

1. Dodieties uz **Debitoru parādi \> Rēķini \> Visi brīva teksta rēķini**.
2. Atlasiet **Jauns**.
3. Laukā **Debitora konts** atlasiet kādu vērtību.

    * Pēc noklusējuma konts, kas ir atlasīts kā debitora konts, tiek izmantots kā rēķina konts.
    * Ja rēķins nav grāmatots, uzskaites statuss sākas ar **Notiek**.
    * Rēķina numurs tiek piešķirts, kad rēķins tiek grāmatots.
    * Ja lietojat vienotās eiro maksājumu zonas (SEPA) mandātus, tad tiešā debeta mandāts automātiski tiek ievadīts, kad atlasāt debitora kontu.

4. Laukā **Apraksts** ievadiet kādu vērtību.
5. Laukā **Galvenais konts** norādiet kāda konta numuru, kuram nav dimensiju. Vēlāk šajā rakstā ievadīsiet dimensijas.

    Lai atrastu kontu, varat arī ievadīt vienu vai vairākas rakstzīmes galvenajam kontam un lietot uzmeklēšanu.

6. Atlasiet kopsavilkuma cilni **Rindas informācija**, lai galvenajam kontam pievienotu dimensijas.
7. Atlasiet cilni **Finanšu dimensiju rinda**.

    * Šīs dimensijas ir tikai atlasītajai rindai.
    * PVN grupu aizpilda no debitora datiem. Ja debitoram nav PVN grupas, tad tiek izmantota PVN grupa no galvenā konta.
    * Krājumu PVN grupa tiek aizpildīta no galvenā konta datiem. Ja galvenajam kontam nav krājuma PVN grupas, tad tiek izmantota Virsgrāmatas PVN parametros norādītā krājuma PVN grupa.

8. Pēc izvēles: laukā **Daudzums** ievadiet skaitli.
9. Pēc izvēles: laukā **Vienības cena** ievadiet skaitli.

    Šī summa tiek aprēķināta kā daudzums reiz vienības cena. Taču varat ignorēt šo aprēķinu, ievadot kādu summu.

10. Atlasiet **PVN**, lai skatītu rēķinam aprēķināto PVN.

    Varat skatīt PVN summas šajā lapā, vai šīs summas varat ignorēt cilnē **Korekcija**.

11. Atlasiet **Labi**.
12. Atlasiet **Maksas**, lai savam rēķinam pievienotu kādu maksu.
13. Laikā **Maksu kods** ierakstiet kādu vērtību.
14. Laukā **Maksu vērtība** ievadiet kādu skaitli.
15. Aizvērt lapu.
16. Atlasiet **Kopsummas**, lai skatītu kopsavilkumu par rēķina detalizēto informāciju un kopsummām.
17. Atlasiet **Aizvērt**.
18. Atlasiet **Grāmatot**, lai rēķinu grāmatotu. Joprojām būs iespēja atcelt pirms faktiskās iegrāmatošanas.

    * Rēķinu drukāšanas laiku var mainīt. Atlasiet **Pašreizējais**, lai katru rēķinu drukātu, līdzko tas ir atjaunināts. Atlasiet **Pēc**, lai drukāšanu veiktu pēc tam, kad ir atjaunināti visi rēķini.
    * Lai mainītu to, kā debitora kredīta limits tiek pārbaudīts pirms rēķina grāmatošanas, mainiet vērtību laukā **Kredīta limita veids**.
    * Varat izvēlēties pārtraukt bezmaksas teksta rēķinu grāmatošanu, ja lapas Debitoru parādu parametri cilnē Atjauninājumi **Debitoru parādu > Debitoru parādu parametri (** Debitoru parādu > Debitoru parādu **parametri**) rodas kļūda **.** Atlasiet **Jā**, lai **pārtrauktu brīvā teksta** rēķinu grāmatošanu pirmajā kļūdas parametrā, lai pārtrauktu brīvā teksta rēķinu grāmatošanu, ja rodas kļūda. Ja grāmatošana ir pakešuzdevumā, kļūda apturēs grāmatošanas procesu un pakešuzdevuma statuss tiks iestatīts uz **Kļūda**. Ja šī opcija nav atlasīta, grāmatošanas process izlaiž rēķinu ar grāmatošanas kļūdu un turpinās grāmatot papildu rēķinus. Ja grāmatošana partijā, grāmatošanas kļūda neļaus grāmatot citus rēķinus. Partijas statuss būs **Pabeigts**. Detalizēts grāmatošanas procesa pārskats būs pieejams pārskatīšanai pakešuzdevumu vēsturē.
    *  Microsoft Dynamics 365. finanšu 10.0.30. brīva teksta rēķinu grāmatošanas uzlabojums kopsummas aprēķina funkcija uzlabo grāmatošanas **veiktspēju,** ļaujot tam darboties efektīvāk. Ja ir iespējota šī funkcija, grāmatošanas laikā aprēķinātās kopsummas tiek saglabātas, nevis pārrēķinātas vairākas reizes grāmatošanas procesa laikā. 
    *  Microsoft Dynamics 365 Finanses 10.0.31 brīvā teksta rēķinu pakešveida grāmatošanas procesa **uzlabošanas funkcija uzlabo grāmatošanas veiktspēju,** ļaujot tam darboties efektīvāk. Kad šī funkcija ir aktivizēta, grāmatošana izmanto modeli, kas pats pārvalda paketes grāmatošanas darba slodzi starp fiksētu pavedienu skaitu, tā vietā, lai piešķirtu fiksētu dokumentu skaitu neierobežotam pavedienu skaitam.
    * Lai izdrukātu rēķinu, iestatiet šo opciju pozīcijā **Jā**.
    * Lai grāmatotu rēķinu, iestatiet šo opciju pozīcijā **Jā**. Rēķinu varat izdrukāt arī bez tā grāmatošanas.

19. Atlasiet **Labi**.

## <a name="copy-lines"></a>Kopēt rindas
Lai kopētu rindas brīva teksta rēķinā, atlasiet vienu vai vairākas rindas un pēc tam atlasiet **Kopēt atlasītās rindas**. Varat norādīt veicamo kopiju skaitu un varat arī kopēt piezīmes un pielikumus. Varat vai nu kopēt sadales, vai atļaut tās no jauna izveidot pēc grāmatošanas.

Pēc rindu kopēšanas informāciju var mainīt pēc nepieciešamības.

## <a name="create-a-free-text-invoice-from-a-template"></a>Brīva teksta rēķina izveide no veidnes
Brīva teksta rēķina izveidei varat izmantot veidni. Cilnes **Rēķins** veidnē atlasot vienumu **Jauns no veidnes**, varat atlasīt veidnes nosaukumu un debitora kontu, ko izmantot jaunā brīva teksta rēķina izveidē. Noklusējuma vērtības, piemēram, maksāšanas termiņus un maksāšanas metodi, var automātiski aizpildīt no debitora datiem, vai arī varat izmantot vērtības, kas tika saglabātas veidnē.

Jauns brīva teksta rēķins ir izveidots, un tā vērtības var rediģēt pēc nepieciešamības.

## <a name="resetting-the-workflow-status-for-free-text-invoices-from-unrecoverable-to-draft"></a>Brīva teksta rēķinu darbplūsmas statusa atiestatīšana no Neatkopjams uz Melnraksts
Darbplūsmas instancei, kas apturēta, jo radās neatkopjama kļūda, būs darbplūsmas statuss **Neatkopjama**. Kad debitora brīva teksta rēķina darbplūsmas statuss ir Neatkopjams **, varat atiestatīt to** **uz Melnraksts, atlasot** Atsaukt **no darbplūsmas darbībām.**  Pēc tam varat labot debitora brīva teksta rēķinu. Šī funkcija ir pieejama, **ja līdzekļu**  **pārvaldības** lapā ir ieslēgta darbplūsmas statusa atiestatīšana brīva teksta rēķiniem no Neizlabojams uz parametru Melnraksts.

Varat izmantot lapu **Darbplūsmas vēsture**, lai atiestatītu darbplūsmas statusu uz **Melnraksts**. Šo lapu var atvērt no brīva **teksta rēķina** vai no **kopējā > vaicājumiem > darbplūsmu**. Lai atiestatītu darbplūsmas statusu uz **Melnraksts**, atlasiet **Atsaukt**. Varat arī atiestatīt darbplūsmas statusu uz **Melnraksts** **, atlasot** atsaukt **darbību** brīva teksta rēķina **lapā vai** visu brīva teksta rēķinu lapā. Kad darbplūsmas statuss ir atiestatīts uz **Melnraksts**, tas kļūst pieejams rediģēšanai brīva **teksta rēķina** lapā.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
