---
title: Ražotā krājuma konstanto izmaksu amortizācija
description: Ražota krājuma konstantas izmaksas atspoguļo operāciju iestatījumu laikus un komponentus ar konstantu daudzumu vai konstantu brāķa apjomu.
author: JennySong-SH
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: d466395859e19874183691e697c8aca3a774d359
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675408"
---
# <a name="amortize-constant-costs-for-a-manufactured-item"></a>Ražotā krājuma konstanto izmaksu amortizācija

[!include [banner](../includes/banner.md)]

Ražota krājuma konstantas izmaksas atspoguļo operāciju iestatījumu laikus un komponentus ar konstantu daudzumu vai konstantu brāķa apjomu. 

Kalkulēšanas laidiena apjoma jēdziens tiek izmantots, lai amortizētu šīs konstantās izmaksas ražota krājuma aprēķinātās izmaksās. Šim jēdzienam ir vairāki sinonīmi, viens no kuriem ir uzskaites laidiena apjoms. Amortizācijas konstantu izmaksu jēdzienam arī ir vairāki sinonīmi, viens no kuriem ir proporcionālas konstantas izmaksas.

Ražota krājuma uzskaites laidiena apjoma daudzums tiek izmantots materiālu komplekta (MK) aprēķinā. Daudzums ir atkarīgs no tā, kā jūs uzsākat un veicat MK aprēķinu, ko paskaidro turpmāk minētais:

-   Noklusējuma aprēķinu daudzums krājuma MK aprēķinā — Krājuma standarta pasūtījuma daudzums inventarizācijai darbojas kā tā uzskaites laidiena apjoms, bet pēc noklusējuma daudzuma vērtība var būt lielāka, lai atspoguļotu krājuma pasūtījuma daudzuma dalāmo. Krājuma standarta pasūtījuma daudzums un dalāmais var tikt definēti to noklusējuma pasūtījuma iestatījumos vai vietai noteiktos pasūtījuma iestatījumos.
-   Noteikts aprēķinu daudzums krājuma MK aprēķinā - Noteikts aprēķina daudzums darbojas kā krājuma kalkulēšanas laidiena apjoms. Aprēķina daudzums sākotnēji izmanto krājuma standarta pasūtījuma daudzumu, bet noklusējuma vērtību var manuāli pārlabot. Norādītais aprēķina daudzums atspoguļo uzskaites laidiena apjomu norādītajam krājumam un ražotiem komponentiem, kuriem ir ražošanas MK līnijas veids. Tas ir tāpēc, ka tiek pieņemts, ka komponenti tiks ražoti līdz noteiktam daudzumam. Uzskaites laidiena apjoms citiem ražotiem komponentiem, kuriem ir krājuma MK līnijas veids, atspoguļo to standarta pasūtījuma daudzumu.
-   Noteikts pasūtījuma veikšanas aprēķinu daudzums krājuma MK aprēķinā - Noteikts aprēķinu daudzums darbojas kā krājuma un tā ražoto komponentu kalkulēšanas laidiena apjoms, kad MK aprēķini izmanto pasūtījuma veikšanas izvēršanas režīmu. Tiek pieņemts, ka ražotie komponenti tiks ražoti līdz noteiktam daudzumam līdzīgi kā ražošanas komponents, kuram ir ražošanas MK līnijas veids.
-   Noteikts aprēķinu daudzums pasūtījumam noteiktā MK aprēķinā − Pasūtījumam noteiktu MK aprēķinu var veikt līnijas krājumam pārdošanas pasūtījumā, pārdošanas pieprasījumā vai pakalpojuma pasūtījumā. Noteiktais aprēķinu daudzums izmanto sākotnējā rindas elementa daudzumu, bet noklusējuma daudzumu var pārlabot. Jūs varat atlasīt, vai pasūtījumam noteiktais MK aprēķins izmanto pasūtījuma veikšanas vai daudzlīmeņu izvēršanas režīmu.

Ražoto krājumu amortizēto konstanto izmaksu aprēķinātais apjoms ir nosaukts par maksām.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]