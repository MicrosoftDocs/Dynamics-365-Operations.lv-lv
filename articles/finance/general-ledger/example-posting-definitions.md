---
title: Grāmatošanas definīciju piemēri
description: Šajā rakstā ir sniegti piemēri, kuros ir redzams, ka grāmatošanas definīcijas tiek lietotas pirkšanas pasūtījumu apgrūtinājumiem un budžeta asignējumiem.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 751be602b701ac7a5b593404bf655e1a9852f863
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990493"
---
# <a name="posting-definition-examples"></a>Grāmatošanas definīciju piemēri

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegti piemēri, kuros ir redzams, ka grāmatošanas definīcijas tiek lietotas pirkšanas pasūtījumu apgrūtinājumiem un budžeta asignējumiem.

Pirms šīs tēmas lasīšanas jums ir jāpārzina grāmatošanas definīcijas un transakciju grāmatošanas definīcijas. Informāciju skatiet rakstā [Grāmatošanas definīcijas](posting-definitions.md). Tālāk sniegtos piemērus var iestatīt lapā **Grāmatošanas definīcijas**. Katrs piemērs satur trīs sadaļas.

-   Grāmatošanas definīcija — atbilstības kritēriji
-   Grāmatošanas definīcija — ģenerētie ieraksti
-   Transakcijas ar kontiem, dimensiju vērtībām un summām
-   Izmantojot grāmatošanas definīciju ģenerētie virsgrāmatas ieraksti

Ja tiek noteikta atbilstība starp kontiem un dimensiju vērtībām grāmatošanas definīcijas rūtī **Atbilstības kritēriji** un transakcijas kontiem un dimensiju vērtībām, tiek ģenerēti virsgrāmatas ieraksti, pamatojoties uz grāmatošanas definīcijas rūti **Ģenerētie ieraksti**. 
> [!NOTE]
> Lai grāmatošanas definīciju saistītu ar konkrētu transakcijas tipu, izmantojiet lapu **Transakciju grāmatošanas definīcijas**. Kad grāmatošanas definīciju esat saistījis ar transakcijas tipu un lapā **Virsgrāmatas parametri** esat atlasījis opciju **Izmantot grāmatošanas definīcijas**, visām atlasītā tipa transakcijām ir jālieto grāmatošanas definīcijas.

## <a name="example-purchase-order-encumbrances"></a>Piemērs: pirkšanas pasūtījuma apgrūtinājumi
Ja iespējojat apgrūtinājumu apstrādi, atlasot opciju **Iespējot apgrūtinājumu apstrādi** lapā **Virsgrāmatas parametri**, visiem kontiem, kas ir jārezervē, ir jāizmanto grāmatošanas definīcijas, lai reģistrētu apgrūtinājumus virsgrāmatā. Parasti visi izdevumu konti tiek rezervēti bilancē. 

Modulim **Pirkšana** apgrūtinājumu grāmatošanas definīcijas tiek iestatītas lapā **Grāmatošanas definīcijas**. Pēc tam lapas **Darījuma grāmatošanas definīcijas** apgabalā **Pirkšana** varat atlasīt transakcijas veidu **Pirkšanas pasūtījums**, lai saistītu grāmatošanas definīciju ar pirkšanas pasūtījumiem. 

Visām pirkšanas pasūtījumu apgrūtinājumu dokumentu transakcijām ir jābūt saskaņotām (debetam ir jābūt vienādam ar kredītu) katrā unikālajā dokumenta dimensijā.

### <a name="posting-definition--match-criteria"></a>Grāmatošanas definīcija — atbilstības kritēriji

| Konta struktūra       | Saskaņot konta numuru | Prioritāte |
|-------------------------|----------------------|----------|
| Konta struktūra — P&Z | \*                   | 1        |

<em>Tukša lauka **Saskaņot konta numuru</em>* vērtība nozīmē, ka visi atbilstošie konti definētajā kontu struktūrā ir ietverti atbilstības noteikšanas kārtulā.

### <a name="posting-definition--generated-entries"></a>Grāmatošanas definīcija — ģenerētie ieraksti

| Konta struktūra | Ģenerētais konta numurs                    | Ģenerētais debets/kredīts |
|-------------------|---------------------------------------------|------------------------|
| Bilance           | 300143 —(apgrūtinājuma konts)             | Tā pati                   |
| Bilance           | 300144 — (apgrūtinājuma rezerves konts) | Līdzsvara noturēšana              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Transakcijas ar kontiem, dimensiju vērtībām un summām

Konti un dimensijas vērtības ir iegūtas no uzskaites sadalēm, kas ir ievadītas pirkšanas pasūtījuma rindām, vai no kontiem un dimensijām, kas tiek automātiski ģenerēti, pamatojoties uz kreditoru, krājumu, kategoriju un dimensiju veidņu noklusējuma iestatījumiem.

