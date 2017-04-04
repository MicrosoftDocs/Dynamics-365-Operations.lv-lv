---
title: "Klientu pasūtījumu pārskats"
description: "Šajā tēmā ir sniegta informācija par klientu pasūtījumus, mazumtirdzniecības mūsdienu POS (MPOS). Klientu pasūtījumu tiek dēvētas arī par īpašiem pasūtījumiem. Tēma ietver diskusiju saistītie parametri un darījumu plūsmu."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2f466dfe53ccf0be15ed0793b4a6dd371bdacc0d
ms.lasthandoff: 03/31/2017


---

# <a name="customer-orders-overview"></a>Klientu pasūtījumu pārskats

Šajā tēmā ir sniegta informācija par klientu pasūtījumus, mazumtirdzniecības mūsdienu POS (MPOS). Klientu pasūtījumu tiek dēvētas arī par īpašiem pasūtījumiem. Tēma ietver diskusiju saistītie parametri un darījumu plūsmu.

Omni-channel mazumtirdzniecības pasaulē, daudzi mazumtirgotāji nodrošina klientam iespēju, vai īpašu pasūtījumu, dažādu produktu un izpildīšanas prasību. Šeit ir daži tipiski scenāriji:

-   Klients vēlas produkti jāpiegādā uz konkrētu adresi noteiktā datumā.
-   Klients vēlas uzņemt produktus no veikala vai atrašanās vietā, kas atšķiras no veikala vai vietu, kur klientam iegādāties šos produktus.
-   Klients vēlas kāds cits uzņemt produktus, kuru klients iegādājies.

Klientu pasūtījumu var izmantot arī mazumtirgotāji minimizēt zaudētos pārdošanas apjomus, kas akciju pārtraukumiem var izraisīt citādi, tāpēc, ka preces var piegādāt vai pacēla uz citu laiku vai vietu.

## <a name="set-up-customer-orders"></a>Iestatītu klientu pasūtījumus
Šeit ir daži no parametriem, kas var iestatīt **mazumtirdzniecības parametrus** lapu, lai noteiktu, kā klientu pasūtījumi tiek izpildīti:

-   **Noklusējuma depozīta procentu** – norādīt summu, kas klientam jāmaksā par depozītu pirms rīkojumu var apstiprināt. Noklusējuma depozīta summu aprēķina kā procentuālo daļu no pasūtījuma vērtības. Atkarībā no privilēģijām, veikals asociētā spētu ignorēt summu, lietojot **depozīta ignorēšanas**.
-   **Atcelšanas maksa procentos** – ja maksa tiks piemēroti, ja klienta pasūtījums ir atcelts, norādīt, ka izmaksu summa.
-   **Atcelšanas maksas kodam** – ja maksa tiks piemēroti, ja klienta pasūtījums ir atcelts, ka maksas atspoguļosies zem maksas kodu pārdošanas pasūtījumā sistēmā Microsoft Dynamics AX. Izmantojiet šo parametru, lai definētu atcelšanas maksas kodam.
-   **Pārvadāšanas maksas kods** -mazumtirgotāji var iekasēt papildu maksu par preču nosūtīšanu klientam. Ka kuģniecības maksu atspoguļosies zem maksas kodam Dynamics AX pārdošanas pasūtījumā. Izmantojiet šo parametru, lai kartētu kuģniecības maksas kodam nosūtīšanas maksas pēc klientu pasūtījuma.
-   **Pārvadājumu maksas kompensāciju** – norādīt sūtīšanas izdevumus, kas saistīti ar klienta pasūtījumu atgriežami.
-   **Maksimālā summa bez apstiprinājuma** – ja kuģošanas maksa tiek atgriezta, norādiet maksimālo summu kuģniecības maksas kompensācijām visās preču atgriešanas pasūtījumos. Ja šī summa ir pārsniegta, pārvaldnieks ignorēšana ir nepieciešama, lai turpinātu kompensāciju. Lai pielāgotos šiem scenārijiem, kuģniecības maksas atmaksu var pārsniegt summu, kas sākotnēji samaksāta:
    -   Maksas tiek piemērotas līmenī pārdošanas pasūtījuma virsrakstā, un, ja kādu produktu līniju daudzums tiek atdots atpakaļ, maksimālās kompensācijas par kuģniecības maksa, kas atļauta attiecībā uz produktiem un daudzumu nevar noteikt tādā veidā, kas der visiem mazumtirdzniecības klientiem.
    -   Kuģniecības jāmaksā par katru gadījumu, ja kuģniecības. Ja klients atgriež produktu vairākas reizes un mazumtirgotājs polisē ir norādīts, ka mazumtirgotājs nesīs atpakaļ nosūtīšanas izmaksas izmaksas, atpakaļ nosūtīšanas izmaksas būs vairāk nekā faktiskās piegādes izmaksas.

