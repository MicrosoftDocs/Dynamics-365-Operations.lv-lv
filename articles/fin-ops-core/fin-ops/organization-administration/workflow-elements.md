---
title: Darbplūsmas elementi
description: Šajā tēmā ir aprakstīti dažādie elementi, kas veido darbplūsmu.
author: ChrisGarty
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2de1f9f3f1785236f9761dd865d9a5500ab044752077cc42a7e0da9df175f2a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749342"
---
# <a name="workflow-elements"></a>Darbplūsmas elementi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti dažādie elementi, kas veido darbplūsmu.

Darbplūsma sastāv no elementiem. Turpmākajās sadaļās ir aprakstīts katrs elementa veids.

## <a name="tasks"></a>Uzdevumi

*Uzdevums* ir darba vienība, kas ir jāveic. Darbplūsmai var pievienot divu viedu uzdevumus: manuālos uzdevumus un automatizētos uzdevumus.

### <a name="manual-task"></a>Manuāls uzdevums

*Manuāls uzdevums* ir darba vienība, kas ir jāveic lietotājam. Piemēram, izdevumu pārskata darbplūsma var būt manuāls uzdevums, kura ietvaros norīkotajam lietotājam ir jāveic tālāk norādītās darbības.

- Jāpārskata kopā ar izdevumu pārskatu iesniegtie čeki.
- Jāzvana darbinieka vadītājam.

### <a name="automated-task"></a>Automatizēts uzdevums

*Automatizēts uzdevums* ir darba vienība, kas ir jāveic sistēmai. Darbiniekam nekas nav jādara. Piemēram,pārdošanas pasūtījuma darbplūsma var būt automatizēts uzdevums, kura ietvaros sistēmai ir jāveic tālāk norādītās darbības.

- Jāveic kredīta pārbaude.
- Jāizveido debitora ieraksts, ja tāda vēl nav.

## <a name="approval-processes"></a>Apstiprināšanas procesi

*Apstiprināšanas process* ir process, kas sastāv no atsevišķiem soļiem. Katrā apstiprināšanas solī lietotājs var veikt tālāk norādītās darbības.

- Apstiprināt dokumentu.
- Noraidīt dokumentu.
- Pieprasīt dokumenta izmaiņas.
- Piešķirt dokumentu apstiprināšanai citam lietotājam.

## <a name="line-item-workflow-elements"></a>Dokumenta rindas darbplūsmas elementi

Var izveidot darbplūsmu dokumentu vai dokumenta rindu apstrādei. Pieņemsim, ka esat izveidojis darba laika uzskaites tabulas apstiprinājuma darbplūsmu. (Šī darbplūsma tiks saukta par *dokumenta darbplūsmu*.) Varat pievienot šai dokumenta darbplūsmai *rindas vienuma darbplūsmas* elementu. Izpildot rindas vienuma elementu, apstrādei tiek nodots katras dokumenta rindas vienums. Iespējams, vēlaties, lai visu rindu vienumu apstrādei tiktu izmantota viena dokumenta rindu darbplūsma, vai arī, iespējams, vēlaties, lai katra rindas vienuma apstrādei tiktu izmantota atšķirīga dokumenta rindas darbplūsma. Iedomājieties, ka darbinieks ir iesniedzis darba laika uzskaites tabulu, kas līdzinās tālāk esošajā attēlā redzamajai.

![Darbplūsma ar rindas elementiem.](./media/workflow_lineitemworkflow.gif)

Šādā scenārijā, iespējams, vēlaties izveidot tālāk norādītās dokumenta rindas darbplūsmas.

- **1. dokumenta rindas darbplūsma** — šī darbplūsma tiek izmantota to rindas vienumu apstrādei, kuru projekta ID ir 1111.
- **2. dokumenta rindas darbplūsma** — šī darbplūsma tiek izmantota to rindas vienumu apstrādei, kuru projekta ID ir 2222.
- **3. dokumenta rindas darbplūsma** — šī darbplūsma tiek izmantota to rindas vienumu apstrādei, kuru projekta ID ir 3333.

## <a name="flow-control-elements"></a>Plūsmas kontroles elementi

Tālāk norādītie elementi ļauj izveidot darbplūsmas ar alternatīviem atzariem vai atzariem, kas tiek izpildītie vienlaikus.

### <a name="manual-decision"></a>Manuāls lēmums

*Manuāls lēmums* ir punkts, kur darbplūsma sadalās divos atzaros. Lietotājam ir jāpieņem lēmums, un šis lēmums nosaka, kurš atzars tiek izmantots iesniegtā dokumenta apstrādei.

### <a name="conditional-decision"></a>Nosacījuma lēmums

*Nosacījuma lēmums* arī ir punkts, kur darbplūsma sadalās divos atzaros. Taču to, kurš atzars ir jāizmanto iesniegtā dokumenta apstrādei, izvēlas sistēma. Lai pieņemtu šo lēmumu, sistēma novērtē dokumentu un nosaka, vai tas atbilst norādītajiem nosacījumiem.

### <a name="parallel-activity"></a>Paralēla aktivitāte

*Paralēla aktivitāte* ir darbplūsmas elements, kas satur divus vai vairāk darbplūsmas atzaru, kas tiek izpildīti vienlaikus.

### <a name="subworkflow"></a>Pakārtotā darbplūsma

*Pakārtotā darbplūsma* ir darbplūsma, kas darbojas citas darbplūsmas kontekstā.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]