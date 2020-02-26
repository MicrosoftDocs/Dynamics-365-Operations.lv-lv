---
title: Teksta bloka modulis
description: Šajā tēmā tiek stāstīts par teksta bloka moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025601"
---
# <a name="text-block-module"></a>Teksta bloka modulis


[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par teksta bloka moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Teksta bloka modulis ir modulis, kas tiek izmantots teksta satura pievienošanai. Tas var būt gan informatīvs, gan reklāmas saturs.

Teksta bloka moduļus vada dati no Satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā. Tas ir savrups moduļi, kas nav atkarīgi no lapas konteksta vai jebkādiem citiem moduļiem.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Teksta bloka moduļu piemēri pakalpojumā e-Commerce

Teksta bloka moduļus var izmantot šādi.

* Lai preces informācijas lapā rādītu preces līdzekļus.
* Informācijas nolūkiem jebkurā lapā. Piemēram, tie var izskaidrot lojalitātes programmu priekšrocības, aprakstīt nosūtīšanas un atgriešanas politiku, atbildēt uz bieži uzdotajiem jautājumiem vai nodrošināt saturu "par mums".
* Pievienot pielāgotus ziņojumus preces informācijas lapā. (piemēram, “brīva piegāde pasūtījumiem virs 50 $”).
* Atrunām un kontaktinformācijai par preču detalizētas informācijas lapām, groza lapām, izrakstīšanās lapām un citām lapām (piemēram, “Piegāde un atgriešana saskaņā ar veikala politikām”).

## <a name="text-block-module-properties"></a>Teksta bloka moduļa rekvizīti

| Rekvizīta nosaukums     | Value                                            | Apraksts |
|-------------------|--------------------------------------------------|-------------|
| Bagātināts teksts         | Bagātināts teksts                                        | Rindkopas teksts. Tiek atbalstītas dažas pamata bagātināta teksta iespējas, piemēram, treknraksts, pasvītrots un slīpraksta teksts. |
| Pielāgotās klases nosaukums | Kaskadētās stila lapas (CSS) klases nosaukums        | Tās pielāgotās CSS klases nosaukums, ko izstrādātājs sniedz, lai formatētu šo moduli. Klases nosaukumam ir jābūt definētam dizaina pakotnē. |
| Fontu lielums         | **Mazs**, **Vidējs**, **Liels** vai **X-liels** | Satura fonta lielums. |

## <a name="add-a-text-block-module-to-a-page"></a>Teksta bloka moduļa pievienošana lapā

Lai pievienotu teksta bloka moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Izveidojiet lapas veidni ar nosaukumu **Satura veidne**. 
1. Slotā **Pamatteksts** pievienojiet moduli **Noklusējuma lapa**.
1. Pabeidziet rediģēt veidni un publicējiet to.
1. Izmantojiet jūsu tikko izveidoto satura veidni, lai izveidotu lapu ar nosaukumu **Satura lapa**.
1. Jaunās lapas **Galvenajā** slotā pievienojiet konteinera moduli.
1. Konteinera moduļa rekvizītu rūtī iestatiet rekvizītu **Platums** uz **Aizpildīt konteineru**.
1. Pievienojiet teksta bloka moduli konteinera modulim. 
1. Teksta bloka moduļa rekvizītu rūtī pievienojiet tekstu laukā **Bagātinātais teksts**.
1. Pabeidziet rediģēt lapu un publicējiet to.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Veicināšanas reklāmkarogu modulis](add-alert.md)

[Karuseļa modulis](add-carousel.md)

[Satura bloka modulis](add-hero-module.md)

[Video atskaņotāja modulis](add-video-player.md)

