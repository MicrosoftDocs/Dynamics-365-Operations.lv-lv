---
title: Sērijveida kontrolētu preču atgriešana POS
description: Šajā rakstā ir aprakstītas serializēto krājumu validēšanas Microsoft Dynamics 365 Commerce iespējas kā daļa no atgriešanas procesa pārdošanas punkta (POS) programmā.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9fa7e47b6d650370afe4b98d7eca01253bd1bc36
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268479"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>Sērijveida kontrolētu preču atgriešana POS

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstītas serializēto krājumu validēšanas Microsoft Dynamics 365 Commerce iespējas kā daļa no atgriešanas procesa pārdošanas punkta (POS) programmā.

> [!NOTE]
> Commerce 10.0.20 un jaunākās versijās ir pieejams jauns līdzeklis ar nosaukumu **Vienotā atpakaļ atdošanas apstrādes pieredze programmā POS**. Lai izmantotu sērijas numura validāciju atgriezto pasūtījumu apstrādes laikā programmā POS, šis līdzeklis ir jāieslēdz. Informāciju par citām iespējām, ko šis līdzeklis nodrošina, kad tas ir ieslēgts, skatiet sadaļā [Atgriešanas izveide programmā POS](POS-returns.md).
>
> Kad līdzeklis ir ieslēgts, to nevar izslēgt.

## <a name="options-for-validating-serialized-returns"></a>Serializēto atgriešanu validēšanas opcijas

Ja ir ieslēgts līdzeklis **Vienotā atgriešanas apstrādes pieredze programmā POS**, organizācijas var veikt atgriešanas validāciju sērijveida kontrolētiem krājumiem, izmantojot POS. Šī iespēja var brīdināt lietotājus, ja atgrieztais sērijas numurs atšķiras no sākotnējā pārdotā sērijas numura. Commerce 10.0.20 un jaunākās versijās šis ziņojums, ko lietotāji saņem, ir tikai brīdinājuma ziņojums. Lietotāji var turpināt apstrādāt atgriešanu sērijas numuram, kas atšķiras no sērijas numura, kas sākotnēji tika pārdots.

Lai konfigurētu sērijas numura validāciju organizācijai pēc tam, kad ir ieslēgts līdzeklis **Vienotā atgriešanas apstrādes pieredze programmā POS**, dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Commerce parametri**, kas atrodami Commerce Headquarters. Cilnes **Krājumi** kopsavilkuma cilnē **Veikala krājumu operācijas** iestatiet opciju **Iespējot sērijas numuru validāciju atgriešanai POS** uz **Jā**.

## <a name="process-returns-for-serialized-items-in-pos"></a>Serializēto krājumu atgriešanas apstrāde programmā POS

Ja opcija **Iespējot sērijas numuru validāciju atgriešanai POS** ir iestatīta uz **Jā**, kad sērijveida kontrolēts krājums tiek atgriezts, izmantojot POS, lietotājs var ievadīt sērijas numuru atgriešanas rindai informācijas rūtī, kas atrodas lapā **Atgriežamās preces**. Ja ievadītais sērijas numurs neatbilst sākotnējam sērijas numuram, kas tika pārdots pārdošanas darbībā, lietotājs saņem brīdinājuma ziņojumu. Tomēr programma neliedz lietotājam turpināt iegrāmatot atgriešanu.

> [!NOTE]
> Pašlaik POS atbalsta sērijas numuru validāciju tikai atgriešanas rindām, kurās oriģinālais pasūtītais daudzums nav lielāks par vienu. Ja sākotnējā pārdošanas pasūtījuma rinda tika izveidota kanālā, kas nav POS, un daudzums, kas tika pasūtīts serializētajam krājumam konkrētajā pārdošanas rindā, ir vairāk nekā viens, tad krājumu nevar pareizi atgriezt, izmantojot POS.

## <a name="additional-resources"></a>Papildu resursi

[Atgriešanas izveide programmā POS](POS-returns.md)
