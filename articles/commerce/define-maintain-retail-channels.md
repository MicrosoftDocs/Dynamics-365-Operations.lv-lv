---
title: Mazumtirdzniecības kanālu definēšana un uzturēšana
description: Šajā tēmā ir sniegts apskats par to, kā iestatīt fiziskos veikalus, kas programmā Dynamics 365 Commerce tiek saukti par veikaliem. Rakstā ir ietverta informācija par uzdevumiem, kas jums ir jāizpilda gan pirms, gan pēc veikala iestatīšanas.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0fbca2c9178cd372653287afdf72deaf75442604
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413967"
---
# <a name="define-and-maintain-retail-channels"></a>Mazumtirdzniecības kanālu definēšana un uzturēšana

[!include [banner](includes/banner.md)]

Šajā tēmā ir sniegts apskats par to, kā iestatīt fiziskos veikalus, kas programmā Dynamics 365 Commerce tiek saukti par veikaliem. Rakstā ir ietverta informācija par uzdevumiem, kas jums ir jāizpilda gan pirms, gan pēc veikala iestatīšanas.

Commerce atbalsta vairākus kanālus, piemēram, tiešsaistes veikalus, zvanu centrus un fiziskos veikalus. Fizisks veikals tiek saukts par veikalu. Katram veikalam var būt savas maksāšanas metodes, cenu grupas, pārdošanas punktu (POS) kases, ienākumu un izdevumu konti, kā arī personāls. Pirms izveidojat veikalu, jums tam ir jāiestata visi šie elementi. Pēc veikala izveidošanas jums ir jāpiešķir preces, kuras vēlaties tajā izmantot. Veikalam var arī piešķirt darbiniekus, kases sistēmas un debitorus. Visbeidzot, pievienojiet jaunu veikalu organizācijas hierarhijai.

## <a name="setting-up-stores"></a>Veikalu iestatīšana

Pirms veikala iestatīšanas programmā Commerce, ir jāveic daži priekšnosacījumu uzdevumi. Pēc tam varat izveidot veikalu un pievienot detalizētu informāciju.

### <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu iestatīt veikalu, jums ir jāizpilda tālāk uzskaitītie uzdevumi.

1. Konfigurējiet savas organizācijas struktūru un iestatiet organizācijas hierarhijas mazumtirdzniecības preču klāstiem, papildināšanai un atskaišu veidošanai.
2. Iestatiet noliktavu, kas pārstāv veikalu.
3. Iestatiet numuru sērijas veikaliem, veikala pārskatiem un deklarācijas dokumentiem.
4. Konfigurējiet programmas Commerce parametrus.
5. Iestatiet veikalam pieņemamas maksājumu metodes.
6. Lai apstrādātu kredītkaršu transakcijas pārdošanas punkta (POS) kases sistēmās, varat iestatīt arī maksāšanas pakalpojumus.
7. Iestatiet PVN grupas.
8. Iestatiet preces. Kā daļu no šī uzdevuma varat arī iestatīt preču hierarhijas, preču variantus un preču klāstus.
9. Iestatiet preču cenu grupas.
10. Iestatiet preču cenu noteikšanu. Kā daļu no šo uzdevuma varat iestatīt arī cenu korekcijas, atlaides un atlaižu periodus.
11. Iestatiet darbiniekus.

    > [!NOTE]
    > Turklāt ir jāpiešķir darbiniekiem atbilstošās atļaujas, lai viņi varētu pierakstīties un izpildīt uzdevumus, izmantojot sistēmu POS.

12. Konfigurējiet POS profilus, kuri tiks piešķirti veikalam. Šis uzdevums iekļauj daudzus citus uzdevumus, piemēram, kases sistēmu iestatīšanu, bezsaistes profilu iestatīšanu un kvīšu formātu un profilu iestatīšanu.

Pārskatiet visus priekšnosacījumos ietvertos uzdevumus un izpildiet tikai tos uzdevumus, kuri attiecas uz jums.

### <a name="set-up-a-store"></a>Veikala iestatīšana

Pēc priekšnosacījumu uzdevumu izpildes izpildiet tālāk uzskaitītos uzdevumus, lai iestatītu detalizētu informāciju par veikalu.

1. Izveidojiet veikalu.
2. Piešķiriet veikalam PVN grupu.
3. Piešķiriet veikalam akceptētās maksājuma metodes.
4. Pievienojiet detalizētu informāciju preču aprakstiem attiecībā uz precēm, kuras tiek piedāvātas jūsu veikalos. Piemēram, var pievienot bagātināto tekstu un attēlus. Šī detalizēta informācija par preci ir redzama dažādos kontekstos, piemēram, POS reģistrā vai drukātajās etiķetēs.
5. Pievienojiet veikalu noklusējuma organizācijas hierarhijai, kura ir piešķirta nolūkiem **Mazumtirdzniecības preču klāsts**, **Mazumtirdzniecības papildināšana** vai **Mazumtirdzniecības atskaišu veidošana**.

### <a name="after-you-set-up-a-store"></a>Pēc veikala iestatīšanas

Pēc detalizētas informācijas par mazumtirdzniecības veikalu ievades, veiciet šos uzdevumus, lai nosūtītu datus par jaunu mazumtirdzniecības veikalu uz POS:

1. Konfigurējiet veikala POS kases sistēmas.
2. Pievienojiet veikalam preču klāstu.
3. Apstrādājiet preču klāstu, lai ģenerētu to preču sarakstu, kuras tiek iekļautas klāstā, un padarītu preces pieejamas veikalā.
4. Nosūtiet datus, piemēram, numuru sērijas, aparatūras profilus un POS ekrāna izkārtojumus, uz POS reģistriem.
5. Publicējiet veikalu, lai nosūtītu veikala datus uz POS.
6. Izpildiet darbus, lai nosūtītu veikala datus uz POS.

## <a name="organization-hierarchies"></a>Organizācijas hierarhijas

Programma Commerce izmanto organizāciju hierarhijas, lai mazumtirdzniecības kanāliem piešķirtu struktūru. Organizācijas hierarhijas pārstāv attiecības starp organizācijām, kas veido jūsu uzņēmumu. Iestatot veikalus, varat tos pievienot organizācijas hierarhijai. Pēc tam veikali koplieto datus, kas tiek izmantoti preču klāstiem, papildināšanai un pārskatu veidošanai.

> [!NOTE]
> Lai izmantotu Commerce pārdošanas funkcionalitāti, jāaktivizē **Vairākas izsūtīšanas** konfigurācijas atslēga. Šo konfigurācijas atslēgu var atrast atslēgās **Tirdzniecības konfigurācija** sadaļā **Sistēmas administrēšana**\> **Iestatījumi** \> **Licences konfigurācija.** Tas ir nepieciešams dažādu validāciju dēļ, pamatojoties uz piegādes adresi, kas konfigurēta pārdošanas pasūtījuma rindas līmenī.

