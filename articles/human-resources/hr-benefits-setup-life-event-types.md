---
title: Konfigurēt dzīves notikumu tipus
description: Microsoft Dynamics 365 Human Resources izmanto dzīves notikumu veidus, lai definētu notikumus, kas ir atļauts atjaunināt darbinieku atvieglojumu reģistrāciju.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5286bcd940f4068531bae624876c8a35e64db4c3
ms.sourcegitcommit: 9723b5ff40c84677316d71e185cf862556b32cf9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/31/2020
ms.locfileid: "3741490"
---
# <a name="configure-life-event-types"></a>Konfigurēt dzīves notikumu tipus

Microsoft Dynamics 365 Human Resources izmanto dzīves notikumu veidus, lai definētu notikumus, kas ir atļauts atjaunināt darbinieku atvieglojumu reģistrāciju. Piemēram, darbinieks apprecas vai ģimenē ir pieaugums. Katru dzīves notikuma veida ID var saistīt tikai ar vienu dzīves notikuma veidu. Piemēram, ja izveidojat dzīves notikuma ID, sauktu par adreses maiņu, kas saistīts ar dzīves notikuma veidu Darbinieka adreses maiņa, nevar izveidot citu ID ar nosaukumu Darbinieka adreses maiņa un saistīt to ar dzīves notikuma veidu Darbinieka adreses maiņa. 

