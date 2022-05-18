---
title: Konfigurēt dzīves notikumu veidus
description: Microsoft Dynamics 365 Human Resources izmanto dzīves notikumu veidus, lai definētu notikumus, kas ir atļauts atjaunināt darbinieku atvieglojumu reģistrāciju.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 64e536bad996e9a1948dad18437ec6f98ad27033
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691727"
---
# <a name="configure-life-event-types"></a>Konfigurēt dzīves notikumu veidus


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources lieto **dzīves notikumu tipus**, lai noteiktu notikumus, kuros ir derīgi atjaunināt darbinieka atvieglojumu reģistrāciju, piemēram, iegūt precēšanos vai bērnu. Katru dzīves notikuma veida ID var saistīt tikai ar vienu dzīves notikuma veidu. Piemēram, ja izveidojat dzīves notikuma **ID** **·** **ar nosaukumu Adreses maiņa,** kas ir saistīts ar dzīves notikuma tipu Darbinieka adreses maiņa, nevar izveidot citu **ID** **ar iezīmi Darbinieka adreses maiņa un saistīt to ar dzīves notikuma tipu Darbinieka adreses maiņa.** Ja dzīves notikuma tips nav saistīts ar plāna tipu, dzīves notikuma tips neaktivizē dzīves notikumu. Papildu informāciju skatiet sadaļā [Plānu veidu izveide](hr-benefits-setup-plan-types.md).

## <a name="create-a-life-event-type"></a>Izveidot dzīves notikuma veidu

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Dzīves notikumu veidi**.

2. Atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Dzīves notikuma veida ID** | Dzīves notikuma veida unikālais identifikators. |
   | **Apraksts** | Dzīves notikuma veida apraksts. |
   | **Dzīves notikuma veids** | Katalizators, lai atjauninātu darbinieka atvieglojumu reģistrāciju. Lai skatītu dzīves notikumu sarakstu, skatiet zemāk esošo sadaļu [Dzīves notikumi](hr-benefits-setup-payment-frequencies.md?life-events). |

4. Atlasiet **Saglabāt**.

## <a name="view-attached-plans"></a>Skatiet pievienotos plānus

Var skatīt plānu sarakstu, kas pievienoti atlasītajam dzīves **notikuma tipam**. Dzīves notikumi ir pievienoti plāna veidam, un plāna veidi ir saistīti ar plānu.

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Dzīves notikumu veidi**.

2. Atlasiet **Darbības**.

3. Atlasiet **Pievienotie plāni**.

## <a name="life-events"></a>Dzīves notikumi

Kad izveidojat dzīves notikuma veidu, varat izvēlēties kādu no tālāk norādītajiem dzīves notikumiem:

