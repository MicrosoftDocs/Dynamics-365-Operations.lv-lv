---
title: Konfigurēt dzīves notikumu tipus
description: Microsoft Dynamics 365 Human Resources izmanto dzīves notikumu veidus, lai definētu notikumus, kas ir atļauts atjaunināt darbinieku atvieglojumu reģistrāciju.
author: andreabichsel
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44a6848b4a3ed6d5dd00ade27d18cce405f09f94284de4bd39c4c9441abfcd8a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732829"
---
# <a name="configure-life-event-types"></a>Konfigurēt dzīves notikumu tipus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources izmanto dzīves notikumu veidus, lai definētu notikumus, kas ir atļauts atjaunināt darbinieku atvieglojumu reģistrāciju, piemēram, precēšanos vai dzemdības. Katru dzīves notikuma veida ID var saistīt tikai ar vienu dzīves notikuma veidu. Piemēram, ja izveidojat dzīves notikuma ID, sauktu par adreses maiņu, kas saistīts ar dzīves notikuma veidu Darbinieka adreses maiņa, nevar izveidot citu ID ar nosaukumu Darbinieka adreses maiņa un saistīt to ar dzīves notikuma veidu Darbinieka adreses maiņa. Ja dzīves notikuma tips nav saistīts ar plāna tipu, dzīves notikuma tips neaktivizē dzīves notikumu. Papildu informāciju skatiet sadaļā [Plānu veidu izveide](hr-benefits-setup-plan-types.md).

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

Varat redzēt sarakstu ar plānie, kas ir pievienoti atlasītajam dzīves notikuma veidam. Dzīves notikumi ir pievienoti plāna veidam, un plāna veidi ir saistīti ar plānu.

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Dzīves notikumu veidi**.

2. Atlasiet **Darbības**.

3. Atlasiet **Pievienotie plāni**.

## <a name="life-events"></a>Dzīves notikumi

Kad izveidojat dzīves notikuma veidu, varat izvēlēties kādu no tālāk norādītajiem dzīves notikumiem:

