---
title: "Informācijas kodi un informācijas kodu grupas"
description: "Šajā rakstā ir sniegts pārskats par informācijas kodiem, informācijas kodu grupām un par to, kā tos izmantot."
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailInfocodeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: c9cd9197f395b69f65137a59392a4d83d692f6fa
ms.contentlocale: lv-lv
ms.lasthandoff: 01/04/2019

---

# <a name="info-codes-and-info-code-groups"></a>Informācijas kodi un informācijas kodu grupas

[!include [banner](includes/banner.md)]

Šajā rakstā ir sniegts pārskats par informācijas kodiem, informācijas kodu grupām un par to, kā tos izmantot.

Infokodi nodrošina veidu, kā iegūt datus pārdošanas punkta (POS) reģistrā. Infokodus varat izmantot, lai kasierim norādītu, ka dažādu POS darbību, piemēram, krājumu pārdošanas, krājumu atgriešanas vai debitoru atlasīšanas, laikā ir jāievada informācija. Kasieri var atlasīt ievadi no saraksta vai ievadīt to kā kodu, numuru, datumu vai tekstu. Infokodus varat piešķirt iepriekš definētām veikala darbībām, mazumtirdzniecības precēm, maksājumu metodēm, debitoriem un noteiktām pārdošanas punkta aktivitātēm. Infokodus var izmantot tālāk aprakstīto darbību izpildei.

- Darījuma laikā iegūt papildu informāciju, piemēram, reisa numuru vai atgriešanas iemeslu.
- Reģistra kasierim likt atlasīt no konkrētu preču cenu saraksta.
- Saistīt apakškodu ar infokodu, kas kasierim pieprasa veikt ievadi, ja tiek veiktas noteiktas aktivitātes. Piemēram, kad debitors atgriež preci, varat likt kasieris vaicāt, kāpēc prece tiek atgriezta. Pēc tam šos apakškodus varat izmantot, lai parādītu iemeslu sarakstu, no kura kasieris var izvēlēties.
- Pārdot preci kā parastu pārdošanu, pārdošanu ar atlaidi vai bezmaksas preci.
- Varat likt kasierim ievadīt vērtību vai atlasīt no apakškodu saraksta, kad kasieris atver kases sistēmas atvilktni, neveicot pārdošanas operāciju.

## <a name="info-codes-group"></a>Infokodu grupa

Programmatūrā Dynamics 365 for Retail varat izveidot infokodu grupas. Infokodu grupas papildina lietošanas iespēju elastību, ļaujot definēt mazāku skaitu informācijas kodu un pēc tam tos izmantot daudzveidīgāk. Infokodu grupas varat izmantot tālāk aprakstītajos veidos.

- Definējiet mazāku skaitu infokodu un ērti izmantojiet tos atkārtoti. Infokodu grupās iekļautajiem infokodiem nav iepriekš definētu atkarību no citiem infokodiem. Vienu un to pašu infokodu varat iekļaut vairākās infokodu grupās, un pēc tam izmantot prioritātes noteikšanu, lai tos pašus infokodus sniegtu katrai konkrētajai situācijai vispiemērotākajā secībā.
- Saistiet informācijas kodus ar citiem informācijas kodiem vai informācijas kodu grupām, lai apkopotu informāciju par preci vai darījumu jums nepieciešamajā veidā, bez nepieciešamības definēt atsevišķu informācijas kodu vai piesaistīt informācijas kodu katram scenārijam.

## <a name="info-code-examples"></a>Informācijas koda piemēri

**1. piemērs: infokodu atkārtota lietošana**

Varat saistīt infokodus, lai pēc viena infokoda aktivizēšanas uzreiz tiktu aktivizēts cits infokods. Piemēram, kad pārdodat noteiktas preces, varat noteikt, lai kasieris vaicā debitoram, vai tas vēlas iegādāties baterijas un preces garantiju. Attiecībā uz citām precēm varat ieteikt kasierim vaicāt debitoram, vai tas vēlas iegādāties baterijas, un uzzināt debitora pasta indeksu. Ja šiem scenārijiem izveidojat saistītus infokodus, ir jāiestata katra infokoda variācija, lai kasierim liktu vaicāt pareizo informāciju. Ja izmantojat informācijas kodu grupas, kopējos informācijas kodus, piemēram, vaicāšanu par baterijām, var iestatīt vienreiz un tad atkārtoti izmantot vairākās informācijas kodu grupās. Infokodu grupām varat arī izmantot prioritāšu noteikšanu, lai noteiktu uzvedņu parādīšanas secību.

**2. piemērs: infokodu piesaistīšana infokodu grupām**

Kad pārdodat noteiktas preces, piemēram, mobilās ierīces, jūs parasti vēlaties iegūt noteiktu informācijas kopumu, piemēram, tālruņa numuru, mobilās ierīces identifikatoru (MEID) un sērijas numuru. Tomēr vēlaties arī planšetdatoriem iegūt citādu informāciju nekā mobilajam tālrunim. Varat iestatīt informācijas kodu grupu, kas ietver uzvednes par tālruņa numuru, MEID un sērijas numuru, un pēc tam saistīt šo informācijas kodu grupu ar atsevišķu informācijas kodu. Kad tiek aktivizēts precei raksturīgais infokods, šo infokodu grupu var aktivizēt kā nākamo, ļaujot jums iegūt kopējos datus bez nepieciešamības definēt vairākas saistītu infokodu kopas katrai ierīcei.

