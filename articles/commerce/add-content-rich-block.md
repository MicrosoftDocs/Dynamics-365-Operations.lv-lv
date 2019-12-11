---
title: Satura bagātinātā bloka modulis
description: Šajā tēmā tiek stāstīts par satura bagātinātā bloka moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785425"
---
# <a name="content-rich-block-module"></a>Satura bagātinātā bloka modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par satura bagātinātā bloka moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Satura bagātinātā bloka modulis ir īpašs konteiners, kurā var ievietot vienu vai vairākus satura bagātinātā bloka elementus. Satura bagātinātā bloka moduļi tiek izmantoti lapas teksta saturam. Tas var būt gan informatīvs, gan reklāmas saturs.

Satura bagātinātā bloka moduļus vada dati no satura pārvaldības sistēmas (CMS), un tos var ievietot jebkurā lapā. Tas ir savrups moduļi, kas nav atkarīgi no lapas konteksta vai jebkādiem citiem moduļiem.

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a>Satura bagātinātā bloka moduļu piemēri E-komercijā

Satura bagātināta bloka moduļus var izmantot šādi.

* Lai preces informācijas lapā rādītu preces līdzekļus.
* Informācijas nolūkiem jebkurā lapā. Piemēram, tie var izskaidrot lojalitātes programmu priekšrocības, aprakstīt nosūtīšanas un atgriešanas politiku, atbildēt uz bieži uzdotajiem jautājumiem vai nodrošināt saturu "par mums".
* Pievienot pielāgotus ziņojumus preces informācijas lapā. (piemēram, “brīva piegāde pasūtījumiem virs 50 $”).
* Atrunām un kontaktinformācijai par preču detalizētas informācijas lapām, groza lapām, izrakstīšanās lapām un citām lapām (piemēram, “Piegāde un atgriešana saskaņā ar veikala politikām”).

## <a name="content-rich-block-module-properties"></a>Satura bagātinātā bloka moduļa rekvizīti

| Rekvizīta nosaukums     | Vērtība                                 | Rekvizīts |
|-------------------|---------------------------------------|----------|
| Kolonnu skaits | Skaitlis no **1** līdz **4**     | Kolonnu skaits satura bagātinātajā blokā. Tur var būt līdz četrām kolonnām. |
| Platums             | **Ietilpināt konteinerā** vai **Aizpildīt ekrānu** | Ja vērtība ir iestatīta uz **Ietilpināt konteinerā**, tad elementi konteinerā tiek ierobežoti ar konteinera platumu. Ja vērtība ir iestatīta uz **Aizpildīt ekrānu**, elementi neaprobežojas ar konteinera platumu, bet var pāriet pilnekrāna režīmā. Varat mainīt vērtību, lai sasniegtu vēlamo izkārtojumu. |

## <a name="content-rich-block-item-module-properties"></a>Satura bagātinātā bloka elementa moduļa rekvizīti

| Rekvizīta nosaukums | Vērtība          | Apraksts |
|---------------|----------------|-------------|
| Rindkopa     | Rindkopas teksts | Teksts, kas pievienots katram saturam bagātinātajam bloka elementam. Tiek atbalstītas dažas pamata bagātināta teksta iespējas, piemēram, treknraksts, pasvītrots un slīpraksta teksts. |

## <a name="add-a-content-rich-block-module-to-a-page"></a>Satura bagātinātā bloka moduļa pievienošana lapā

Lai pievienotu satura bagātinātā bloka moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.

1. Izveidojiet lapas veidni ar nosaukumu **Satura veidne**.
1. Noklusējuma lapas **Galvenajā** slotā pievienojiet satura bagātinātā bloka moduli.
1. Pārbaudiet veidni un publicējiet to.
1. Izmantojiet jūsu tikko izveidoto satura veidni, lai izveidotu lapu ar nosaukumu **Satura lapa**.
1. Jaunās lapas **Galvenajā** slotā pievienojiet satura bagātinātā bloka moduli.
1. Satura bagātinātā bloka moduļa rekvizītos iestatiet kolonnu skaitu uz **2**.
1. Satura bagātinātā bloka modulī atlasiet **Pievienot moduli**un pievienojiet satura bagātinātā bloka elementu (piemēram, **elements1**).
1. Jaunajā satura bagātinātā bloka elementā pievienojiet rindkopas tekstu.
1. Satura bagātinātā bloka modulī atlasiet **Pievienot moduli**un pievienojiet satura bagātinātā bloka elementu (piemēram, **elements2**).
1. Jaunajā satura bagātinātā bloka elementā pievienojiet rindkopas tekstu.
1. Saglabājiet lapu un priekšskatiet izmaiņas Divu kolonnu skatā ir jāredz divi bagātināta teksta bloki.
1. Pārbaudiet lapu un publicējiet to.

> [!NOTE]
> Ja pievienojat trešo satura bagātinātā bloka elementu, tas tiks novietots zem diviem iepriekš pievienotajiem elementiem. Mainot kolonnu skaitu un elementus konteinerā, varat iegūt dažādus izkārtojumus teksta saturam.

## <a name="additional-resources"></a>Papildu resursi

[Sākuma komplekta pārskats](starter-kit-overview.md)

[Brīdinājuma modulis](add-alert.md)

[Karuseļa modulis](add-carousel.md)

[Satura izvietojuma modulis](add-content-placement-modules.md)

[Līdzekļa modulis](add-feature-module.md)

[Centrālais modulis](add-hero-module.md)

[Video atskaņotāja modulis](add-video-player.md)

