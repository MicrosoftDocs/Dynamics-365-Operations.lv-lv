--- 
title: "Brīva teksta rēķina izveidošana"
description: "Šajā rakstā ir paskaidrots, kā izveidot brīva teksta rēķinu."
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 2a611bdd4dd97109709ed355eb80471e27413744
ms.contentlocale: lv-lv
ms.lasthandoff: 06/28/2018

---

# <a name="create-a-free-text-invoice"></a>Brīva teksta rēķina izveidošana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrots, kā izveidot brīva teksta rēķinu. Šai procedūrai izmantojiet demonstrācijas uzņēmuma “USMF” datus.

## <a name="create-a-free-text-invoice"></a>Brīva teksta rēķina izveidošana

1. Pārejiet uz sadaļu Debitori > Rēķini > Visi brīva teksta rēķini.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts atlasiet kādu vērtību.
    * Rēķina konts pēc noklusējuma būs tas pats konts, kas tiek izmantots debitora kontam.   
    * Uzskaites statuss sākas ar Notiek, ja rēķins nav grāmatots.   
    * Rēķina numurs tiek piešķirts, kad rēķins tiek grāmatots.  
    * Ja lietojat SEPA mandātus, tad tiešā debeta mandāts automātiski tiks aizpildīts ar mandātu, kad atlasāt debitora kontu.  
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Galvenais konts norādiet kāda konta numuru bez dimensijām.
    * Lai atrastu savu kontu, varat arī ievadīt vienu vai vairākas rakstzīmes galvenajam kontam un lietot uzmeklēšanu. Dimensijas jūs ievadīsiet vēlākā šī ceļveža posmā.  
6. Izvērsiet kopsavilkuma cilni Detalizēta informācija par rindu, lai savam galvenajam kontam pievienotu dimensijas.
7. Noklikšķiniet uz cilnes Finanšu dimensiju rinda.
    * Šīs dimensijas ir tikai atlasītajai rindai.    
    * PVN grupa tiek aizpildīta no debitora datiem. Ja debitoram nav PVN grupas, tad tiek izmantota PVN grupa no galvenā konta.  
    * Krājumu PVN grupa tiek aizpildīta no galvenā konta datiem. Ja galvenajam kontam nav krājuma PVN grupas, tiek izmantota Virsgrāmatas PVN parametru sadaļā norādītā krājuma PVN grupa.    
8. Laukā Daudzums ievadiet skaitli.
    * Daudzums ir neobligāts.  
9. Laukā Vienības cena ievadiet kādu skaitli.
    * Vienības cena ir neobligāta.  
    * Šī summa tiek aprēķināta kā daudzums reiz vienības cena. Taču varat ignorēt šo aprēķinu un ievadīt kādu summu.  
10. Noklikšķiniet uz PVN, lai skatītu savam rēķinam aprēķināto PVN.
    * Skatiet PVN summas šajā lapā, vai šīs summas varat ignorēt cilnē Korekcija.  
11. Noklikšķiniet uz OK.
12. Noklikšķiniet uz Maksas, lai savam rēķinam pievienotu kādu maksu. 
13. Laukā Maksu kods ierakstiet kādu vērtību.
14. Laukā Maksu vērtība ievadiet kādu skaitli.
15. Aizvērt lapu.
16. Noklikšķiniet uz Kopsummas, lai apskatītu kopsavilkumu par rēķina detalizēto informāciju un kopsummām.
17. Noklikšķiniet uz Aizvērt.
18. Lai grāmatotu rēķinu, klikšķiniet uz Grāmatot. Pirms grāmatošanas varēsiet to atcelt.
    * Lai mainītu savu rēķinu drukāšanas laiku: atlasiet Pašreizējais, lai katru rēķinu drukātu, līdzko tas ir atjaunināts, vai atlasiet Pēc, lai drukāšanu veiktu pēc tam, kad ir atjaunināti visi rēķini.  
    * Ja vēlaties mainīt to, kā pirms grāmatošanas tiek pārbaudīts debitora kredīta limits, mainiet vienumu Kredīta limita tips.  
    * Ja vēlaties drukāt rēķinu, atlasiet Jā.  
    * Ja vēlaties grāmatot rēķinu, atlasiet Jā. Rēķinu varat izdrukāt arī bez grāmatošanas.  
19. Noklikšķiniet uz OK.

## <a name="copy-lines"></a>Kopēt rindas
Lai kopētu rindas brīva teksta rēķinā, atlasiet vienu vai vairākas rindas un pēc tam noklikšķiniet uz Kopēt atlasītās rindas. Var norādīt kopiju skaitu vai kopēt piezīmes un pielikumus. Varat kopēt sadales vai atļaut tās no jauna uzveidot pēc grāmatošanas. Kopējot rindas, informāciju var mainīt pēc nepieciešamības. 

## <a name="create-a-free-text-invoice-from-a-template"></a>Brīva teksta rēķina izveide no veidnes
Brīva teksta rēķina izveidei varat izmantot veidni. Cilnes “Rēķins” veidnē atlasot vienumu “Jauns”, varat atlasīt veidnes nosaukumu un debitora kontu, ko izmantot jaunā brīva teksta rēķina izveidē. Varat arī izvēlēties noklusējuma vērtības, piemēram, maksāšanas termiņus un debitora maksāšanas metodi, vai izmantot vērtības, kas tika saglabātas veidnē. Jauns brīva teksta rēķins tiks izveidots un varēsit rediģēt tajā esošās vērtības. 