## <a name="transaction-flow-for-customer-orders"></a>Darbības plūsmas klientu pasūtījumus
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Izveidot klientu pasūtījumu mazumtirdzniecības mūsdienu POS

1.  Pievienojiet darbībai debitoru.
2.  Pievienot produktu grozam.
3.  Noklikšķiniet uz **izveidot klientu pasūtījumu**, un pēc tam atlasiet pasūtījuma tipu. Pasūtījuma tipu var būt vai nu **klienta pasūtījumu** vai **citēt**.
4.  Noklikšķiniet uz **kuģis izvēlēts** vai **kuģis, visi** nosūtīt produktus uz adresi uz debitora kontu, jānorāda pieprasītais nosūtīšanas datums un norādīt sūtīšanas izdevumus.
5.  Noklikšķiniet uz **uzņemt atlasīti** vai **pick-up visu** izvēlēties produktus, kas būs palielinājies no pašreizējā veikalā vai citu veikalu noteiktā datumā.
6.  Noguldījuma summu savākt, ja depozīts ir vajadzīga.

### <a name="edit-an-existing-customer-order"></a>Rediģēt esošo klientu pasūtījumu

1.  Mājas lappusē, noklikšķiniet uz **atrast pasūtījuma**.
2.  Atrodiet un atlasiet Rediģēt pasūtījumu. Lapas apakšdaļā noklikšķiniet uz **rediģēt**.

### <a name="pick-up-an-order"></a>Uzņemt rīkojumu

1.  Mājas lappusē, noklikšķiniet uz **atrast pasūtījuma**.
2.  Atlasiet pasūtījumu, lai paceltu. Lapas apakšdaļā noklikšķiniet uz **izdošanu un iepakojuma**.
3.  Noklikšķiniet uz **uzņemt**.

### <a name="cancel-an-order"></a>Atcelt pasūtījumu

1.  Mājas lappusē, noklikšķiniet uz **atrast pasūtījuma**.
2.  Atlasiet pasūtījumu, lai atceltu. Lapas apakšdaļā noklikšķiniet uz **atcelt**.

#### <a name="create-a-return-order"></a>Atgriešanas pasūtījuma izveidošana

1.  Mājas lappusē, noklikšķiniet uz **atrast pasūtījuma**.
2.  Atlasiet pasūtījumu, lai atgrieztos, atlasiet pasūtījuma rēķins un pēc tam atlasiet preces atgriezt produktu līniju.
3.  Lapas apakšdaļā noklikšķiniet uz **atgriezto preču pasūtījums**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Asinhrono darbības plūsmas klientu pasūtījumus
Klientu pasūtījumu var izveidot sale (POS) klienta viedokļa vai nu sinhronas vai asinhronas režīmā.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Iespējot klientu pasūtījumiem jāveido asinhronā režīmā

1.  Dynamics AX noklikšķiniet **mazumtirdzniecības un komercijas**&gt;**kanāla iestatījumu**&gt;**POS uzstādīšanas**&gt;**POS profilu**&gt;**funkcionalitāti profili**.
2.  Par **vispārējā** FastTab, iestatiet **izveidot klientu pasūtījumu async režīmā** iespēju **Jā**.

Kad **izveidot klientu pasūtījumu async režīmā** opcija ir iestatīta uz **Jā**, klients vienmēr pasūtījumus asinhronā režīmā, pat ja mazumtirdzniecības darbības pakalpojumu (RTS) ir pieejama. Ja šī opcija ir iestatīta, **Nr**, klientu pasūtījumi vienmēr tiek veidotas sinhronais režīms, izmantojot RTS. Veidojot klientu pasūtījumus asinhronā režīmā, viņi velk un ievietots Dynamics AX ar Pull (P) darbus. Atbilstošo pārdošanas pasūtījumi ir izveidoti programmā Dynamics AX kad **sinhronizēt pasūtījumus** darbojas vai nu manuāli, vai izmantojot pakešuzdevuma process.

<a name="see-also"></a>Skatiet arī
--------

[Hibrīda klientu pasūtījumus](hybrid-customer-orders.md)