Kad dzīves notikumu veidi ir izveidoti, tie ir jāsaista ar plānu veidiem. Papildu informāciju skatiet sadaļā [Plānu veidu izveide](hr-benefits-setup-plan-types.md).

   > [!NOTE]
   > Pēc dzīves notikuma izveidošanas tas ir jāsaista ar plāna veidu. Papildu informāciju skatiet sadaļā [Plānu veidu izveide](hr-benefits-setup-life-event-types.md).

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
| **Nodarbinātības statusa maiņa** | <ul><li>Nodarbinātais > Nodarbinātība</li><li>Nodarbinātības vēstures lapa</li></ul> | Nodarbinātības statusa maiņa |
| **Darbinieka adreses maiņa** | <ul><li>Nodarbinātais > Profils > Adreses </li><li>Nodarbinātais > Personiskā informācija > Personiskie kontakti > Adrese</li></ul> Pievienota, rediģēta vai dzēsta adrese |
| **Pakārtotā maiņa** | <ul><li>Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Pievienot vai dzēst pakārtoto</li><li>Darbinieku patstāvīgi izmantojamais pakalpojums</li></ul> | Pievienots vai dzēsts pakārtotais. Personisko kontaktpersonu attiecībām ir jābūt bērnam, dzīvesbiedram, dzīvesbiedram vai bijušajam dzīvesbiedram. Datuma **Derīgs no** atjaunošana aktivizē dzīves notikumu. Ja neatjaunināsit šo datumu, netiks aktivizēts dzīves notikums. |
| **Dzimšana vai adopcija (pakārtotais)** | <ul><li>Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Informācija par pakārtoto</li><li>Darbinieku patstāvīgi izmantojamais pakalpojums</li></ul> | Ir aizpildīts lauks**Pieņemšanas datums**. Ir jānorāda bērna dzimšanas datums. |
| **Vajadzības zaudēšana (laulātais/dzīvesbiedrs)** | Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Vajadzības zudums | **Vajadzības zudums** atlasīts personiskajai kontaktpersonai kopā ar **Spēkā stāšanās datumu** |
| Dzīvesbiedra nodarbinātības izmaiņas | Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Informācija par pakārtoto > Nodarbināts. | <ul><li>Izveidota pakārtotā informācija un lauks **Personiskā kontaktpersona nodarbināta** = Jā</li><li>**Personiskā kontaktpersona** lauks ir nomainīts (Jā vai Nē)</li></ul> |
| **Atvaļinājums (laulātais/dzīvesbiedrs)** | Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Pakārtotā informācija > Atvaļinājums | <ul><li>Ir izveidots pakārtotā informācijas ieraksts un aizpildīts **EhrLOAEffectiveDate**</li><li>**personPrivateDetails.EhrIsLOA** ir mainīts (Jā vai nē)</li><li>**personPrivateDetails.EhrLOAEffectiveDate** ir mainīts</li></ul> |
| **Vajadzības izmaiņas (amats)** | <ul><li>Nodarbinātais > Amata piešķire > Nodarbinātā amata piešķires</li><li>Amati > Amati</li></ul> | <ul><li>Mainīt uz pozīciju darbinieka amata piešķires ierakstos</li><li>Nodarbinātā amata piešķires maiņa</li></ul> |
| **Medicīniskā aprūpe (darbinieks/pakārtotais)** | Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Pakārtotā informācija > Medicīniskās aprūpes spēkā stāšanās datums | Netiek aktivizēts automātiski, kad personiskā kontaktpersona ievada spēkā stāšanās datumu. |
| **Ar tiesu piespriests atbalsts** | Nodarbinātais > Profils > Personiskā informācija > Personiskie Kontakti > Pakārtotie > Atbalsts pēc tiesas prasības (QMSCO/QDRO un spēkā stāšanās datumi | Neaktivizē nevienu automātisko atjauninājumu. Tas neietekmē piemērojamību; tas ieraksta dzīves notikumu. |
| **Miris** | Nodarbinātais > Profils > Personiskā informācija > Miršanas datums | Ir ievadīts miršanas datums |
| **Apliecinājums par apdrošināšanu** | <ul><li>Nodarbinātais > Nodarbinātais > Versijas > Nodarbinātības vēsture > Datumu pārvaldnieka > Informācija par atvieglojumiem</li><li> Nodarbinātais > Nodarbinātība > Informācija par atvieglojumiem > Pārbaudes datums</li></ul> | <ul><li>Nodarbinātais ievada pārbaudes datumu</li><li>Nodarbinātais iestata EvidenceOfInsurability lauku uz **Jā**</li></ul> |
| **Saņēmējs** | Nodarbinātais >Profils > Personiskā informācija > Personiskie kontakti | Tiek pievienota personīgā kontaktpersona un ir aizpildīts lauks **Saņēmējs** un **Spēkā stāšanās datums**. Personiskajai kontaktpersonai ir jābūt ar veidu **Bērns**, **Laulātais**, **Dzīvesbiedrs**, **Atvase**, **Ģimenes kontaktpersona**, **Cita kontaktpersona**, **Vecāks**,**Saņēmēja īpašums**,**Saņēmēja organizācija** vai **Saņēmēja trests**. |
| **Darbinieka medicīniskā aprūpe** | Nodarbinātais > Nodarbinātais > Versijas > Nodarbinātības vēsture > Datumu pārvaldnieka > Informācija par atvieglojumiem | <ul><li>**EhrMedicareEligibilityDate** ir mainīts</li><li>**MedicareEligibile** ir iestatīts uz **Jā**</li></ul> |
| **Dzimšanas diena** | Nodarbinātais > Profils > Personiskā informācija > Personiskās kontaktpersonas > Informācija par pakārtoto > Informācija par dzimšanu | Tiek pievienots vai atjaunināts dzimšanas datums (ne pēc dzīves notikuma izmaiņu apstrādes). Piemērs: Ja bērna **Personīgā kontakta piemērojamības opcijas** ir iestatītas uz Vecums: 26 sadaļā Iestatījumi > Atvieglojumi > Personiskās kontaktpersonas piemērojamības opcijas un, ja cilvēkresursu personāls veic dzīves notikuma izmaiņas jebkurā dienā pēc tam, kad pakārtotais kļuvis 26 gadu vecs, parādās ziņojums, ka uz pakārtoto vairs neattiecas nodrošinājums. |
| **Nodarbinātā piemērojamības izmaiņas (nav noteiktas ASV)** | <ul><li>Nodarbinātais > Nodarbinātība</li><li>Nodarbinātais > Nodarbinātais > Versijas > Nodarbinātības vēsture</li></ul> | <ul><li>Nodarbinātā veida, nodarbinātības kategorijas vai piecu lietotājam definējamu piemērojamības lauku maiņa</li><li>**HcmEmploymentDetail.EhrEmploymentType** izmaiņas (tiek apstrādātas tikai *mainītiem* nodarbinātības informācijas ierakstiem, bet ne *jauniem* nodarbinātības ierakstiem, piemēram, atkārtotai līgšanai vai pārtraukšanai).</li></ul> |
| **Jaunas piemērojamības labošana (ne ASV)** | Papildu cilvēkresursi > Atvieglojumi > Plāni > Atvieglojumi > Piemērotības nosacījumu labošana | Dzīves notikumu apstrādes lietošana | EhrBenefitEligibilityRuleOverride.ValidFrom |
| **Piemērojamības kārtulas labošanas maiņa (ne ASV)** | Papildu cilvēkresursi > Atvieglojumi > Plāni > Atvieglojumi > Piemērotības nosacījumu labošana | Dzīves notikumu apstrādes lietošana (tver tikai izmaiņas laukos**ValidFrom** un **ValidTo** Piemērojamības kārtulas labošanā) |
| **Piemērojamības kārtulas labošanas termiņa beigas (ne ASV)** | Papildu cilvēkresursi > Atvieglojumi > Plāni > Atvieglojumi > Piemērotības nosacījumu labošana | Dzīves notikumu izmaiņu apstrādes izmantošana. Piemēram, ja rediģējat plāna piemērojamības kārtulas labošanas beigu datumu, lai tas būtu šodien, plkst. 17:00, jebkurā laikā pēc 17:00 vai nākamajās dienās un pēc tam palaižat dzīves notikuma izmaiņu apstrādi, parādās ziņojums, kas apgalvo, ka piemērojamības kārtulas labošanai ir beidzies derīgums. |
| **Jauns atvieglojumu plāns (nav ASV)** | Papildu cilvēkresursi > Atvieglojumi > Plāni > Jauns | <ul><li>Piemērojamības opcijas tiek pievienotas pašreizējam plānam</li><li>Ir pievienots jauns plāns ar pievienotām piemērojamības opcijām</li></ul></br></br>Cilvēkresursu personālam vajadzētu šajā instancē palaist dzīves notikuma piemērojamības apstrādi |
| **Piemērojamības kārtulas maiņa (ne ASV)** | Papildu cilvēkresursi > Atvieglojumi > Noteikumi/opcija > Piemērojamības noteikumi | Dzīves notikumu piemērojamības apstrādes izmantošana. Reģistrēti, ja**EhrBenefitEligibilityRule** ierakstiem ir mainītas šādas vērtības: **UseEmplCategory**, **UseEmplStatus** vai **UseEmplType**. Atjaunina tikai dzīves notikuma darbības, kas jau pastāv mainītai kārtulai vai piemērojamības kritērijam. |
