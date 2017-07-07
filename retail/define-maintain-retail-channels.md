---
title: "Mazumtirdzniecības kanālu definēšana un uzturēšana"
description: "Šajā rakstā ir sniegts pārskats par to, kā iestatīt fiziskos veikalus, kas programmatūrā Microsoft Dynamics 365 for Retail tiek saukti par mazumtirdzniecības veikaliem. Rakstā ir ietverta informācija par uzdevumiem, kas jums ir jāizpilda gan pirms, gan pēc mazumtirdzniecības veikala iestatīšanas."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 3f0b566963574569cb40b72550e2337c9ba8a2ce
ms.contentlocale: lv-lv
ms.lasthandoff: 06/20/2017


---

# <a name="define-and-maintain-retail-channels"></a>Mazumtirdzniecības kanālu definēšana un uzturēšana

[!include[banner](includes/banner.md)]


Šajā rakstā ir sniegts pārskats par to, kā iestatīt fiziskos veikalus, kas programmatūrā Microsoft Dynamics 365 for Retail tiek saukti par mazumtirdzniecības veikaliem. Rakstā ir ietverta informācija par uzdevumiem, kas jums ir jāizpilda gan pirms, gan pēc mazumtirdzniecības veikala iestatīšanas.

Dynamics 365 for Retail atbalsta vairākus mazumtirdzniecības kanālus, piemēram, tiešsaistes veikalus, zvanu centrus un fiziskus veikalus. Fizisks veikals tiek saukts par mazumtirdzniecības veikalu. Katram mazumtirdzniecības veikalam var būt savas maksāšanas metodes, cenu grupas, pārdošanas punktu (POS) kases, ienākumu un izdevumu konti, kā arī personāls. Pirms izveidojat mazumtirdzniecības veikalu, jums tam ir jāiestata visi šie elementi. Pēc mazumtirdzniecības veikala izveidošanas jums ir jāpiešķir preces, kuras vēlaties tajā izmantot. Veikalam var arī piešķirt darbiniekus, kases sistēmas un debitorus. Visbeidzot, pievienojiet jaunu veikalu organizācijas hierarhijai.

## <a name="setting-up-retail-stores"></a>Mazumtirdzniecības veikalu iestatīšana
Pirms mazumtirdzniecības veikala iestatīšanas programmatūrā Dynamics 365 for Retail, ir jāizpilda daži priekšnosacījumu uzdevumi. Pēc tam varat izveidot mazumtirdzniecības veikalu un pievienot detalizētu informāciju.

### <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu iestatīt mazumtirdzniecības veikalu, jums ir jāizpilda tālāk uzskaitītie uzdevumi.

1.  Konfigurējiet savas organizācijas struktūru un iestatiet organizācijas hierarhijas mazumtirdzniecības preču klāstiem, papildināšanai un atskaišu veidošanai.
2.  Iestatiet noliktavu, kas pārstāv mazumtirdzniecības veikalu.
3.  Iestatiet numuru sērijas mazumtirdzniecības veikaliem, veikala pārskatiem un deklarācijas dokumentiem.
4.  Konfigurējiet mazumtirdzniecības parametrus.
5.  Iestatiet veikalam pieņemamas maksājumu metodes.
6.  Lai apstrādātu kredītkaršu transakcijas mazumtirdzniecības pārdošanas punkta (POS) kases sistēmās, varat iestatīt arī maksāšanas pakalpojumus.
7.  Iestatiet PVN grupas.
8.  Iestatiet mazumtirdzniecības preces. Kā daļu no šī uzdevuma varat arī iestatīt mazumtirdzniecības preču hierarhijas, preču variantus un preču klāstus.
9.  Iestatiet preču cenu grupas.
10. Iestatiet mazumtirdzniecības preču cenu noteikšanu. Kā daļu no šo uzdevuma varat iestatīt arī cenu korekcijas, atlaides un atlaižu periodus.
11. Iestatiet darbiniekus. **Piezīme.** Ir arī jāpiešķir darbiniekiem atbilstošas atļaujas, lai viņi varētu pierakstīties un izpildīt uzdevumus, izmantojot sistēmu Dynamics 365 for Retail for Retail POS.
12. Konfigurējiet Retail POS profilus, ko piešķirt veikalam. Šis uzdevums iekļauj daudzus citus uzdevumus, piemēram, kases sistēmu iestatīšanu, bezsaistes profilu iestatīšanu un kvīšu formātu un profilu iestatīšanu.

Pārskatiet visus priekšnosacījumā ietvertos uzdevumus un izpildiet tikai tos uzdevumus, kuri attiecas uz jums.

### <a name="set-up-a-retail-store"></a>Iestatīt mazumtirdzniecības veikalu

Pēc priekšnosacījumu uzdevumu izpildīšanas izpildiet tālāk uzskaitītos uzdevumus, lai iestatītu detalizētu informāciju par mazumtirdzniecības veikalu.

1.  Izveidojiet mazumtirdzniecības veikalu.
2.  Piešķiriet veikalam PVN grupu.
3.  Piešķiriet veikalam akceptētās maksājuma metodes.
4.  Pievienojiet detalizētu informāciju preču aprakstiem attiecībā uz precēm, kuras tiek piedāvātas jūsu mazumtirdzniecības veikalos. Piemēram, var pievienot bagātināto tekstu un attēlus. Šī detalizēta informācija par preci ir redzama dažādos kontekstos, piemēram, POS reģistrā vai drukātajās etiķetēs.
5.  Pievienojiet veikalu noklusējuma organizācijas hierarhijai, kura ir piešķirta nolūkiem **Mazumtirdzniecības preču klāsts**, **Mazumtirdzniecības papildināšana** vai **Mazumtirdzniecības atskaišu veidošana**.

### <a name="after-you-set-up-a-retail-store"></a>Pēc mazumtirdzniecības veikala iestatīšanas

Kad ir ievadīta detalizēta informācija par mazumtirdzniecības veikalu, izpildiet tālāk uzskaitītos uzdevumus, lai mazumtirdzniecības veikala datus nosūtītu uz Retail POS.

1.  Konfigurējiet veikala POS kases sistēmas.
2.  Pievienojiet veikalam preču klāstu.
3.  Apstrādājiet preču klāstu, lai ģenerētu to preču sarakstu, kuras tiek iekļautas klāstā, un padarītu preces pieejamas mazumtirdzniecības veikalā.
4.  Nosūtiet datus, piemēram, numuru sērijas, aparatūras profilus un POS ekrāna izkārtojumus, uz Retail POS reģistriem.
5.  Publicējiet mazumtirdzniecības veikalu, lai veikala datus nosūtītu uz Retail POS.
6.  Izpildiet darbus, lai veikala datus nosūtītu uz Retail POS.

## <a name="organization-hierarchies"></a>Organizācijas hierarhijas
Programmatūrā Dynamics 365 for Retail tiek izmantotas organizācijas hierarhijas, lai strukturētu mazumtirdzniecība kanālus. Organizācijas hierarhijas pārstāv attiecības starp organizācijām, kas veido jūsu uzņēmumu. Iestatot veikalus, varat tos pievienot organizācijas hierarhijai. Pēc tam veikali koplieto datus, kas tiek izmantoti preču klāstiem, papildināšanai un pārskatu veidošanai.




