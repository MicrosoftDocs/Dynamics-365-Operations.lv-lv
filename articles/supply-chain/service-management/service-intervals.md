---
title: Pakalpojumu intervāli
description: Šajā rakstā sniegts pārskats par darbu ar pakalpojumu intervāliem. Pakalpojumu līgumu intervāls norāda biežumu, ar kādu pakalpojuma pasūtījuma rindas tiek izveidotas pakalpojumu līguma rindām, kad automātiski veidojat pakalpojumu pasūtījumus.
author: sorenva
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62708258ac3dca9ac03b44efdc96e3bfd643a255
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887230"
---
# <a name="service-intervals"></a>Pakalpojumu intervāli

[!include [banner](../includes/banner.md)]

Pakalpojumu līgumu intervāls norāda biežumu, ar kādu pakalpojuma pasūtījuma rindas tiek izveidotas pakalpojumu līguma rindām, kad automātiski veidojat pakalpojumu pasūtījumus.

Kad jūs veidojat pakalpojumu pasūtījumus automātiski, pakalpojuma pasūtījuma rindas tiek veidotas atbilstoši intervālam, kuru esat norādījuši pakalpojumu pasūtījuma rindai no vienošanās rindas sākuma datuma.

Ja pakalpojumu līguma rindas lauks **Intervāls** lapā **Pakalpojumu līgumi** ir tukšs, rinda ir vienreizējs notikums un netiek lietota, lai izveidotu pakalpojumu pasūtījumus atkārtoti.

## <a name="example"></a>Paraugs

Šis piemērs parāda, kā pakalpojumu intervāls ietekmēs pakalpojumu līguma rindas un pakalpojuma pasūtījuma rindas pakalpojuma pasūtījumā.

### <a name="create-a-service-agreement"></a>Pakalpojumu līguma izveide

Vispirms jūs izveidojat pakalpojumu līgumu un opcijai **Kombinēt pakalpojumu pasūtījumus** iestatāt vērtību **Pēc pakalpojumu līguma**.

1. Noklikšķiniet uz **Pakalpojumu līgumi**.
2. **Darbību rūtī** cilnē **Pakalpojumu līgums** grupā **Jauns** noklikšķiniet uz **Pakalpojumu līgums**, lai izveidotu jaunu pakalpojumu līgumu.
3. Ievadiet aprakstu, atlasiet projekta lauku **Projekta ID** un ievadiet datumu laukā **Sākuma datums**.
4. Laukā **Kombinēt pakalpojumu pasūtījumus** atlasiet **Pēc pakalpojumu līguma**.

Tagad jūs esat izveidojuši sekojošo pakalpojumu līgumu:

| Projekts      | Pieņemšanas datums                                                                         |
|--------------|------------------------------------------------------------------------------------|
| Jūsu projekts | Norādītais projekta datums. Šajā piemērā tiek izmantots pašreizējais datums. |

### <a name="create-a-service-agreement-line"></a>Pakalpojumu līguma rindas izveide

Pēc tam izveidojiet pakalpojumu līguma rindu ar darbības tipu **Stunda**.

Lai pabeigtu šo piemēra daļu, sadaļā **Pakalpojumu intervāli** izveidojiet 10 dienu pakalpojumu intervālu. 

1. Atlasiet tikko izveidoto pakalpojumu līgumu. 
2. Kopsavilkuma cilnē **Rindas** noklikšķiniet uz pogas **Pievienot**, lai izveidotu jaunu rindu lapas **Pakalpojumu līgumi** apakšdaļā.
3. Laukā **Darbības tips** atlasiet **Stunda**.
4. Laukā **Darbinieks** atlasiet darbinieku, kurš sniegs pakalpojumu.
5. Laukā **Pakalpojumu intervāls** atlasiet 10 dienu intervālu.

Tagad jūs esat izveidojuši pakalpojumu līguma rindu ar šādu informāciju:

| Darbības veids | Pieņemšanas datums                               | Pakalpojumu intervāls |
|------------------|------------------------------------------|------------------|
| Stundas             | Pašreizējais datums.                        | Ik pēc 10 dienām    |
| Darbinieks           | Darbinieks, kurš izpildīs pakalpojumu. |                  |

Rindai nav norādīts laika logs. 

### <a name="create-planned-service-orders"></a>Plānoto pakalpojumu pasūtījumu izveide

Tagad varat izveidot plānotos pakalpojumu pasūtījumus un pakalpojumu pasūtījumu rindas nākamajam mēnesim.

1. Lapā **Pakalpojumu līgumi** sadaļā **Darbību rūts** cilnē **Piegādāt** noklikšķiniet uz **Plānotie pakalpojumu pasūtījumi**.
2. Lapā **Pakalpojumu pasūtījumu izveide** laukā **No datuma** ievadiet pašreizējo datumu, bet laukā **Līdz datumam** ievadiet datumu, kas ir vienu mēnesi no pašreizējā datuma.
3. Slīdnim **Stunda** iestatiet vērtību **Jā**. 
4. Noklikšķiniet uz **Labi**.

Tā kā pakalpojuma pasūtījumā nepastāv grupēšana (to nosaka opcija **Pēc pakalpojumu līguma** laukā **Kombinēt pakalpojumu pasūtījumus**), katram pakalpojumu pasūtījumam tiek izveidota viena pakalpojumu pasūtījuma rinda.

### <a name="service-orders-created"></a>Izveidotie pakalpojuma pasūtījumi

Laika periodā, kuru norādījāt dialoglodziņā **Pakalpojumu pasūtījumu izveide**, iekļaujas trīs izveidotās pakalpojuma pasūtījuma rindas. Pakalpojuma pasūtījuma rindas var skatīt lapā **Pakalpojumu līgumi** (**Darbību rūts** \> cilne **Piegādāt** \> poga **Skatīt**).

## <a name="related-articles"></a>Saistītie raksti

[Pakalpojumu intervālu iestatīšana](set-up-service-intervals.md)  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]