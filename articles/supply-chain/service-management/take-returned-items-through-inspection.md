---
title: Atgriezto krājumu pārbaudes veikšana
description: Veiciet atgriezto krājumu pārbaudi.
author: sorenva
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41214663ec48a8cbcd8bec7f6801adb4311b2373
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669941"
---
# <a name="take-returned-items-through-inspection"></a>Atgriezto krājumu pārbaudes veikšana 

[!include [banner](../includes/banner.md)]


1.  Noklikšķiniet uz **Krājumu pārvaldība** \> **Periodiskās darbības** \> **Kvalitātes pārvaldība** \> **Karantīnas pasūtījumi**.

2.  Izvietojiet pasūtījuma rindu, kas atbilsts atgrieztajam krājumam, kurš tiek pārbaudīts.

    > [!NOTE]
    > <P>Karantīnas pasūtījumu var saistīt tikai ar vienu krājuma numuru. Ja 10 krājumi ar dažādiem krājumu numuriem tiek atgriezti vienā sūtījumā un nosūtīti uz karantīnu, tiek izveidoti 10 atsevišķi karantīnas pasūtījumi.</P>

3.  Pēc krājuma pārbaudīšanas ir jāveic atzīme laukā **Atgriešanas metodes kods**, lai norādītu, kas ir jādara ar šo vienību un kā ir jāapstrādā saistītā finanšu transakcija. Piemēri iekļauj vienības atgriešanu noliktavā un naudas atgriešanu klientam, vienības brāķēšanu un jaunas nosūtīšanu klientam vai arī vienības atgriešanu klientam bez jebkāda kredīta.
    
    > [!NOTE]
    > <P>Ja vairākām atgrieztajām vienībām vienas vienības numura paketē nevar piešķirt to pašu atgriešanas metodes kodu, karantīnas pasūtījums ir jāsadala (<STRONG>Funkcijas</STRONG> &gt; <STRONG>Sadalīt</STRONG>), lai katrai apakšpaketei piešķirtu citu atgriešanas metodes kodu.</P>


4.  Kad pārbaude ir pabeigta, noklikšķiniet uz **Ziņot kā pabeigtu**, lai izlaistu atgrieztās vienības un izveidotu vienību saņemšanas žurnāla ierakstu. Darbinieks vai nodaļa, kas saņēmusi krājumus, tad veic žurnāla apstrādi, lai atgrieztu krājumus inventārā.
    
    –vai–
    
    Pabeidziet karantīnas pasūtījumu un pārvietojiet vienības atpakaļ uz krājumiem tiešā veidā, izmantojot vienu no funkcijām **Krājumi**.

5.  Aizveriet formu, lai saglabātu izmaiņas.

## <a name="see-also"></a>Skatiet arī

[Noteikšana, kā atbrīvoties no atgrieztiem krājumiem](specify-how-to-dispose-of-returned-items.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]