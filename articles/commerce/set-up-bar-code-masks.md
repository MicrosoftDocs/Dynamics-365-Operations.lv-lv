---
title: Svītrkodu masku iestatīšana
description: Šajā rakstu ir aprakstīts, kā iestatīt svītrkoda maskas rakstzīmes, svītrkodu maskas un kā svītrkodiem piešķirt svītrkodu maskas.
author: BrianShook
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 97b490384cff27c60191a87dc623eb6a2ef868f0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853716"
---
# <a name="set-up-bar-code-masks"></a>Svītrkodu masku iestatīšana

[!include [banner](includes/banner.md)]

Šajā rakstu ir aprakstīts, kā iestatīt svītrkoda maskas rakstzīmes, svītrkodu maskas un kā svītrkodiem piešķirt svītrkodu maskas.

## <a name="set-up-bar-code-mask-characters"></a>Svītrkoda maskas rakstzīmju iestatīšana

Svītrkoda maskas tiek izmantotas, lai izveidotu svītrkodus un ātri identificētu svītrkodus, kuri tiek skenēti pārdošanas punktā (POS). Maskas sastāv no rakstzīmēm, kas darbojas kā vietturi, kuri norāda izveidojamo svītrkodu formātu. Lai konfigurētu svītrkoda masku, ir jāiestata svītrkoda maskas rakstzīmes. Dodieties uz **Retail un Commerce** &gt; **Krājumu pārvaldība** &gt; **Svītrkodi un uzlīmes** &gt; **Maskas rakstzīmes**. Noklikšķiniet uz **Jauns**, lai izveidotu svītrkoda maskas rakstzīmes. Maskas rakstzīmes nevar izveidot, lai norādītu šādus svītrkoda datus.

| Lauks            | apraksts |
|------------------|-------------|
| Prece          | Vietturis preces identifikatoram. |
| Jebkurš skaitlis       | Tiek izmantots, lai norādītu numuru, kas tiks stingri kodēts svītrkodos. |
| Kontrolcipars      | Norāda, ka svītrkoda formāts svītrkoda maskā izmanto kontrolciparu, lai apstiprinātu svītrkoda derīgumu. |
| Cipara lielums       | Norāda izmēru svītrkodā, kas izveidots preces variantam, kurā ietilpst izmērs. |
| Cipara krāsa      | Norāda krāsu svītrkodā, kas izveidots preces variantam, kurā ietilpst krāsa. |
| Cipara stils      | Norāda stilu svītrkodā, kas izveidots preces variantam, kurā ietilpst stils. |
| EAN licences kods | Vietturis EAN licencei, kas izdota EAN licences kodiem. |
| Cena            | Norāda cenu svītrkodos, kuros iegulta cena. |
| Daudzums         | Norāda daudzumu svītrkodos, kuros iegults daudzums/nejaušs svars. |
| Darbinieks         | Norāda svītrkoda segmentu darbinieka ID numuram, kas tiek izmantots, lai veiktu POS pieteikšanos ar svītrkodu. |
| Debitors         | Norāda debitora ID segmentu. |
| Datu ievade       | *Vēl nav ieviests.* |
| Atlaides kods    | *Novecojis*, sākot ar Dynamics 365 for Retail 2017. gada pavasara laidienu. Iepriekš: norāda atlaižu kodu svītrkodam, kas tiek izmantots, lai pievienotu atlaidi pārdošanas punkta transakcijai. |
| Kupona kods      | Norāda svītrkoda kupona kodu, kas izmantots, lai pievienotu atlaidi pasūtījumam. Tas aizstāja atlaides kodu. |
| Dāvanu karte        | Norāda dāvanu kartes numuru, izdodot dāvanu karti vai veicot ar to apmaksu. |
| Lojalitātes programmas karte     | Pievieno transakcijai lojalitātes programmas debitoru, un to var izmantot, veicot maksājumu lojalitātes programmas ietvaros. |

## <a name="define-bar-code-masks"></a>Noteikt svītrkoda maskas

Pēc svītrkoda maskas rakstzīmju norādīšanas nepieciešamajām svītrkoda maskām, dodieties uz **Retail un Commerce** &gt; **Krājumu pārvaldība** &gt; **Svītrkodi un uzlīmes** &gt; **Svītrkoda maskas iestatīšana**. Šajā lapā varat definēt svītrkoda maskas, kurās tiek izmantotas iepriekš norādītās rakstzīmes. Šīs svītrkoda maskas tiks izmantotas, izveidojot svītrkodus un arī palīdzēs identificēt svītrkodus, kuri tiek skenēti POS.

1. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu svītrkoda masku.
2. Ievadiet vērtības laukā **Maskas ID** un **Apraksts** un pēc tam atlasiet svītrkoda maskas tipu laukā **Tips**.
3. Sadaļā **Vispārīgi** atlasiet vērtību laukā **Svītrkoda standarts** un pēc tam norādiet svītrkoda prefiksu, ja tas ir nepieciešams.
4. Sadaļā **Svītrkoda maskas segments** pievienojiet svītrkoda segmentus, kuri tiks izmantoti veidojamajā svītrkodā.

Piemēram, lai izveidotu svītrkoda masku ar maskas ID “Prece”, jāveic šādas darbības:

1. Izveidojiet jaunu svītrkoda masku un atlasiet tipu “Prece”.
2. Atlasiet svītrkoda standartu, piemēram, “Kods 39”.
3. Norādiet prefiksu, kas tiks izmantots, lai viegli identificētu svītrkodu. Piemēram, “22”.
4. Pievienojiet maskas segmentu. Tiks atlasīts maskas segments “Prece”.
5. Norādiet preces segmenta garumu, piemēram, “10”. Garumam ir jāatbilst veikalā parasti izmantotā produkta ID garumam. Maska tiks parādīta kā priekšskatījums vienuma **Maska** sadaļā **Vispārīgi**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Svītrkoda masku piešķiršana svītrkodiem

Svītrkoda maskas ir jāpiešķir svītrkodiem, pirms tos var izmantot. Turpinot iepriekš minēto piemēru, lai piešķirtu svītrkoda masku svītrkodam, jāveic šādas darbības:

1. Dodieties uz **Organizācijas administrēšana** &gt; **Iestatīšana** &gt; **Svītrkodi**. Noklikšķiniet uz **Jauns**, lai izveidotu jaunu svītrkodu.
2. Ievadiet vērtības laukos **Svītrkodu** **iestatījumi** un **Iestatījumi**.
3. Sadaļas **Vispārīgi** laukā **Svītrkoda tips** atlasiet “Kods 39”. Laukā **Maskas** **ID** atlasiet iepriekš izveidoto masku “Prece”.
4. Sadaļā **Izmērs** ievadiet “12”.
5. Noklikšķiniet uz **Saglabāt**.

Svītrkoda masku var izmantot, lai izveidotu svītrkodus precēm. Minētās darbības ir piemēri, kā izveidot svītrkoda maskas precēm, taču tās arī norāda, kā izveidot svītrkoda maskas visiem pārējiem atbalstītajiem svītrkodu tipiem. Svītrkodu maskas, tipi un garumi jāpielāgo izmantošanai attiecīgajā vidē.


[!INCLUDE[footer-include](../includes/footer-banner.md)]