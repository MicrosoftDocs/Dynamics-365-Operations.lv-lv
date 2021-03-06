---
title: Sagatavošanās saglabāt ražotajiem krājumiem standarta izmaksas
description: Šajā tēmā aprakstītas darbības, kas jāveic, lai sagatavotos ražoto krājumu izmaksu uzturēšanai.
author: AndersGirke
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
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a82b0a205ac6b7a86b9aca0771303469c6666c1
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187750"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Sagatavošanās saglabāt ražotajiem krājumiem standarta izmaksas

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstītas darbības, kas jāveic, lai sagatavotos ražoto krājumu izmaksu uzturēšanai. Ražotajiem krājumiem veicamās darbības nedaudz atšķiras no iegādātajiem krājumiem izmantotajām darbībām.

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

## <a name="related-topics"></a>Saistītās tēmas

[Ražotā krājuma konstanto izmaksu amortizācija](amortize-constant-costs-manufactured-item.md)

[Saražojamo vai sagādājamo preču iestatīšana](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]