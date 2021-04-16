---
title: Problēmu novēršana saistībā ar noliktavu partiju un sēriju rezervācijas hierarhijām
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu rezervāciju hierarhijām, kas izmanto partijas vai sēriju dimensijas.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: a1abb6f8657484d43d434076e5ee38d1c63fe2ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838182"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a>Problēmu novēršana saistībā ar noliktavu partiju un sēriju rezervācijas hierarhijām

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu rezervāciju hierarhijām, kas izmanto partijas vai sēriju dimensijas.

Papildu informāciju skatiet [Elastīga noliktavas līmeņa dimensijas rezervēšanas politika](flexible-warehouse-level-dimension-reservation.md).

Krājuma rezervāciju hierarhija nosaka noliktavas dimensiju vajadzību, kas ir jāizpilda, lai pieprasījuma pasūtījumam piešķirtu vietu. Šīs dimensijas var aprakstīt kā *dimensijas virs novietojuma*, visām dimensijām, kas jāizpilda pirms novietojuma piešķiršanas, un *dimensijām zem novietojuma*, dimensijām, ko var piešķirt pēc vietas piešķiršanas pieprasījuma pasūtījumam. Šīs rezervāciju hierarhijas tiek sauktas arī par *pakešuzdevumu, kas atrodas augstāk* un *atrodas zem* rezervāciju hierarhijām, vai arī rezervāciju hierarhijas, kas atrodas *augstāk par sēriju* un pārsniedz *sērijas numuru zem* rezervāciju hierarhijām.

Krājumus var sekmīgi sadalīt tikai tad, ja dimensijās virs novietojuma nav atstarpju. Piemēram, *paketē virs* rezervāciju hierarhijas jūs sagaidāt, ka pieprasījuma pasūtījumā tiks norādīta **Vieta**, **Noliktava** un **Partijas numura** dimensijas. Ja kāda no šīm dimensijām trūkst, sadalījuma process neizdosies. Pretēji, pakešveida rezervācijas hierarhijā, kas atrodas *zem paketes* vai *zem sērijas*, pieprasījuma pasūtījumā var norādīt paketes vai sērijas numuru, bet sadalījuma procesam tā nav nepieciešama.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Tiek parādīts šāds kļūdas ziņojums: "Jāpiešķir kopumam, noslodzes rindām ir jānorāda dimensijas virs novietojuma. Lai piešķirtu šīs dimensijas, rezervējiet un atkārtoti izveidojiet noslodzes rindu."

### <a name="issue-description"></a>Problēmas apraksts

Kad izmantojat krājumu, kam ir *partija virs* rezervāciju hierarhija (ar Partijas numura dimensiju, kas novietota virs Novietojuma dimensijas), **Izlaist uz noliktavu** komanda lapā **Kravas plānošanas rīks** daļējam daudzumam nestrādā. Šis kļūdas ziņojums tiek parādīts, un nav izveidots neviens darbs daļējam daudzumam.

Tomēr, ja izmantojat krājumu, kam ir *partija zem* rezervāciju hierarhija (ar Partijas numura dimensiju, kas novietota zem Novietojuma dimensijas), varat izlaist kravu no lapas **Kravas plānošanas rīks** daļējam daudzumam.

### <a name="issue-cause"></a>Izsniegšanas iemesls

Ja jūs ievietojat dimensiju virs **Novietojuma** dimensijas rezervāciju hierarhijā, tas ir jānorāda pirms izdošanas uz noliktavu. Daļējus daudzumus nevar izlaist, ja nav norādīta viena vai vairākas dimensijas virs **Novietojuma**.

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a>Partijas numura automātiskās rezervēšanas uzvedne tiek izraisīta pat tad, ja ir pieejami krājumi.

### <a name="issue-description"></a>Problēmas apraksts

Izmantojot krājumu, kam noliktavā nav iespējoti noliktavas procesi un ir iespējota automātiska rezervācija, rezervāciju hierarhiju *virs* rezervāciju hierarhijas, un ir iespējota automātiskā rezervācija, partijas numura automātiskās rezervēšanas uzvedne tiek parādīta pat tad, ja izdošanai ir pieejama tikai viena partija.

Tomēr, ja izmantojat to pašu krājumu noliktavā, kur ir iespējoti noliktavas procesi, netiek parādīta automātiskās rezervācijas uzvedne.

### <a name="issue-cause"></a>Izsniegšanas iemesls

Ja rezervāciju hierarhija ir definēta kā *virs* vai *pārsniedz sēriju*, atsauces dimensija (**Partijas numurs** vai **Sērijas numurs**) vienmēr jānorāda pieprasījuma pasūtījumos. Noliktavas procesi, iespējams, var pabeigt informāciju, ja ir pieejams viens paketes vai sērijas numurs. Tomēr, tā kā noliktava nav iespējota noliktavas procesiem, lietotājam vienmēr ir jānorāda visas dimensijas virs **Novietojuma**.

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a>Nišu veidnes, kuras izmanto rīcībā esošo nišas kritēriju, neuztēr pašreizējos rīcībā esošos krājumus partijas iespējotiem krājumiem.

Plašāku informāciju skatiet [Noliktavas niša](warehouse-slotting.md).

### <a name="issue-description"></a>Problēmas apraksts

Nišu veidnes, kurām ir *Rīcībā esošais nišas kritērijs*, neuztver pašreizējos rīcībā esošos krājumus *virs partijas* iespējotiem krājumiem. Viņi to apsver, ja partijas numurs ir norādīts pārdošanas pasūtījuma rindā.

Tomēr, ja izmantojat partijas krājumus, kas ir *zemāki par krājumiem*, pašreizējie rīcībā esošie krājumi tiek uzskatīti par paredzamiem.

### <a name="issue-cause"></a>Izsniegšanas iemesls

Slotēšanas veidnes virsrakstu var definēt stratēģijai *Pasūtīts*, *Rezervēts* vai *Nodots izpildei*. *Pasūtītā* pieprasījuma stratēģijai tiek lietotas tās pašas rezervāciju hierarhijas prasības, kas attiecas uz rezervācijas vai izlaišanas noliktavas procesiem. Tāpēc krājumiem, kuru pakešuzdevums atrodas *virs* un sērijas atrodas *zem* rezervāciju hierarhijām, pieprasījuma pasūtījumā (pārdošana vai pārsūtīšana) ir jānorāda paketes vai sērijas numurs. Alternatīvi *Rezervētā* pieprasījuma stratēģiju var izmantot, lai atlasītu partiju vai sērijas numuru pirms noliktavas pieprasījuma ģenerēšanas noliktavas slotā.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
