---
title: Uzskaites sadales
description: Šajā rakstā ir sniegta informācija par sadalījumiem grāmatvedībā un aprakstītas pieejamās apstrādes iespējas.
author: sunfzam
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: twheeloc
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4330c86ee9ae35ce0f2c7bb85db533a39eafac46
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779586"
---
# <a name="accounting-distributions"></a>Uzskaites sadales

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par uzskaites sadalēm un aprakstītas opcijas, kas ir pieejamas to apstrādāšanai. Uzskaites sadales tiek izmantotas, lai pirmdokumenta naudas summas sadalītu konkrētos virsgrāmatas kontos. 

Uzskaites sadales ir programmā pieejama iespēja, kas tiek izmantota un paplašināta katram avota dokumentam, piemēram, pirkšanas pasūtījumam, kreditora rēķinam, izdevumu pārskatam un brīva teksta rēķinam. Pēc noklusējuma noklusētā uzskaites sadale tiek ģenerēta katrai avota pirmdokumenta rindai un naudas summai un tai ir iespējota modificēšana ar nosacījumiem. 

> [!NOTE] 
> Daži dokumenti atbalsta arī virsraksta dokumenta naudas summas, piemēram, pasūtījumu un rēķinu maksas. 

Vispārīgās uzskaites sadales iespējas nodrošina tālāk aprakstītās uzskaites sadales apstrādes opcijas.

-   **Sadalīt summas** — skatiet un modificējiet uzskaites sadales atsevišķam dokumenta virsrakstam vai rindai un jebkurai apakšrindai, piemēram, nodokļiem vai izmaksām.
    -   Augšējo naudas summu sadaļu (pamata sadales) galvenais konts un finanšu dimensijas var būt rediģējami tieši režģa segmentētajā vadīklā. Pilna cena ir tipisks šādas pamata sadales piemērs.
    -   Sadales summas tiek balstītas uz dokumenta valūtu. Parasti šī valūta ir transakcijas valūta. Uzskaites un pārskata valūtas summas tiek ģenerētas kā daļa no apakšgrāmatas uzskaites.
    -   Sadales parāda uzskaites datumu un uzskaites notikumu. Parasti uzskaites notikums ir iestatīts uz **Nav** līdz brīdim, kad dokuments tiek grāmatots/reģistrēts žurnālā. Šajā brīdī uzskaites notikums kļūst par **Sākotnējais**. Pēc tam, kad sadales tika grāmatotas, sadales nevar modificēt.
    -   Poga **Sadalīt** var būt iespējota pamata sadalēm. Izmantojot pogu **Sadalīt**, tiek ģenerētas jaunas uzskaites sadales. Sadales var tikt izteiktas kā procentuālā vērtība, summa vai daudzums.
    -   Pogu **Sadalīt vienādi** var izmantot kopā ar pogu **Sadalīt**, lai visās sadalēs automātiski sadalītu summu vienādās daļās.
    -   Poga **Atiestatīt** var būt iespējota pamata sadalēm, ja pastāv vairāk nekā viena sadale. Izmantojot pogu **Atiestatīt**, tiek anulētas manuāli veiktās sadales modifikācijas, dzēšot visas esošās sadales un atkārtoti ģenerējot noklusējuma sadales.
    -   Visas apakšsadales, piemēram, atlaides, maksa un PVN, vienmēr seko pēc pamata sadales. Pamata/bērna relāciju var skatīt sadaļā **Atsauce** &gt; **Pamatinformācija**.
    -   Galveno kontu un finanšu dimensiju var rediģēt arī bērna relācijai.
    -   Uzskaites sadales finanšu dimensijas seko noklusējuma modelim, ko dokuments var paplašināt.
    -   Novirzes sadales var tikt ģenerētas atbilstošos scenārijos, piemēram, kreditora rēķina un pirkšanas pasūtījuma atbilstības gadījumā. Atbilstības relācijas starp uzskaites sadali var skatīt sadaļā **Atsauce** &gt; **Dokumenta informācija**.
    -   Poga **Labot** parādās un ir iespējota dokumentiem, kas atbalsta labojumus. Komanda **Labot** izveido jaunas sadales. Vispirms tiek izveidotas sadales, kas atsauc sākotnējās sadales. Šīs sadales nevar modificēt. Pēc tam tiek izveidotas jaunas, pareizas uzskaites sadales. Šīs sadales var modificēt, ja var modificēt sākotnējās sadales.
    -   Poga **Detalizēta informācija par projektu** ir iespējota kā paplašinājums, ja rinda ir saistīta ar projektu. Projekta uzskaites sadales ļauj modificēt detalizētu informāciju, piemēram, finansējuma avotu un rindas rekvizītus.
    -   Pašreizējā dokumenta uzskaites statusu varat redzēt sadaļā **Atsauce**. Statuss ir visam dokumentam, un tas norāda, vai dokumenta apstrāde vēl notiek vai ir pabeigta.
-   **Skatīt sadales** – skatiet visu dokumenta rindu un naudas summu uzskaites sadales. No šī skata uzskaites sadales nevar modificēt.

Ir pievienots līdzeklis, kas validē grāmatvedības sadalījuma tabulu, lai nodrošinātu, ka jaunie lauki ir pareizi iestatīti. Šo līdzekli sauc **Iespējot papildu datu validēšanu dokumentiem, izmantojot pirmdokumenta uzskaites struktūru**. Šis līdzeklis pēc noklusējuma tika ieslēgts versijā 10.0.29. 

Papildinformāciju skatiet sadaļā [Uzskaites sadales un apakšgrāmatas žurnāla ieraksti kreditora rēķiniem](accounting-distributions-subledger-journal-entries-vendor-invoices.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
