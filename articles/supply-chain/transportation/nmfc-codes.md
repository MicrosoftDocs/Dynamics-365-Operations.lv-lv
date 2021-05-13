---
title: Valsts autotransporta kravu klasifikācijas (National Motor Freight Classification — NMFC) kodi
description: Šajā tēmā aprakstīts, kā strādāt ar Valsts autotransporta kravu klasifikācijas (National Motor Freight Classification — NMFC) kodiem programmā Microsoft Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941886"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a>Valsts autotransporta kravu klasifikācijas (National Motor Freight Classification — NMFC) kodi

[!include [banner](../includes/banner.md)]

Valsts autotransporta kravu klasifikācijas (National Motor Freight Classification — NMFC) kodi palīdz klasificēt krājumus, ko var nosūtīt. NMFC kods ir apzīmējums, ko izmanto, lai grupētu preces. Tas ļauj transporta uzņēmumiem novērtēt preces nosūtīšanai, klasificējot krājumus, balstoties uz tādiem apsvērumiem kā kravas automašīnas iederība, iekraušanas problēmas, apstrādes problēmas un bīstamība. Preces ir grupētas vienā no 18 kravas klasēm, izmantojot skaitļu diapazonu no 50 līdz 500. Klase, kurā prece ir grupēta, ir balstīta uz novērtējumu, kas norāda četras transportēšanas īpašības: blīvums, kraušanas iespēja, apstrādes un atbildība. Kopā šīs īpašības veido preču transportējamību.

NMFC kods ir saistīts ar katru no māzāk par krāvu (LTL) piegādes krājumu. Piemēram, klēpjdatoram var piešķirt NMFC, kas ir klasificēta kā 2,5, bet elektriskās instalācijas var piešķirt NMFC, kas ir klasificēta kā 65.

Šis līdzeklis palīdzēs darbiniekiem izmantot NMFC kodus LTL nosūtīšanas krājumu klasificēšanai. Daži piemēri:

- Ja jūsu uzņēmumā ietilpst preču transporta pavadzīmes (bill of lading - BOL) kravas apraksts, pārvadātājam būs kaut kāda nojausma, par kravu. Krava ir svarīga klasifikācija, jo daudzi transporta uzņēmumi izmanto visu savu biznesa modeli uz kravas tipiem, ko tie nosūta.
- Šī klasifikācija var būt būtiska uzņēmumam, jo tā tiek izmantota, lai noteiktu dotās kravas izmaksas.
- Jūsu uzņēmums var noteikt LTL loģistikas un transportēšanas uzņēmuma rentabilitāti.

Šajā tēmā ir aprakstīts, kā strādāt ar NMFC kodiem programmā Microsoft Dynamics 365 Supply Chain Management.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms izveidīt NMFC kodus, jāiestata visas LTL kravas klases, kas tiem ir jākartē. LTL kravas klases pārstāv preču kategorijas, turpretim NMFC kodi ir saistīti ar konkrētām precēm katrā no 18 kravas kategorijām. Papildinformāciju par to, kā strādāt ar LTL klasēm, skatiet sadaļā [Mazāk par kravu (LTL) klases](ltl-class.md).

## <a name="create-an-nmfc-code"></a>Izveidot NMFC kodu

Lai izveidotu NMFC kodu, veiciet šādas darbības.

1. Izpildiet kādu no šīm darbībām:

    - Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Inventarizācija \> NMFC kodi**.
    - Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Transportēšanas standarti \> NMFC kodi**.

1. Atlasiet **Jauns**, lai izveidotu NMFC kodu. Pēc tam iestatiet tālāk minētos laukus.

    - **NMFC kods** - ievadiet NMFC kodu preces veidam.
    - **Nosaukums** - ievadiet elementa NMFC kodu.
    - **Par LTL klasi** — atlasiet LTL klasi, kas ir saistīta ar NMFC kodu.
    - **BOL materiālu apstrādes vienība** - definējiet noklusējuma kravas apstrādes veidu.

## <a name="example-set-up-nmfc-codes"></a>Piemērs: NMFC kodu iestatīšana

Šajā piemērā parādīts, kā iestatīt divus dažādus NMFC kodus, ko var lietot ar dažādiem produktiem.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Inventarizācija \> NMFC kodi**.
1. Darbību rūtī atlasiet **Jauns**.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **NMFC kods:** *92,5*
    - **Nosaukums:** *Dators*
    - **LTL klase:** *92,5*
    - **BOL materiālu apstrādes vienība:** *Vienība*

1. Darbību rūtī atlasiet **Saglabāt**.
1. Darbību rūtī atlasiet **Jauns**.
1. Jaunajā rindā iestatiet šādas vērtības:

    - **NMFC kods:** *125*
    - **Nosaukums:** *Tālruņi*
    - **LTL klase:** *125*
    - **BOL materiālu apstrādes vienība:** *Vienība*

1. Darbību rūtī atlasiet **Saglabāt**.

## <a name="additional-resources"></a>Papildu resursi

- [Mazāk par autokravu (LTL) klases](ltl-class.md)
- [Preču transporta pavadzīmes izveide](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
