---
title: Mazāk par autokravu (LTL) klases
description: Šajā tēmā skaidrots, kas ir mazāk par autokravu (LTL) klases, un apraksta, kā to iestatīt sistēmā Microsoft Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941814"
---
# <a name="less-than-truckload-ltl-classes"></a>Mazāk par autokravu (LTL) klases

[!include [banner](../includes/banner.md)]

Mazāk par autokravu (LTL) klase, ir kravas pārvadāšanas klase, ko izmanto, lai klasificētu krājumus, ko var nosūtīt. Parasti katram preces veidam ir Valsts autotransporta kravu klasifikācijas (National Motor Freight Classification — NMFC) kods, kas atbilst noteiktam kravas klases numuram par LTL sūtījumiem. LTL kravas klases pārstāv preču kategorijas, turpretim NMFC kodi ir saistīti ar konkrētām precēm katrā no 18 kravas kategorijām.

Šis līdzeklis ļauj izmantot sistēmu, lai veiktu šādus uzdevumus:

- Nosakiet LTL kravas klases, kas tiek izmantotas jūsu uzņēmumā.
- Piešķiriet katru LTL klasi NMFC kodam lapā **NMFC kodi**. Papildinformāciju skatiet [Valsts autotransporta kravu klasifikācijas (National Motor Freight Classification — NMFC)](nmfc-codes.md) kodi.
- Piešķiriet NMFC kodu (un tādēļ tas ir saistīts ar LTL kodu) katrai precei lapā **Preces**.
- Precīzi novērtējiet LTL klasi katrai precei, pie kuras ir piešķirts NMFC kods.
- Nosakiet iepakojuma prasības katrai LTL klasei, pārbaudot starptautiskos LTL standartus. Šādā veidā tiek nodrošināts, ka preces ir labi aizsargātas un droši nosūtītas.
- Iegūstiet precīzus nosūtīšanas novērtējumus, balstoties uz LTL kravas klasi katrai precei.

Šajā tēmā aprakstīts, kā izveidot LTL klasi programmā Microsoft Dynamics 365 Supply Chain Management.

## <a name="create-an-ltl-class"></a>Izveidot LTL klasi

Lai izveidotu LTL klasi, veiciet šādas darbības.

1. Izpildiet kādu no šīm darbībām:

    - Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Inventarizācija \> LTL klases**.
    - Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Transportēšanas standarti \> LTL klases**.

2. Lai izveidotu LTL klasi, darbību rūtī atlasiet **Jauns**. Pēc tam iestatiet tālāk minētos laukus.

    - **LTL klase** – ievadiet uzņēmuma iekšējo LTL klases identifikatoru (ID) preču tipam. Lielākā daļa uzņēmumu izmanto starptautisko standartu. Šādā gadījumā šī lauka vērtība atbilst lauka **Klase** vērtībai. Tomēr, ja jūsu uzņēmums izmanto savu standartu, ievadiet kodu, kas atbilst standartam.
    - **Nosaukums** – ievadiet aprakstošu nosaukumu, kas jums un citiem lietotājiem palīdzēs izvēlēties pareizo LTL klasi katram NMFC kodam.
    - **Klase** – ievadiet starptautisko standarta LTL klases ID preču tipam. Kodam, kuru šeit ievadāt, jāatbilst oficiālajam standartam.

## <a name="example-set-up-ltl-classes"></a>Piemērs: LTL klašu iestatīšana

Šajā piemērā parādīts, kā iestatīt divas dažādas LTL klases, ko var lietot ar dažādiem produktu tipiem.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Inventarizācija \> LTL klases**.
1. Darbību rūtī atlasiet **Jauns**.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **LTL klase:** *92,5*
    - **Nosaukums:** *Datori, monitori, ledusskapji*
    - **Klase:** *92,5*

1. Darbību rūtī atlasiet **Saglabāt**.
1. Darbību rūtī atlasiet **Jauns**.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **LTL klase:** *125*
    - **Nosaukums:** *Mazās mājsaimniecības ierīces*
    - **Klase:** *125*

1. Darbību rūtī atlasiet **Saglabāt**.

## <a name="additional-resources"></a>Papildu resursi

- [Valsts autotransporta kravu klasifikācijas (National Motor Freight Classification — NMFC) kodi](nmfc-codes.md)
- [Preču transporta pavadzīmes izveide](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