| Dzīves notikums | Vieta | Trigeris |
| --- | --- | --- |
| **Ģimenes stāvokļa maiņa** | Darbinieks > Profils > Personiskā informācija > Ģimenes stāvoklis| Ģimenes stāvokļa maiņa |
| **Nodarbinātības statusa maiņa** | Nodarbinātais > Nodarbinātība<br>Nodarbinātības vēstures lapa | Darbiniekam ar detalizētu informāciju par nodarbinātību, izveidojot jaunu detalizēto informāciju par nodarbinātību ar citu nodarbinātības statusu, tiks izraisīts dzīves notikums.  Esošas nodarbinātības detaļu atjaunināšana ar citu nodarbinātības statusu arī izraisīs dzīves notikumu.  |
| **Darbinieka adreses maiņa** | Nodarbinātais > Profils > Adreses<br>Nodarbinātais > Personiskā informācija > Personiskie kontakti > Adrese | Izmaiņas adresē. Lai izraisītu dzīves notikumu, adresei ir jābūt primārai. |
| **Pakārtotā maiņa** | Nodarbinātais >Profils > Personiskā informācija > Personiskie kontakti<br>Darbinieku patstāvīgi izmantojamais pakalpojums | Pievienojiet personīgo kontaktpersonu, kas norāda to kā apgādājamo, un definējot **Spēkā no**. Atjauniniet personīgās kontaktpersonas apgādājamā **Derīgs līdz** informāciju. Personisko kontaktpersonu attiecībām ir jābūt bērnam, dzīvesbiedram, dzīvesbiedram vai bijušajam dzīvesbiedram.  |
| **Dzimšana vai adopcija (pakārtotais)** | Nodarbinātais >Profils > Personiskā informācija > Personiskie kontakti<br>Darbinieku pašapkalpošanās > Rediģēt personas datus > Personīgā pontaktpersona | **Dzimšanas datums** vai **Papildu datums** tiek pievienots vai atjaunināts. Ir jānorāda bērna **Dzimšanas datums**. |
| **Vajadzības zaudēšana (laulātais/dzīvesbiedrs)** | Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Vajadzības zudums | **Vajadzības zudums** atlasīts personiskajai kontaktpersonai kopā ar **Spēkā stāšanās datumu** |
| Dzīvesbiedra nodarbinātības izmaiņas | Nodarbinātais > Profils > Personiskā informācija > Personīgās kontaktpersonas > Informācija par pakārtoto > Nodarbināts | Tiek radīta personīgā kontaktpersona un iestatījums **Nodarbināts** uz **Jā**. Personīgās kontaktpersonas atjaunināšana un **Nodarbinātā** mainīšana.  |
| **Atvaļinājums (laulātais/dzīvesbiedrs)** | Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Pakārtotā informācija > Atvaļinājums | Izveidota personīgā kontaktpersona un ir noteikts **Atvaļinājuma spēkā stāšanās datums**. Personīgā kontaktpersona **Prombūtne** ir atjaunināts. Personīgā kontaktpersona **Prombūtnes spēkā stāšanās datums** ir atjaunināts.  |
| **Vajadzības izmaiņas (amats)** | Nodarbinātais > Amata piešķire > Nodarbinātā amata piešķires<br>Amati > Amati | Mainīt uz pozīciju darbinieka amata piešķires ierakstos. Nodarbinātā amata piešķires maiņa. |
| **Vajadzības izmaiņas (alga)** | Nodarbinātais > Atlīdzība > Fiksētais plāns<br>Darbinieks > Personīgā informācija > Atvieglojumu gada alga | Ja atvieglojumu pārvaldība > Personāla vadības kopīgie parametri > Atvieglojumi > Nav iespējota atvieglojumu gada alga, atjauninot Darbinieks > Atlīdzība > Fiksētais plāns izveidos dzīves notikumu. Ja atvieglojumu pārvaldība > Personāla vadības kopīgie parametri > Atvieglojumi > Ir iespējota atvieglojumu gada alga, atjauninot Darbinieks > Personīgā informācija > Atvieglojumu gada alga izveidos dzīves notikumu. |
| **Medicīniskā aprūpe (darbinieks/pakārtotais)** | Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Pakārtotā informācija > Medicīniskās aprūpes spēkā stāšanās datums | Pievienojot vai atjauninot **Medicare spēkā stāšanās** datumu personiskām kontaktpersonām, tiek izveidots šis dzīves notikums. |
| **Ar tiesu piespriests atbalsts** | Nodarbinātais > Profils > Personiskā informācija > Personiskie Kontakti > Pakārtotie > Atbalsts pēc tiesas prasības (QMSCO/QDRO un spēkā stāšanās datumi | Veidojot personisku kontaktpersonu, tiks izveidots dzīves notikums, ja **Tiesas pasūtītais atbalsts** ir **Jā**. Atjauninot **Tiesas pasūtīto atbalstu** vai **Tiesas pasūtīto beigu datumu**, tiks izraisīts arī dzīves notikums. |
| **Miris** | Nodarbinātais > Profils > Personiskā informācija > Miršanas datums | Ir ievadīts vai atjaunots miršanas datums. |
| **Apliecinājums par apdrošināšanu** | Nodarbinātais > Nodarbinātais > Versijas > Nodarbinātības vēsture > Datumu pārvaldnieka > Informācija par atvieglojumiem | **Piestātības apliecinājums** ir iestatīts uz **Jā**. **Pierādījumi par apdrošināmības pārbaudes datumu** ir definēts. |
| **Saņēmējs** | Nodarbinātais >Profils > Personiskā informācija > Personiskie kontakti | Tiek pievienota personīgā kontaktpersona un ir aizpildīts lauks **Saņēmējs** un **Spēkā stāšanās datums**. Personiskajai kontaktpersonai ir jābūt ar veidu **Bērns**, **Laulātais**, **Dzīvesbiedrs**, **Atvase**, **Ģimenes kontaktpersona**, **Cita kontaktpersona** vai **Vecāks**. |
| **Darbinieka medicīniskā aprūpe** | Nodarbinātais > Nodarbinātais > Versijas > Nodarbinātības vēsture > Datumu pārvaldnieka > Informācija par atvieglojumiem | **Medicare atbilstošs** ir iestatīts uz **Jā**. **Medicare atbilstības datums** ir mainīts. |
| **Dzimšanas diena** | Atvieglojumu pārvaldība > Dzīves notikumu izmaiņu apstrāde | Šie dzīves notikumi tiek izveidoti no **Dzīves notikumu izmaiņu apstrādes**. Šis process analizē izvēlēto periodu un juridisko personu un atrod saistītos darbiniekus. Tas aprēķina viņu pēdējo dzimšanas dienu un izveido dzimšanas dienas notikumu, ja tas vēl nav izveidots. |
| **Nodarbinātā piemērojamības izmaiņas (nav noteiktas ASV)** | Nodarbinātais > Nodarbinātība<br>Nodarbinātais > Nodarbinātais > Versijas > Nodarbinātības vēsture | Izveido dzīves notikumu, kad:<br><ul><li>Izveidojot jaunu darba vietu, un ir iepriekšējā darba vieta, un darba ņēmēja tips mainās.</li><li>Izveidojot jaunu darba vietas informāciju, un ir iepriekšējā darba vietas informācija, un darba vietas tips vai darba vietas kategorija mainās.</li><li>Tiek atjaunināti darba vietas ieraksti un definēts cits darbinieka tips.</li><li>Tiek atjaunināts darba vietas detalizētas informācijas ieraksts un ir norādīts cits darba vietas tips vai kategorija.</li></ul> |
| **Jaunas piemērojamības labošana (ne ASV)** | Papildu cilvēkresursi > Atvieglojumi > Plāni > Atvieglojumi > Piemērotības nosacījumu labošana | Dzīves notikumu apstrādes lietošana<br>Izveidojot jaunu atvieglojumu plāna piemērotības ignorējumu darbiniekam, tiek izraisīts šis dzīves notikums.<br>BenefitEligibilityRuleOverride.ValidFrom. |
| **Piemērojamības kārtulas labošanas maiņa (ne ASV)** | Papildu cilvēkresursi > Atvieglojumi > Plāni > Atvieglojumi > Piemērotības nosacījumu labošana | Atjauninot atvieglojumu plāna piemērotības ignorēšanu **Derīgs no** vai **Derīgs līdz**, šī dzīves notikums tiek izraisīts. |
| **Piemērojamības kārtulas labošanas termiņa beigas (ne ASV)** | Atvieglojumu pārvaldība > Dzīves notikumu izmaiņu apstrāde  | Šie dzīves notikumi tiek izveidoti no **Dzīves notikumu izmaiņu apstrādes**. Šis process analizē izvēlēto periodu un juridisko personu un atrod saistītos atvieglojumu plāna atbilstības pārlabojumus. Tas izveido dzīves notikumus, ja ignorēšanai ir beidzies termiņš. |
| **Jauns atvieglojumu plāns (nav ASV)** | Papildu cilvēkresursi > Atvieglojumi > Plāni > Jauns | Piemērojamības opcijas tiek pievienotas pašreizējam plānam. Ir pievienots jauns plāns ar pievienotām piemērojamības opcijām.</br></br>Cilvēkresursu personālam vajadzētu šajā instancē palaist dzīves notikuma piemērojamības apstrādi |
| **Piemērojamības kārtulas maiņa (ne ASV)** | Atvieglojumu pārvaldība > Piemērotības nosacījumi | Dzīves notikumu piemērojamības apstrādes izmantošana. Reģistrēti, ja **BenefitEligibilityRule** ierakstiem ir mainītas šādas vērtības: **UseEmplCategory**, **UseEmplStatus** vai **UseEmplType**. Atjaunina tikai dzīves notikuma darbības, kas jau pastāv mainītai kārtulai vai piemērojamības kritērijam. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]