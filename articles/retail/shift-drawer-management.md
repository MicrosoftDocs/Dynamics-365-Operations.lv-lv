---
title: "Maiņu un naudas kastes pārvaldība"
description: "Šajā rakstā ir paskaidrots, kā iestatīt un izmantot abus mazumtirdzniecības pārdošanas punkta (POS) maiņu tipus — koplietoto un savrupo. Koplietotās maiņas var izmantot vairāki lietotāji vairākās vietās, bet savrupās maiņas vienlaicīgi var izmantot tikai viens darbinieks."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b8e12f3f4c2f8f5a596c8994f2a4571d8a907062
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="shift-and-cash-drawer-management"></a>Maiņu un naudas kastes pārvaldība

[!include[banner](includes/banner.md)]


Šajā rakstā ir paskaidrots, kā iestatīt un izmantot abus mazumtirdzniecības pārdošanas punkta (POS) maiņu tipus — koplietoto un savrupo. Koplietotās maiņas var izmantot vairāki lietotāji vairākās vietās, bet savrupās maiņas vienlaicīgi var izmantot tikai viens darbinieks.

Pastāv divi mazumtirdzniecības pārdošanas punktu (POS) maiņu tipi: savrupā un koplietotā. Savrupās maiņas vienlaicīgi var lietot tikai viens darbinieks. Koplietotās maiņas var izmantot vairāki lietotāji vairākās vietās. Tāpēc tās efektīvi izveido vienu maiņu vairākiem darbiniekiem veikalā.

## <a name="standalone-shifts"></a>Savrupās maiņas
Savrupās maiņas tiek izmantotas tradicionālajā, fiksēta POS scenārijā, kur katram POS reģistram nauda tiek saskaņota atsevišķi. Piemēram, pārtikas preču veikalā parasti ir vairāki fiksēti POS reģistri un katram reģistram ir nozīmēts kāds kasieris. Šādā gadījumā katram reģistram, visticamāk, tiek izmantota savrupa maiņa, un kasieris ir atbildīgs par kases aparātu vai fizisko kasi attiecīgajā reģistrā. Savrupā maiņa ietver visas aktivitātes attiecīgajā reģistrā, kas notiek kasiera darba maiņas laikā. Šīs aktivitātes var ietvert sākuma summu, kas ir deponēta kases aparātā, visas naudas izņemšanas un pielikšanas operācijas, izmantojot tādas operācijas kā noguldījumus bankā un mainīgo ierakstu, kā arī norēķinu uzskaiti maiņas beigās.

### <a name="set-up-a-stand-alone-shift"></a>Savrupās maiņas iestatīšana

Savrupā maiņa tiek norādīta naudas kastes līmenī. Šajā procedūrā ir paskaidrots, kā iestatīt savrupu maiņu POS reģistrā.

1.  Noklikšķiniet uz **Retail** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS profili** &gt; **Aparatūras profili**.
2.  Atlasiet aparatūras profilu, kuru izmantot savrupajai maiņai.
3.  Kopsavilkuma cilnē **Naudas kaste** pārliecinieties, ka opcija **Koplietotās maiņas naudas kaste** ir iestatīta uz **Nē**.
4.  Noklikšķiniet uz **Saglabāt**.
5.  Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **Reģistri**.
6.  Atlasiet reģistru, kam ir nepieciešama savrupa maiņa, un pēc tam noklikšķiniet uz **Rediģēt**.
7.  Laukā **Aparatūras profils** atlasiet aparatūras profilu, ko atlasījāt 2. darbībā.
8.  Noklikšķiniet uz **Saglabāt**.
9.  Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiks**.
10. Atlasiet sadales grafiku **1090** un pēc tam noklikšķiniet uz **Izpildīt tūlīt**, lai veiktās izmaiņas sinhronizētu uz POS.

### <a name="use-a-stand-alone-shift"></a>Lietot savrupu maiņu

1.  Pierakstieties pārdošanas punktā (POS).
2.  Ja nav atvērta neviena maiņa, atlasiet vienumu **Atvērt jaunu maiņu**.
3.  Dodieties uz operāciju **Deklarēt sākuma summu** un norādiet naudas summu, kas kases aparātam tiek pievienota darba dienas sākumā.
4.  Izpildiet kādas transakcijas.
5.  Dienas beigās atlasiet vienumu **Norēķinu uzskaite**, lai deklarētu naudas kastē atlikušo naudas summu.
6.  Ievadiet šo naudas summu un pēc tam noklikšķiniet uz **Saglabāt**, lai saglabātu norēķinu uzskaiti.
7.  Atlasiet vienumu **Slēgt maiņu**, lai slēgtu šo maiņu.

**Piezīme.** Atkarībā no izmantotajiem biznesa procesiem maiņas laikā ir pieejamas citas operācijas. Operācijas **Noguldījums seifā**, **Noguldījums bankā** un **Norēķinu noņemšana** var izmantot, lai izņemtu naudu no kases aparāta dienas laikā vai pirms maiņas slēgšanas. Ja kases aparātā sāk pietrūkt skaidras naudas, varat izmantot operāciju **Mainīgais ieraksts**, lai kases aparātam pievienotu skaidru naudu.

