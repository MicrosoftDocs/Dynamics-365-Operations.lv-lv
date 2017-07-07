---
title: "Krājumu žurnāli"
description: "Šajā rakstā ir aprakstīts, kā lietot krājumu žurnālus, lai grāmatotu dažādu veidu fizisko krājumu transakcijas."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: fa629b4b8f7fcbd15ee89bc66cbc0bd7ca45215c
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017


---

# <a name="inventory-journals"></a>Krājumu žurnāli

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Šajā rakstā ir aprakstīts, kā lietot krājumu žurnālus, lai grāmatotu dažādu veidu fizisko krājumu transakcijas. 

Krājumu žurnāli programmatūrā Microsoft Dynamics 365 for Finance and Operations tiek izmantoti, lai grāmatotu dažādu veidu fizisko krājumu transakcijas, piemēram, izejas un ieejas plūsmu grāmatošanai, krājumu kustībām, materiālu komplektu (MK) izveidošanai un fizisko krājumu saskaņošanai. Visi šie krājumu žurnāli tiek izmantoti līdzīgā veidā, bet tie ir sadalīti dažādos tipos.

## <a name="types-of-inventory-journals"></a>Krājumu žurnālu tipi
Ir pieejami tālāk minētie krājumu žurnālu tipi.

-   Kustība
-   Krājumu korekcija
-   Pārcelšana
-   MK
-   Krājumu saņemšana
-   Ražošanas ievade
-   Uzskaite
-   Etiķešu skaitīšana

### <a name="movement"></a>Kustība

Kad lietojat krājumu kustības žurnālu, izmaksas krājumam varat pievienot, kad pievienojat inventāru, bet papildu izmaksas ir nepieciešams manuāli sadalīt uz noteiktu virsgrāmatas kontu, norādot virsgrāmatas korespondējošo kontu, kad veidojat šo žurnālu. Šis krājumu žurnālu tips ir noderīgs, ja kādam krājumam izdevumus vēlaties saskaņot pret citu nodaļu vai ja krājumus vēlaties noņemt no inventāra izdevumu nolūkos.

### <a name="inventory-adjustment"></a>Krājumu korekcija

Ja izmantojat krājuma korekciju žurnālu, izmaksas krājumam varat pievienot, kad pievienojot inventāru. Papildu izmaksas tiek automātiski grāmatota uz noteiktu virsgrāmatas kontu, pamatojoties uz iestatījumiem krājumu grupas grāmatošanas metodē. Izmantojiet šo krājumu žurnālu tipu, lai atjauninātu peļņas un zaudējumus uz krājumu daudzumiem, kad krājumam ir jāsaglabā tā noklusējuma virsgrāmatas korespondējošais konts. Kad grāmatojat krājumu korekciju žurnālu, tiek iegrāmatota krājumu ieejas plūsma vai izejas plūsma, krājuma vērtības tiek mainītas un tiek izveidotas virsgrāmatas transakcijas.

### <a name="transfer"></a>Pārcelšana

Pārsūtīšanas žurnālus varat lietot, lai pārsūtītu krājumus starp dimensiju novietojumiem, partijām vai preču variantiem, nepiesaistot nekādas izmaksu saistības. Piemēram, varat pārsūtīt krājumus no vienas noliktavas uz citu noliktavu viena un tā paša uzņēmuma ietvaros. Ja izmantojat pārsūtīšanas žurnālu, jums ir jānorāda gan “no”, gan “uz” krājumu dimensijas (piemēram, vietai un noliktavai). Rīcībā esošie krājumi pēc definētajām krājuma dimensijām tiek atbilstoši mainīgi. Krājumu pārsūtīšanas atspoguļo tūlītējo materiāla kustību. Tranzītā esošais inventārs netiek izsekots. Ja tranzītā esošo inventāru nepieciešams izsekot, tā vietā ir jāizmanto pārsūtīšanas pasūtījums. Grāmatojot pārsūtīšanas žurnālu, katrai žurnāla rindai tiek izveidotas divas krājumu transakcijas:

-   Krājuma izejas plūsma atrašanās vieta “no”
-   Krājuma ieejas plūsma atrašanās vieta “uz”

### <a name="bom"></a>MK

Kad reģistrējat MK pabeigšanu, varat izveidot MK žurnālu. Lietojot MK žurnālu, varat grāmatot tieši MK. Šī grāmatošana izveido preces krājumu ieejas plūsmu kopā ar saistīto MK un MK iekļauto preču krājumu izejas plūsmu. Šis krājumu žurnālu tips noder vienkāršos vai liela apjoma ražošanas scenārijos, kur maršruti nav nepieciešami.

