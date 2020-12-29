---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 10. septembris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent — Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: ff5d21a8a71b068a276bedaf6e4b9964adcb4027
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461915"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-10-2018"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 10. septembris)

**8.1.138.0 būvējums**

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent: Core HR.

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>Noteikta darba dienas laika izmantošana brīvā laika pieprasījumos (nepilna darba diena)

Ja atvaļinājuma un prombūtnes iestatījumi ir iestatīti tā, ka brīvai laika pieprasījumā tiek norādīts dienu skaits, tagad var aktivizēt arī nepilnas darba dienas definīciju. Pēc tam, iesniedzot brīva laika pieprasījumus, lietotāji var norādīt, vai viņi pieprasa brīvu pirmo vai otro darba dienas daļu.

Šī opcija pēc noklusējuma ir izslēgta. Lai darbinieki varētu pieprasīt brīvu pirmo vai otro darba dienas daļu, šī opcija ir jāaktivizē personāla vadības parametru apgabalā **Atvaļinājums un prombūtne**.

Šī līdzekļa drošības privilēģija ir uzturēt personāla vadības parametrus.

## <a name="validation-of-leave-and-absence-entries"></a>Atvaļinājumu un prombūtnes ierakstu apstiprināšana

Atkarībā no atvaļinājumu konfigurācijas veida darbiniekiem, kuri mēģina iesniegt brīvā laika pieprasījumu, kas pārsniedz to darba dienas ilgumu, tiek parādīts brīdinājuma ziņojums. Tas nozīmē, ka viņi tiek brīdināti, ja viņi jebkurā datumā mēģina pieprasīt brīvu vairāk nekā pilnu darba dienu.

Šī validācijas opcija vienmēr ir ieslēgta. Ikreiz, kad darbinieki pārsniedz darba dienas definēto robežvērtību, viņu brīvā laika pieprasījumā tiek parādīts brīdinājums.

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>Nosacījuma pārskatu papildu lauki darbplūsmās

Programmā Core HR vairākās darbplūsmās nosacījuma pārskatiem ir pievienoti papildu lauki un vietturi.

Tālāk norādītie lauki ir pievienoti kompensācijas, darba attiecību izbeigšanas un pārcelšanas darbplūsmās.

- Nodarbinātības veids
- Juridiska persona
- Koriģētais nodarbinātā pieņemšanas darbā datums
- Darba devēja paziņotā summa
- Darba devēja paziņojuma vienība
- Pārejas datums
- Nodarbinātajam paziņotā summa
- Nodarbinātā pieņemšanas darbā datums
- Nodarbinātā paziņojuma vienība
- Pārbaudes laika beigu datums
- Pozīcija
- Vienība
- Nodaļa
- Amata veids
- Uzņēmuma atrašanās vieta
- Amats
- Amats
- Darba veids
- Darbu grupa
- Darba funkcija

Tālāk norādītie lauki ir pievienoti amata darbplūsmai.

- Pozīcija
- Vienība
- Nodaļa
- Amata veids
- Uzņēmuma atrašanās vieta
- Amats
- Amats
- Darba veids
- Darbu grupa
- Darba funkcija

Nosacījuma pārskatu lauki un vietturi ir pieejami visiem lietotājiem, kuriem ir piekļuves tiesības konfigurēt iepriekš norādītās darbplūsmas.

## <a name="navigation-to-attract-from-personnel-management"></a>Pāriešana uz Attract no personāla vadības lapas

Ja ir iestatīts līdzeklis Attract, lietotājiem personāla vadības lapā **Darbā pieņemamie kandidāti** tiek parādīta norāde sākt ar Attract un netiek rādīts ziņojums “Mēs neatradām neko, ko šeit rādīt”.

## <a name="other-changes"></a>Cita izmaiņas

Šis laidiens ietver vairākus papildu kļūdu labojumus.

- Pieņemot darbā līgumdarbinieku, cilnei **Kompensācija** pieprasījumu/darbību lapā nav jābūt pieejamai.
- Pieprasījuma par darba attiecību pārtraukšanu procesu var turpināt tikai tad, kad visos pieprasītajos laukos ir ievadīti dati.
- Ir novērstas kārtošanas secības un datumu parādīšanas problēmas personāla vadības analīzē.
