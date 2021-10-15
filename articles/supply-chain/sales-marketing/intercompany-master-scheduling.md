---
title: Starpuzņēmumu vispārējā (grafika) plānošana
description: Šajā tēmā skaidrots starpuzņēmumu vispārējā (grafika) plānošana
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e28051097905503e291e0c15a50e9363b39b2daa
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548401"
---
# <a name="intercompany-master-scheduling"></a>Starpuzņēmumu vispārējā (grafika) plānošana

[!include [banner](../../includes/banner.md)]

Starpuzņēmumu vispārējā (grafika) plānošana ir paņēmiens, ar kuru tiek aprēķinātas vajadzības un veidoti plānotie starpuzņēmumu pasūtījumi starp vairākiem iekšējiem uzņēmumiem. Starpuzņēmumu vispārējā (grafika) plānošana tiek veikta ar norādīto atkārtojumu skaitu. Lai aktivizētu Microsoft Dynamics 365 Supply Chain Management veikt starpuzņēmumu vispārējo (grafika) plānošanu, jāiestata vispārējā (grafika) plānošana katrā no starpuzņēmumu uzņēmumiem. Tas izveido atkārtošanos skaitu, kur Microsoft Dynamics 365 Supply Chain Management automātiski izveido starpuzņēmumu pirkšanas pasūtījumu, un tas ved uz automātisku starpuzņēmumu pārdošanas pasūtījuma izveidi, kas atkal ved uz jaunām prasībām.

Iestatiet starpuzņēmumu vispārējo plānu un starpuzņēmumu plānošanas pasūtījumu **Vispārējās plānošanas** parametros katrā starpuzņēmumu uzņēmumā.

Lai ieviestu prasību visā starpuzņēmumu ķēdē, jāiestata parametri, lai nodrošinātu, ka plānotie pirkšanas pasūtījumi tiek automātiski apstiprināti, tas ir, pasūtījumus nevar mainīt pēc laika termiņiem vai daudzuma. Iestatiet **Apstiprināšanas periodu** vajadzību grupai vai **Apstiprināšanas periodu** Vispārējā plānā. Ja nav iestatīts neviens **Apstiprināšanas periods**, neviens starpuzņēmumu pirkšanas pasūtījums netiek izveidots automātiski. Tikai pirmā vispārējās (grafika) plānošanas izpilde rezultātā rodas plānotie pasūtījumi. Tomēr, tā kā nav izveidots neviens starpuzņēmumu pirkšanas pasūtījums, netiek izveidots neviens starpuzņēmumu pārdošanas pasūtījums un tādēļ vairs netiek izveidoti starpuzņēmumu pirkšanas pasūtījumi utt.

Startējot starpuzņēmuma vispārējo (grafika) plānošanu, Microsoft Dynamics 365 Supply Chain Management veic vienu vispārējo (grafika) plānošanu katrā starpuzņēmuma uzņēmumā, pēc tam veic otro vispārējo (grafika) plānošanu katrā starpuzņēmuma uzņēmumā utt., kamēr tiek sasniegts norādītais atkārtošanu skaits. Ir iespējams 30 atkārtošanu maksimums, bet, jo vairāk atkārtošanos izvēlas, jo ilgāk notiek plānošana.

Starpuzņēmumu vispārējo (grafika) plānošanu var sākt no jebkura starpuzņēmumu uzņēmuma, jo vispārējo (grafika) plānošanu uzņēmumos kontrolē starpuzņēmumu plānošanas secība, tas ir, pasūtījums, kurā programma nosaka prioritāti vispārējiem (grafika) plāniem starp katru starpuzņēmumu uzņēmumu. Tā kā starpuzņēmumu plānošanas (grafika) secība nosaka secību, kādā tiek veikta vispārējā (grafika) plānošana uzņēmumos, nav svarīgi, kur tiek sākta starpuzņēmumu vispārējā (grafika) plānošana. Katrā atkārtojumā pašreizējais uzņēmums tiek veikts pēdējais.

> [!NOTE]
> Vislabākā prakse ir ļaut vispārējo plānošanu sākt no viena Microsoft Dynamics 365 Supply Chain Management uzņēmuma.

Lapā **Starpuzņēmumu vispārējā plānošana** var sākt vispārējās (grafika) plānošanas secību, kas veic vispārējo (grafika) plānošanu pirmajā reizē ar principu vajadzības aprēķina atjaunināšanai, kas atlasīts pirmajā atkārtošanā visiem starpuzņēmuma uzņēmumiem. Tālākie atkārtojumi izmanto sekundāro principu, kas atlasīts nākamajai atkārtošanai, un šis princips tiek piemērots, kamēr ir sasniegts norādīto atkārtošanu skaits.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
