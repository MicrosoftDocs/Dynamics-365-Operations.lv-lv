---
title: Darbvieta Datu validēšanas kontrolsaraksts
description: Darbvieta Datu validēšanas kontrolsaraksts sniedz iespēju sekot datu validēšanas procesam vairākos uzņēmumos un jomās un saistībā ar vairākām personām.
author: bking
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DataValidationWorkspace
audience: Application User
ms.reviewer: rhaertle
ms.assetid: ''
ms.search.region: Global
ms.author: bking
ms.openlocfilehash: 96385f94ac8e3f3d16924c079af0d6d258d5ec39
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752644"
---
# <a name="data-validation-checklist-workspace"></a>Datu validēšanas kontrolsaraksta darbvieta

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts pārskats par darbvietu **Datu validēšanas kontrolsaraksts** un saistīto konfigurāciju.

Darbvieta **Datu validēšanas kontrolsaraksts** sniedz iespēju sekot datu validēšanas procesam vairākos uzņēmumos un jomās un saistībā ar vairākām personām. Kontrolsarakstu var izmantot jaunas implementēšanas laikā, pēc jaunināšanas vai pēc migrācijas. Atkarībā no skata darbvietā **Datu validēšanas kontrolsaraksts** jums tiek rādīti visi datu pārbaudes projekta uzdevumi un statusi vai tikai jums piešķirtie uzdevumi.

Vispirms darbvietas augšpusē ir jāatlasa datu validēšanas projekts. Pēc tam visi darbvietā rādītie dati tiek filtrēti atbilstoši atlasītajam datu validēšanas projektam.

## <a name="summary-tiles"></a>Kopsavilkuma elementi

Elementi **Kopsavilkums** sniedz apskatu par procesu, un indikatori palīdz sekot līdzi datu validēšanas procesam. Tiek rādīti visi procesa atlikušie uzdevumi, pabeigtie uzdevumi, uzdevumi, kuru izpilde vēl notiek, un nesāktie uzdevumi. Šī informācija tiek sniegta par visiem uzņēmumiem, kas ir ietverti atlasītajā datu validēšanas projektā.

## <a name="tasks-and-status-section"></a>Uzdevumu un statusa sadaļā

Sadaļā **Uzdevumi un statuss** dažādos veidos tiek rādīts kopējā datu validēšanas projekta statuss: pēc juridiskās personas, pēc jomas un pēc uzdevumu saraksta. Varat atlasīt filtru, lai skatītu noteikta uzņēmuma statusu. Katrā statusa cilnē ir sniegta detalizēta informācija gan par izpildīto apjomu procentos, gan atlikušo uzdevumu skaitu.

Pēdējā cilne ir paredzēta detalizētajam uzdevumu sarakstam. Šajā sarakstā ir ietverti visi uzdevumi. Uzdevumu sarakstu varat filtrēt vairākos veidos. Noklikšķiniet uz **Rediģēt uzdevumu**, lai mainītu uzdevuma statusu vai piešķirtu uzdevumu. Noklikšķiniet uz **Pielikumi**, lai skatītu uzdevuma pielikumus.

Uzdevuma nosaukums ir hipersaite uz lapu, uz kuru lietotājam ir jāpāriet, lai pabeigtu darbu. Šo hipersaiti var iestatīt, izmantojot lauku **Izvēlnes vienuma nosaukums**, kad izveidojat vai rediģējat uzdevumu veidlapā **Konfigurēt datu validēšanas projektu**.

Uzdevumam varat pievienot failus, piezīmes, attēlus un vietrāžus URL, izmantojot darbību **Pielikumi**. Piemēram, varat uzdevumam pievienot izdrukātu pārskata failu. Ja pastāv pielikums, uzdevumam tiek parādīta ikona kolonnā **Pielikums**.

Pēc uzdevuma pabeigšanas laukā **Aizpildījis** tiek automātiski ievadīts tā nodarbinātā vārds, kurš ir pabeidzis uzdevumu. Kad uzdevums ir atzīmēts kā pabeigts, lauks **Pabeigšanas datums** automātiski tiek atjaunināts ar pašreizējo datumu un laiku.

## <a name="configure-data-validation-project-page"></a>Lapa Konfigurēt datu validēšanas projektu

Lai varētu lietot darbvietu **Datu validēšanas kontrolsaraksts**, vispirms ir jākonfigurē process, izmantojot lapu **Konfigurēt datu validēšanas projektu**. (Noklikšķiniet uz **Darbvietas** \> **Datu validēšanas kontrolsaraksts** \> **Konfigurēt datu validēšanas projektu**.)

## <a name="task-areas"></a>Uzdevumu apgabali

Izmantojot uzdevumu jomas, varat grupēt datu validēšanas uzdevumus loģiskās jomās atbilstošo to piederībai organizācijā. Piemēram, Kreditori, Debitori vai Virsgrāmata var izmantot kā uzdevumu jomas.

**Izvēlnes vienuma nosaukums** ir saistīts ar uzdevuma darbu, un to var lietot, lai tieši pārietu uz saistīto lapu, izmantojot darbvietā pieejamo uzdevuma saiti. Piemēram, moduļa Parādi kreditoriem pārskata **Kreditoru vecumstruktūras** izpildes datu validēšanas uzdevums var būt saistīts ar lapu **Kreditoru vecumstruktūras pārskats**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]