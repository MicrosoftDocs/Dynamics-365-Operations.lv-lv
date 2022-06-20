---
title: Sagatavošanās saglabāt ražotajiem krājumiem standarta izmaksas
description: Šajā rakstā ir aprakstīti soļi ražoto krājumu izmaksu uzturēšanai.
author: JennySong-SH
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 423da8022faf8066c5aa524c49c5071d0871de04
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886020"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Sagatavošanās saglabāt ražotajiem krājumiem standarta izmaksas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti soļi ražoto krājumu izmaksu uzturēšanai. Ražotajiem krājumiem veicamās darbības nedaudz atšķiras no iegādātajiem krājumiem izmantotajām darbībām.

Ražotajiem krājumiem piešķirtās politikas var ietekmēt ražoto vecākkrājumu izmaksu aprēķinus. Lai sagatavotos ražoto krājumu izmaksu uzturēšanai, veiciet tālāk aprakstītās darbības.

1. Piešķiriet ražotajam krājumam modeļa grupu. 

   Krājumu modeļa grupa identificē standarta izmaksu lietojumu.

2. Piešķiriet grupu ražotajam krājumam. 

   Krājuma grupa satur virsgrāmatas kontus, kas attiecas uz ražoto krājumu. Ražotā krājuma ar standarta izmaksu krājumu modeli virsgrāmatas konti ietver vairākas ražošanas novirzes, izmaksu maiņas novirzi un krājumu izmaksu pārvērtēšanu.

3. Piešķiriet šim krājumam mērvienību. 

   Krājumu izmaksas vienmēr tiek attēlotas krājumu mērvienībās.

4. Nepiešķiriet ražotajam krājumam izmaksu grupu, ja vien tas netiks uzskatīts par iegādātu krājumu.

5. Piešķiriet ražotajam krājumam materiālu komplekta (MK) aprēķinu grupu. 

   Krājuma MK aprēķinu grupa definē lietojamus brīdinājuma nosacījumus. Šādi, kad ir pabeigts MK aprēķins, var ģenerēt brīdinājuma ziņojumus par iespējamiem aprēķinu kļūdu avotiem. Piemēram, brīdinājuma ziņojums var identificēt gadījumu, kad nepastāv aktīvs MK vai maršruts. MK aprēķinu grupa ietver izvēršanas apturēšanas politiku, kas norāda, kad ražots krājums jāuzskata par iegādātu krājumu.

6. Ja ražotajam krājumam ir konstantas izmaksas, piešķiriet tam standarta pasūtījuma daudzumu. 

   Standarta pasūtījuma daudzums ir uzskaites laidiena apjoms konstantu izmaksu amortizēšanai. Konstantu izmaksu piemēri ietver maršrutēšanas operāciju iestatīšanas laiku un konstantu komponentu daudzumu materiālu komplektā.

7. Definējiet MK ražotajam krājumam. 

   Ražotajam krājumam var tikt definēta viena vai vairākas MK versijas. Apstipriniet, ka jums vajadzīgās versijas ir atzīmētas kā apstiprinātas un aktīvas un tām ir jums vajadzīgie spēkā stāšanās datumi. MK versija var būt uzņēmuma mēroga vai vietas mēroga.

8. Definējiet ražotā krājuma maršrutēšanu. 

   Ražotajam krājumam var tikt definēta viena vai vairākas maršruta versijas. Apstipriniet, ka jums vajadzīgās versijas ir atzīmētas kā apstiprinātas un aktīvas un tām ir jums vajadzīgie spēkā stāšanās datumi. Maršruta versijai jābūt vietas mēroga.

Ja maršrutēšanas informāciju vēlaties izmantot izmaksu aprēķināšanai, ir javeic papildu sagatavošanās soļi. Piemēram, maršrutēšanas operācijām piešķirtajām izmaksu kategorijām ir jābūt pareizām un pabeigtām.

## <a name="related-articles"></a>Saistītie raksti

[Ražotā krājuma konstanto izmaksu amortizācija](amortize-constant-costs-manufactured-item.md)

[Saražojamo vai sagādājamo preču iestatīšana](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]