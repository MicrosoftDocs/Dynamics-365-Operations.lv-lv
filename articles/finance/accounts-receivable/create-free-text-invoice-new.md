---
title: Brīva teksta rēķina izveide
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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 7ccc652a407e9ed09c2ffffd3c86ff5070d6399b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217510"
---
# <a name="create-a-free-text-invoice"></a>Brīva teksta rēķina izveide

[!include [banner](../includes/banner.md)]

Šajā tēmā izskaidrots, kā izveidot brīva teksta rēķinus. Šai procedūrai izmantojiet demonstrācijas uzņēmuma **USMF** datus.

## <a name="create-a-free-text-invoice"></a>Izveidot brīva teksta rēķinu

1. Dodieties uz **Debitori (vai Pārdošanas virsgrāmata) \> Rēķini \> Visi brīva teksta rēķini**.
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]