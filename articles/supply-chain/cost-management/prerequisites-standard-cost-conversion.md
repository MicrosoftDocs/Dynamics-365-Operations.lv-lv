---
title: Standarta izmaksu konvertēšanas priekšnoteikumi
description: Šajā rakstā ir apskatīti uzdevumi, kas jāveic pirms standarta izmaksu pārveidošanas palaišanas.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 50891
ms.assetid: 73af66cf-c924-45be-837a-a648dbd05a31
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9295269c9979fb693d6f2976d4960a799d88f5ca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887563"
---
# <a name="prerequisites-for-a-standard-cost-conversion"></a>Standarta izmaksu konvertēšanas priekšnoteikumi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir apskatīti uzdevumi, kas jāveic pirms standarta izmaksu pārveidošanas palaišanas. 

Pirms veicat standarta izmaksu konvertēšanu, izpildiet šīs darbības:

1.  Definējiet standarta izmaksu **krājumu modeļu grupu**. Izmantojiet lapu Krājumu modeļu grupas, lai izveidotu krājumu modeļu grupu, kas izmanto standarta izmaksu krājumu modeli. Iestatot standarta izmaksu konvertēšanu, šī krājumu modeļu grupa ir jāpiešķir krājumiem, kas tiek konvertēti.
2.  Piešķiriet katram krājumam **izmaksu grupu**.
    -   Pamatojoties uz krājumu grupu, kas ir piešķirta nopirktajam krājumam, var piešķirt virsgrāmatas kontus, kas ir saistīti ar standarta izmaksām. Tostarp var piešķirt pirkšanas cenu novirzes virsgrāmatas kontus. Ražošanas vidē izmaksu grupa, kas tikusi piešķirta iegādātajiem elementiem, nodrošina arī izmaksu segmentāciju saražotā krājuma aprēķinātajās izmaksās.
    -   Izmaksu grupa, kas tikusi piešķirta saražotajam krājumam, var darboties kā pamats virsgrāmatas kontu piešķiršanai, kas ir saistīti ar standarta izmaksām, piemēram, virsgrāmatas kontu piešķiršana ražošanas variācijām.

3.  Piešķiriet **standarta pasūtījuma daudzumu** saražotajam krājumam, ja tam ir konstantas izmaksas. Saražotā krājuma standarta pasūtījuma daudzums tiek izmantots kā uzskaites laidiena apjoms konstanto izmaksu amortizācijai vai likmes noteikšanai. Tas var attiekties uz maršrutēšanas operāciju iestatīšanas laiku vai konstantu komponentu daudzumu materiālu komplektā (MK).
4.  Piešķiriet **virsgrāmatas kontus**, kas ir saistīti ar standarta izmaksām, it īpaši pārvērtēšanas novirzi. Izmantojiet lapu **Grāmatošana** (**Krājumu pārvaldība** &gt; **Iestatījumi**), lai piešķirtu Virsgrāmatas kontus, kas ir saistīti ar standarta izmaksām. Kā standarta izmaksu pārveidošanas procesa minimumu, ir jāpiešķir kontu pārvērtēšanas variācijai visiem krājumiem un visām izmaksu grupām. Izmantojiet lapu **Kontu diagramma**, lai definētu virsgrāmatas kontus, kas būs nepieciešami standarta izmaksām. Lietojiet lapu **Darbību kombinācijas**, lai iespējotu izmaksu attiecības (tabulām, grupām un visiem elementiem) pirms krājumu grāmatošanas kārtulu definēšanas.
5.  Definējiet krājumu parametrus, kas ir saistīti ar standarta izmaksām. Izmantojiet cilmi **Numuru sērijas** lapā **Krājumu un noliktavas vadības parametri**, lai piešķirtu numuru sēriju pārvērtēšanas dokumentiem. Pārvērtēšanas dokuments tiek ģenerēts, kad standarta izmaksu konvertēšana izraisa krājuma vērtības izmaiņas. Izmantojiet lapu **Krājumu un noliktavas vadības parametri**, lai definētu izmaksu kontroles parametrus (cilnē **rājumu uzskaite**), definējot divus parametrus, kas ir saistīti ar standarta izmaksām.
    -   Laukā **Izmaksu sadalījums** atlasiet opciju Nav vai Palīggrāmata. Ja tiek atlasīta opcija Palīggrāmata, tiek izmantots aktīvs izmaksu sadalījums. Aktīvs izmaksu sadalījums ir ļoti svarīgs priekšnoteikums, lai aprēķinātu, uzturētu un skatītu standarta izmaksu krājumu izmaksu grupu segmentāciju daudzlīmeņu struktūrā. Ja izmaksu sadalījums ir aktīvs, varat ietvert pārskatos un analizēt tālāk norādīto informāciju vienlīmeņa, daudzlīmeņu vai kopējā formāta.
        1.  Krājumi
        2.  Resursi nepabeigtajā ražošanā (RNR)
        3.  Pārdoto preču pašizmaksa (PPPI) pēc izmaksu grupas

        Aktīvs izmaksu sadalījums nozīmē to, ka, iespējojot saražotā krājuma izmaksas, rezultāts tiek saglabāts izmaksu grupas segmentā krājuma izmaksu ierakstā. Ja nenoradāt vērtību laukā **Izmaksu sadalījums**, standarta izmaksu krājumiem netiek uzturēta izmaksu grupas segmentācija. T.i., saražoto krājumu standarta cena tiks aprēķināta un pielietota kā viena summa bez izmaksu grupas segmentācijas un saražoto elementu izmaksu ieguldījums tiks apvienots vienā summā.
    -   Izmantojiet lauku **Novirzes no standarta**, lai atlasītu apkopoto novirzi vai novirzi pēc izmaksu grupas. Ja atlasāt novirzi pēc izmaksu grupas, varat norādīt pirkšanas cenas novirzes un ražošanas novirzes pēc izmaksu grupas. Tas ļauj arī norādīt četrus ražošanas novirzes vidus (laidiena lieluma, daudzuma, cenas un aizvietošanas novirzes). Ja atlasāt apkopoto novirzi, nevarat norādīt novirzes pēc izmaksu grupas un četrus ražošanas novirzes veidus. Ir iespējams tikai apskatīt apkopoto produkcijas novirzi. Ierobežojumi attiecībā uz novirzēm no standarta ir neatkarīgi no izmaksu sadalījuma ierobežojumiem. T.i., ir iespējams atlasīt tikai izmaksu sadalījumu ierobežojumu un atlasīt novirzes pēc izmaksu grupas, tā, lai produkcijas novirzes pēc izmaksu grupas joprojām tiks paturētas.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]