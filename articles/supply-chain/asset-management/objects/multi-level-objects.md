---
title: Vairāklīmeņu līdzekļi
description: Šajā rakstā ir izskaidrots, kā izveidot un dzēst daudzlīmeņu līdzekļus.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34ab83c9f9673c39006b3985ebaac9e17a45da82
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908777"
---
# <a name="multi-level-assets"></a>Vairāklīmeņu līdzekļi

[!include [banner](../../includes/banner.md)]

 

Šajā rakstā ir izskaidrots, kā izveidot un dzēst daudzlīmeņu līdzekļus. Varat izveidot līdzekļus un saistītos pakārtotos līdzekļus hierarhiskā koka struktūrā. Šādā veidā var parādīt relācijas un atkarības starp līdzekļiem. Uzturēšanas darbi var būt saistīti ar visiem koka struktūras līmeņiem. Statistiku var izveidot arī individuālam līmenim vai kā visu pakārtoto līdzekļu līmeņu summu.

Saraksta lapā **Visi līdzekļi** (**Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi**) kolonnā **Līdzeklis** līdzekļi ir uzskaitīti hierarhiskā kārtībā. Kolonnā **Vecākelements** tiek rādīts saistītais vecākelements. Turklāt, ja līdzekļi un pakārtotie līdzekļi jau ir izveidoti, sadaļā **Līdzekļu koks** rūtī **Saistītā informācija** tiek parādīti līdzekļi koka struktūrā.

Papildinformāciju par līdzekļa izveidi skatiet nodaļā [Līdzekļa izveide](../objects/create-an-object.md). Lai izveidotu pakārtotu līdzekli, kopsavilkuma cilnē **Vispārīgi** atlasiet primāro līdzekli laukā **Vecākelements**.

## <a name="copy-an-asset-or-asset-structure"></a>Līdzekļa vai līdzekļu struktūras kopēšana

Ja jūsu uzņēmumam ir vairākas līdzīgas līdzekļu struktūras, varat izmantot funkciju Kopēt Līdzekļu pārvaldībā, lai tos ātri izveidotu.

1. Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi**.
2. Saraksta lapā **Visi līdzekļi** atlasiet līdzekli, kuru kopēt. Piemēram, ja vēlaties kopēt visu līdzekļu struktūru, tostarp pakārtotos līdzekļus, atlasiet primāro līdzekli.
3. Atlasiet **Kopēt līdzekli**. Sadaļā **Kopēt no** lauks **Līdzeklis** ir iestatīts uz saraksta lapā atlasīto līdzekli.
4. Sadaļā **Kopēt uz** laukā **Līdzeklis** ievadiet jaunā līdzekļa nosaukumu.
5. Ja līdzeklim, kas tiek veidots, ir jābūt daļai no esošas līdzekļu struktūras, sadaļas **Primārais līdzeklis** laukā **Līdzeklis** atlasiet vecākelementa ID.
6. Atlasiet **Labi**. Jaunā līdzekļu struktūra tiek rādīta saraksta lapā **Visi līdzekļi**. Visi līdzekļu atribūti, uzturēšanas plāni un uzturēšanas cikli, kas saistīti ar nokopēto līdzekli, tiek pārsūtīti uz jauno līdzekli vai līdzekļu struktūru.

Kopējot līdzekļu struktūru, jaunās struktūras pakārtotajiem līdzekļiem ir tāds pats nosaukums kā apakšlīdzekļiem, kurus nokopējāt. Pēc kopēšanas procedūras pabeigšanas varat viegli mainīt līdzekļa nosaukumu un citus iestatījumus. Atlasiet līdzekli saraksta lapā **Visi līdzekļi** un pēc tam atlasiet pogu **Rediģēt**.

> [!NOTE]
> Kopējot līdzekli vai līdzekļu struktūru, jauno līdzekļu dzīves cikla stāvoklis tiek atiestatīts uz stāvokli, ko jūs definējat kā līdzekļu sākotnējo dzīves cikla stāvokli. Funkcionālais novietojums tiek atiestatīts uz noklusējuma funkcionālo novietojumu.

## <a name="delete-an-asset-or-asset-structure"></a>Līdzekļa vai līdzekļu struktūras dzēšana

Ja līdzeklim ir saistītie pakārtotie līdzekļi, to var dzēst tikai tad, ja nav uzturēšanas pieprasījumu, darba pasūtījuma darbu, defektu reģistrāciju vai nosacījumu novērtējumu, kas reģistrēti kādam no līdzekļiem.

1. Saraksta lapā **Visi līdzekļi** atlasiet līdzekli, kuru dzēst.
2. Atlasiet **Dzēst**.

> [!NOTE]
> Ja nevarat dzēst līdzekli, izmantojot šo procedūru, vēl viens veids, kā rīkoties ar dzēšanu, ir iestatīt līdzekļa dzīves cikla stāvokli šim nolūkam. Piemēram, lapā **Līdzekļa dzīves cikla stāvokļi** varat iestatīt **Brāķis** vai **Dzēsts**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]