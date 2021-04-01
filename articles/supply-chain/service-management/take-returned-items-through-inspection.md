---
title: Atgriezto krājumu pārbaudes veikšana
description: Veiciet atgriezto krājumu pārbaudi.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f30937eb44893a3cb3587d072b685a855b0ecd3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224910"
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