| Dzīves notikums | Vieta | Trigeris |
| --- | --- | --- |
| **Ģimenes stāvokļa maiņa** | **Darbinieks > Profils > Personiskā informācija > Ģimenes stāvoklis**| Ģimenes stāvokļa maiņa |
| **Nodarbinātības statusa maiņa** |**Darbinieku > nodarbinātības > vēstures lapa** | Darbiniekam ar detalizētu informāciju par nodarbinātību, izveidojot jaunu detalizēto informāciju par nodarbinātību ar citu nodarbinātības statusu, tiks izraisīts dzīves notikums.  Esošas nodarbinātības detaļu atjaunināšana ar citu nodarbinātības statusu arī izraisīs dzīves notikumu.  |
| **Darbinieka adreses maiņa** |**Nodarbinātais > Profils > Adreses**</li><li>**Nodarbinātais > Personiskā informācija > Personiskie kontakti > Adrese**</li></ul> | Izmaiņas adresē. Lai izraisītu dzīves notikumu, adresei ir jābūt **Primārai**. |
| **Pakārtotā maiņa** |<br><ul><li>**Darbinieka >, > informāciju par personu> personas kontaktinformācija**/li><li>**Darbinieku patstāvīgi izmantojamais pakalpojums**</li></ul> | Pievienojiet personīgo kontaktpersonu, kas norāda to kā apgādājamo, un definējot **Spēkā no**. Atjauniniet personīgās kontaktpersonas apgādājamā **Derīgs līdz** informāciju. Personisko kontaktpersonu attiecībām ir jābūt bērnam, dzīvesbiedram, dzīvesbiedram vai bijušajam dzīvesbiedram.  |
| **Dzimšana vai adopcija (pakārtotais)** |<br><ul><li>**Nodarbinātais >Profils > Personiskā informācija > Personiskie kontakti**</li><li>**Darbinieku pašapkalpošanās > Rediģēt personas datus > Personīgā pontaktpersona**</li></ul>| **Dzimšanas datums** vai **Papildu datums** tiek pievienots vai atjaunināts. Ir jānorāda bērna **Dzimšanas datums**. |
| **Vajadzības zaudēšana (laulātais/dzīvesbiedrs)** | Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Vajadzības zudums | **Vajadzības zudums** atlasīts personiskajai kontaktpersonai kopā ar **Spēkā stāšanās datumu** |
| Dzīvesbiedra nodarbinātības izmaiņas | **Nodarbinātais > Profils > Personiskā informācija > Personīgās kontaktpersonas > Informācija par pakārtoto > Nodarbināts** | Tiek radīta personīgā kontaktpersona un iestatījums **Nodarbināts** uz **Jā**. Personīgās kontaktpersonas atjaunināšana un **Nodarbinātā** mainīšana.  |
| **Atvaļinājums (laulātais/dzīvesbiedrs)** | **Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Pakārtotā informācija > Atvaļinājums** | Izveidota personīgā kontaktpersona un ir noteikts **Atvaļinājuma spēkā stāšanās datums**. Personīgā kontaktpersona **Prombūtne** ir atjaunināts. Personīgā kontaktpersona **Prombūtnes spēkā stāšanās datums** ir atjaunināts.  |
| **Vajadzības izmaiņas (amats)** |<br><ul><li>**Nodarbinātais > Amata piešķire > Nodarbinātā amata piešķires**</li><li>**Amati > Amati**</li></ul>| Mainīt uz pozīciju darbinieka amata piešķires ierakstos. Nodarbinātā amata piešķires maiņa. |
| **Vajadzības izmaiņas (alga)** |<br><ul><li>**Nodarbinātais > Atlīdzība > Fiksētais plāns**</li><li>**Darbinieks > Personīgā informācija > Atvieglojumu gada alga**</li></ul>| Ja **atvieglojumu pārvaldība > Cilvēkresursu kopīgie parametri > nav iespējoti >** Atvieglojumu gada alga, **atjauninot darbinieka > atlīdzības >** fiksētais plāns izveidos dzīves notikumu. Ja **atvieglojumu pārvaldība > Cilvēkresursu kopīgie parametri > Atvieglojumi >** Ir aktivizēta atvieglojumu gada alga, **atjaunina darbinieka > Personīgā informācija >** Atvieglojumu gada alga izveidos dzīves notikumu. |
| **Medicīniskā aprūpe (darbinieks/pakārtotais)** | **Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Pakārtotā informācija > Medicīniskās aprūpes spēkā stāšanās datums** | Pievienojot vai atjauninot **Medicare spēkā stāšanās** datumu personiskām kontaktpersonām, tiek izveidots šis dzīves notikums. |
| **Ar tiesu piespriests atbalsts** | **Darbinieka > profils > personisko informāciju > personas kontaktiem > pakārtotā > Tiesas** pasūtīts atbalsts (QMSCO/QDRO) un efektīvos datumus | Veidojot personisku kontaktpersonu, tiks izveidots dzīves notikums, ja **Tiesas pasūtītais atbalsts** ir **Jā**. Atjauninot **Tiesas pasūtīto atbalstu** vai **Tiesas pasūtīto beigu datumu**, tiks izraisīts arī dzīves notikums. |
| **Miris** | **Nodarbinātais > Profils > Personiskā informācija > Miršanas datums** | Ir ievadīts vai atjaunots **Beigu datums**. |
| **Apliecinājums par apdrošināšanu** | **Nodarbinātais > Nodarbinātais > Versijas > Nodarbinātības vēsture > Datumu pārvaldnieka > Informācija par atvieglojumiem** | **Piestātības apliecinājums** ir iestatīts uz **Jā**. **Pierādījumi par apdrošināmības pārbaudes datumu** ir definēts. |
| **Saņēmējs** | **Nodarbinātais >Profils > Personiskā informācija > Personiskie kontakti** | Tiek pievienota personīgā kontaktpersona un ir aizpildīts lauks **Saņēmējs** un **Spēkā stāšanās datums**. Personiskajai kontaktpersonai ir jābūt ar veidu **Bērns**, **Laulātais**, **Dzīvesbiedrs**, **Atvase**, **Ģimenes kontaktpersona**, **Cita kontaktpersona** vai **Vecāks**. |
| **Darbinieka medicīniskā aprūpe** | **Nodarbinātais > Nodarbinātais > Versijas > Nodarbinātības vēsture > Datumu pārvaldnieka > Informācija par atvieglojumiem** | **Medicare atbilstošs** ir iestatīts uz **Jā**. **Medicare atbilstības datums** ir mainīts. |
| **Dzimšanas diena** | **Atvieglojumu pārvaldība > Dzīves notikumu izmaiņu apstrāde** | Šie dzīves notikumi tiek izveidoti no **Dzīves notikumu izmaiņu apstrādes**. Šis process analizē izvēlēto periodu un juridisko personu un atrod saistītos darbiniekus. Tas aprēķina viņu pēdējo dzimšanas dienu un izveido dzimšanas dienas notikumu, ja tas vēl nav izveidots. |
| **Nodarbinātā piemērojamības izmaiņas (nav noteiktas ASV)** |<br><ul><li>**Nodarbinātais > Nodarbinātība**</li><li>**Nodarbinātais > Nodarbinātais > Versijas > Nodarbinātības vēsture**</li></ul>| Izveido dzīves notikumu, kad:<br><ul><li>Izveidojot jaunu darba vietu, un ir iepriekšējā darba vieta, un darba ņēmēja tips mainās.</li><li>Izveidojot jaunu darba vietas informāciju, un ir iepriekšējā darba vietas informācija, un darba vietas tips vai darba vietas kategorija mainās.</li><li>Tiek atjaunināti darba vietas ieraksti un definēts cits darbinieka tips.</li><li>Tiek atjaunināts darba vietas detalizētas informācijas ieraksts un ir norādīts cits darba vietas tips vai kategorija.</li></ul> |
| **Jaunas piemērojamības labošana (ne ASV)** | **Papildu cilvēkresursi > Atvieglojumi > Plāni > Atvieglojumi > Piemērotības nosacījumu labošana** | Dzīves notikumu apstrādes lietošana<br>Izveidojot jaunu atvieglojumu plāna piemērotības ignorējumu darbiniekam, tiek izraisīts šis dzīves notikums.<br>BenefitEligibilityRuleOverride.ValidFrom. |
| **Piemērojamības kārtulas labošanas maiņa (ne ASV)** | **Papildu cilvēkresursi > Atvieglojumi > Plāni > Atvieglojumi > Piemērotības nosacījumu labošana** | Atjauninot atvieglojumu plāna piemērotības ignorēšanu **Derīgs no** vai **Derīgs līdz**, šī dzīves notikums tiek izraisīts. |
| **Piemērojamības kārtulas labošanas termiņa beigas (ne ASV)** | Atvieglojumu pārvaldība > Dzīves notikumu izmaiņu apstrāde  | Šie dzīves notikumi tiek izveidoti no **Dzīves notikumu izmaiņu apstrādes**. Šis process analizē izvēlēto periodu un juridisko personu un atrod saistītos atvieglojumu plāna atbilstības pārlabojumus. Tas izveido dzīves notikumus, ja ignorēšanai ir beidzies termiņš. |
| **Jauns atvieglojumu plāns (nav ASV)** | **Papildu cilvēkresursi > Atvieglojumi > Plāni > Jauns** | Piemērojamības opcijas tiek pievienotas pašreizējam plānam. Ir pievienots jauns plāns ar pievienotām piemērojamības opcijām.</br></br>Cilvēkresursu personālam vajadzētu šajā instancē palaist dzīves notikuma piemērojamības apstrādi |
| **Piemērojamības kārtulas maiņa (ne ASV)** | **Atvieglojumu pārvaldība > Piemērotības nosacījumi** | Dzīves notikumu piemērojamības apstrādes izmantošana. Reģistrēti, ja **BenefitEligibilityRule** ierakstiem ir mainītas šādas vērtības: **UseEmplCategory**, **UseEmplStatus** vai **UseEmplType**. Atjaunina tikai dzīves notikuma darbības, kas jau pastāv mainītai kārtulai vai piemērojamības kritērijam. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
