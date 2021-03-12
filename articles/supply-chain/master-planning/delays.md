---
title: Aizkaves
description: Šajā tēmā ir sniegta informācija par aizkavēšanās datumiem vispārējā plānošanā. Aizkavēšanās datums ir reālistisks izpildes datums, kuru transakcija saņem, ja vispārējās plānošanas aprēķinātais drīzākais izpildes datums ir vēlāks par pieprasīto datumu.
author: roxanadiaconu
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dcb11b3665c5d2f296f1ba2ce4708c4eff241b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977992"
---
# <a name="delays"></a>Aizkaves

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par aizkavēšanās datumiem vispārējā plānošanā. Aizkavēšanās datums ir reālistisks izpildes datums, kuru transakcija saņem, ja vispārējās plānošanas aprēķinātais drīzākais izpildes datums ir vēlāks par pieprasīto datumu.

Veicot vispārējo plānošanu, var aprēķināt agrāko transakcijas izpildes datumu, pamatojoties uz izpildes laikiem, materiālu pieejamību, noslodzes pieejamību un dažādiem plānošanas parametriem. 

Ja vispārējā plānošana aprēķina pasūtījuma datumu, kas ir pirms pašreizējā datuma, pasūtījumu nevar izpildīt savlaicīgi. Tāpēc pasūtījuma izpilde aizkavējas. Šajā gadījumā vispārējās plānošanas tiek veikta uz priekšu — pasūtījums tiek ieplānots ar pašreizējo datumu, un tiek iekļauti izpildes laiki. Šie izpildes laikus sākas ar jebkuru zemāka līmeņa komponentu. Pēc tam pasūtījums saņem aizkaves datumu. Aizkaves datums ir faktiskais apmaksas datums, kas pamatots uz pašreizējiem datiem. Vispārējā plānošana aprēķina arī aizkaves dienu skaitu. 

Dažās situācijās varat izvēlēties neaprēķināt aizkaves, piemēram, ja lietotāji zina, ka viņi var paātrināt izpildes laikus, atlasot alternatīvu piegādes veidu. 

Var konfigurēt, kā aizkavēšanās tiek aprēķinātas seguma grupai. Seguma grupu krājumam var pievienot vēlāk. 

Lapā **Vispārējās plānošanas parametri** var iestatīt sākuma laiku aprēķina kavējumiem. Ja pasūtījums tiek izpildīts pēc šī laika, vienas dienas aizkave tiek pievienota pasūtījuma aiskaves datumam. 

> [!NOTE]
> Iepriekšējās versijās aprēķinātās aizkaves tika sauktas par *aizkavēšanās paziņojumiem*, aizkaves datums tika saukts par *aizkavēšanās datumu* un aizkavētā transakcija tika saukta par *transakciju, kas tika aizkavēta*.

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a>Ierobežota ražošanas iestatījuma aizkave ar vairākiem MK līmeņiem
Strādājot ar kavēšanos ražošanas iestatījumā, kam ir vairāki MK līmeņi, ir svarīgi atzīmēt, ka tikai tie krājumi, kas atrodas tieši virs krājuma (MK struktūrā), kas izraisa kavēšanos, tiks atjaunināti ar kavēšanos kā daļa no vispārējās plānošanas izpildes. Citi krājumi MK struktūrā netiks lietoti līdz pirmajai vispārējai plānošanai, kad plānotais pasūtījums augstākajam līmenim ir apstiprināts. 

Lai apietu šo zināmo ierobežojumu, ražošanas pasūtījumus MK struktūras virspusē ar kavējumiem var apstiprināt pirms nākamās vispārējās plānošanas izpildes. Šādā veidā aizkave no aizkavētā, apstiprinātā, plānotā ražošanas pasūtījuma tiks paturēta, un visi pakārtotie komponenti tiks attiecīgi atjaunināti.
Darbības ziņojumus var arī izmantot, lai noteiktu plānotos pasūtījumus, ko var pārlikt uz vēlāku datumu citu kavējumu MK struktūrā dēļ.

## <a name="desired-date"></a>Vēlamais datums

Lapas **Plānotais pasūtījums** cilnē **Aizkaves** ir pieejams plānotā pasūtījuma **Vēlamais datums**. Plānotā pasūtījuma vēlamais datums ir aizkavju bāzes datums, un tas ir aprēķināts datums, kas ir vienāds ar vērtību **Pieprasītais datums**, kura aprēķināta, balstoties uz parametriem **Neto prasības**. Ja plānotais pasūtījums ir MK rinda, ražošanas rinda vai Kanban rinda, vēlamais datums balstās uz vērtību **Vajadzības datums**, un vēlamais datums netiks rādīts lapā **Plānotais pasūtījums**.

<a name="additional-resources"></a>Papildu resursi
--------

[Seguma iestatījumi](coverage-settings.md)
