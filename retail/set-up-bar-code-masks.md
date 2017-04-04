---
title: "Svītrkodu masku iestatīšana"
description: "Šajā tēmā aprakstīts, kā iestatīt svītrkoda maskas rakstzīmes, svītru kodu maskas un kā piešķirt svītrkodu maskē ar svītrkodiem."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fe598799d52cacd84da775ac7ace8cf9a30ae5fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bar-code-masks"></a>Svītrkodu masku iestatīšana

Šajā tēmā aprakstīts, kā iestatīt svītrkoda maskas rakstzīmes, svītru kodu maskas un kā piešķirt svītrkodu maskē ar svītrkodiem.

<a name="set-up-bar-code-mask-characters"></a>Svītrkoda maskas rakstzīmju iestatīšana
-------------------------------

Svītrkodu maskas tiek izmantoti, lai izveidotu svītrkodus un ātri noteikt svītrkodus, tas ir ieskenēts pārdošanu (POS). Maskas, kas sastāv no burtiem, kas kalpo kā vietturi, kas norāda svītrkodiem, kas tiks izveidots formātā. Lai konfigurētu svītrkoda maska, jums nepieciešams iestatīt svītrkoda maskas rakstzīmes. Dodieties uz **mazumtirdzniecības un komercijas**&gt;**krājumu vadība**&gt;**svītrkodi un etiķetes**&gt;**maskas rakstzīmes**. Noklikšķiniet uz **New** lai izveidotu svītrkoda maskas rakstzīmes. Maskas rakstzīmes var izveidot, lai norādītu šādu svītrkoda datus.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Field**            | **Description**                                                                                                 |
| **Product**          | Vietturis produkta ID.                                                                                     |
| **Any number**       | Lieto, lai norādītu numuru, kas būs grūti kodē svītrkodus.                                                  |
| **Check digit**      | Norāda, ka svītrkoda maska svītru kodu formātu izmanto kontrolcipars apstiprināt derīgumu svītrkodu. |
| **Size digit**       | Norāda izmēru svītru kodu, kas izveidots preču varianta, kas ietver lielumu.                                 |
| **Color digit**      | Norāda krāsas svītru kodu, kas izveidots produkta varianta, kurā iekļauti krāsu.                               |
| **Style digit**      | Norāda stilu svītru kodu, kas izveidots preču varianta, kas ietver stilu.                             |
| **EAN license code** | EAN licences izsniegtas licences kodus EAN vietturis.                                                       |
| **Cena**            | Norāda cenu, jo cenu iegult svītrkodus.                                                                   |
| **Quantity**         | Norāda daudzumu daudzumu izlases svaru iegults svītrkodiem.                                                |
| **Employee**         | Norāda, ka svītrkoda segmenta darbinieka ID numuru, kas lietots svītrkodu POS pieteikšanās.                                  |
| **Customer**         | Norāda klienta ID segmentu.                                                                                  |
| **Datu ievades**       | *Vēl nav implementēts.*                                                                                          |
| **Discount code**    | Norāda atlaides kods svītru kodu, kas tiek izmantota, lai pievienotu atlaidi līdz punktam pārdošanas darījums             |
| **Dāvanu karte**        | Norāda, ka dāvanu kartes numurs, izdevēja vai maksājot ar dāvanu karti.                                               |
| **Loyalty card**     | Pievieno lojalitāte klienta darījumu un var tikt izmantotas, maksājot ar lojalitāti.                             |

## <a name="define-bar-code-masks"></a>Definētu svītrkodu maskas
Pēc svītrkodu maskas rakstzīmes ir norādīta nepieciešama svītrkodu maskas, dodieties uz **mazumtirdzniecības un komercijas**&gt;**krājumu vadība**&gt;**svītrkodi un etiķetes**&gt;**svītrkoda maska uzstādīšanas**. Šajā lapā varat definēt svītrkodu maskas, kas izmanto iepriekš norādītajām rakstzīmēm. Šīs maskas svītrkods tiks izmantots, kad ģenerē svītrkodus un būs arī palīdzēs noteikt svītrkodus skenēta POS.

1.  Noklikšķiniet uz **New** izveidot jaunu svītru kodu maskā.
2.  Ievadiet vērtības **masku ID** un **aprakstu** laukus un pēc tam atlasiet svītrkoda maska tips **tipa** lauks.
3.  Šajā **vispārējā** sadaļu, atlasiet vērtību **svītru kodu standarta** lauks un pēc tam norādiet svītrkodu prefikss, ja tas ir vajadzīgs.
4.  Šajā **svītrkoda maska segmenta** sadaļu, svītru kodu segmenti, kas tiks izmantota pievienojumprogramma jāizveido svītrkodu.

Kā, piemēram, lai izveidotu svītrkoda maska ar masku ID "Produkts", varētu rīkoties šādi:

1.  Izveidot jaunu svītru kodu masku un atlasiet tipu "Produkts".
2.  Atlasiet svītrkoda standartu, piemēram, kodu 39' '.
3.  Nodrošināt prefiksu izmantot, lai viegli identificētu svītru kods. Piemēram, "22".
4.  Pievienot maska segmentā. "Produkts" masku segmentā tiks izvēlēti.
5.  Garums nodrošina produktu segmentā, piemēram, "10". Garums ir jāatbilst produkta ID, ko parasti izmanto veikalā garumu. Maska tiek parādīts kā priekšskatījumu pārlūkprogrammā **vispārējā** sadaļu zem **maska**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Piešķirtu svītrkodus svītrkodu maskas
Svītrkodus maskas ir nepieciešams piešķirt svītrkodus, pirms tās var lietot. Turpinot iepriekšējo piemēru, lai piešķirtu svītrkoda maska svītru kodu, rīkojieties šādi:

1.  Dodieties uz **organizācijas administrācija**&gt;**Setup**&gt;**svītrkodus**. Noklikšķiniet uz **New** izveidot jaunu svītru kodu.
2.  Ievadiet vērtības **svītrkods****uzstādīšanas** un * uzstādīšanas * * laukus.
3.  Šajā **vispārējās** sadaļu, jo **svītrkoda tipu** lauku, atlasiet "Code 39". Šajā **maska****ID** lauku, atlasiet iepriekš izveidojis "Produkts" maska.
4.  Zem **Size**, ievadiet '12'.
5.  Click **Save**.

Svītrkoda maska tagad var izmantot, lai izveidotu produktu svītrkodus. Iepriekš aprakstītās darbības ir piemēri, kā, lai izveidotu svītrkoda maskas produktiem, bet tie arī parāda, kā izveidot svītrkodu maskas jebkuram citas atbalstītās svītrkoda tipu. Svītrkodu maskas, veidus un garuma būtu jāpielāgo izmantošanai konkrētā vidē.