### <a name="item-arrival"></a>Krājumu saņemšana

Krājumu saņemšanas žurnālu varat izmantot, lai reģistrētu krājumu ieejas plūsmu (piemēram, no pirkšanas pasūtījumiem). Krājumu saņemšanas žurnālu var veidot kā daļu no saņemšanas pārvaldības lapā **Saņemšanas darbību apskats**, vai žurnāla ierakstu varat manuāli izveidot no lapas **Krājumu saņemšana**. Ja iespējojat krājumu saņemšanas žurnāla nosaukumu, lai pārbaudītu izdošanas vietas, tad Finance and Operations meklē novietojumu saņemtajiem krājumiem, un, ja ir vieta, ģenerē novietojuma mērķus ienākošajiem krājumiem.

### <a name="production-input"></a>Ražošanas ievade

Ražošanas ievades žurnāli darbojas kā krājumu saņemšanas žurnāli, bet tiek izmantoti ražošanas pasūtījumiem.

### <a name="counting"></a>Uzskaite

Inventarizācijas žurnāli jums ļauj labot pašreizējos rīcībā esošos krājumus, kas ir reģistrēti krājumiem vai krājumu grupām, un tad grāmatot faktisko fizisko skaitu, tādējādi varat veikt atšķirību saskaņošanai nepieciešamos pielāgojumus. Inventarizācijas politikas varat saistīt ar inventarizācijas grupām, lai palīdzētu grupēt krājumus, kuriem ir dažādas īpašības un šos krājumus varētu iekļaut inventarizācijas žurnālā. Piemēram, varat iestatīt inventarizācijas grupas, lai saskaitītu krājumus, kuriem ir specifisks biežums, vai lai saskaitītu krājumus, ja krājumu daudzums nokrītas līdz noteiktam līmenim. Informāciju par to, kā definēt inventarizācijas grupas, skatiet tēmā [Krājumu inventarizācijas procesu definēšana (uzdevuma ceļvedis)](http://ax.help.dynamics.com/en/wiki/define-inventory-counting-processes/).

### <a name="tag-counting"></a>Etiķešu skaitīšana

Etiķešu inventarizācijas žurnāli tiek izmantoti, lai uzskaites laidienam piešķirtu numurētu etiķeti. Etiķetēs ir jāietver etiķetes numurs, krājuma kods un krājuma daudzums. Lai palīdzētu nodrošināt, ka etiķete tiek lietota tikai vienu reizi un tiek izmantotas visas etiķetes, katram krājuma kodam ir nepieciešama unikāla etiķešu kopa, kam ir pašai sava numuru sērija. Katrai etiķetei var iestatīt trīs statusa vērtības:

-   **Izmantots** — šai etiķetei krājuma kods ir uzskaitīts.
-   **Anulēts** — šai etiķetei krājuma kods ir anulēts.
-   **Trūkst** — šai etiķetei trūkst krājuma koda.

Kad grāmatojat etiķešu inventarizācijas žurnālu, tiek izveidots jauns inventarizācijas žurnāls, pamatojoties uz etiķešu inventarizācijas žurnāla rindām. Plašāku informāciju par etiķešu inventarizāciju skatiet rakstā [Krājumu etiķešu inventarizācija](inventory-tag-counting.md).

## <a name="working-with-journals"></a>Darbs ar žurnāliem
Žurnālam vienlaicīgi var piekļūt tikai viens lietotājs. Ja vairākiem lietotājiem vienlaicīgi jāpiekļūst žurnāliem, lai izveidotu žurnāla rindas, šiem lietotājiem ir jāatlasa žurnāli, kas pašlaik netiek lietoti, lai novērstu informācijas pārrakstīšanu. Situācijās, kur vairākas nodaļas izmantot to pašu žurnāla tipu, ir noderīgi izveidot vairākus žurnālu nosaukumus (piemēram, vienu katrai nodaļai). Var būt arī noderīgi žurnālus sadalīt tā, lai katrs kārtējais grāmatojums tiktu ievadīts savā unikālajā krājumu žurnālā. Kārtējiem grāmatojumiem, kas saistīti ar krājumu darbībām, izveidojiet vienu žurnālu periodiskajiem krājumu pielāgojumiem un citu — krājumu inventarizācijai.

## <a name="posting-journal-lines"></a>Žurnāla rindu grāmatošana
Savas izveidotās žurnāla rindas varat grāmatot jebkurā laikā līdz brīdim, kad krājumu esat bloķējis no papildu transakcijām. Žurnālā ievadītie dati paliek šajā žurnālā pat tad, ja žurnālu aizverat, negrāmatojot rindas.




