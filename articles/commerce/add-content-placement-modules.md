---
title: Satura izvietojuma modulis
description: Šajā tēmā tiek stāstīts par satura izvietojumu un satura izvietojuma elementu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785304"
---
# <a name="content-placement-module"></a>Satura izvietojuma modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par satura izvietojumu un satura izvietojuma elementu moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Satura izvietošanas modulis ir īpašs konteiners, kurā var ievietot citus moduļus noteiktā izkārtojumā. Satura izvietošanas moduļi atbalsta šādus moduļu tipus kā pakārtotos moduļus: satura izvietošanas elementu, konta sveiciena elementu, konta pasūtījuma elementu, konta vēlmju saraksta elementu un konta profila elementu.

Satura izvietojuma moduļi iegūst datus no viņu atbalstītajiem pakārtotajiem moduļiem. Tāpēc satura izvietošanas moduļus var izmantot dažādos veidos atkarībā no tam pievienotajiem moduļiem.

Satura izvietošanas elementa moduļi izmanto abus attēlus un tekstu, lai parādītu veicināšanas pasākumus, politikas un preču līdzekļus. Piemēram, satura izvietošanas preču modulis var tikt izmantots mājas lapā, lai parādītu veikala politikas vai piegādes informāciju. Satura izvietojuma elementa moduļus vada dati no satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā. Tomēr tos var izmantot tikai satura izvietojuma modulī.

## <a name="examples-of-content-placement-modules-in-e-commerce"></a>Satura izvietojuma moduļu piemēri E-komercijā

* Satura izvietojuma moduļi, kuros ir satura izvietojuma elementu moduļi, var tikt izmantoti sākumlapā vai mārketinga lapās, lai parādītu preču līdzekļus, veicināšanas pasākumus, veikala ierobežojumus, piegādes informāciju un citu informāciju, izmantojot gan attēlus, gan tekstu.
* Satura izvietojuma moduļi, kuros ir satura izvietojuma elementu moduļi, var tikt izmantoti preču informācijas lapās, lai parādītu preču līdzekļus.
* Satura izvietojuma moduļi, kas ietver konta sveiciena elementu vai konta pasūtījuma elementu moduļus, var tikt izmantoti konta pārvaldības lapās.

## <a name="content-placement-module-properties"></a>Satura izvietojuma moduļa rekvizīti

| Rekvizīta nosaukums | Vērtība | Apraksts |
|---------------|-------|-------------|
| Platums         | **Ietilpināt konteinerā** vai **Pilnekrāna režīms** | Ja vērtība ir iestatīta uz **Ietilpināt konteinerā**, elementi satura izvietojuma modulī ir ierobežoti ar satura izvietojuma moduļa platumu. Ja vērtība ir iestatīta uz **Pilnekrāna režīms**, elementi neaprobežojas ar satura izvietojuma moduļa platumu, bet var pāriet pilnekrāna režīmā. |

## <a name="content-placement-item-module-properties"></a>Satura izvietojuma elementa moduļa rekvizīti

| Rekvizīta nosaukums | Vērtība | Apraksts |
|---------------|-------|-------------|
| Virsraksts       | Virsraksta teksts un virsraksta etiķetes (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Katram satura izvietošanas elementa modulim var būt virsraksts. **Virsraksta** rekvizīts atbalsta virsraksta etiķetes. Pēc noklusējuma tiek izmantota virsraksta etiķete **H2**, bet virsraksta etiķeti var mainīt atbilstoši pieejamības prasībām. |
| Rindkopa     | Rindkopas teksts | Satura izvietošanas elementu moduļi atbalsta rindkopu tekstu bagātinātā teksta formātā. Tiek atbalstītas dažas pamata bagātinātā teksta iespējas, piemēram, treknraksts, pasvītrots un slīpraksta teksts, kā arī hipersaites. Modulim piemērots lapas dizains var ignorēt dažas no šīm iespējām. |
| Attēls         | Attēla fails | Attēlu var saistīt ar tekstu. |
| Saistīt          | Saites URL un saites teksts | Tekstam var pievienot saiti, lai novirzītu lietotājus uz konkrētu lapu. |
| Elementa lielums     | Skaitlis no **1** līdz **12** | Katram satura izvietojuma elementam šis rekvizīts nosaka slotu skaitu, kas elementam jāaizpilda satura izvietojuma modulī. Satura izvietošanas moduļa maksimālais apmērs ir 12 sloti. Ja kopējais elementu apmērs pirmajam *n* krājumiem satura izvietojuma modulī pārsniedz 12 slotus, elementi tiek pārnesti uz nākamo rindu. |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a>Satura izvietošanas moduļa pievienošana, kurā ir satura izvietošanas elements, lapai

Lai pievienotu satura izvietojuma moduli, kurā ir satura izvietošanas elementa modulis, uz jaunu lapu un iestatītu pieprasītos rekvizītus, veiciet šādas darbības.

1. Izveidojiet veidni ar nosaukumu **satura izvietojuma veidne**.
1. Noklusētās lapas **Galvenajā** slotā pievienojiet satura izvietojuma moduli.
1. Satura izvietojuma modulī pievienojiet satura izvietojuma elementa moduli
1. Pārbaudiet veidni un publicējiet to.
1. Izmantojiet jūsu tikko izveidoto satura izvietojuma veidni, lai izveidotu lapu ar nosaukumu **Satura izvietojuma lapa**.
1. Jaunās lapas **Galvenajā** slotā pievienojiet satura izvietojuma moduli.
1. Satura izvietojuma modulī pievienojiet satura izvietojuma elementa moduli
1. Rekvizītu rūtī satura izvietošanas elementa modulim atlasiet attēlu, pievienojiet virsrakstu, pievienojiet rindkopu, pievienojiet saiti, iestatiet saites vietrādi URL un iestatiet elementa lielumu uz **6**.
1. Atkārtojiet 7. un 8. darbību, lai pievienotu citu satura izvietošanas krājumu moduli ar vienādu elementu izmēru.
1. Saglabājiet un priekšskatiet lapu. Jābūt redzamiem diviem satura izvietošanas elementiem, kas parādās līdzās. Varat pielāgot katra satura izvietojuma krājuma moduļa rekvizītu **Elementa izmērs** vai pievienot papildu moduļus, lai sasniegtu vēlamo izkārtojumu.
1. Pārbaudiet lapu un publicējiet to.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Brīdinājuma modulis](add-alert.md)

[Karuseļa modulis](add-carousel.md)

[Bagātinātā satura bloka modulis](add-content-rich-block.md)

[Līdzekļa modulis](add-feature-module.md)

[Centrālais modulis](add-hero-module.md)

[Video atskaņotāja modulis](add-video-player.md)
