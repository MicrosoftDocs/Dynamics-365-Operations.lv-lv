---
title: Aizkaves
description: Šajā tēmā ir sniegta informācija par aizkavēšanās datumiem vispārējā plānošanā. Aizkavēšanās datums ir reālistisks izpildes datums, kuru transakcija saņem, ja vispārējās plānošanas aprēķinātais drīzākais izpildes datums ir vēlāks par pieprasīto datumu.
author: roxanadiaconu
manager: AnnBe
ms.date: 03/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1a8c738fffda76f2a8492c20e2c67a154c68559
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1522293"
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

## <a name="desired-date"></a>Vēlamais datums

Lapas **Plānotais pasūtījums** cilnē **Aizkaves** ir pieejams plānotā pasūtījuma **Vēlamais datums**. Plānotā pasūtījuma vēlamais datums ir aizkavju bāzes datums, un tas ir aprēķināts datums, kas ir vienāds ar vērtību **Pieprasītais datums**, kura aprēķināta, balstoties uz parametriem **Neto prasības**. Ja plānotais pasūtījums ir MK rinda, ražošanas rinda vai Kanban rinda, vēlamais datums balstās uz vērtību **Vajadzības datums**, un vēlamais datums netiks rādīts lapā **Plānotais pasūtījums**.

<a name="additional-resources"></a>Papildu resursi
--------

[Seguma iestatījumi](coverage-settings.md)
