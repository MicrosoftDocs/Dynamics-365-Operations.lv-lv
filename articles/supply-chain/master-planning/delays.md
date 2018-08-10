---
title: Aizkaves
description: "Šajā rakstā ir sniegta informācija par aizkavēšanās datumiem vispārējā plānošanā. Aizkavēšanās datums ir reālistisks izpildes datums, kuru transakcija saņem, ja vispārējās plānošanas aprēķinātais drīzākais izpildes datums ir vēlāks par pieprasīto datumu."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fed78a7eba16d286a81b1e9ad709142422298c91
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="delays"></a>Aizkaves

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par aizkavēšanās datumiem vispārējā plānošanā. Aizkavēšanās datums ir reālistisks izpildes datums, kuru transakcija saņem, ja vispārējās plānošanas aprēķinātais drīzākais izpildes datums ir vēlāks par pieprasīto datumu.

Veicot vispārējo plānošanu, var aprēķināt agrāko transakcijas izpildes datumu, pamatojoties uz izpildes laikiem, materiālu pieejamību, noslodzes pieejamību un dažādiem plānošanas parametriem. 

Ja vispārējā plānošana aprēķina pasūtījuma datumu, kas ir pirms pašreizējā datuma, pasūtījumu nevar izpildīt savlaicīgi. Tāpēc pasūtījuma izpilde aizkavējas. Šajā gadījumā vispārējās plānošanas tiek veikta uz priekšu — pasūtījums tiek ieplānots ar pašreizējo datumu, un tiek iekļauti izpildes laiki. Šie izpildes laikus sākas ar jebkuru zemāka līmeņa komponentu. Pēc tam pasūtījums saņem aizkaves datumu. Aizkaves datums ir faktiskais apmaksas datums, kas pamatots uz pašreizējiem datiem. Vispārējā plānošana aprēķina arī aizkaves dienu skaitu. 

Dažās situācijās varat izvēlēties neaprēķināt aizkaves, piemēram, ja lietotāji zina, ka viņi var paātrināt izpildes laikus, atlasot alternatīvu piegādes veidu. 

Var konfigurēt, kā aizkavēšanās tiek aprēķinātas seguma grupai. Seguma grupu krājumam var pievienot vēlāk. 

Lapā **Vispārējās plānošanas parametri** var iestatīt sākuma laiku aprēķina kavējumiem. Ja pasūtījums tiek izpildīts pēc šī laika, vienas dienas aizkave tiek pievienota pasūtījuma aiskaves datumam. 

**Piezīme.** Iepriekšējās versijās aprēķinātās aizkaves tika sauktas par *aizkavēšanās paziņojumiem*, aizkaves datums tika saukts par *aizkavēšanās datumu* un aizkavētā transakcija tika saukta par *transakciju, kas tika aizkavēta*.

<a name="additional-resources"></a>Papildu resursi
--------

[Vajadzības iestatījumi](coverage-settings.md)