| Konts + dimensijas           | Debetkarte  | Kredītkarte | Komentārs |
|--------------------------------|--------|--------|---------|
| 606400-OU\_1-OU\_3566-Apmācība | 250,00 |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Izmantojot grāmatošanas definīciju ģenerētie virsgrāmatas ieraksti

Tiek izveidoti ģenerētie virsgrāmatas ieraksti, lai reģistrētu apgrūtinājumus.

| Konts + dimensijas           | Debetkarte  | Kredītkarte | Komentārs |
|--------------------------------|--------|--------|---------|
| 300143-OU\_1-OU\_3566-Apmācība | 250,00 |        |         |
| 300144-OU\_1-OU\_3566-Apmācība |        | 250,00 |         |

Šajā piemērā jebkurš konts, kas ietilpst konta struktūrā — P&Z, atbilst grāmatošanas definīcijas kritērijiem. Tāpēc, novērtējot 606500-OU\_1-OU\_3566-Apmācība, ģenerētie ieraksti tiek izveidoti kontiem, kas grāmatošanas definīcijai ir definēti rūtī **Ģenerētie ieraksti**.

## <a name="example-budget-appropriations"></a>Piemērs: budžeta asignēšana
Ja iespējot budžeta asignēšanu, atlasot opciju **Iespējot budžeta asignēšanu** lapā **Virsgrāmatas parametri**, grāmatošanas definīcijas ir jāizmanto, lai reģistrētu budžeta reģistra ierakstus virsgrāmatā. Kad ir aktivizēta un ieslēgta budžeta kontroles konfigurācija, grāmatošanas definīcijas un transakciju grāmatošanas definīcijas var izmantot, lai atbalstītu asignējumu, pārskatījumu, pārsūtījumu, projektu, pamatlīdzekļu un piedāvājuma un pieprasījuma prognožu ierakstu reģistrēšanai virsgrāmatā. 

Lai iestatītu grāmatošanas definīciju budžeta reģistra ierakstiem, kuru budžeta veids ir **Sākotnējais budžets** un kam ir iespējota asignēšana, lapā **Grāmatošanas definīcijas** atlasiet moduli **Budžets**. Pēc tam lapas **Darījuma grāmatošanas definīcijas** apgabalā **Budžets** varat izmantot budžeta kodus, lai saistītu grāmatošanas definīciju ar budžeta reģistra ierakstiem, kuru budžeta veids ir **Sākotnējais budžets**. 

Kad ir iespējoti budžeta asignējumi un grāmatošanas definīcijas, budžeta reģistra ieraksti tiek reģistrēti budžeta kontroles nolūkā un virsgrāmatā.

### <a name="posting-definition--match-criteria"></a>Grāmatošanas definīcija — atbilstības kritēriji

| Konta struktūra       | Saskaņot konta numuru | Prioritāte |
|-------------------------|----------------------|----------|
| Konta struktūra — P&Z | \*                   | 1        |

<em>Tukša lauka **Saskaņot konta numuru</em>* vērtība nozīmē, ka visi atbilstošie konti definētajā kontu struktūrā ir ietverti atbilstības noteikšanas kārtulā.

### <a name="posting-definition--generated-entries"></a>Grāmatošanas definīcija — ģenerētie ieraksti

| Konta struktūra | Ģenerētais konta numurs              | Ģenerētais debets/kredīts |
|-------------------|---------------------------------------|------------------------|
| Konta struktūra | 300145 — (novērtēto ieņēmumu konts) | Tā pati                   |
| Konta struktūra | 300146 — (asignēšanas konts)     | Līdzsvara noturēšana              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Transakcijas ar kontiem, dimensiju vērtībām un summām

Budžeta konta ieraksta kontus, dimensiju vērtības un summas var ievadīt lapā **Budžeta reģistra ieraksts**.

| Konts + dimensijas           | Debetkarte | Kredītkarte | Komentārs |
|--------------------------------|-------|--------|---------|
| 606400-OU\_1-OU\_3566-Apmācība |       | 250,00 |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Izmantojot grāmatošanas definīciju ģenerētie virsgrāmatas ieraksti

Tiek izveidoti ģenerētie virsgrāmatas ieraksti, lai reģistrētu sākotnējo budžetu katrā dimensijā.

| Konts + dimensijas           | Debetkarte  | Kredītkarte | Komentārs |
|--------------------------------|--------|--------|---------|
| 300145-OU\_1-OU\_3566-Apmācība |        | 250,00 |         |
| 300146-OU\_1-OU\_3566-Apmācība | 250,00 |        |         |

Šajā piemērā jebkurš konts, kas ietilpst konta struktūrā — P&Z, atbilst grāmatošanas definīcijas kritērijiem. Tāpēc, novērtējot 606400-OU\_1-OU\_3566-Apmācība, tiek izveidoti ģenerētie virsgrāmatas ieraksti.





