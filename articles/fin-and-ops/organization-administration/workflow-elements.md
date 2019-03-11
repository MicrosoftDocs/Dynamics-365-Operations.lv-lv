---
title: Darbplūsmas elementi
description: Šajā tēmā ir aprakstīti dažādie elementi, kas veido darbplūsmu.
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 48fa9613b37fceeda1ea73c5fd5d4f7a7edc74cf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "333810"
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

![Darbplūsma ar rindas elementiem](./media/workflow_lineitemworkflow.gif)

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
