---
title: Tūlītēja papildināšana
description: Šajā rakstā ir aprakstīts, kā var izmantot tūlītēju papildināšanu, lai papildinātu krājumus, ja ar novietojuma direktīvu netiek sadalīti krājumi.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: cf48f2f34f574503bbcae827f8013afe8532fc14
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899271"
---
# <a name="immediate-replenishment"></a>Tūlītēja papildināšana

[!include [banner](../includes/banner.md)]

Tūlītēja papildināšana ļauj papildināt krājumu tūlīt pēc tam, kad atrašanās vietas direktīvas rindai neizdodas piešķirt krājumu. Papildināšanas pamatā ir atsevišķa rinda atrašanās vietas direktīvas iestatījumos. Ja krājumi nav pieejami mērvienībās, kas ir norādītas attiecīgajā rindā, nekavējoties tiek veikta attiecīgās mērvienības papildināšana.

Tūlītēja papildināšana nodrošina alternatīvu tādai metodi, saskaņā ar kuru krājumu sadalījums balstās uz vairākām rindām atrašanās vietas direktīvā un pieprasījums tiek summēts sadalījuma beigās un papildināts, izmantojot mērvienības, kas norādītas atrašanās vietas direktīvas pēdējā rindā.

Tūlītējas papildināšanas priekšrocības ir tās, ka papildināšanu var ierobežot, izmantojot noteiktas vienības, un daudzumu var novirzīt uz noteiktām vietām.

## <a name="business-scenario"></a>Biznesa scenārijs

Piemēram, jums ir noliktava, kurā ir atsevišķas izdošanas zonas mērvienībām “kārba" un “gabals”. Jūs vēlaties optimizēt izdošanas procesu, izdodot pēc iespējas vairāk kārbu un pēc tam izdodot atlikušo daudzumu, kas ir mazāks par vienu kārbu, no zonas “gabali”.

Šajā gadījumā, var izmantot tūlītēju papildināšanu. Atrašanās vietas direktīvā var iestatīt tūlītēju papildināšanu kārbām, lai pieprasījuma papildināšana tiktu izmantota, tiklīdz trūkst kārbu, kuras izdot pieprasītajam daudzumam. Šādā veidā tiek optimizēts izdošanas process, lai izdošanā tiktu ietvertas pēc iespējas vairāk kārbas. Tūlītējā papildināšanas ģenerēs kārbu papildināšanu, un pieprasījums netiks nodots, lai izdotu daudzumus, izmantojot mērvienības "gabals". Citiem vārdiem sakot, no zonas “gabals” tiks izdoti tikai daudzumi, kas ir jāizdod, izmantojot mērvienību “gabals” (t. i., daudzumi, kas ir mazāki nekā “kārba”). Ja zonā “kārba” ir nepietiekams daudzums, varat izdot maksimāli iespējamo kārbu daudzumu no kopējā pieprasījuma. Pēc tam atlikušie daudzumi tiks izdoti no zonas “gabali”.

## <a name="where-it-applies"></a>Darbības tvērums

Tūlītēja papildināšana tiek izmantota kopuma izpildes laikā, ja notiek nesekmīgs sadalījums kādai atrašanās vietas direktīvas rindai, kurai ir iestatīta papildinājuma veidne.

## <a name="set-up-immediate-replenishment"></a>Tūlītējas papildināšanas iestatīšana

- Atveriet sadaļu **Noliktavas pārvaldība** \> **Iestatīšana** \> **Atrašanās vietas direktīvas** un pēc tam cilnes **Rindas** sarakstā **Tūlītējas papildināšanas veidne** atlasiet papildināšanas veidni kopuma pieprasījumam.

Papildināšanas veidne tiek lietota, ja atrašanās vietas direktīvas rindai neizdodas sadalīt atvēlēto mērvienību.

## <a name="troubleshooting"></a>Problēmu novēršana

Ja atrašanās vietas direktīvas rindai ir atlasīta tūlītēja papildināšana, bet netiek ģenerēts papildināšanas darbs, kad izmantojat pieprasījuma papildināšanas veidnes attiecīgajai atrašanās vietas direktīvas rindai, ir jāpārbauda divi galvenie iemesli.

- Pārliecinieties, ka lietotā pieprasījuma papildināšanas veidne ir iestatīta tā, lai izmantotu pareizās atrašanās vietas veidnes un darba veidnes, kuru tips ir **Papildināšana**.
- Pārliecinieties, ka ir pietiekami daudz pieejamu krājumu atrašanās vietās, kurās pieprasījuma papildināšanas veidne meklē pieejamus krājumus papildināšanai.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]