## <a name="shared-shifts"></a>Koplietotās maiņas
Koplietotā maiņa tiek izmantota vidē, kur vairāki kasieri strādā pie vienas naudas kastes vai vairākām naudas kastēm visā darba dienas garumā. Parasti koplietotas maiņas tiek izmantotas mobilās POS vidēs. Mobilā vidē katrs kasieris nav norīkots pie vienas naudas kastes un nav atbildīgs par vienu naudas kasti. Tā vietā visiem kasieriem ir jāspēj iemaksāt par pārdošanu saņemto naudu un pievienot naudu tajā naudas kastē, kas atrodas tuvāk. Šādā scenārijā kasieru kopīgi lietotās naudas kastes tiek iekļautas koplietotā maiņā. Ar attiecīgās maiņas naudas pārvaldību saistīto aktivitāšu nolūkos visas šīs naudas kastes koplietotajā maiņā ir ietvertas vienā un tajā pašā maiņā. Tādēļ šādas maiņas sākuma summai ir jāietver visa naudas summa visās koplietotajā maiņā iekļautajās naudas kastēs. Līdzīgi arī norēķinu uzskaite ir visa naudas summa visās koplietotajā maiņā iekļautajās naudas kastēs. **Piezīme:** katrā veikalā vienlaicīgi var būt atvērta tikai viena koplietotā maiņa. Vienā veikala var lietot gan koplietotās maiņas, gan savrupās maiņas.

### <a name="set-up-a-shared-shift"></a>Koplietotās maiņas iestatīšana

1.  Noklikšķiniet uz **Retail** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **POS profili** &gt; **Aparatūras profili**.
2.  Atlasiet aparatūras profilu, kuru izmantot koplietotajai maiņai.
3.  Kopsavilkuma cilnē **Naudas kaste** opciju **Koplietotās maiņas naudas kaste** iestatiet uz **Jā**.
4.  Noklikšķiniet uz **Saglabāt**.
5.  Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Kanāla iestatīšana** &gt; **POS iestatīšana** &gt; **Reģistri**.
6.  Atlasiet reģistru, kam ir nepieciešama koplietotā maiņa, un pēc tam noklikšķiniet uz **Rediģēt**.
7.  Laukā **Aparatūras profils** atlasiet aparatūras profilu, ko atlasījāt 2. darbībā.
8.  Noklikšķiniet uz **Saglabāt**.
9.  Noklikšķiniet uz **Mazumtirdzniecība** &gt; **Mazumtirdzniecības IT** &gt; **Sadales grafiks**.
10. Atlasiet sadales grafiku **1090** un pēc tam noklikšķiniet uz **Izpildīt tūlīt**, lai veiktās izmaiņas sinhronizētu uz POS.

### <a name="use-a-shared-shift"></a>Lietot koplietoto maiņu

1.  Pierakstieties pārdošanas punktā (POS).
2.  Ja šis POS vēl nav savienots ar aparatūras staciju, atlasiet vienumu **Operācija bez naudas kastes** un pēc tam atlasiet operāciju **Atlasīt aparatūras staciju**, lai šo aparatūras staciju aktivizētu koplietotajai maiņai. Šo darbību ir nepieciešams izpildīt tikai pirmajā reizē, kad reģistrs tiek pievienots koplietotās maiņas videi.
3.  Izrakstieties no POS un pēc tam pierakstieties tajā atkal.
4.  Atlasiet vienumu **Izveidot jaunu maiņu**.
5.  Atlasiet vienumu **Deklarēt sākuma summu**.
6.  Ievadiet sākuma summu visām šī veikala naudas kastēm, kas veido daļu no koplietotās maiņas, un pēc tam noklikšķiniet uz **Saglabāt**.
    -   Lai katrai secīgajai naudas kastei pievienotu daļu no sākuma summas, izmantojiet operāciju **Atlasīt aparatūras staciju**, lai aktivizētu aparatūras staciju.
    -   Lai kases aparātu pievienotu kādai konkrētai naudas kastei, izmantojiet operāciju **Atvērt naudas kasti**.
    -   Turpiniet, līdz visām naudas kastēm koplietotajā maiņā ir to attiecīgā daļa no sākuma summas.

7.  Dienas beigās atveriet katru naudas kasti un izņemiet naudu.
8.  Kad nauda ir izņemta no pēdējās naudas kastes, saskaitiet visu naudu no visām naudas kastēm.
9.  Izmantojiet operāciju **Norēķinu uzskaite**, lai deklarētu kopējo naudas summu no visām koplietotajā maiņā iekļautajām naudas kastēm.
10. Izmantojiet operāciju **Slēgt maiņu**, lai slēgtu koplietoto maiņu.





