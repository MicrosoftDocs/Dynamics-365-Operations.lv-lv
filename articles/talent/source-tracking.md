---
title: Kandidātu avotu izsekošana sistēmā Attract
description: Šajā tēmā ir sniegta informācija par kandidātu profilu un pieteikumu avotu izsekošanu.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 8860f508eebc377042c4e101eeb08a14a737ba0c
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832669"
---
# <a name="track-candidate-sources-in-attract"></a>Kandidātu avotu izsekošana sistēmā Attract

[!include [banner](includes/banner.md)]

> [!NOTE] 
> Šajā tēmā minētā funkcionalitāte ir pieejama kā daļa no priekšskatījuma laidiena. Saturs un funkcionalitāte var tikt mainīti. Lai lietotu šo funkciju, lūdziet administratoram iespējot to, izmantojot sadaļu **Administratora iestatījumi** programmā Attract. Turpmākajos laidienos būs pieejami avotu izsekošanas pārskati. Papildinformāciju skatiet tēmā [Piekļuve priekšskatījuma līdzekļiem programmā Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

Kad kandidāti piesakās kādam darbam, Attract automātiski izseko viņu pieteikumu avotu, sniedzot jums vērtīgu informāciju, kas palīdz mērķēt jūsu personāla atlases aktivitātes. Darbinieku atlases speciālisti un par pieņemšanu darbā atbildīgie vadītāji pieteikuma avotu var arī atlasīt, kad kādu kandidātu manuāli pievieno darbam vai kandidātu kopai.

Pieteikuma avotu varat apskatīt pieteikuma aktivitātes detalizētajā informācijā cilnē **Aktivitāte**, kā arī pieteikuma vēsturē, kas kandidātu kopās ir pieejama sadaļā **Profils**. Kandidāta profila avots ir atrodams kandidāta detalizētajā informācijā, cilnē **Profils** gan pieteikumos, gan kandidātu kopās.

> [!NOTE] 
> Procesa veidnes ir atrodamas [visaptverošajā darbā pieņemšanas pievienojumprogrammā](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).

## <a name="pre-configured-sources"></a>Iepriekš konfigurētie avoti

Noklusējuma avotu sarakstā ir parastie pieteikumu avoti. Noteiktiem avotu tipiem, piemēram, **Darba sludinājumu dēlis** un **Sociālais tīkls**, ir papildu informācija par avotu. Piemēram, tipā **Sociālais tīkls** ietilpst Facebook un Twitter. Avota tips **Ieteikums** ļauj jums norādīt iekšēju darbinieku kā ieteicēju. Noklusējuma avotu sarakstā ir šādi iepriekš konfigurētie avoti.

-   Attract karjeras vietne

-   Aģentūra

-   Karjeras gadatirgus

-   Uzņēmuma mārketings

-   Konferences un tirdzniecības izstādes

-   Profesionālā asociācija

-   Darba sludinājumu dēlis

    -   Indeed

    -   Seek

    -   CareerBuilder

    -   Google Jobs

    -   Xing

    -   Glassdoor

    -   Monster Jobs

-   Žurnāli un publikācijas

-   Sociālais tīkls

    -   Facebook

    -   Twitter

-   University Recruiting

-   LinkedIn

-   Classifieds

-   Ieteikums

-   Pievienoja personāla atlases darbinieks

-   Cits

## <a name="customize-the-source-list"></a>Avotu saraksta pielāgošana 

Avotu sarakstu varat paplašināt, lai iekļautu citus pieteikumu avotus. Lai pielāgotu šo sarakstu, izpildiet norādījumus rakstā [Opciju kopu paplašināšana programmā Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract). Rediģējiet elementu **TalentSource**, lai iekļautu papildu avotus. 

Lai nerastos negatīva ietekme uz lietotāja interfeisu (UI), nerediģējiet un nedzēsiet **TalentCategory** uzskaitījuma vērtības (nevis nosaukumus) šādiem vienumiem.

- **Ieteikums**
- **LinkedIn**
- **Cits**

Tā vietā varat paplašināt **TalentSource** uzskaitījumu, pievienojot citus avotu tipus.
