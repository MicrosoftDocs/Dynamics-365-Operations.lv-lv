---
title: Izveidot brīvā teksta rēķinus
description: Šajā tēmā izskaidrots, kā izveidot brīva teksta rēķinus.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 4498f5c9ce0e3830ffe1857c0363ca962561fc59
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178898"
---
# <a name="create-free-text-invoices"></a>Izveidot brīvā teksta rēķinus

[!include [banner](../includes/banner.md)]

Šajā tēmā izskaidrots, kā izveidot brīva teksta rēķinus. Šai procedūrai izmantojiet demonstrācijas uzņēmuma **USMF** datus.

## <a name="create-a-free-text-invoice"></a>Brīva teksta rēķina izveidošana

1. Dodieties uz **Debitoru parādi \> Rēķini \> Visi brīva teksta rēķini**.
2. Atlasiet **Jauns**.
3. Laukā **Debitora konts** atlasiet kādu vērtību.

    * Pēc noklusējuma konts, kas ir atlasīts kā debitora konts, tiek izmantots kā rēķina konts.
    * Ja rēķins nav grāmatots, uzskaites statuss sākas ar **Notiek**.
    * Rēķina numurs tiek piešķirts, kad rēķins tiek grāmatots.
    * Ja lietojat vienotās eiro maksājumu zonas (SEPA) mandātus, tad tiešā debeta mandāts automātiski tiek ievadīts, kad atlasāt debitora kontu.

4. Laukā **Apraksts** ievadiet kādu vērtību.
5. Laukā **Galvenais konts** norādiet kāda konta numuru, kuram nav dimensiju. Dimensijas jūs ievadīsiet vēlākā šīs tēmas posmā.

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
    * Lai izdrukātu rēķinu, iestatiet šo opciju pozīcijā **Jā**.
    * Lai grāmatotu rēķinu, iestatiet šo opciju pozīcijā **Jā**. Rēķinu varat izdrukāt arī bez tā grāmatošanas.

19. Atlasiet **Labi**.

## <a name="copy-lines"></a>Kopēt rindas
Lai kopētu rindas brīva teksta rēķinā, atlasiet vienu vai vairākas rindas un pēc tam atlasiet **Kopēt atlasītās rindas**. Varat norādīt veicamo kopiju skaitu un varat arī kopēt piezīmes un pielikumus. Varat vai nu kopēt sadales, vai atļaut tās no jauna izveidot pēc grāmatošanas.

Pēc rindu kopēšanas informāciju var mainīt pēc nepieciešamības.

## <a name="create-a-free-text-invoice-from-a-template"></a>Brīva teksta rēķina izveide no veidnes
Brīva teksta rēķina izveidei varat izmantot veidni. Cilnes **Rēķins** veidnē atlasot vienumu **Jauns no veidnes**, varat atlasīt veidnes nosaukumu un debitora kontu, ko izmantot jaunā brīva teksta rēķina izveidē. Noklusējuma vērtības, piemēram, maksāšanas termiņus un maksāšanas metodi, var automātiski aizpildīt no debitora datiem, vai arī varat izmantot vērtības, kas tika saglabātas veidnē.

Jauns brīva teksta rēķins ir izveidots, un tā vērtības var rediģēt pēc nepieciešamības.