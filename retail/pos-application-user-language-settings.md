---
title: "POS programma un lietotāja valodas iestatījumi"
description: "Šajā tēmā ir aprakstīts, kā mainīt valodas iestatījumus mazumtirdzniecības mūsdienu POS (MPOS) un mākonis POS."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf5b75572529bb497d3079752de187f30aa59294
ms.lasthandoff: 03/31/2017


---

# <a name="pos-application-and-user-language-settings"></a>POS programma un lietotāja valodas iestatījumi

Šajā tēmā ir aprakstīts, kā mainīt valodas iestatījumus mazumtirdzniecības mūsdienu POS (MPOS) un mākonis POS.

<a name="overview"></a>Pārskats
========

Mazumtirdzniecība modernas POS (MPOS) un mākonis POS atbalsta vidēs, ja valodas iestatījumi un tulkojumus var svārstīties starp veikalu un lietotāja iestatījumus. Piemēram, veikalā varēja atrodas reģionā, kur latviešu valoda ir visizplatītākā saviem klientiem, bet daži darbinieki labprāt izmanto pieteikumu ar franču valodas tulkojumi.

## <a name="data-language"></a>Datu valoda
Neatkarīgi no lietotāja iestatījumiem MPOS un mākonis POS vienmēr izmantos veikala valodu iestatījumi noteikt tulkojumi lietot attiecībā uz datiem. Tas nodrošinās, ka visiem lietotājiem un klientiem būs atbilstošu pieredzi.  Datu piemēri:

-   Preces
-   Atribūti un vērtības
-   Kategoriju nosaukumi
-   Drukātas vai e-pastā sūtītas transakciju kvītis
-   Maksāšanas metožu nosaukumi
-   Rindu displeja ziņojumi

Veikala valoda tiks izmantota arī galveno POS pieteikšanās ekrānu, jo lietotājs nav zināms pirms pieteikšanās. Ja tulkojums nav pieejams veikala valodai, POS atgriezīsies pie uzņēmuma valodu.

### <a name="configuring-the-stores-language-setting"></a>Veikala valodas iestatījumu konfigurēšana

Veikala valodas iestatījums ir no **visiem mazumtirdzniecības veikalos** par **mazumtirdzniecības veikalu** lapa zem * * vispārējā &gt;reģionālos iestatījumus &gt;valodu. * * Izmantot kritums noteikti izvēlēties valodu, katrā noliktavā.

## <a name="user-interface-language"></a>Lietotāja interfeisa valoda
POS lietotāja valodas iestatījums nosaka tulkojumiem izmantotas lietojumprogrammu lietotāja interfeisā. Tas ietver visu etiķetēm, izvēlnes un sarakstus, kas nav uzskatāmi par datu. Vienīgais izņēmums ir teksts, kas tiek parādīts uz pogas grids POS. Pogas grids neatbalsta tulkojumi, tāpēc viņi vienmēr rādīt tekstu, kā noteikts uz pogas. Lai atbalstītu tulkoto pogu, jums nāksies kopēt un saglabāt atsevišķu pogu režģus un tos piesaistīt lietotājiem pēc vajadzības.

### <a name="configuring-the-users-language-setting"></a>Lietotāja valodas iestatījumu konfigurēšana

POS lietotāja valodas iestatījums ir no **visiem darba ņēmējiem** par **darbinieku** lapa zem **mazumtirdzniecības &gt;valodas**.  Tas nav iestatīts profils galvenajā cilnē.  Šo iestatījumu izmanto, POS. Ja lietotāja valoda nav iestatīta vai tā ir iestatīta uz valodu, kurā tulkojumi nav pieejami, POS atgriezīsies pie veikala valodas.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **Lietotāja interfeisa valodu** * * * *      | **Datu valoda (preces, kvīšu formāti, rindu displejs utt.)** |
| **Uzņēmums** | Noklusējums                    | Noklusējums                                                           |
| **Veikals**   | Ignorē uzņēmumu          | Ignorē uzņēmumu                                                 |
| **User**    | Ignorē veikalu vai uzņēmumu | Nekad                                                             |




